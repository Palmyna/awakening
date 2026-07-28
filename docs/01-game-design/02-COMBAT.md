# Combat

> **Statut : draft de conception**
>
> Ce document décrit les règles structurelles du système de combat de Project Awakening.
>
> Les formules, caps, coefficients, durées et valeurs numériques qui ne sont pas explicitement validés restent des paramètres de balancing et pourront évoluer sans remettre en cause les règles structurelles décrites ici.

---

## 1. Principes généraux

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

# 2. Composition des équipes

Une équipe peut contenir jusqu'à **6 créatures**.

Les 6 créatures sont présentes simultanément sur le terrain.

Une équipe utilise une formation composée de :

* 3 lignes ;
* jusqu'à 6 positions par ligne ;
* maximum 6 créatures au total.

Le joueur choisit :

* la ligne de chaque créature ;
* leur ordre gauche → droite dans cette ligne.

Le positionnement exact en colonnes est ensuite géré automatiquement.

---

# 3. Grille de formation

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

# 4. Positions pendant le combat

Les positions restent fixes pendant tout le combat.

Aucun déplacement automatique n'a lieu.

Lorsqu'une créature meurt :

* sa position devient vide ;
* les autres créatures ne se déplacent pas ;
* la formation n'est pas recentrée.

Les espaces vides peuvent donc apparaître pendant un combat, même s'ils sont interdits lors de la préparation de l'équipe.

Un Skill peut exceptionnellement déplacer ou modifier une position si sa description le prévoit explicitement.

---

# 5. Créatures vivantes, présentes et non vivantes

Une créature **vivante et présente dans le combat** peut normalement :

* agir ;
* être ciblée ;
* subir des dégâts ;
* recevoir des soins ;
* recevoir des buffs et debuffs.

Certains effets peuvent modifier temporairement cet état.

## 5.1 Créature morte

Une créature à 0 PV est considérée comme morte.

Elle :

* ne peut plus agir ;
* ne peut plus être ciblée ;
* ne compte plus comme survivante ;
* ne revient pas grâce à un soin classique.

Il n'existe pas de résurrection générale d'un allié.

Seules certaines Passives propres à la créature peuvent permettre une **auto-résurrection**.

## 5.2 Créature exclue

Une créature sous un effet d'Exclusion :

* est toujours vivante ;
* est temporairement retirée du combat ;
* ne peut ni agir ni être ciblée ;
* ne peut recevoir ni dégâts, ni soins, ni buffs, ni debuffs ;
* ne compte pas comme une créature actuellement présente/ciblable.

Ses effets et timers personnels sont gelés pendant l'Exclusion.

## 5.3 Cas du Phoenix / auto-résurrection

Une créature disposant d'une auto-résurrection peut avoir un état intermédiaire, par exemple un Phoenix transformé en œuf.

Dans cet état :

* la créature est considérée comme **non vivante** ;
* elle ne compte pas comme survivante ;
* elle ne peut pas être ciblée ;
* elle ne peut pas agir ;
* elle peut revenir après le délai prévu par sa Passive si le combat n'est pas déjà terminé.

Si toutes les créatures d'une équipe sont non vivantes, le combat se termine immédiatement.

Ainsi, si le Phoenix est la dernière créature et passe en œuf, l'équipe perd avant sa prochaine résurrection.

Une auto-résurrection peut fonctionner plusieurs fois ou indéfiniment si la Passive le prévoit, mais uniquement tant que le combat reste actif.

---

# 6. Début du combat

Sauf indication contraire :

* toutes les créatures commencent à **0 / 100 énergie** ;
* aucun Basic Attack n'est exécuté immédiatement à `0,000 s`.

Les effets « au début du combat » sont résolus à `0,000 s`.

Ils sont appliqués avant le démarrage normal des premières actions.

Ordre déterministe en cas d'effets nécessitant réellement une résolution successive :

1. équipe attaquante ;
2. équipe défenseuse ;
3. dans chaque équipe :

   * ligne 1 gauche → droite ;
   * ligne 2 gauche → droite ;
   * ligne 3 gauche → droite.

---

# 7. Temps de combat

La durée maximale standard d'un combat est de :

**120 secondes de simulation.**

Cette durée est indépendante de la vitesse de visualisation choisie par le joueur.

À la fin du temps réglementaire, la règle de victoire dépend du mode.

## 7.1 Combat standard

Priorités :

Priorités :

1. équipe possédant le plus de créatures vivantes ;
2. si égalité, équipe possédant le meilleur ratio global de PV restants parmi ses survivants ;
3. si égalité parfaite, victoire de l'attaquant.

Le ratio global de PV restants est calculé ainsi :

> somme des PV actuels des survivants / somme des PV maximum de ces mêmes survivants.

Une créature non vivante, comme un Phoenix en œuf, ne compte pas comme survivante.

## 7.2 Modes à objectif

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

# 8. Vitesse de visualisation

Le combat repose sur 120 secondes de **temps de simulation**, indépendamment de sa vitesse d'affichage.

Des vitesses de visualisation accélérées peuvent être proposées comme **services de confort payants**.

Principe prévu :

* ×1 disponible gratuitement ;
* ×2 comme premier palier de confort payant ;
* ×4 comme palier supérieur ;
* possibilité d'acheter directement le palier supérieur ou de payer seulement la différence lors d'un upgrade ;
* prix exacts à définir ultérieurement.

La vitesse peut être modifiée à tout moment pendant le combat, y compris en mode Manuel.

Le jeu mémorise la dernière vitesse utilisée et la réutilise par défaut lors du combat suivant.

Ces options ne changent jamais :

* la durée de simulation ;
* les caractéristiques ;
* les événements ;
* le RNG ;
* la seed ;
* les récompenses ;
* le coût en énergie ;
* le résultat du combat.

Elles modifient uniquement le temps réel nécessaire à la visualisation.

---

# 9. Structure des actions d'une créature

Chaque créature possède :

* 1 Basic Attack ;
* exactement 4 Skills :

  * 3 Skills parmi Active et Passive ;
  * exactement 1 Ultimate.

Le nombre d'Active et de Passive peut varier.

Exemples :

* 1 Active + 2 Passive + 1 Ultimate ;
* 2 Active + 1 Passive + 1 Ultimate.

Le joueur ne choisit pas les Skills de la créature.

Ils font partie de son identité de gameplay.

---

# 10. Basic Attack

Le Basic Attack est une action automatique propre à chaque créature.

Il est représenté sur sa fiche de manière comparable à un Skill.

Il définit notamment :

* son nom ;
* son coefficient de dégâts ;
* la caractéristiques offensive utilisée ;
* sa catégorie de dégâts ;
* son élément ;
* son intervalle de base ;
* son gain d'énergie ;
* son éventuel nombre de hits ;
* son éventuelle règle de ciblage particulière.

## 10.1 Catégorie de dégâts

Un Basic peut être :

* **Physique** ;
* **Spécial**.

Un Basic Physique utilise :

* Attaque ;
* Défense de la cible.

Un Basic Spécial utilise :

* Attaque spéciale ;
* Défense spéciale de la cible.

Un Basic n'est donc pas obligatoirement Physique.

## 10.2 Première attaque

Une créature doit attendre son intervalle complet avant sa première Basic Attack.

Exemple :

> intervalle final = 1,500 s
> première Basic = `1,500 s`.

---

# 11. Active Skills

Les Active Skills sont déclenchés automatiquement selon leur cycle.

Une Active se déclenche après **X Basic Attacks réussies**.

La Basic correspondante est alors remplacée par l'Active.

Si plusieurs Active sont prêtes au même moment, elles sont résolues selon leur ordre défini sur la fiche de la créature.

Une seule Active peut remplacer une même opportunité de Basic Attack.

Les autres Active déjà prêtes restent disponibles et sont utilisées lors des prochaines opportunités d'action, selon leur ordre de priorité.

Une Active :

* ne compte pas elle-même comme Basic ;
* ne fait pas progresser les autres compteurs de Basic, sauf règle explicitement contraire.

Une Basic esquivée :

* ne compte pas dans les compteurs d'Active ;
* ne génère pas d'énergie.

---

# 12. Passive Skills

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

---

# 13. Ultimate

Chaque créature possède exactement **1 Ultimate**.

La jauge d'Ultimate va de :

**0 à 100 énergie.**

Lorsqu'une Ultimate est utilisée :

* la jauge revient de 100 à 0.

La jauge ne peut jamais dépasser 100.

Toute énergie supplémentaire gagnée à 100 est perdue.

## 13.1 Priorité d'action

L'Ultimate utilise la même opportunité d'action qu'une Active ou une Basic Attack.

Elle ne constitue pas une action supplémentaire indépendante entre deux Basics.

Lorsqu'une créature est prête à agir, la priorité standard est :

1. Ultimate prête ;
2. Active prête ;
3. Basic Attack.

Si l'Ultimate est disponible au moment où une Active devait être utilisée :

> l'Ultimate est prioritaire.

L'Active reste prête et sera utilisée lors de la prochaine opportunité d'action valide.

L'action effectivement utilisée remplace la Basic Attack qui aurait normalement eu lieu à cet instant.

Une règle explicite de Skill peut exceptionnellement modifier cette priorité.

## 13.2 Gain d'énergie

La quantité d'énergie générée par une Basic fait partie des propriétés de cette Basic.

Une Basic réussie donne l'énergie indiquée.

Une Basic esquivée :

* ne donne aucune énergie ;
* ne progresse pas les Active.

Sauf effet explicite, seule la créature qui effectue l'action gagne l'énergie liée à sa Basic.

Des Skills ou Passives peuvent :

* ajouter de l'énergie ;
* retirer de l'énergie ;
* voler de l'énergie ;
* modifier la quantité d'énergie générée.

## 13.3 Auto

En mode Auto :

> l'Ultimate est utilisée immédiatement dès que la jauge atteint 100.

## 13.4 Manuel

En mode Manuel :

* le joueur peut conserver son Ultimate à 100 ;
* aucune énergie supplémentaire ne peut être stockée au-delà de 100 ;
* le joueur choisit le moment de son déclenchement.

La vitesse de visualisation peut être changée même en mode Manuel.

---

# 14. Timers et contrôle

Les actions se déroulent sur une timeline continue.

Par défaut :

* les Active et Ultimate sont résolues instantanément au moment de leur déclenchement ;
* il n'existe pas de channeling ou cast time général.

Un Skill peut explicitement définir :

* un délai ;
* une bombe retardée ;
* un effet périodique ;
* une autre temporalité particulière.

## 14.1 Crowd Control total

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

## 14.2 Égalité temporelle avec un CC

Si un CC empêchant une action et l'action elle-même sont programmés exactement au même timestamp :

> le CC empêchant l'action est prioritaire.

---

# 15. Événements simultanés

Tous les événements déclenchés au même timestamp forment un bloc temporel commun.

Lorsque l'ordre est réellement nécessaire, l'ordre de position peut être utilisé :

1. ligne 1 gauche → droite ;
2. ligne 2 gauche → droite ;
3. ligne 3 gauche → droite.

Cependant, des dégâts déjà déclenchés au même timestamp sont considérés comme simultanés.

Deux créatures peuvent donc s'éliminer mutuellement au même timestamp.

Si les deux équipes remplissent simultanément leur condition de défaite :

> l'attaquant remporte le combat.

---

# 16. Ciblage standard des Basic Attacks

Le ciblage standard fonctionne comme suit.

## 16.1 Ligne prioritaire

Le moteur identifie la **première ligne ennemie occupée**.

Les Basics standards ne ciblent normalement que cette ligne.

## 16.2 Ordre des cibles

Les cibles valides de la ligne sont ordonnées :

> gauche → droite.

## 16.3 Ordre des attaquants

Les attaquants sont ordonnés :

1. ligne 1 gauche → droite ;
2. ligne 2 gauche → droite ;
3. ligne 3 gauche → droite.

## 16.4 Distribution cyclique

Les attaquants sont distribués cycliquement parmi les cibles valides.

Exemples avec 6 attaquants :

* 1 cible → 6 attaques sur elle ;
* 2 cibles → 3 / 3 ;
* 3 cibles → 2 / 2 / 2 ;
* 4 cibles → 2 / 2 / 1 / 1 ;
* 6 cibles → 1 attaque chacune.

Le ciblage est recalculé lorsqu'une cible meurt ou que la composition de la ligne change.

---

# 17. Priorité des règles de ciblage

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

---

# 18. Voisinage et géométrie

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

# 19. AoE et multi-ciblage

Les Skills peuvent utiliser différentes formes de ciblage.

## 19.1 AoE globale

Touche toutes les créatures ennemies vivantes et ciblables.

## 19.2 AoE de ligne

Touche toutes les créatures ciblables d'une ligne.

Sans précision supplémentaire :

> l'AoE cible la première ligne ennemie occupée.

Une AoE de ligne ne déborde jamais automatiquement vers une ligne suivante.

## 19.3 AoE de colonne

Un Skill peut cibler toutes les créatures présentes dans une même colonne.

## 19.4 Splash de proximité

Un Skill peut toucher :

* sa cible ;
* ses voisins directs horizontaux ;
* la créature directement devant ;
* la créature directement derrière.

Les diagonales ne sont jamais incluses.

## 19.5 Multi-cible limité

Un Skill peut cibler un nombre défini de créatures selon une règle explicite.

Exemples :

* 2 ennemis ;
* 3 premiers ennemis ;
* ennemis avec les PV les plus faibles ;
* ennemis aléatoires ;
* etc.

---

# 20. Basic Attacks AoE

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

# 21. Résolution indépendante des cibles

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

---

# 22. Multi-hit

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

---

# 23. Caractéristiques principales

Les 6 caractéristiques principales sont :

* PV ;
* Attaque ;
* Attaque spéciale ;
* Défense ;
* Défense spéciale ;
* Agilité.

Seules ces caractéristiques peuvent recevoir les points de caractéristiques gagnés lors des montées de niveau.

---

# 24. Caractéristiques secondaires

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

# 25. Philosophie des valeurs numériques

Project Awakening privilégie des **valeurs numériques compactes et lisibles**.

L'objectif est d'éviter l'inflation permanente des caractéristiques et des dégâts.

Chaque point doit avoir une valeur perceptible.

Les constantes mathématiques doivent être calibrées autour de cette philosophie.

Les exemples utilisant de très grands nombres pendant la conception ne constituent pas des valeurs de production.

---

# 26. Précision des calculs

Le moteur conserve **3 décimales** pour les calculs internes.

L'interface n'affiche normalement pas ces décimales pour les caractéristiques standards.

Les dégâts, soins et protections sont calculés avec cette précision jusqu'à leur application finale.

Lorsqu'une valeur doit réellement modifier des PV ou un Bouclier :

> elle est arrondie à l'entier le plus proche.

Exemples :

* 37,492 → 37 ;
* 37,500 → 38.

---

# 27. PV

Les PV utilisent une conversion simple :

> **1 point de PV = 10 PV réels.**

Exemples :

* 10 points de PV → 100 PV ;
* 50 points de PV → 500 PV.

Les Skills manipulant directement les PV utilisent des **valeurs de PV réelles**.

Exemples :

* soigne 80 PV ;
* augmente les PV max de 50 ;
* inflige des dégâts égaux à X % des PV max.

---

# 28. Modifications des autres caractéristiques

Toutes les caractéristiques autres que les PV sont modifiées au niveau de leurs **points internes**.

Exemple :

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

# 29. Valeur de départ en combat

Le moteur de combat reçoit directement les caractéristiques finales de la créature préparées hors combat.

Ces valeurs intègrent déjà notamment :

* les valeurs de base ;
* le niveau ;
* les points distribués ;
* l'évolution ;
* les étoiles ;
* l'équipement ;
* les autres bonus permanents.

Les effets de l'équipement sont visibles directement sur la fiche de la créature.

---

# 30. Modifications chronologiques des caractéristiques

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

# 31. Modifications jusqu'à la fin du combat

Certains effets peuvent modifier une caractéristique jusqu'à la fin du combat.

Ces effets :

* ne sont pas des buffs temporaires ;
* ne possèdent pas nécessairement de timer ;
* ne sont pas Dispellables ;
* peuvent être cumulés indéfiniment si le Skill le permet ;
* disparaissent après le combat.

Exemple :

> « Augmente les PV max de cette créature de 50 jusqu'à la fin du combat. »

Si cette augmentation est répétée en boucle, elle peut continuer à se cumuler sans limite propre.

Une augmentation de PV max :

* augmente les PV max ;
* ajoute immédiatement la même quantité aux PV actuels.

Exemple :

> 100 / 200 PV
> +50 PV max
> devient
> 150 / 250 PV.

Cela permet notamment des créatures de scaling dont la puissance augmente avec la durée du combat.

---

# 32. Buffs et debuffs

Les buffs et debuffs sont des effets temporaires distincts des modifications permanentes de combat.

Ils peuvent modifier les points de :

* caractéristiques principales ;
* caractéristiques secondaires.

Les modifications successives sont appliquées dans leur ordre réel.

Deux effets en pourcentage sont donc successifs / multiplicatifs.

Exemple :

> +20 %
> puis +30 %

devient :

> ×1,20 puis ×1,30.

---

# 33. Attaque et Attaque spéciale

Formule standard :

> **Dégâts bruts = caractéristique offensive × coefficient de l'action.**

Une action Physique utilise :

> Attaque.

Une action Spéciale utilise :

> Attaque spéciale.

Les Skills peuvent explicitement utiliser d'autres formules.

Exemples :

* dégâts basés sur les PV max ;
* dégâts basés sur la Défense ;
* dégâts utilisant plusieurs caractéristiques ;
* etc.

---

# 34. Défense et Défense spéciale

La Défense réduit les dégâts Physiques.

La Défense spéciale réduit les dégâts Spéciaux.

Les deux utilisent une courbe à rendement décroissant de type :

> **Réduction = Cap × Défense / (Défense + K)**

La valeur exacte :

* du cap ;
* de K ;

reste à déterminer pendant le balancing.

La courbe doit :

* donner de la valeur à chaque point ;
* réduire progressivement le rendement des investissements élevés ;
* approcher un cap sans le dépasser.

Le même principe s'applique à Défense spéciale.

---

# 35. Agilité

L'Agilité contrôle la vitesse des Basic Attacks.

Chaque Basic possède son propre intervalle de base.

L'Agilité réduit cet intervalle selon une **courbe exponentielle à rendement décroissant**.

Principe conceptuel :

> plus l'Agilité augmente, plus la Basic devient rapide, mais chaque point supplémentaire apporte progressivement moins de réduction.

Il existe un **intervalle minimal absolu** qu'aucune Basic ne peut dépasser.

La valeur exacte de ce minimum reste à équilibrer.

L'Agilité n'augmente pas le Crit.

---

# 36. Crit

Le Crit est exprimé en points.

À :

> 0 point de Crit = 0 % de chance de Critique.

Les créatures disposent normalement déjà de points de Crit de base.

La conversion des points de Crit en chance réelle utilise une courbe à rendement décroissant avec cap, similaire dans son principe à la Défense :

> **Chance Crit = CapCrit × Crit / (Crit + KCrit)**

Les constantes sont des paramètres de balancing.

---

# 37. Dégâts critiques

Le multiplicateur Critique de base est prévu autour de :

> **×1,10 à 0 point de Dégâts critiques.**

La valeur finale exacte pourra être ajustée.

Contrairement au Crit ou à l'Esquive :

* les Dégâts critiques progressent de manière **linéaire** ;
* la progression est volontairement lente ;
* il n'existe pas de cap système.

Principe :

> Multiplicateur Crit = multiplicateur de base + PointsCritDamage × coefficient.

Le coefficient exact sera défini pendant le balancing.

---

# 38. Esquive

L'Esquive est exprimée en points.

À :

> 0 point d'Esquive = 0 % d'Esquive.

Les créatures possèdent normalement déjà des points d'Esquive de base.

La conversion vers la chance réelle utilise une courbe à rendement décroissant avec cap :

> **Chance Esquive = CapEsquive × Esquive / (Esquive + KEsquive)**

Le cap d'Esquive doit être contrôlé car une Esquive possède plusieurs conséquences.

Lorsqu'une Basic est esquivée :

* aucun dégât ;
* aucune énergie gagnée ;
* aucune progression des compteurs Active ;
* les effets liés au hit ne sont normalement pas appliqués.

Un Skill peut être explicitement **inesquivable**.

---

# 39. Ordre Esquive / Critique

Pour un hit standard :

1. jet d'Esquive ;
2. si le hit touche, jet de Critique ;
3. calcul des dégâts.

Aucun jet de Critique n'est effectué sur une attaque esquivée.

---

# 40. Critiques autorisés

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

# 41. Éléments des attaques

Chaque Basic possède un élément.

Chaque Skill possède également son propre élément.

L'élément utilisé pour calculer une résistance est toujours :

> **l'élément de l'attaque réellement utilisée.**

Il ne s'agit pas automatiquement de l'élément de la créature attaquante.

Un Skill peut utiliser un élément différent des 1 ou 2 éléments naturels de sa créature si son design le justifie.

Une attaque peut également être **Neutre / sans élément**.

Une attaque Neutre ne déclenche aucune interaction élémentaire.

---

# 42. Résistances élémentaires

Le système élémentaire est principalement **défensif**.

Un avantage élémentaire ne donne pas de bonus offensif automatique.

Lorsqu'un élément de la cible résiste à l'élément de l'attaque :

> les dégâts reçus sont réduits selon une valeur globale de résistance élémentaire.

Cette valeur est la même pour toutes les relations standard et constitue un paramètre de balancing.

Il n'existe pas de résistance automatique lorsqu'une attaque et la cible partagent simplement le même élément.

Un même élément contre lui-même est neutre.

Il n'existe pas d'immunité élémentaire naturelle.

Un Skill peut exceptionnellement créer une immunité spécifique.

---

# 43. Créatures bi-élément

Une créature peut avoir 1 ou maximum 2 éléments.

Si un seul de ses éléments résiste à l'attaque :

> la résistance est appliquée une fois.

Si ses deux éléments résistent :

> les deux résistances sont appliquées successivement / multiplicativement.

Exemple avec une valeur théorique de 30 % :

> dégâts ×0,70 ×0,70.

Les résistances ne sont jamais additionnées directement.

---

# 44. Tableau des résistances élémentaires

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

# 45. Chaîne de calcul des dégâts standards

Ordre conceptuel :

1. action / hit ;
2. Esquive si applicable ;
3. Critique si applicable ;
4. calcul offensif brut ;
5. Défense ou Défense spéciale ;
6. résistance élémentaire ;
7. autres réductions de dégâts ;
8. Absorption ;
9. Bouclier ;
10. PV ;
11. événements déclenchés ;
12. mort éventuelle.

Les valeurs intermédiaires sont conservées avec 3 décimales.

---

# 46. True Damage

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

# 47. Soins

Les soins peuvent Critiquer.

Un soin standard :

* ne peut pas ressusciter une créature morte ;
* ne peut pas dépasser les PV maximum.

Tout surplus de soin est perdu.

L'Overheal n'existe pas comme mécanique générale.

Un Skill peut explicitement créer une mécanique utilisant le surplus de soin.

---

# 48. HoT

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

# 49. Vol et drain de vie

Le Vol de vie peut restaurer une partie des dégâts réellement infligés.

Il se base sur les dégâts ayant réellement traversé toutes les protections.

Exemple :

> 20 % de Vol de vie
> 500 dégâts réellement infligés
> → 100 PV restaurés.

Un Skill peut également utiliser un Drain de vie avec sa propre formule explicite.

---

# 50. Boucliers

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

# 51. Absorption

L'Absorption est distincte du Bouclier.

Elle réduit un **pourcentage** de dégâts selon les conditions définies par le Skill.

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

# 52. DoT

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

# 53. Brûlure

La Brûlure :

* inflige des dégâts périodiques ;
* réduit les soins reçus par la cible.

Des Skills peuvent interagir avec le tag `Brûlure`.

Exemple :

> « Inflige +20 % de dégâts aux cibles Brûlées. »

Les valeurs exactes et règles de stacks seront détaillées ultérieurement.

---

# 54. Poison

Le Poison :

* inflige des dégâts périodiques ;
* peut accumuler des stacks ;
* devient progressivement plus puissant avec les stacks.

La progression du Poison doit être accélérée par les stacks mais contrôlée afin d'éviter une croissance incontrôlable.

La formule exacte reste à équilibrer.

Des Skills peuvent interagir spécifiquement avec le tag `Poison`.

---

# 55. Saignement

Le Saignement :

* inflige des dégâts périodiques ;
* utilise notamment les PV de la cible dans son calcul.

Il possède donc naturellement une fonction anti-cible à gros PV / anti-tank.

La formule exacte et les éventuels caps spécifiques restent à définir.

Des Skills peuvent interagir avec le tag `Saignement`.

---

# 56. Sources multiples de DoT / HoT

Deux créatures différentes appliquant le même type d'effet créent des effets indépendants.

Chaque effet conserve notamment :

* sa source ;
* son snapshot ;
* sa durée ;
* ses stacks éventuels ;
* ses dégâts ou soins propres.

La mort de la source ne supprime pas l'effet.

---

# 57. Réapplication des statuts

La règle de réapplication dépend du statut.

Un statut peut :

* refresh sa durée ;
* ajouter de la durée ;
* ajouter des stacks ;
* utiliser une autre règle explicite.

Les règles détaillées doivent être définies par type de statut.

---

# 58. Application d'un statut

Deux comportements existent.

## 58.1 Statut lié directement au hit

Exemple :

> « Inflige X dégâts et applique Stun pendant 2 secondes. »

Si l'attaque touche :

* les dégâts sont appliqués ;
* le Stun est appliqué.

Si l'attaque est esquivée :

* aucun dégât ;
* aucun Stun.

Il n'existe pas de second jet d'application caché.

## 58.2 Probabilité explicitement définie

Exemple :

> « Inflige X dégâts et a 40 % de chances d'appliquer Stun pendant 2 secondes. »

Résolution :

1. jet d'Esquive ;
2. si l'attaque touche, dégâts ;
3. jet spécifique de 40 % pour le Stun.

Un Skill inesquivable peut toujours conserver une probabilité indépendante d'application du statut.

---

# 59. CC total et tags

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

# 60. Diminishing returns des CC

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

# 61. Immunités aux CC

Un Skill peut donner temporairement une immunité à certains CC ou statuts.

Une immunité bloque totalement l'application.

L'effet n'est pas appliqué avec une durée de 0.

Le jeu peut afficher :

> `Immunisé`.

Il n'existe pas d'immunité naturelle permanente basée uniquement sur l'élément.

---

# 62. Silence

Pendant Silence :

* Basic Attacks autorisées ;
* gain d'énergie autorisé ;
* progression des compteurs Active autorisée ;
* Active Skills bloquées ;
* Ultimate bloquée.

Une Active devenue prête pendant Silence reste prête.

Elle est utilisée à la première occasion valide après la fin du Silence.

Une Ultimate à 100 reste également disponible après la fin du Silence.

---

# 63. Exclusion

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

# 64. Ralentissement et accélération

Il n'existe pas de système séparé de Slow / Haste.

Un Ralentissement agit directement sur les points d'Agilité.

Une Accélération agit directement sur les points d'Agilité.

Exemples :

> -20 % Agilité
> +30 % Agilité.

La conversion normale de l'Agilité détermine ensuite la vitesse réelle de Basic.

---

# 65. Réduction des soins

La réduction des soins reçus peut exister comme debuff indépendant.

La Brûlure utilise également ce type de mécanique.

La réduction des soins doit utiliser un cap système afin d'éviter une réduction incontrôlée, sauf effet exceptionnel explicitement conçu pour fonctionner autrement.

La valeur exacte du cap reste à équilibrer.

---

# 66. Cleanse

Cleanse retire des effets négatifs d'un allié ou de soi-même.

Sans précision supplémentaire :

> un Cleanse retire 1 effet négatif aléatoire.

Un Skill peut définir une règle différente.

Exemples :

* retire tous les DoT ;
* retire 2 debuffs ;
* retire tous les effets négatifs ;
* retire uniquement les CC.

---

# 67. Dispel

Dispel retire des effets positifs d'un ennemi.

Sans précision supplémentaire :

> un Dispel retire 1 effet positif aléatoire.

Un Skill peut définir une autre règle.

---

# 68. Buff identique réappliqué

Plusieurs buffs provenant de sources différentes peuvent coexister et leurs modifications sont appliquées successivement.

Lorsqu'une même source réapplique exactement le même buff :

> la règle par défaut est de refresh sa durée, sauf si le Skill indique explicitement un stacking.

---

# 69. Drain et vol d'énergie

Un Skill peut :

* retirer de l'énergie à une cible ;
* voler de l'énergie ;
* augmenter la génération d'énergie ;
* réduire la génération d'énergie.

Le Vol d'énergie transfère tout ou partie de l'énergie réellement retirée selon la définition du Skill.

Il n'existe pas de statut général empêchant totalement toute génération d'énergie.

---

# 70. Root et Taunt

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

# 71. Snapshot

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

# 72. Éléments à équilibrer ultérieurement

Les décisions structurelles sont validées, mais de nombreux paramètres numériques restent volontairement ouverts.

Notamment :

* cap de Défense ;
* cap de Défense spéciale ;
* constantes K de Défense ;
* constante et courbe exacte d'Agilité ;
* intervalle minimal absolu des Basic ;
* cap de Crit ;
* constante K du Crit ;
* cap d'Esquive ;
* constante K de l'Esquive ;
* coefficient linéaire de Dégâts critiques ;
* valeur exacte du multiplicateur Critique de base autour de ×1,10 ;
* résistance élémentaire standard ;
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

# 73. Documents spécialisés liés

Ce document définit les règles communes du moteur de combat.

Les systèmes spécialisés devront être développés plus précisément dans leurs documents dédiés, notamment :

* `03-CREATURES.md`
* `04-SKILLS.md`
* `05-ELEMENTS.md`
* `06-STATUS_EFFECTS.md`
* `07-EVOLUTIONS.md`
* `08-ITEMS.md`
* `10-PROGRESSION.md`

Ces documents doivent respecter les règles structurelles définies ici et peuvent préciser leurs propres données, valeurs, interactions et exceptions.

---

# 74. Principe d'exception explicite

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
