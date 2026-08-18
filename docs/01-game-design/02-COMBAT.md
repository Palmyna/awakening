# Project Awakening — Combat

**Statut :** Rédigé — référence actuelle, à maintenir à jour

## 1. Rôle et périmètre du document

Ce document définit les règles structurelles communes du système de combat de **Project Awakening**.

Il constitue la référence actuelle pour le moteur de combat, notamment pour :

* la simulation temporelle ;
* les équipes et la formation ;
* les actions et leur priorité ;
* le ciblage et les zones ;
* les caractéristiques et autres statistiques ;
* les dégâts, soins et protections ;
* les éléments ;
* les effets de statut ;
* les états de vie, de présence et de contrôle ;
* les conditions de fin d’un combat standard.

Il reste un document de game design. Il ne constitue pas une spécification technique d’implémentation.

Les formules, caps, coefficients, durées et valeurs numériques explicitement indiqués comme restant à équilibrer peuvent évoluer sans remettre en cause les décisions structurelles présentées ici.

Les futurs documents consacrés aux créatures, aux Skills, aux éléments et aux effets de statut reprennent et approfondissent leurs domaines respectifs sans contredire les règles système nécessaires au combat.

## 2. Principes de simulation

Les combats de Project Awakening reposent sur une **simulation mathématique en temps continu**.

Le combat n'est pas un système au tour par tour.

Le moteur calcule les événements selon une timeline continue et déterministe, tandis que le joueur observe une représentation animée du combat.

Le résultat d'un combat doit pouvoir être reproduit à partir des mêmes conditions initiales et de la même seed RNG.

Cela doit notamment permettre :

* les replays ;
* le debugging ;
* la validation serveur ;
* les simulations de balancing ;
* la reproduction exacte d'un résultat lorsque les mêmes données et la même seed sont utilisées.

Le RNG reste présent pour certaines mécaniques, notamment :

* l'Esquive ;
* les Critiques ;
* les probabilités explicitement définies par certains Skills ou effets.

---

## 3. Équipes, formation et états de présence

### 3.1. Composition des équipes

Une équipe peut contenir jusqu'à **6 créatures**.

Toutes les créatures sélectionnées sont présentes simultanément sur le terrain.

Une équipe utilise une formation composée de :

* 3 lignes ;
* jusqu'à 6 positions par ligne ;
* maximum 6 créatures au total.

Le joueur choisit :

* la ligne de chaque créature ;
* leur ordre gauche → droite dans cette ligne.

Le positionnement exact en colonnes est ensuite géré automatiquement.

---

### 3.2. Grille de formation

Le terrain utilise conceptuellement une grille de :

* **3 lignes** ;
* **6 colonnes**.

Les créatures d'une même ligne sont automatiquement regroupées dans des positions contiguës.

Il est impossible de laisser volontairement un espace vide entre deux créatures lors de la préparation de l'équipe.

Exemple interdit :

```text
[X][ ][X]
```

Les positions sont automatiquement centrées autant que possible sur la grille.

Exemple conceptuel :

```text
1 créature :       [ ][ ][X][ ][ ][ ]
2 créatures :      [ ][ ][X][X][ ][ ]
3 créatures :      [ ][X][X][X][ ][ ]
4 créatures :      [ ][X][X][X][X][ ]
5 créatures :      [X][X][X][X][X][ ]
6 créatures :      [X][X][X][X][X][X]
```

Lorsqu'un centrage parfait est impossible, une convention déterministe est utilisée.

Le joueur ne choisit pas directement les colonnes.

---

### 3.3. Positions pendant le combat

Les positions restent fixes pendant tout le combat.

Aucun déplacement automatique n'a lieu.

Lorsqu'une créature meurt :

* sa position devient vide ;
* les autres créatures ne se déplacent pas ;
* la formation n'est pas recentrée.

Les espaces vides peuvent donc apparaître pendant un combat, même s'ils sont interdits lors de la préparation de l'équipe.

Un Skill peut exceptionnellement déplacer ou modifier une position si sa description le prévoit explicitement.

---

### 3.4. Créatures vivantes, présentes et non vivantes

Une créature **vivante et présente dans le combat** peut normalement :

* agir ;
* être ciblée ;
* subir des dégâts ;
* recevoir des soins ;
* recevoir des buffs et debuffs.

Certains effets peuvent modifier temporairement cet état.

#### 3.4.1. Créature morte

Une créature à 0 PV est considérée comme morte.

Elle :

* ne peut plus agir ;
* ne peut plus être ciblée ;
* ne compte plus comme survivante ;
* ne revient pas grâce à un soin classique.

Il n'existe pas de résurrection générale d'un allié.

Seules certaines Passives propres à la créature peuvent permettre une **auto-résurrection**.

#### 3.4.2. Créature exclue

Une créature sous un effet d'Exclusion :

* est toujours vivante ;
* est temporairement retirée du combat ;
* ne peut ni agir ni être ciblée ;
* ne peut recevoir ni dégâts, ni soins, ni buffs, ni debuffs ;
* ne compte pas comme une créature actuellement présente/ciblable.

Ses effets et timers personnels sont gelés pendant l'Exclusion.

#### 3.4.3. Cas du Phoenix et auto-résurrection

Une créature disposant d'une auto-résurrection peut avoir un état intermédiaire, par exemple un Phoenix transformé en œuf.

Dans cet état :

* la créature est considérée comme **non vivante** ;
* elle ne compte pas comme survivante ;
* elle ne peut pas être ciblée ;
* elle ne peut pas agir ;
* elle peut revenir après le délai prévu par sa Passive si le combat n'est pas déjà terminé.

La mort et cet état non vivant n'agissent pas comme un Cleanse. Les statuts déjà présents restent attachés à la créature et leurs timers continuent à s'écouler normalement. Les effets nécessitant une cible vivante, notamment les dégâts d'un DoT, ne produisent toutefois pas leur effet normal pendant cet état.

Cette règle est distincte de l'Exclusion, qui gèle les timers et effets personnels.

Si toutes les créatures d'une équipe sont non vivantes, le combat se termine immédiatement.

Ainsi, si le Phoenix est la dernière créature et passe en œuf, l'équipe perd avant sa prochaine résurrection.

Une auto-résurrection peut fonctionner plusieurs fois ou indéfiniment si la Passive le prévoit, mais uniquement tant que le combat reste actif.

---

## 4. Déroulement global du combat

### 4.1. Début du combat

Sauf indication contraire :

* chaque créature utilise sa jauge structurelle standard `0 → 100` ;
* son état initial est `0 / 100 énergie` ;
* aucune Basic Attack n'est exécutée immédiatement à `0,000 s`.

Une Passive peut définir une énergie initiale différente ou modifier la capacité maximale effective de la jauge. Ces modifications d'état initial sont appliquées avec les autres effets de début de combat.

Les effets « au début du combat » sont résolus à `0,000 s`.

Ils sont appliqués avant le démarrage normal des premières actions.

Lorsque plusieurs effets de début de combat nécessitent une résolution successive, ils utilisent la priorité générale :

1. Agilité effective actuelle ;
2. équipe attaquante ;
3. ordre des positions, de la ligne 1 à la ligne 3 puis de gauche à droite.

L'état est réévalué après chaque effet résolu.

---

### 4.2. Temps de combat

La durée maximale standard d'un combat est de :

**120 secondes de simulation.**

Cette durée est indépendante de la vitesse de visualisation choisie par le joueur.

À la fin du temps réglementaire, la règle de victoire dépend du mode.

#### 4.2.1. Combat standard

Priorités :

1. équipe possédant le plus de créatures vivantes ;
2. si égalité, équipe possédant le meilleur ratio global de PV restants parmi ses survivants ;
3. si égalité parfaite, victoire de l'attaquant.

Le ratio global de PV restants est calculé ainsi :

> **RatioPVSurvivants = SommePVActuelsSurvivants / SommePVMaximumSurvivants**

Avec :

* `SommePVActuelsSurvivants` : somme des PV actuels de toutes les créatures vivantes de l'équipe ;
* `SommePVMaximumSurvivants` : somme des PV maximum de ces mêmes créatures ;
* `RatioPVSurvivants` : proportion de PV restants utilisée pour comparer les équipes.

Le ratio compare donc uniquement l'état des survivants de chaque équipe. Les créatures mortes ou non vivantes sont exclues des deux sommes.

Une créature non vivante, comme un Phoenix en œuf, ne compte pas comme survivante.

#### 4.2.2. Modes à objectif

Tous les combats utilisent par défaut une durée maximale de **120 secondes de simulation**, quel que soit le mode.

Le mode détermine en revanche sa propre condition de victoire, de défaite ou de score.

Cela peut notamment concerner :

* un combat contre un boss ;
* un objectif de dégâts ;
* un objectif de survie ;
* d'autres objectifs spécifiques.

Un mode ne peut utiliser une durée différente que si cette exception est explicitement définie.

Exemple :

> infliger le maximum de dégâts à un Boss pendant 120 secondes.

---

### 4.3. Vitesse de visualisation

Le combat repose sur 120 secondes de **temps de simulation**, indépendamment de sa vitesse d'affichage.

Les vitesses de visualisation accélérées constituent des **services de confort payants**.

Principe validé :

* ×1 disponible gratuitement ;
* ×2 comme premier palier de confort payant ;
* ×4 comme palier supérieur ;
* possibilité d'acheter directement le palier supérieur ou de payer seulement la différence lors d'un upgrade ;
* prix exacts à définir ultérieurement.

La vitesse peut être modifiée à tout moment pendant le combat, y compris en mode Manuel.

Le jeu mémorise la dernière vitesse utilisée et la réutilise par défaut lors du combat suivant.

Ces options ne changent jamais :

* la durée de simulation ;
* les calculs ;
* les caractéristiques ;
* les événements ;
* la seed RNG ;
* les récompenses ;
* le coût en énergie ;
* le résultat du combat.

Elles modifient uniquement le temps réel nécessaire à la visualisation.

---

## 5. Modèle d’action

### 5.1. Structure des actions d’une créature

Chaque créature possède :

* 1 Basic Attack ;
* exactement 4 Skills :

  * 3 Skills répartis en une ou deux Active et une ou deux Passive ;
  * exactement 1 Ultimate.

Seules deux répartitions sont autorisées :

* 1 Active + 2 Passive + 1 Ultimate ;
* 2 Active + 1 Passive + 1 Ultimate.

Une créature possède donc toujours au moins une Active et au moins une Passive.

Le joueur ne choisit pas les Skills de la créature.

Ils font partie de son identité de gameplay.

---

### 5.2. Basic Attack

La Basic Attack est une action automatique propre à chaque créature.

Elle est représentée sur sa fiche de manière comparable à un Skill et inflige toujours des dégâts. Elle peut également produire des effets supplémentaires explicitement définis.

Elle définit notamment :

* son nom ;
* son coefficient de dégâts ;
* la caractéristique offensive utilisée ;
* sa catégorie de dégâts ;
* son élément ;
* son intervalle de base ;
* son gain d'énergie ;
* son éventuel nombre de hits ;
* son éventuelle règle de ciblage particulière.

#### 5.2.1. Catégorie de dégâts

Une Basic Attack peut utiliser des dégâts Physiques, Spéciaux, hybrides, True Damage ou une autre formule explicitement définie.

Une Basic Attack Physique utilise :

* Attaque ;
* Défense de la cible.

Une Basic Attack Spéciale utilise :

* Attaque spéciale ;
* Défense spéciale de la cible.

Une Basic Attack n'est donc pas obligatoirement Physique et peut comporter plusieurs composantes lorsque sa fiche les déclare.

#### 5.2.2. Première attaque

Une créature doit attendre son intervalle complet avant sa première Basic Attack.

Exemple :

> intervalle final = 1,500 s
> première Basic = `1,500 s`.

---

### 5.3. Active Skills

Les Active Skills sont déclenchés automatiquement selon leur cycle.

Chaque Active possède son propre compteur et devient prête après **X Basic Attacks réussies**. Lorsqu'une créature possède deux Active, une même Basic réussie fait progresser leurs compteurs indépendants en parallèle.

Un compteur ayant atteint son seuil reste bloqué à sa valeur maximale jusqu'au lancement de l'Active. Aucun dépassement n'est stocké.

L'action qui aurait normalement eu lieu à l'opportunité concernée est alors remplacée par l'Active.

Si plusieurs Active sont prêtes au même moment, elles sont résolues selon leur ordre défini sur la fiche de la créature.

Une seule Active peut remplacer une même opportunité de Basic Attack.

Les autres Active déjà prêtes restent disponibles et sont utilisées lors des prochaines opportunités d'action, selon leur ordre de priorité.

Une Active :

* ne compte pas elle-même comme Basic ;
* ne fait pas progresser les autres compteurs de Basic, sauf règle explicitement contraire.

Dès que l'Active commence son lancement, son compteur revient à zéro, même si le Skill rate, si sa cible esquive ou si aucun de ses hits ne touche.

Une capacité peut explicitement modifier le seuil ou la progression d'un cycle d'Active. Elle ne retire pas rétroactivement, comme comportement standard, des Basic Attacks déjà accomplies dans un compteur adverse.

Une Basic esquivée :

* ne compte pas dans les compteurs d'Active ;
* ne génère pas d'énergie.

---

### 5.4. Passive Skills

Les Passive Skills réagissent à des événements ou conditions.

Exemples :

* début du combat ;
* dégâts reçus ;
* dégâts infligés ;
* kill ;
* mort d'un allié ;
* Critique ;
* application d'un statut ;
* seuil de PV ;
* utilisation d'une Ultimate ;
* etc.

Une Passive peut créer des exceptions aux règles générales si sa description les définit explicitement.

Elle peut contenir plusieurs effets et conditions et se déclencher autant de fois que sa description le prévoit. Une Passive peut également réagir à la mort de son propre porteur ; la mort n'annule pas l'effet dont elle constitue précisément le déclencheur.

Un effet conditionnel ou déclenché intégré à une Basic Attack, une Active ou une Ultimate ne transforme pas cette capacité en Passive supplémentaire.

---

### 5.5. Ultimate

Chaque créature possède exactement **1 Ultimate**.

Chaque créature possède une jauge structurelle standard allant de **0 à 100 énergie** et un seuil standard d'Ultimate fixé à 100.

Une Passive ou un autre effet peut explicitement modifier :

* l'énergie initiale ;
* la capacité maximale effective de la jauge ;
* le seuil de disponibilité de l'Ultimate.

Une capacité maximale effective supérieure à 100 autorise l'accumulation au-delà de 100. Lorsque la capacité effective reste égale à 100, tout gain excédentaire est perdu.

Lorsqu'une Ultimate commence réellement son utilisation, toute l'énergie présente est consommée et la jauge revient à 0, même si son seuil était inférieur à l'énergie accumulée.

#### 5.5.1. Priorité d’action

L'Ultimate utilise la même opportunité d'action qu'une Active ou une Basic Attack.

Elle ne constitue pas une action supplémentaire indépendante entre deux Basics.

Lorsqu'une créature est prête à agir, la priorité standard est :

1. Ultimate prête, autorisée et disposant d'une cible valide ;
2. Active prête, autorisée et disposant d'une cible valide ;
3. Basic Attack.

Si l'Ultimate est disponible au moment où une Active devait être utilisée :

> l'Ultimate est prioritaire.

L'Active reste prête et sera utilisée lors de la prochaine opportunité d'action valide.

L'action effectivement utilisée remplace la Basic Attack qui aurait normalement eu lieu à cet instant.

Une règle explicite de Skill peut exceptionnellement modifier cette priorité.

#### 5.5.2. Gain d’énergie

La quantité d'énergie générée par une Basic fait partie des propriétés de cette Basic.

Une Basic réussie donne l'énergie indiquée.

Une Basic esquivée :

* ne donne aucune énergie ;
* ne progresse pas les Active.

Sauf effet explicite, seule la créature qui effectue l'action gagne l'énergie liée à sa Basic.

Pendant le combat, les autres Skills ne constituent pas des sources autonomes de gain direct d'énergie. Ils peuvent en revanche :

* modifier ou empêcher le gain produit par une Basic ;
* retirer ou voler de l'énergie ;
* modifier le seuil de l'Ultimate ;
* modifier la capacité maximale effective ;
* exploiter l'énergie accumulée.

La disponibilité de l'Ultimate est recalculée en live après toute modification de l'énergie ou de son seuil.

#### 5.5.3. Auto

En mode Auto :

> lorsqu'une Ultimate atteint son seuil, elle est sélectionnée à la prochaine opportunité d'action valide.

Elle reste prioritaire sur une Active prête et sur la Basic Attack.

#### 5.5.4. Manuel

En mode Manuel :

* le joueur peut conserver son Ultimate une fois son seuil atteint ;
* l'énergie peut continuer à s'accumuler jusqu'à la capacité maximale effective ;
* le joueur choisit de demander son déclenchement ;
* l'Ultimate demandée est utilisée à la prochaine opportunité d'action valide.

Le mode de contrôle est global au combat. Les Basic Attacks et Active restent automatiques dans les deux modes.

Une demande manuelle d'Ultimate est irréversible. Le joueur contrôle son autorisation, mais ni sa cible ni son comportement interne.

Lors du passage de Manuel à Auto, une Ultimate prête devient automatiquement autorisée à la prochaine opportunité valide. Lors du passage d'Auto à Manuel, une Ultimate prête dont le lancement n'a pas commencé reste disponible et attend une demande manuelle.

La vitesse de visualisation peut être changée même en mode Manuel.

---

### 5.6. Timers et contrôle

Les actions se déroulent sur une timeline continue.

Par défaut :

* les Active et Ultimate sont résolues instantanément au moment de leur déclenchement ;
* il n'existe pas de channeling ou cast time général.

Un Skill peut explicitement définir :

* un délai ;
* une bombe retardée ;
* un effet périodique ;
* une autre temporalité particulière.

#### 5.6.1. Crowd Control total

Les CC totaux standards comprennent notamment :

* Stun ;
* Glacé ;
* Peur.

Ils possèdent la même mécanique de contrôle mais des tags différents.

Pendant un CC total :

* la créature ne peut effectuer aucune action ;
* son timer d'action est gelé ;
* la progression de ses Active s'arrête naturellement puisqu'elle ne peut plus réussir de Basics.

À la fin du CC :

> le timer reprend là où il avait été interrompu.

Les DoT, HoT, buffs et debuffs continuent cependant à évoluer normalement pendant un CC classique.

#### 5.6.2. Interaction temporelle avec un CC

Lorsqu'un CC est appliqué avant le début réel de l'action d'une créature, il peut empêcher cette action selon ses règles.

Si plusieurs créatures devaient agir au même timestamp, leur ordre est d'abord établi selon la priorité générale définie en section 5.7. Un CC produit par l'action prioritaire est entièrement résolu avant l'évaluation de l'action suivante.

Une action dont le lancement a déjà commencé n'est pas annulée par un CC, sauf interruption explicitement prévue.

---

### 5.7. Actions au même timestamp et chaînes de résolution

Lorsque plusieurs créatures doivent agir exactement au même timestamp, leur ordre est déterminé par :

1. l'Agilité effective actuelle la plus élevée ;
2. en cas d'égalité, l'équipe attaquante avant l'équipe défenseuse ;
3. en cas de nouvelle égalité, l'ordre des positions : ligne 1 à ligne 3, puis gauche à droite.

L'Agilité est évaluée en live au moment où l'action doit réellement commencer.

Une action et toute sa chaîne de conséquences sont entièrement résolues avant le passage à l'action normale suivante. Cette chaîne comprend les hits, dégâts, soins, statuts, réactions, Passive, morts, effets à la mort et réactions aux réactions.

Une action dont le lancement a commencé continue jusqu'à sa fin même si son lanceur meurt pendant sa résolution. Une interruption n'existe que si une mécanique particulière la prévoit explicitement.

Si plusieurs effets à la mort attendent la même priorité temporelle, ils utilisent le même départage par Agilité effective, équipe attaquante puis position.

Les boucles infinies de réactions doivent être empêchées par la conception des capacités et les garde-fous techniques appropriés.

---

## 6. Ciblage, géométrie et résolution des hits

### 6.1. Ciblage standard des Basic Attacks

Le ciblage standard fonctionne comme suit.

#### 6.1.1. Ligne prioritaire

Le moteur identifie la **première ligne ennemie occupée**.

Les Basics standards ne ciblent normalement que cette ligne.

#### 6.1.2. Ordre des cibles

Les cibles valides de la ligne sont ordonnées :

> gauche → droite.

#### 6.1.3. Ordre des attaquants

Les attaquants sont ordonnés :

1. ligne 1 gauche → droite ;
2. ligne 2 gauche → droite ;
3. ligne 3 gauche → droite.

#### 6.1.4. Distribution cyclique

Les attaquants sont distribués cycliquement parmi les cibles valides.

Exemples avec 6 attaquants :

* 1 cible → 6 attaques sur elle ;
* 2 cibles → 3 / 3 ;
* 3 cibles → 2 / 2 / 2 ;
* 4 cibles → 2 / 2 / 1 / 1 ;
* 6 cibles → 1 attaque chacune.

Le ciblage est recalculé lorsqu'une cible meurt ou que la composition de la ligne change.

---

### 6.2. Priorité des règles de ciblage

Ordre général :

1. règle explicite du Skill ;
2. effet ou statut modifiant le ciblage ;
3. ciblage standard.

Il n'existe pas de mécanique générale de Taunt / Provocation.

Les tanks protègent principalement leur équipe via :

* leur placement ;
* les lignes ;
* les règles naturelles de ciblage ;
* leurs propres Skills.

Le terme **allié** inclut le lanceur lui-même. Une capacité qui doit l'exclure utilise la formulation **autre allié**.

---

### 6.3. Voisinage et géométrie

Deux créatures sont voisines uniquement si elles sont directement adjacentes :

* à gauche ;
* à droite ;
* devant ;
* derrière.

Une diagonale n'est **jamais** considérée comme un voisin.

Cette règle reste vraie même pour les Skills.

Si un Skill doit toucher une zone plus importante, il utilise une autre règle d'AoE plutôt qu'une notion de voisin diagonal.

Lorsqu'une créature meurt et laisse une case vide, le voisinage n'ignore pas cette case.

Deux créatures séparées par un emplacement vide ne sont plus voisines.

---

### 6.4. AoE et multi-ciblage

Les Skills peuvent utiliser différentes formes de ciblage.

#### 6.4.1. AoE globale

Touche toutes les créatures ennemies vivantes et ciblables.

#### 6.4.2. AoE de ligne

Touche toutes les créatures ciblables d'une ligne.

Sans précision supplémentaire :

> l'AoE cible la première ligne ennemie occupée.

Une AoE de ligne ne déborde jamais automatiquement vers une ligne suivante.

#### 6.4.3. AoE de colonne

Un Skill peut cibler toutes les créatures présentes dans une même colonne.

#### 6.4.4. Splash de proximité

Un Skill peut toucher :

* sa cible ;
* ses voisins directs horizontaux ;
* la créature directement devant ;
* la créature directement derrière.

Les diagonales ne sont jamais incluses.

#### 6.4.5. Multi-cible limité

Un Skill peut cibler un nombre défini de créatures selon une règle explicite.

Exemples :

* 2 ennemis ;
* 3 premiers ennemis ;
* ennemis avec les PV les plus faibles ;
* ennemis aléatoires ;
* etc.

---

### 6.5. Basic Attacks AoE

Une Basic Attack peut être multi-cible ou AoE si sa fiche le prévoit.

Afin de limiter leur puissance :

> une Basic AoE reste confinée à une seule ligne ennemie.

Elle peut par exemple :

* toucher toute la ligne ;
* toucher plusieurs cibles de la ligne ;
* toucher la cible standard et ses voisins horizontaux.

Une Basic ne traverse normalement pas plusieurs lignes.

Les Active et Ultimate peuvent utiliser des AoE plus complexes.

---

### 6.6. Résolution indépendante des cibles

Chaque cible d'une attaque multi-cible ou AoE est résolue indépendamment.

Pour chaque cible :

* jet d'Esquive indépendant ;
* jet de Critique indépendant ;
* calcul de Défense indépendant ;
* résistance élémentaire indépendante ;
* absorption indépendante ;
* bouclier indépendant ;
* application de statut indépendante lorsque nécessaire.

Une même AoE peut donc :

* être esquivée par certaines cibles ;
* Critiquer sur certaines ;
* toucher normalement les autres.

Un effet offensif visant une cible reste soumis à son Esquive même s'il n'inflige aucun dégât, sauf exception explicitement inesquivable.

---

### 6.7. Multi-hit

Pour une attaque comportant plusieurs hits :

* chaque hit possède son propre jet d'Esquive ;
* chaque hit possède son propre jet de Critique.

Pour une Basic Attack multi-hit ou multi-cible, la Basic est considérée comme réussie si au moins un de ses hits touche au moins une cible.

Dans ce cas :

* son gain d'énergie est accordé une seule fois ;
* les compteurs d'Active progressent une seule fois ;

indépendamment du nombre de hits ou de cibles effectivement touchés.

Si tous les hits sont esquivés par toutes les cibles :

* aucune énergie n'est gagnée ;
* les compteurs d'Active ne progressent pas.

### 6.8. Détermination des cibles et état live

L'action à utiliser et ses cibles sont évaluées à partir de l'état live du combat lorsque l'action commence réellement. Les décisions de toutes les créatures prévues au même timestamp ne sont pas figées à l'avance.

Par défaut, les cibles d'un Skill sont déterminées à son lancement et restent les mêmes pendant sa résolution. Un Skill peut explicitement prévoir une nouvelle sélection pour chaque hit ou chaque étape.

Si une cible fixe meurt pendant un multi-hit, les hits restants qui lui étaient destinés sont perdus. Ils ne cherchent une nouvelle cible que lorsque la capacité prévoit des sélections successives.

Une capacité prête sans cible valide n'est pas lancée et conserve son compteur ou son énergie. Le moteur recherche l'action valide suivante selon les priorités.

Les zones de ligne, de colonne ou d'équipe ne sont pas interrompues par les positions vides. Les règles d'adjacence et de proximité peuvent en revanche être rompues par ces positions.

Un ciblage aléatoire utilise la seed RNG déterministe du combat.

---

## 7. Caractéristiques et conventions numériques

### 7.1. Caractéristiques principales

Les 6 caractéristiques principales sont :

* PV ;
* Attaque ;
* Attaque spéciale ;
* Défense ;
* Défense spéciale ;
* Agilité.

Seules ces caractéristiques peuvent recevoir les points de caractéristiques gagnés lors des montées de niveau.

---

### 7.2. Caractéristiques secondaires

Les caractéristiques secondaires système retenues sont :

* Crit ;
* Dégâts critiques ;
* Esquive.

Contrairement aux six caractéristiques principales, elles ne peuvent pas recevoir directement les points de caractéristiques gagnés lors des montées de niveau.

Elles peuvent notamment provenir de :

* valeurs de base de la créature ;
* équipements ;
* Skills ;
* Passives ;
* buffs ;
* debuffs ;
* autres systèmes de progression.

Il n'est pas prévu d'ajouter systématiquement des caractéristiques secondaires comme :

* Puissance de soin ;
* Puissance de bouclier ;
* Vol de vie ;
* Résistance aux CC.

Ces mécaniques sont principalement gérées directement par les Skills.

---

### 7.3. Philosophie des valeurs numériques

Project Awakening privilégie des **valeurs numériques compactes et lisibles**.

L'objectif est d'éviter l'inflation permanente des caractéristiques et des dégâts.

Chaque point doit avoir une valeur perceptible.

Les constantes mathématiques doivent être calibrées autour de cette philosophie.

Les exemples utilisant de très grands nombres pendant la conception ne constituent pas des valeurs de production.

---

### 7.4. Précision des calculs

Le moteur conserve **3 décimales** pour les calculs internes.

L'interface n'affiche normalement pas ces décimales pour les caractéristiques standards.

Les dégâts, soins et protections sont calculés avec cette précision jusqu'à leur application finale.

Lorsqu'une valeur doit réellement modifier des PV ou un Bouclier :

> **ValeurAppliquée = arrondi(ValeurCalculée)**

Avec :

* `ValeurCalculée` : résultat conservé avec 3 décimales jusqu'à l'application finale ;
* `ValeurAppliquée` : entier qui modifie réellement les PV ou le Bouclier ;
* `arrondi` : arrondi à l'entier le plus proche.

Exemples :

* 37,492 → 37 ;
* 37,500 → 38.

---

### 7.5. PV

Les PV utilisent une conversion simple :

> **PVRéels = PointsPV × 10**

Avec :

* `PointsPV` : nombre de points de la caractéristique principale PV ;
* `PVRéels` : quantité de PV maximum fournie au moteur de combat.

Le facteur `10` est une constante système validée. Il permet de conserver des valeurs de caractéristiques compactes tout en utilisant des réserves de PV suffisamment lisibles en combat.

Exemples :

* 10 points de PV → 100 PV ;
* 50 points de PV → 500 PV.

Les Skills manipulant directement les PV utilisent des **valeurs de PV réelles**.

Exemples :

* soigne 80 PV ;
* augmente les PV max de 50 ;
* inflige des dégâts égaux à X % des PV max.

---

### 7.6. Modifications des autres caractéristiques

Toutes les caractéristiques autres que les PV sont modifiées au niveau de leurs **points internes**.

Un modificateur en pourcentage utilise le principe suivant :

> **ValeurModifiée = ValeurActuelle × (1 + ModificateurPourcentage)**

Avec :

* `ValeurActuelle` : nombre de points de la caractéristique au moment où le modificateur est appliqué ;
* `ModificateurPourcentage` : variation exprimée sous forme décimale, par exemple `0,10` pour `+10 %` ;
* `ValeurModifiée` : nouveau nombre de points avant l'application des modificateurs suivants.

Exemple avec le Crit :

Une créature possède :

> 20 points de Crit.

Un Skill donne :

> +10 % Crit.

La nouvelle valeur devient :

> 20 × 1,10 = 22 points de Crit.

Les 22 points sont ensuite convertis par la formule de Crit en chance réelle.

Cela ne signifie jamais :

> +10 points de pourcentage de Critique.

Cette règle s'applique notamment à :

* Attaque ;
* Attaque spéciale ;
* Défense ;
* Défense spéciale ;
* Agilité ;
* Crit ;
* Dégâts critiques ;
* Esquive.

---

### 7.7. Valeur de départ en combat

Le moteur de combat reçoit directement les caractéristiques finales de la créature préparées hors combat.

Ces valeurs intègrent déjà notamment :

* les valeurs de base de la forme actuelle ;
* le multiplicateur de son stade d’évolution, appliqué aux caractéristiques principales et secondaires de base ;
* le multiplicateur de son niveau d’étoiles, appliqué uniquement aux six caractéristiques principales de base ;
* les points distribués, appliqués après ces multiplicateurs ;
* l'équipement ;
* les autres bonus permanents.

Le niveau n’augmente aucune caractéristique automatiquement. Les points de caractéristiques non attribués ne sont pas transmis comme puissance active au combat.

Les effets de l'équipement sont visibles directement sur la fiche de la créature.

---

### 7.8. Modifications chronologiques des caractéristiques

Pendant le combat, les modificateurs sont appliqués dans leur **ordre réel de déclenchement**.

Exemple :

Valeur initiale :

> 30 Attaque.

Puis :

> +20 % Attaque.

Résultat :

> 36.

Puis :

> +5 Attaque.

Résultat :

> 41.

Si l'ordre était inversé :

> 30 + 5 = 35
> 35 × 1,20 = 42.

L'ordre de lancement des effets peut donc réellement modifier le résultat.

Le moteur conserve la liste chronologique des modificateurs encore actifs.

Lorsqu'un modificateur expire ou est retiré :

> la valeur est recalculée en rejouant les modificateurs restants dans leur ordre d'origine.

Une caractéristique ne peut jamais descendre sous 0 point.

---

### 7.9. Modifications jusqu’à la fin du combat

Tous les effets produits pendant un combat sont limités à ce combat. Aucun ne modifie définitivement l'instance ou ne persiste dans le combat suivant.

Certains effets peuvent modifier une caractéristique jusqu'à la fin du combat.

Ces effets :

* ne sont pas des buffs temporaires ;
* ne possèdent pas nécessairement de timer ;
* ne sont pas Dispellables ;
* peuvent être cumulés indéfiniment si le Skill le permet ;
* disparaissent après le combat.

Dans le contexte d'un effet de combat, le terme « permanent » signifie au maximum « jusqu'à la fin du combat ».

Exemple :

> « Augmente les PV max de cette créature de 50 jusqu'à la fin du combat. »

Si cette augmentation est répétée en boucle, elle peut continuer à se cumuler sans limite propre.

Une augmentation de PV max :

* augmente les PV max ;
* ajoute immédiatement la même quantité aux PV actuels.

Le changement d'état suit donc les formules suivantes :

> **NouveauxPVMaximum = AnciensPVMaximum + AugmentationPVMaximum**

> **NouveauxPVActuels = AnciensPVActuels + AugmentationPVMaximum**

Avec :

* `AugmentationPVMaximum` : quantité de PV maximum ajoutée par l'effet ;
* `AnciensPVMaximum` et `AnciensPVActuels` : valeurs avant l'application ;
* `NouveauxPVMaximum` et `NouveauxPVActuels` : valeurs immédiatement après l'application.

Exemple :

> 100 / 200 PV
> +50 PV max
> devient
> 150 / 250 PV.

Cela permet notamment des créatures de scaling dont la puissance augmente avec la durée du combat.

---

### 7.10. Buffs et debuffs

Les buffs et debuffs sont des effets temporaires distincts des modifications permanentes de combat.

Ils peuvent modifier les points de :

* caractéristiques principales ;
* caractéristiques secondaires.

Les modifications successives sont appliquées dans leur ordre réel.

Deux effets en pourcentage sont donc successifs / multiplicatifs.

Pour plusieurs effets successifs :

> **ValeurFinale = ValeurInitiale × (1 + Modificateur1) × (1 + Modificateur2) × …**

Avec :

* `ValeurInitiale` : nombre de points avant l'application de la séquence ;
* `Modificateur1`, `Modificateur2`, etc. : variations successives exprimées sous forme décimale ;
* `ValeurFinale` : résultat obtenu après application de tous les modificateurs dans leur ordre réel.

Exemple :

> +20 %
> puis +30 %

devient :

> ×1,20 puis ×1,30.

---

## 8. Dégâts et interactions élémentaires

### 8.1. Attaque et Attaque spéciale

Les dégâts bruts d'une action sont calculés avant les défenses, les résistances et les autres protections.

La formule standard est :

> **DégâtsBruts = CaractéristiqueOffensive × CoefficientAction**

Avec :

* `CaractéristiqueOffensive` : Attaque pour une action Physique ou Attaque spéciale pour une action Spéciale ;
* `CoefficientAction` : coefficient propre à la Basic Attack, à l'Active ou à l'Ultimate utilisée ;
* `DégâtsBruts` : montant obtenu avant le Critique, la Défense, les résistances et les autres protections applicables.

Les coefficients exacts appartiennent au balancing de chaque action.

Cette formule permet :

* de conserver une relation lisible entre la caractéristique offensive et la puissance de l'action ;
* de différencier les actions d'une même créature grâce à leurs coefficients propres ;
* de faire évoluer les dégâts avec la progression de la caractéristique utilisée.

Les Skills peuvent explicitement utiliser d'autres formules.

Exemples :

* dégâts basés sur les PV max ;
* dégâts basés sur la Défense ;
* dégâts utilisant plusieurs caractéristiques ;
* etc.

---

### 8.1.1. Hit hybride

Une même Basic Attack ou un même Skill peut comporter plusieurs composantes de dégâts, par exemple une composante Physique et une composante Spéciale.

Un hit hybride reste **un seul hit** :

* l’Esquive est résolue une seule fois ;
* le Critique est résolu une seule fois ;
* si le hit est esquivé, toutes ses composantes échouent ;
* les effets liés au hit se déclenchent une seule fois.

Les composantes de dégâts sont cependant calculées séparément. Chaque composante utilise sa caractéristique offensive, sa défense, ses résistances et ses modificateurs applicables, puis leurs résultats constituent ensemble les dégâts du hit.

Cette structure n’autorise aucune formule numérique implicite : la fiche de l’action doit déclarer ses composantes et leurs coefficients.

---

### 8.2. Défense et Défense spéciale

La Défense réduit les dégâts Physiques.

La Défense spéciale réduit les dégâts Spéciaux.

Les deux utilisent une courbe à rendement décroissant selon le principe suivant :

> **RéductionDéfensive = CapDéfensif × CaractéristiqueDéfensive / (CaractéristiqueDéfensive + KDéfensif)**

Puis :

> **DégâtsAprèsDéfense = DégâtsAvantDéfense × (1 − RéductionDéfensive)**

Avec :

* `CaractéristiqueDéfensive` : Défense contre des dégâts Physiques ou Défense spéciale contre des dégâts Spéciaux ;
* `CapDéfensif` : réduction maximale théorique applicable à la catégorie concernée ;
* `KDéfensif` : constante contrôlant la vitesse à laquelle la courbe approche son cap ;
* `RéductionDéfensive` : proportion de dégâts retirée par la caractéristique défensive ;
* `DégâtsAvantDéfense` : montant obtenu après le calcul offensif et les éventuels effets précédant la Défense, dont le Critique lorsqu'il s'applique ;
* `DégâtsAprèsDéfense` : montant restant avant la résistance élémentaire et les autres protections.

Les valeurs exactes des caps et des constantes `K` de Défense et de Défense spéciale restent des paramètres de balancing.

La courbe doit :

* donner de la valeur à chaque point ;
* réduire progressivement le rendement des investissements élevés ;
* approcher un cap sans le dépasser.

---

### 8.3. Agilité

L'Agilité contrôle la vitesse des Basic Attacks.

Chaque Basic Attack possède son propre **intervalle de base**. Il n'existe donc pas d'intervalle universel commun à toutes les créatures.

L'Agilité réduit cet intervalle selon une courbe exponentielle à rendement décroissant.

La réduction de l'intervalle est calculée selon le principe suivant :

> **RéductionIntervalle = RéductionMax × (1 − e^(−Agilité / K))**

Puis :

> **IntervalleAprèsAgilité = IntervalleBaseBasic × (1 − RéductionIntervalle)**

Enfin, un intervalle minimum global est appliqué :

> **IntervalleFinal = max(IntervalleMinimum, IntervalleAprèsAgilité)**

Avec :

* `Agilité` : nombre de points d'Agilité de la créature ;
* `e` : base de la fonction exponentielle ;
* `K` : constante globale contrôlant la vitesse de progression de la courbe ;
* `RéductionMax` : réduction maximale théorique apportée par l'Agilité ;
* `RéductionIntervalle` : proportion de l'intervalle de base retirée par l'Agilité ;
* `IntervalleBaseBasic` : intervalle propre à la Basic Attack concernée ;
* `IntervalleAprèsAgilité` : intervalle obtenu avant l'application de la limite minimale ;
* `IntervalleMinimum` : limite absolue en dessous de laquelle aucun intervalle de Basic Attack ne peut descendre ;
* `IntervalleFinal` : intervalle réellement utilisé après la réduction et l'application de la limite minimale.

Les valeurs exactes de `K`, `RéductionMax` et `IntervalleMinimum` restent des paramètres de balancing.

Cette courbe permet :

* aux premiers points d'Agilité d'avoir un impact perceptible ;
* de ralentir progressivement les gains à haute Agilité ;
* d'empêcher une croissance incontrôlée de la vitesse d'attaque ;
* de conserver des différences naturelles entre une Basic rapide et une Basic lente.

L'Agilité n'augmente pas la chance de Critique.

---

### 8.4. Crit

Le Crit est exprimé en points.

La conversion des points de Crit en chance réelle utilise une courbe à rendement décroissant avec cap :

> **ChanceCrit = CapCrit × Crit / (Crit + KCrit)**

Avec :

* `Crit` : nombre de points de Crit de la créature au moment du jet ;
* `CapCrit` : chance maximale théorique de Critique apportée par cette courbe ;
* `KCrit` : constante contrôlant la vitesse à laquelle la courbe approche son cap ;
* `ChanceCrit` : probabilité finale utilisée pour le jet de Critique.

À `0` point de Crit, la formule produit `0 %` de chance de Critique.

Les créatures disposent normalement déjà de points de Crit de base.

Les valeurs exactes de `CapCrit` et `KCrit` restent des paramètres de balancing.

Cette courbe permet :

* de donner un impact perceptible aux premiers points de Crit ;
* de réduire progressivement le rendement des investissements élevés ;
* d'approcher un cap sans permettre une croissance incontrôlée de la chance de Critique.

---

### 8.5. Dégâts critiques

Les Dégâts critiques augmentent de manière linéaire le multiplicateur appliqué lorsqu'un Critique est réussi.

La formule suit le principe suivant :

> **MultiplicateurCritFinal = MultiplicateurCritBase + PointsDégâtsCritiques × CoefficientDégâtsCritiques**

Avec :

* `PointsDégâtsCritiques` : nombre de points de la caractéristique secondaire Dégâts critiques ;
* `MultiplicateurCritBase` : multiplicateur appliqué à `0` point de Dégâts critiques ;
* `CoefficientDégâtsCritiques` : gain linéaire de multiplicateur apporté par chaque point ;
* `MultiplicateurCritFinal` : multiplicateur utilisé lorsqu'un effet produit un Critique.

Lorsqu'un hit produit un Critique :

> **DégâtsAprèsCritique = DégâtsAvantCritique × MultiplicateurCritFinal**

Avec :

* `DégâtsAvantCritique` : montant offensif avant application du multiplicateur ;
* `DégâtsAprèsCritique` : montant transmis aux étapes défensives suivantes.

Le multiplicateur de base est actuellement prévu autour de `×1,10`, mais sa valeur exacte reste ajustable.

Le coefficient exact reste un paramètre de balancing.

Cette progression :

* reste volontairement lente ;
* conserve la même valeur marginale pour chaque point ;
* ne possède pas de cap système.

---

### 8.6. Esquive

L'Esquive est exprimée en points.

La conversion vers la chance réelle utilise une courbe à rendement décroissant avec cap :

> **ChanceEsquive = CapEsquive × Esquive / (Esquive + KEsquive)**

Avec :

* `Esquive` : nombre de points d'Esquive de la créature au moment du jet ;
* `CapEsquive` : chance maximale théorique d'Esquive apportée par cette courbe ;
* `KEsquive` : constante contrôlant la vitesse à laquelle la courbe approche son cap ;
* `ChanceEsquive` : probabilité finale utilisée pour le jet d'Esquive.

À `0` point d'Esquive, la formule produit `0 %` d'Esquive.

Les créatures possèdent normalement déjà des points d'Esquive de base.

Les valeurs exactes de `CapEsquive` et `KEsquive` restent des paramètres de balancing.

Cette courbe permet :

* de donner un impact perceptible aux premiers points d'Esquive ;
* de réduire progressivement le rendement des investissements élevés ;
* d'approcher un cap sans rendre l'Esquive incontrôlable.

Le cap d'Esquive doit être contrôlé car une Esquive possède plusieurs conséquences.

Lorsqu'une Basic est esquivée :

* aucun dégât ;
* aucune énergie gagnée ;
* aucune progression des compteurs Active ;
* les effets liés au hit ne sont normalement pas appliqués.

Un Skill peut être explicitement **inesquivable**.

---

### 8.7. Ordre Esquive et Critique

Pour un hit standard :

1. jet d'Esquive ;
2. si le hit touche, jet de Critique ;
3. calcul des dégâts.

Aucun jet de Critique n'est effectué sur une attaque esquivée.

---

### 8.8. Critiques autorisés

Peuvent Critiquer :

* Basic directes ;
* Active directes ;
* Ultimate directes ;
* ticks de DoT ;
* dégâts retardés ;
* soins.

Chaque hit d'un multi-hit possède son propre jet de Critique.

Les Boucliers ne Critiquent pas.

Les Absorptions ne Critiquent pas.

Le True Damage ne Critique pas par défaut.

Un Skill peut définir explicitement une exception.

---

### 8.9. Éléments des attaques

Chaque Basic possède un élément.

Chaque Skill possède également son propre élément.

L'élément utilisé pour calculer une résistance est toujours :

> **l'élément de l'attaque réellement utilisée.**

Il ne s'agit pas automatiquement de l'élément de la créature attaquante.

Un Skill peut utiliser un élément différent des 1 ou 2 éléments naturels de sa créature si son design le justifie.

Une attaque peut également être **Neutre / sans élément**.

Une attaque Neutre ne déclenche aucune interaction élémentaire.

---

### 8.10. Résistances élémentaires

Le système élémentaire est principalement **défensif**.

Un avantage élémentaire ne donne pas de bonus offensif automatique.

Lorsqu'un élément de la cible résiste à l'élément de l'attaque :

> **DégâtsAprèsRésistance = DégâtsAvantRésistance × (1 − TauxRésistanceÉlémentaire)**

Avec :

* `DégâtsAvantRésistance` : montant obtenu après la Défense ou montant de True Damage avant l'interaction élémentaire ;
* `TauxRésistanceÉlémentaire` : proportion globale retirée par une résistance élémentaire standard ;
* `DégâtsAprèsRésistance` : montant restant avant les autres réductions, l'Absorption et les Boucliers.

Le `TauxRésistanceÉlémentaire` est identique pour toutes les relations standard. Sa valeur exacte reste un paramètre de balancing.

Cette formule permet :

* de conserver une lecture uniforme de toutes les résistances standard ;
* de séparer l'élément de l'attaque de sa catégorie Physique, Spéciale ou True Damage ;
* d'appliquer la même règle avant les protections suivantes.

Il n'existe pas de résistance automatique lorsqu'une attaque et la cible partagent simplement le même élément.

Un même élément contre lui-même est neutre.

Il n'existe pas d'immunité élémentaire naturelle.

Un Skill peut exceptionnellement créer une immunité spécifique.

---

### 8.11. Créatures bi-élément

Une créature peut avoir 1 ou maximum 2 éléments.

Si un seul de ses éléments résiste à l'attaque :

> **DégâtsAprèsRésistanceSimple = DégâtsAvantRésistance × (1 − TauxRésistanceÉlémentaire)**

Si ses deux éléments résistent :

> **DégâtsAprèsDoubleRésistance = DégâtsAvantRésistance × (1 − TauxRésistanceÉlémentaire) × (1 − TauxRésistanceÉlémentaire)**

Soit, sous une forme condensée :

> **DégâtsAprèsDoubleRésistance = DégâtsAvantRésistance × (1 − TauxRésistanceÉlémentaire)²**

Avec :

* `DégâtsAvantRésistance` : montant entrant avant toute résistance élémentaire ;
* `TauxRésistanceÉlémentaire` : valeur globale d'une résistance standard ;
* `DégâtsAprèsRésistanceSimple` : montant restant lorsqu'un seul élément de la cible résiste ;
* `DégâtsAprèsDoubleRésistance` : montant restant lorsque les deux éléments de la cible résistent.

Exemple avec une valeur théorique de 30 % :

> **DégâtsAprèsDoubleRésistance = DégâtsAvantRésistance × 0,70 × 0,70**

Les résistances ne sont jamais additionnées directement.

---

### 8.12. Table des résistances élémentaires

Élément de la cible → éléments d'attaque auxquels il résiste :

| Élément de la cible | Résiste à                    |
| ------------------- | ---------------------------- |
| Feu                 | Plante, Métal, Ténèbres      |
| Eau                 | Feu, Lumineux, Métal         |
| Plante              | Eau, Terre, Lumineux         |
| Terre               | Électricité, Feu, Eau        |
| Vent                | Terre, Feu, Plante           |
| Électricité         | Vent, Eau, Ténèbres          |
| Métal               | Plante, Terre, Vent          |
| Ténèbres            | Lumineux, Vent, Électricité  |
| Lumineux            | Ténèbres, Électricité, Métal |

Chaque élément possède exactement 3 résistances.

Chaque élément offensif est résisté par exactement 3 éléments.

---

### 8.13. Chaîne de calcul des dégâts standards

Ordre conceptuel :

1. action / hit ;
2. Esquive si applicable ;
3. jet de Critique si applicable ;
4. calcul offensif brut et application éventuelle du multiplicateur Critique ;
5. Défense ou Défense spéciale ;
6. résistance élémentaire ;
7. autres réductions de dégâts ;
8. Absorption ;
9. Bouclier ;
10. PV ;
11. événements déclenchés ;
12. mort éventuelle.

Les valeurs intermédiaires sont conservées avec 3 décimales.

Pour un hit hybride, les étapes offensives, défensives, élémentaires et les autres réductions ou protections applicables à chaque composante sont résolues séparément après l’unique jet d’Esquive et l’unique jet de Critique. Les résultats des composantes constituent ensuite les dégâts du hit.

---

### 8.14. True Damage

Le True Damage ignore :

* Défense ;
* Défense spéciale ;
* réduction générale de dégâts ;
* réduction Physique ;
* réduction Spéciale ;
* effets du type « subit X % de dégâts en moins ».

Le True Damage **n'ignore pas la résistance élémentaire**.

Il reste affecté par :

* résistance élémentaire ;
* Absorption ;
* Bouclier.

Par défaut :

* il peut être esquivé ;
* il ne peut pas Critiquer.

Un Skill peut explicitement rendre un True Damage inesquivable ou autoriser une autre exception.

Chaîne :

1. Esquive si applicable ;
2. pas de Critique par défaut ;
3. montant de True Damage ;
4. résistance élémentaire ;
5. ignore toutes les autres réductions ;
6. Absorption ;
7. Bouclier ;
8. PV.

---

## 9. Soins et protections

### 9.1. Soins

Les soins peuvent Critiquer.

Un soin standard :

* ne peut pas ressusciter une créature morte ;
* ne peut pas dépasser les PV maximum.

Tout surplus de soin est perdu.

L'Overheal n'existe pas comme mécanique générale.

Un Skill peut explicitement créer une mécanique utilisant le surplus de soin.

---

### 9.2. HoT

Les HoT fonctionnent selon les mêmes principes temporels généraux que les DoT.

Ils :

* utilisent le tick global ;
* peuvent avoir plusieurs sources indépendantes ;
* persistent après la mort de leur source ;
* continuent pendant Stun / Glacé / Peur ;
* sont gelés pendant une Exclusion ;
* utilisent un snapshot lors de leur application ;
* peuvent Critiquer à chaque tick.

---

### 9.3. Vol et drain de vie

Le Vol de vie peut restaurer une partie des dégâts réellement infligés.

Il se base sur les dégâts ayant réellement traversé toutes les protections.

La formule standard suit le principe suivant :

> **PVRestaurés = DégâtsRéellementInfligés × TauxVolDeVie**

Avec :

* `DégâtsRéellementInfligés` : quantité de PV effectivement retirée à la cible après toutes les protections ;
* `TauxVolDeVie` : proportion des dégâts réels convertie en soin ;
* `PVRestaurés` : soin produit avant son application finale.

Le taux exact appartient au Skill ou à l'effet qui accorde le Vol de vie.

Exemple avec un taux théorique de 20 % :

> 20 % de Vol de vie
> 500 dégâts réellement infligés
> **PVRestaurés = 500 × 0,20 = 100 PV**

Un Skill peut également utiliser un Drain de vie avec sa propre formule explicite.

---

### 9.4. Boucliers

Un Bouclier est une **réserve universelle de dégâts flat**.

Exemple :

> Bouclier de 100 PV.

Il ne possède pas de type Physique ou Spécial.

Les Boucliers peuvent se stacker.

Chaque application ajoute une nouvelle réserve.

Les Boucliers possèdent une durée.

À expiration :

> toute valeur restante est perdue.

Lorsqu'un dégât doit être appliqué :

> le Bouclier compatible le plus ancien est consommé en premier.

Pour chaque Bouclier consommé, le calcul suit le principe suivant :

> **DégâtsAprèsBouclier = max(0, DégâtsAvantBouclier − ValeurBouclierDisponible)**

> **BouclierRestant = max(0, ValeurBouclierDisponible − DégâtsAvantBouclier)**

Avec :

* `DégâtsAvantBouclier` : montant restant après les étapes précédentes de la chaîne et arrondi au moment de son application au Bouclier ;
* `ValeurBouclierDisponible` : réserve restante du Bouclier actuellement consommé ;
* `DégâtsAprèsBouclier` : montant transmis au Bouclier suivant ou aux PV ;
* `BouclierRestant` : réserve conservée par le Bouclier après l'impact.

Si plusieurs Boucliers sont nécessaires, le même calcul est répété dans leur ordre de consommation.

Les Boucliers sont appliqués avant les PV.

Les Boucliers ne Critiquent pas.

Leur valeur peut dépendre de différentes caractéristiques selon le Skill :

* PV du lanceur ;
* Attaque ;
* Attaque spéciale ;
* Défense ;
* etc.

Il n'existe pas nécessairement de caractéristique système « Puissance de Bouclier ».

---

### 9.5. Absorption

L'Absorption est distincte du Bouclier.

Elle réduit un **pourcentage** de dégâts selon les conditions définies par le Skill.

Lorsqu'elle s'applique, la formule suit le principe suivant :

> **DégâtsAprèsAbsorption = DégâtsAvantAbsorption × (1 − TauxAbsorption)**

Avec :

* `DégâtsAvantAbsorption` : montant obtenu après les réductions précédentes de la chaîne de dégâts ;
* `TauxAbsorption` : proportion de dégâts retirée par l'effet d'Absorption ;
* `DégâtsAprèsAbsorption` : montant transmis aux Boucliers puis, si nécessaire, aux PV.

Le taux et les conditions d'application appartiennent au Skill qui crée l'Absorption.

Exemples :

* absorbe 30 % des dégâts reçus pendant X secondes ;
* absorbe 80 % du prochain Ultimate.

Une Absorption :

* n'est pas une réserve de PV ;
* n'est pas considérée comme un Bouclier ;
* ne se stacke pas avec une nouvelle application du même effet ;
* une nouvelle application identique réinitialise simplement son timer.

Plusieurs Absorptions différentes peuvent potentiellement coexister selon leurs règles.

Elles sont appliquées avant les Boucliers.

---

## 10. Effets périodiques et application des statuts

### 10.1. DoT

Les DoT utilisent une fréquence de tick globale.

Une application initiale peut être esquivée si l'effet qui l'applique est esquivable.

Une fois appliqué :

* les ticks ne peuvent plus être esquivés ;
* chaque tick peut Critiquer ;
* l'effet continue même si sa source meurt ;
* plusieurs sources peuvent créer plusieurs effets indépendants.

Chaque DoT utilise un **snapshot** au moment de son application.

Les modifications ultérieures des caractéristiques de la source ne modifient pas un DoT déjà appliqué.

---

### 10.2. Brûlure

La Brûlure :

* inflige des dégâts périodiques ;
* réduit les soins reçus par la cible.

Des Skills peuvent interagir avec le tag `Brûlure`.

Exemple :

> « Inflige +20 % de dégâts aux cibles Brûlées. »

Les valeurs exactes et règles de stacks seront détaillées ultérieurement.

---

### 10.3. Poison

Le Poison :

* inflige des dégâts périodiques ;
* peut accumuler des stacks ;
* devient progressivement plus puissant avec les stacks.

La progression du Poison doit être accélérée par les stacks mais contrôlée afin d'éviter une croissance incontrôlable.

La formule exacte reste à équilibrer.

Des Skills peuvent interagir spécifiquement avec le tag `Poison`.

---

### 10.4. Saignement

Le Saignement :

* inflige des dégâts périodiques ;
* utilise notamment les PV de la cible dans son calcul.

Il possède donc naturellement une fonction anti-cible à gros PV / anti-tank.

La formule exacte et les éventuels caps spécifiques restent à définir.

Des Skills peuvent interagir avec le tag `Saignement`.

---

### 10.5. Sources multiples de DoT et HoT

Deux créatures différentes appliquant le même type d'effet créent des effets indépendants.

Chaque effet conserve notamment :

* sa source ;
* son snapshot ;
* sa durée ;
* ses stacks éventuels ;
* ses dégâts ou soins propres.

La mort de la source ne supprime pas l'effet.

---

### 10.6. Réapplication des statuts

La règle de réapplication dépend du statut.

Un statut peut :

* refresh sa durée ;
* ajouter de la durée ;
* ajouter des stacks ;
* utiliser une autre règle explicite.

Les règles détaillées doivent être définies par type de statut.

---

### 10.7. Application d’un statut

Deux comportements existent.

#### 10.7.1. Statut lié directement au hit

Exemple :

> « Inflige X dégâts et applique Stun pendant 2 secondes. »

Si l'attaque touche :

* les dégâts sont appliqués ;
* le Stun est appliqué.

Si l'attaque est esquivée :

* aucun dégât ;
* aucun Stun.

Il n'existe pas de second jet d'application caché.

#### 10.7.2. Probabilité explicitement définie

Exemple :

> « Inflige X dégâts et a 40 % de chances d'appliquer Stun pendant 2 secondes. »

Résolution :

1. jet d'Esquive ;
2. si l'attaque touche, dégâts ;
3. jet spécifique de 40 % pour le Stun.

Un Skill inesquivable peut toujours conserver une probabilité indépendante d'application du statut.

#### 10.7.3. Nature d'une probabilité

La description doit préciser si une probabilité est :

* globale pour le déclenchement de la capacité ou d'un effet ;
* testée pour chaque cible ;
* liée à un hit réussi ;
* attachée à une autre unité de résolution explicitement nommée.

Une probabilité globale peut être testée avant les Esquives individuelles des cibles. Aucun jet d'application implicite ne doit être ajouté.

#### 10.7.4. Ordre des effets

Une capacité peut produire plusieurs effets possédant chacun leurs cibles, probabilités, durées et règles propres.

Ils sont résolus dans l'ordre réellement décrit. Un debuff appliqué après le calcul des dégâts d'un hit ne modifie pas rétroactivement ces dégâts. Si la capacité applique explicitement le debuff avant de calculer les dégâts, le nouvel état de la cible peut être utilisé.

---

## 11. Contrôles et autres effets de statut

### 11.1. CC total et tags

Les statuts suivants partagent la même mécanique de CC total :

* Stun ;
* Glacé ;
* Peur.

Ils possèdent cependant leurs propres tags.

Un Skill peut donc interagir spécifiquement avec :

* une cible Stun ;
* une cible Glacée ;
* une cible apeurée.

Ils partagent néanmoins les mêmes règles générales de diminishing returns sur les CC.

---

### 11.2. Diminishing returns des CC

Chaque créature possède son propre historique temporaire de CC.

Lorsqu'elle subit plusieurs CC rapprochés :

> leur durée effective diminue progressivement.

Les CC partageant la même famille mécanique utilisent le même système de diminishing returns.

Cela empêche de contourner le système avec :

> Stun → Glacé → Peur → Stun.

Après X secondes sans nouveau CC :

> la résistance temporaire commence à revenir progressivement à son état normal.

Les valeurs exactes restent à équilibrer.

La diminution porte prioritairement sur la **durée du CC** plutôt que sur sa chance d'application.

---

### 11.3. Immunités aux CC

Un Skill peut donner temporairement une immunité à certains CC ou statuts.

Une immunité bloque totalement l'application.

L'effet n'est pas appliqué avec une durée de 0.

Le jeu peut afficher :

> `Immunisé`.

Il n'existe pas d'immunité naturelle permanente basée uniquement sur l'élément.

---

### 11.4. Silence

Pendant Silence :

* Basic Attacks autorisées ;
* gain d'énergie autorisé ;
* progression des compteurs Active autorisée ;
* Active Skills bloquées ;
* Ultimate bloquée.

Une Active devenue prête pendant Silence reste prête.

Elle est utilisée à la première occasion valide après la fin du Silence.

Une Ultimate ayant atteint son seuil reste également disponible après la fin du Silence.

---

### 11.5. Exclusion

L'Exclusion retire temporairement une créature du combat.

Pendant l'Exclusion :

* aucune action ;
* non ciblable ;
* aucun dégât reçu ;
* aucun soin reçu ;
* aucun nouveau buff ;
* aucun nouveau debuff ;
* timers personnels gelés ;
* DoT gelés ;
* HoT gelés ;
* buffs existants gelés ;
* debuffs existants gelés.

La créature revient ensuite :

* à la même position ;
* avec son état interne conservé ;
* ses timers reprenant là où ils étaient arrêtés.

L'Exclusion ne déclenche pas une mort.

Elle ne compte pas comme créature actuellement présente/ciblable pour une AoE standard.

---

### 11.6. Ralentissement et accélération

Il n'existe pas de système séparé de Slow / Haste.

Un Ralentissement agit directement sur les points d'Agilité.

Une Accélération agit directement sur les points d'Agilité.

Exemples :

> -20 % Agilité
> +30 % Agilité.

La conversion normale de l'Agilité détermine ensuite la vitesse réelle de Basic.

---

### 11.7. Réduction des soins

La réduction des soins reçus peut exister comme debuff indépendant.

La Brûlure utilise également ce type de mécanique.

La réduction des soins doit utiliser un cap système afin d'éviter une réduction incontrôlée, sauf effet exceptionnel explicitement conçu pour fonctionner autrement.

La valeur exacte du cap reste à équilibrer.

---

### 11.8. Cleanse

Cleanse retire des effets négatifs d'un allié. Selon la convention générale, le terme « allié » inclut le lanceur ; « autre allié » l'exclut.

Sans précision supplémentaire :

> un Cleanse retire 1 effet négatif aléatoire.

Un Skill peut définir une règle différente.

Exemples :

* retire tous les DoT ;
* retire 2 debuffs ;
* retire tous les effets négatifs ;
* retire uniquement les CC.

---

### 11.9. Dispel

Dispel retire des effets positifs d'un ennemi.

Sans précision supplémentaire :

> un Dispel retire 1 effet positif aléatoire.

Un Skill peut définir une autre règle.

---

### 11.10. Buff identique réappliqué

Plusieurs buffs provenant de sources différentes peuvent coexister et leurs modifications sont appliquées successivement.

Lorsqu'une même source réapplique exactement le même buff :

> la règle par défaut est de refresh sa durée, sauf si le Skill indique explicitement un stacking.

---

### 11.11. Drain et vol d’énergie

Un Skill peut :

* retirer de l'énergie à une cible ;
* voler de l'énergie ;
* augmenter ou réduire l'énergie générée par une Basic Attack ;
* empêcher temporairement ce gain.

Le Vol d'énergie transfère tout ou partie de l'énergie réellement retirée selon la définition du Skill.

Il n'existe pas de statut général empêchant totalement toute génération d'énergie.

---

### 11.12. Root et Taunt

Il n'existe pas de mécanique générale de :

* Root ;
* Taunt / Provocation.

Les créatures ne se déplacent normalement pas, ce qui rend Root inutile.

Le ciblage défensif repose sur :

* la formation ;
* les lignes ;
* les règles de ciblage ;
* les Skills spécifiques.

---

### 11.13. Snapshot

Les effets périodiques comme les DoT et HoT utilisent un snapshot de leur source.

Lorsqu'un effet est appliqué :

> les paramètres offensifs, de soin et autres valeurs dépendant de la source sont enregistrés à cet instant.

Les modifications ultérieures des caractéristiques de la source ne modifient pas l'effet déjà présent.

Une nouvelle application utilise un nouveau snapshot correspondant à l'état de la source au moment de cette nouvelle application.

En revanche, l'état de la cible reste dynamique.

À chaque tick, le moteur utilise les valeurs et protections actuelles de la cible lorsque celles-ci sont pertinentes, notamment :

* Défense ou Défense spéciale ;
* résistances élémentaires ;
* réductions de dégâts ;
* Absorption ;
* Boucliers ;
* réduction des soins reçus ;
* autres effets défensifs applicables.

Ainsi :

> **la source est snapshotée à l'application, tandis que la cible est recalculée à chaque tick.**

---

## 12. Paramètres à équilibrer ultérieurement

Les décisions structurelles sont validées, mais de nombreux paramètres numériques restent volontairement ouverts.

Notamment :

* valeurs exactes de `CapDéfensif` et `KDéfensif` pour la Défense et la Défense spéciale ;
* valeurs exactes de `K`, `RéductionMax` et `IntervalleMinimum` pour l'Agilité ;
* valeurs exactes de `CapCrit` et `KCrit` ;
* valeurs exactes de `CapEsquive` et `KEsquive` ;
* valeur exacte de `CoefficientDégâtsCritiques` ;
* valeur exacte de `MultiplicateurCritBase`, actuellement prévue autour de `×1,10` ;
* valeur exacte de `TauxRésistanceÉlémentaire` ;
* diminishing returns des CC ;
* durée avant récupération des diminishing returns ;
* durée standard des différents statuts ;
* valeur/cap de réduction des soins ;
* formules exactes de Brûlure ;
* formules exactes de Poison ;
* formules exactes de Saignement ;
* valeurs des Boucliers ;
* durées des Boucliers ;
* valeurs d'Absorption ;
* génération d'énergie des Basic ;
* coefficients des Basic ;
* coefficients des Active ;
* coefficients des Ultimate ;
* autres paramètres d'équilibrage.

Ces éléments devront être déterminés par :

* prototypage ;
* simulation ;
* playtests ;
* équilibrage progressif.

---

## 13. Dépendances et principe d’exception

### 13.1. Documents spécialisés liés

Ce document définit les règles communes du moteur de combat.

Les systèmes spécialisés devront être développés plus précisément dans leurs documents dédiés, notamment :

* [`03-CREATURES.md`](./03-CREATURES.md)
* [`04-SKILLS.md`](./04-SKILLS.md)
* [`05-ELEMENTS.md`](./05-ELEMENTS.md)
* [`06-STATUS_EFFECTS.md`](./06-STATUS_EFFECTS.md)
* `07-EVOLUTIONS.md`
* `08-ITEMS.md`
* `10-PROGRESSION.md`

Ces documents doivent respecter les règles structurelles définies ici et peuvent préciser leurs propres données, valeurs, interactions et exceptions.

---

### 13.2. Principe d’exception explicite

Les règles de ce document constituent le comportement standard du moteur.

Un Skill, une Passive, un statut, un mode de jeu ou une autre mécanique peut créer une exception uniquement si cette exception est **explicitement définie**.

Principe général :

> **règle système simple par défaut, exception clairement décrite lorsqu'un design particulier le nécessite.**

Cette approche doit préserver :

* la lisibilité ;
* la cohérence ;
* la capacité de balancing ;
* la diversité des créatures ;
* la simplicité du moteur ;
* la possibilité de créer des kits originaux sans multiplier inutilement les règles générales.
