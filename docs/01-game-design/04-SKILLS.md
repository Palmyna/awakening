# Project Awakening — Skills

**Statut :** Rédigé — référence actuelle, à maintenir à jour

## 1. Rôle et périmètre du document

Ce document définit la conception du système de capacités des créatures de **Project Awakening** : la Basic Attack, les Active, les Passive et l’Ultimate.

Il constitue la référence actuelle pour :

* la structure fixe de l’ensemble de capacités d’une créature ;
* les moteurs de disponibilité et de déclenchement propres à chaque catégorie ;
* les interactions entre Skills, énergie et opportunités d’action ;
* les règles générales de ciblage et de résolution portées par les capacités ;
* les conventions de rédaction et de données des fiches de capacités ;
* la continuité des capacités entre les formes et les branches d’une famille.

Il complète les [règles de combat](./02-COMBAT.md), les [règles des créatures](./03-CREATURES.md), les [éléments](./05-ELEMENTS.md) et les [Effets de combat](./06-COMBAT_EFFECTS.md) sans les remplacer.

Il ne constitue :

* ni une liste exhaustive des capacités concrètes des créatures ;
* ni une base de données de production ;
* ni une spécification technique d’implémentation ;
* ni un document d’équilibrage détaillé.

Les règles communes du moteur, dont les formules, la timeline et la résolution numérique, appartiennent au document Combat. Les données propres à chaque capacité devront être conservées dans les sources de production appropriées.

## 2. Structure et identité des capacités

### 2.1. Ensemble fixe

Chaque créature possède :

* une **Basic Attack**, distincte de ses Skills ;
* exactement quatre **Skills** prédéfinis.

Parmi les quatre Skills :

* exactement un est une Ultimate ;
* les trois autres utilisent obligatoirement l’une des deux répartitions suivantes :

  * une Active et deux Passive ;
  * deux Active et une Passive.

Une créature possède donc toujours au moins une Active, au moins une Passive et exactement une Ultimate. Les répartitions comprenant trois Active ou trois Passive ne sont pas autorisées.

Le joueur ne choisit pas ces capacités dans une liste, ne les remplace pas et ne sélectionne pas d’ensemble alternatif. Elles font partie de l’identité fonctionnelle de la famille.

### 2.2. Catégorie persistante

La catégorie d’un Skill appartient à son identité :

* une Active reste une Active ;
* une Passive reste une Passive ;
* une Ultimate reste une Ultimate.

Une évolution ou une branche ne transforme pas un Skill d’une catégorie en une autre.

### 2.3. Continuité entre les formes

La Basic Attack et les quatre Skills conservent une continuité conceptuelle à travers les formes et les branches d’une famille.

Une nouvelle forme peut simplement enrichir une capacité existante, notamment par :

* ses coefficients ;
* ses résultats directs et Effets de combat ;
* ses cibles ;
* son nombre de hits ;
* sa durée ;
* ses probabilités.

Une évolution ou une branche peut aussi transformer fortement la fonction d’une capacité lorsque cette transformation reste cohérente avec l’évolution de la créature. Un même Skill familial peut, par exemple, devenir principalement offensif dans une branche et principalement curatif dans une autre.

La continuité d’identité prime sur la conservation stricte de la fonction initiale. Une capacité ne doit pas être remplacée arbitrairement par une capacité sans relation conceptuelle.

La continuité du nom constitue la norme, mais pas une obligation absolue. Un nom très différent reste possible lorsqu’il exprime plus naturellement une transformation cohérente de la capacité.

### 2.4. Trois moteurs structurels

Les trois catégories de Skills reposent sur des moteurs distincts :

* **Active** : cycle fondé sur les Basic Attacks réussies ;
* **Passive** : événements, conditions ou combinaison des deux ;
* **Ultimate** : énergie.

Cette séparation est structurelle, même lorsqu’une capacité particulière modifie explicitement certaines règles de son moteur.

## 3. Basic Attack

### 3.1. Fonction générale

La Basic Attack est une action offensive automatique. Elle inflige toujours des dégâts ; une Basic Attack entièrement utilitaire et sans dégât n’est pas prévue.

Elle peut néanmoins produire des effets supplémentaires, par exemple :

* appliquer ou retirer un Effet de combat ;
* soigner ;
* accorder un buff ou un Bouclier ;
* déclencher un effet intégré ;
* activer une autre mécanique explicitement définie.

Une Basic Attack peut être mono-cible, multi-cible, multi-hit ou AoE. Elle peut infliger des dégâts Physiques, Spéciaux, hybrides, True Damage ou utiliser une autre formule explicitement déclarée.

Elle possède notamment son propre intervalle, exactement un des neuf éléments officiels, son ciblage, ses composantes de dégâts, son éventuel nombre de hits et son gain d’énergie.

### 3.2. Basic Attack réussie

Une Basic Attack réussie :

* fournit normalement l’énergie déclarée par cette Basic Attack ;
* fait progresser d’une unité chaque compteur d’Active qui n’est pas déjà prêt ;
* déclenche les effets qui dépendent explicitement d’une Basic Attack réussie.

Une Basic Attack multi-hit ou multi-cible est considérée comme réussie si au moins un hit touche au moins une cible.

Son énergie et la progression de ses compteurs d’Active sont alors accordées une seule fois, quel que soit le nombre de hits ou de cibles touchés. Un hit non esquivé reste touché lorsque ses effets sont ensuite annulés par une immunité élémentaire. Si tous les hits sont esquivés, la Basic Attack n’accorde ni énergie, ni progression d’Active, ni effet exigeant une Basic Attack réussie.

Les règles détaillées de l’intervalle, de l’Esquive et de la résolution des hits appartiennent au [document Combat](./02-COMBAT.md).

## 4. Active

### 4.1. Compteur et disponibilité

Chaque Active possède un seuil propre exprimé en nombre de Basic Attacks réussies.

Lorsqu’une créature possède deux Active :

* chacune possède son compteur indépendant ;
* une même Basic Attack réussie fait progresser les deux compteurs en parallèle ;
* plusieurs Active peuvent devenir prêtes simultanément.

Une fois son seuil atteint, une Active reste prête. Son compteur est bloqué à sa valeur maximale et n’accumule aucun dépassement.

### 4.2. Lancement et remise à zéro

Une Active prête est utilisée lorsqu’elle obtient la priorité à une opportunité d’action valide.

Dès que son lancement commence, son compteur revient à zéro, même si :

* le Skill rate ;
* sa cible esquive ;
* tous ses hits sont esquivés ;
* aucune cible n’est finalement touchée.

Le compteur mesure le cycle nécessaire pour lancer l’Active, non le succès de sa résolution.

Une Active ne constitue pas une Basic Attack et ne fait pas progresser par défaut les compteurs d’Active. Une exception doit être explicitement définie par la capacité concernée.

### 4.3. Plusieurs Active prêtes

Si plusieurs Active sont prêtes, leur ordre prédéfini sur la fiche de la créature détermine leur priorité.

Une seule action est utilisée à chaque opportunité. Les autres Active restent prêtes et peuvent être utilisées lors des opportunités suivantes. Aucune Basic Attack ne doit obligatoirement être insérée entre deux Skills prêts.

### 4.4. Modification d’un cycle

Une capacité peut explicitement :

* réduire ou augmenter le seuil d’une Active ;
* ajouter de la progression à son cycle ;
* modifier sa progression ou sa remise à zéro ;
* faire évoluer son seuil après certains événements.

Ces comportements ne constituent pas la règle standard.

Le compteur ne représente pas une ressource ennemie normalement manipulable. Une mécanique adverse ne retire pas rétroactivement des Basic Attacks déjà accomplies. Elle peut en revanche ralentir indirectement l’accès à l’Active, par exemple en réduisant l’Agilité et donc la fréquence des Basic Attacks.

## 5. Passive et effets intégrés

### 5.1. Déclenchement d’une Passive

Une Passive fonctionne à partir :

* d’un événement ;
* d’une condition ;
* ou d’une combinaison des deux.

Elle n’occupe normalement pas une opportunité d’action comme une Active ou une Ultimate.

Une Passive peut contenir plusieurs effets et plusieurs conditions cohérentes. Elle peut se déclencher autant de fois que sa description le prévoit. Ses limitations peuvent notamment être exprimées en temps, en Basic Attacks réussies, en utilisations de Skills, en événements, en nombre maximal de déclenchements ou par toute autre règle explicite.

### 5.2. Granularité des événements

La description doit préciser l’événement observé.

Un déclenchement « à chaque instance de dégâts reçue » peut se produire plusieurs fois pendant un Skill multi-hit. Un déclenchement « lorsqu’une Active est lancée contre cette créature » ne se produit qu’une fois pour cette Active, quel que soit son nombre de hits.

Les termes `hit`, `instance de dégâts`, `Basic Attack`, `Active`, `Ultimate`, `utilisation d’un Skill` et `cible touchée` ne sont donc pas interchangeables.

### 5.3. Mort, auras et effets appliqués

Une Passive peut être explicitement déclenchée par la mort de son porteur. La mort n’empêche pas la résolution d’un effet dont elle constitue précisément le déclencheur, notamment une auto-résurrection ou un effet à la mort.

Une aura dépendant de la présence de son porteur cesse lorsque sa condition n’est plus remplie. À l’inverse, un effet déjà appliqué avec sa propre durée ne disparaît pas automatiquement lorsque sa source meurt.

### 5.4. Effets intégrés à une autre capacité

Une Basic Attack, une Active ou une Ultimate peut posséder un effet déclenché, persistant ou conditionnel sans devenir une Passive.

La catégorie de la capacité reste inchangée. La documentation doit parler d’**effet intégré**, d’**effet déclenché** ou d’**effet persistant**, plutôt que de présenter cet effet comme une Passive supplémentaire.

## 6. Élément des capacités et de leurs effets

### 6.1. Élément obligatoire et indépendant

La Basic Attack et chacun des quatre Skills, y compris les Passive, possèdent exactement un des neuf éléments officiels.

L’élément d’une capacité est indépendant du ou des éléments de sa créature. Une capacité conserve un seul élément à un instant donné, y compris lorsqu’elle est multi-hit, multi-cible, AoE, hybride ou composée de plusieurs effets.

### 6.2. Héritage et snapshot

Tous les résultats directs et Effets de combat produits par une capacité héritent de son élément actuel au moment où ils sont créés ou appliqués. Cela comprend les dégâts, soins, buffs, debuffs, CC, DoT, HoT, applications de Bouclier et effets retardés.

Un effet déjà créé conserve cet élément pendant toute son existence. Un changement ultérieur de l’élément de la capacité source ne le modifie pas rétroactivement.

Une application de Bouclier utilise cet élément pour sa résolution, notamment face à une immunité élémentaire. Une fois sa valeur ajoutée, la réserve commune de Bouclier de la cible ne possède plus d’élément propre.

### 6.3. Modification et déclenchement

Un Skill peut modifier explicitement l’élément d’une capacité pendant le combat. Les effets produits après cette modification utilisent le nouvel élément.

Lorsqu’une capacité en déclenche une autre, la capacité déclenchée conserve son propre élément actuel. Elle n’hérite de l’élément de la capacité déclencheuse que si une modification explicite le prévoit.

### 6.4. Immunités accordées par des Skills

Un Skill peut accorder explicitement une immunité élémentaire. Celle-ci bloque tous les effets positifs et négatifs de l’élément concerné sur la cible immunisée, quelle que soit leur source.

La table, la portée détaillée des résistances et immunités ainsi que leur ordre de résolution appartiennent au [document Éléments](./05-ELEMENTS.md).

## 7. Ultimate et énergie

### 7.1. Jauge structurelle et état initial

Chaque créature possède structurellement une jauge d’énergie standard :

> `0 → 100`

Une créature n’est pas conçue intrinsèquement avec une autre capacité naturelle.

Sans effet contraire, son état initial est `0 / 100`. Une Passive peut définir directement une autre énergie initiale. Cette valeur constitue alors l’état initial du combat et non un gain d’énergie intervenu après le début du combat.

### 7.2. Capacité maximale effective et overcharge

Une Passive ou un autre effet peut modifier la capacité maximale effective de la jauge pendant le combat. La structure de base reste `0 → 100`, mais son état effectif peut, par exemple, devenir `0 → 200`.

Une capacité maximale supérieure à 100 autorise l’accumulation correspondante et permet des mécaniques d’overcharge explicitement définies. L’énergie n’est perdue à 100 que lorsque la capacité maximale effective est elle-même égale à 100.

### 7.3. Gain et manipulation de l’énergie

Pendant le combat, la source normale du gain d’énergie est la Basic Attack réussie.

Les autres Skills ne constituent pas des sources autonomes de gain direct. Ils peuvent toutefois interagir explicitement avec le système, notamment pour :

* modifier le gain produit par une Basic Attack ;
* empêcher temporairement ce gain ;
* retirer ou voler de l’énergie ;
* modifier le seuil de disponibilité de l’Ultimate ;
* modifier la capacité maximale effective ;
* définir l’énergie initiale ;
* exploiter l’énergie accumulée dans leur résolution.

L’état de la jauge et la disponibilité de l’Ultimate sont recalculés immédiatement après chaque modification.

### 7.4. Seuil de disponibilité

Le seuil standard de l’Ultimate est 100 énergie. Une capacité peut explicitement modifier ce seuil.

Si l’énergie actuelle atteint déjà un nouveau seuil abaissé, l’Ultimate devient immédiatement prête. Si une perte d’énergie ramène la jauge sous son seuil, elle redevient indisponible.

La disponibilité standard d’une Ultimate repose sur l’énergie. Des conditions supplémentaires sans rapport avec l’énergie ne constituent pas le modèle général.

### 7.5. Consommation complète

Lorsqu’une Ultimate commence réellement son utilisation, elle consomme toute l’énergie présente et la jauge revient à zéro.

L’énergie fonctionne comme une jauge à remplir, non comme une monnaie dont seul un coût serait soustrait. Une Ultimate utilisée avec 95 énergie et un seuil de 80 ne conserve donc pas les 15 points excédentaires.

## 8. Opportunités d’action et modes de contrôle

### 8.1. Cycle temporel commun

La Basic Attack, les Active et l’Ultimate utilisent les mêmes opportunités d’action. Une Active ou une Ultimate remplace l’action qui aurait normalement eu lieu à cet instant et ne crée pas, par défaut, une action supplémentaire entre deux opportunités.

L’intervalle jusqu’à l’opportunité suivante continue selon les règles du moteur de combat.

### 8.2. Priorité au sein d’une créature

À chaque opportunité d’action, le moteur sélectionne la première action prête, autorisée et disposant d’une cible valide selon cet ordre :

1. Ultimate prête et autorisée ;
2. première Active prête et autorisée selon l’ordre de la fiche ;
3. Basic Attack.

Une capacité prête mais temporairement interdite, par exemple par Silence, reste prête. Le moteur passe à l’action valide suivante et la capacité bloquée attend une future opportunité.

Une capacité sans cible valide n’est pas lancée, ne consomme pas son compteur ou son énergie et reste prête. Le moteur poursuit la recherche d’une action valide.

### 8.3. Modes Auto et Manuel

Le mode de contrôle est global au combat. Il n’est pas configuré séparément pour chaque créature.

En **Auto** :

* les Basic Attacks sont automatiques ;
* les Active sont automatiques ;
* les Ultimate autorisées sont automatiques.

En **Manuel** :

* les Basic Attacks restent automatiques ;
* les Active restent automatiques ;
* le joueur autorise le lancement des Ultimate.

Le joueur ne choisit ni la cible ni le comportement interne d’une Ultimate. Ces éléments restent déterminés par la capacité et les règles de combat.

### 8.4. Demande manuelle et changement de mode

Une demande manuelle d’Ultimate prête est irréversible. Elle reste autorisée jusqu’à son lancement à la prochaine opportunité valide.

Lors du passage de Manuel à Auto, une Ultimate prête mais conservée devient automatiquement autorisée sans se lancer entre deux opportunités d’action.

Lors du passage d’Auto à Manuel, une Ultimate prête dont le lancement n’a pas commencé reste disponible et attend une demande manuelle.

Dès que la résolution d’une Ultimate a commencé, un changement de mode ne l’annule pas.

## 9. Ordre des actions et chaînes de résolution

### 9.1. Actions prévues au même timestamp

Lorsque plusieurs créatures doivent agir au même timestamp, leur ordre est déterminé par :

1. l’Agilité effective actuelle la plus élevée ;
2. en cas d’égalité, l’équipe attaquante avant l’équipe défenseuse ;
3. en cas de nouvelle égalité, l’ordre déterministe des positions.

L’Agilité utilisée est la valeur active au moment de la résolution, après les buffs, debuffs et autres modifications applicables.

### 9.2. Résolution complète

Une action est entièrement résolue avant le passage à l’action normale suivante, même lorsque plusieurs actions étaient prévues au même timestamp.

Cette résolution comprend notamment :

* ses hits, dégâts et soins ;
* ses résultats directs et Effets de combat ;
* les réactions déclenchées ;
* les Passive ;
* les morts et effets à la mort ;
* les réactions produites par d’autres réactions.

Une chaîne se poursuit jusqu’à sa fin, puis le moteur reprend la file normale. Les boucles infinies doivent être empêchées par la conception des capacités et par les garde-fous techniques appropriés.

### 9.3. Effets à la mort

Lorsqu’une créature meurt :

1. les dégâts létaux sont résolus ;
2. la créature atteint 0 PV ;
3. l’événement de mort est déclenché ;
4. les effets explicitement liés à cette mort et leurs réactions sont résolus ;
5. la chaîne reprend jusqu’à sa fin.

Si plusieurs effets à la mort attendent la même priorité temporelle, ils utilisent l’Agilité effective, puis l’équipe attaquante, puis l’ordre de position.

### 9.4. Action déjà lancée

Une Basic Attack, une Active ou une Ultimate dont le lancement a commencé termine sa résolution même si son lanceur meurt pendant celle-ci.

Les hits restants d’un multi-hit déjà lancé continuent donc selon la règle de ciblage de la capacité. Seule une interruption explicitement prévue peut déroger à ce principe.

## 10. Ciblage, multi-hit et état live

### 10.1. Règles de ciblage

Une capacité peut définir sa propre règle de ciblage : cible unique, ligne, colonne, équipe entière, nombre limité de cibles, cible aléatoire, cible répondant à une condition ou autre règle explicite.

Lorsqu’elle ne définit aucune exception, elle utilise les conventions du [document Combat](./02-COMBAT.md).

Le terme **allié** inclut le lanceur. La formulation **autre allié** l’exclut. Cette convention s’applique notamment aux soins, buffs, Boucliers, Cleanse et autres effets alliés.

### 10.2. Détermination des cibles

L’action à employer et ses cibles sont évaluées à partir de l’état live du combat au moment où son lancement commence réellement.

Par défaut, les cibles d’un Skill sont ensuite déterminées pour toute sa résolution. Elles ne sont pas recalculées après chaque hit simplement parce que l’état du combat change.

Une capacité peut explicitement prévoir des sélections successives, par exemple une nouvelle cible aléatoire pour chaque hit.

### 10.3. Mort d’une cible pendant un multi-hit

Si un multi-hit vise une cible fixe et que cette cible meurt, les hits restants destinés à cette cible sont perdus. Ils ne cherchent pas automatiquement une nouvelle cible.

Si la capacité prévoit une nouvelle sélection pour chaque hit, les hits restants continuent en sélectionnant des cibles valides selon cette règle.

### 10.4. Zones, positions vides et hasard

Une zone couvrant une ligne, une colonne ou une équipe n’est pas interrompue par des emplacements vides. Une règle de proximité ou d’adjacence peut en revanche être rompue par une position vide.

Le ciblage aléatoire reste déterministe à partir de la seed RNG du combat et doit pouvoir être reproduit.

## 11. Résultats directs, Effets de combat et composition

Une Active ou une Ultimate peut être entièrement consacrée au soin, à la protection, au contrôle, à une transformation, à la manipulation d’énergie ou à une autre fonction. Contrairement à la Basic Attack, elle n’est pas obligée d’infliger des dégâts.

Une même capacité peut combiner des **résultats directs** et des **Effets de combat** dans un ordre explicitement défini.

Un résultat direct est entièrement résolu au moment où il se produit : dégâts ou soin immédiat, modification immédiate d’énergie ou de compteur, destruction du Bouclier, Cleanse ou Dispel. Un Effet de combat continue d’exister avec son propre lifecycle, par exemple un DoT, HoT, Buff, Debuff, CC, Silence, Exclusion, Bouclier, Absorption ou effet retardé.

Une capacité peut ainsi enchaîner dégâts, soins, modifications immédiates, applications ou retraits d’Effets de combat. Elle peut également utiliser plusieurs hits ou composantes de dégâts, dont des dégâts Physiques, Spéciaux, hybrides ou True Damage, à condition de les définir sans ambiguïté.

Le Crit est une mécanique générale pour les effets produisant une valeur critique compatible. Les dégâts directs, les soins directs, les DoT et les HoT peuvent Critiquer selon les règles communes. Les Boucliers, l’Absorption et les autres mécanismes particuliers conservent leurs règles propres.

Les calculs, protections et catégories de dégâts appartiennent au [document Combat](./02-COMBAT.md).

## 12. Esquive, probabilités et ordre des effets

### 12.1. Effets offensifs

Un effet offensif visant une cible est soumis à l’Esquive de cette cible même lorsqu’il n’inflige aucun dégât, sauf s’il est explicitement inesquivable.

Pour un effet lié à un hit :

1. l’Esquive du hit est résolue ;
2. si le hit réussit, il est considéré comme ayant touché et l’immunité élémentaire est vérifiée ;
3. si l’effet n’est pas bloqué, ses dégâts et effets certains sont résolus ;
4. une probabilité explicitement liée à ce hit est testée selon l’ordre déclaré par la capacité.

### 12.2. Nature des probabilités

Une capacité doit préciser si une probabilité est :

* globale pour le déclenchement de la capacité ou d’un effet ;
* testée séparément pour chaque cible ;
* liée à un hit réussi ;
* ou attachée à une autre unité de résolution explicitement nommée.

Une probabilité globale peut être testée avant les résolutions individuelles d’Esquive des cibles. Aucun jet implicite ou caché ne doit être ajouté à une capacité.

### 12.3. Effets multiples et ordre réel

Chaque résultat ou Effet de combat d’une capacité peut posséder ses propres cibles, durée, probabilité, règles de réapplication et conditions.

La description mécanique doit présenter les événements dans leur véritable ordre lorsque celui-ci influence le résultat. « Réduit la Défense, puis inflige des dégâts » ne produit pas le même résultat que l’ordre inverse.

Par défaut, les dégâts d’un hit utilisent l’état de la cible au moment de leur calcul. Un debuff appliqué par ce même hit ne modifie pas rétroactivement des dégâts déjà calculés. Une capacité peut explicitement appliquer d’abord un effet, puis calculer les dégâts avec le nouvel état.

Les règles de lifecycle spécialisées appartiennent au [document Effets de combat](./06-COMBAT_EFFECTS.md).

## 13. Mort, Effets de combat et limite temporelle

### 13.1. Mort et auto-résurrection

La mort n’agit pas comme un Cleanse. Les Effets de combat présents ne sont pas automatiquement retirés lorsqu’une créature meurt ou passe dans un état non vivant lié à une auto-résurrection.

Leurs timers continuent normalement à s’écouler pendant cet état. Un Effet de combat peut donc expirer avant le retour de la créature ou rester présent avec sa durée restante.

Un effet nécessitant une cible vivante ne produit pas son résultat normal tant que la créature est non vivante. Une opportunité de tick correspondante est consommée. Cette règle est distincte de l’Exclusion, qui gèle les timers et Effets de combat selon ses propres règles.

### 13.2. Limite au combat en cours

Tous les résultats et Effets de combat produits par les capacités sont limités au combat en cours. Aucun ne modifie définitivement l’instance et aucun ne persiste d’un combat à l’autre.

Une durée peut être exprimée en secondes, en Basic Attacks, en déclenchements, jusqu’à une condition ou jusqu’à la fin du combat. « Jusqu’à la fin du combat » est un type de durée normal, pas une catégorie séparée d’effet.

Dans le contexte du combat, un effet qualifié de **permanent** signifie au maximum **jusqu’à la fin du combat**. Son éligibilité au Cleanse ou au Dispel dépend de ses propriétés explicites, pas de cette durée.

## 14. Fiches et données de capacités

### 14.1. Fiche lisible

Une fiche de capacité peut présenter séparément les propriétés structurelles utiles, notamment :

* le nom ;
* la catégorie ;
* l’élément ;
* le cycle d’une Active lorsqu’il est pertinent.

La description mécanique rassemble ensuite les cibles, valeurs, effets, durées, probabilités et exceptions nécessaires. Elle ne doit pas être transformée en formulaire répétant chaque information déjà exprimée clairement.

Sur la fiche destinée au joueur, les valeurs finales calculables pour l’instance sont affichées autant que possible plutôt que leurs coefficients internes. Lorsqu’une valeur dépend d’une cible future, la formule relative reste visible et aucun montant artificiel n’est présenté. Les besoins fonctionnels détaillés appartiennent au [document UI Flow](./18-UI_FLOW.md).

Les règles système communes, comme l’Esquive standard d’un hit offensif, n’ont pas à être répétées sur chaque fiche. La capacité décrit ce qui lui est propre et ses exceptions.

### 14.2. Terminologie mécanique

La compréhension mécanique prime sur une formulation narrative ambiguë. Les termes officiels comme Brûlure, Agilité, énergie, Bouclier, Active ou Ultimate doivent être employés de manière cohérente.

Un texte de lore séparé n’est pas obligatoire. L’identité peut être portée par le nom, les effets nommés et une formulation naturelle qui reste mécaniquement précise.

### 14.3. Source de vérité data-driven

Les capacités concrètes doivent être conçues à partir de données structurées : élément, coefficients, durées, probabilités, hits, stacks, ticks, seuils et autres paramètres. Cette structure reste extensible et ne remplace pas le texte mécanique précis de chaque capacité.

Le texte présenté au joueur reflète ces données. Une valeur ne doit pas être saisie indépendamment dans plusieurs sources susceptibles de diverger.

`04-SKILLS.md` décrit les contrats du système. Les données concrètes des capacités appartiendront au code, à une base de données, à des fichiers de données ou à un outil de contenu choisi pendant la conception technique.

Les valeurs d’équilibrage peuvent évoluer sans remettre en cause une mécanique structurelle inchangée.

## 15. Exceptions et extensibilité

Le système suit le principe :

> **règle générale simple, exception locale explicitement définie.**

Une exception ne modifie que la capacité ou l’effet qui la porte. Une Ultimate inesquivable ne rend pas toutes les Ultimate inesquivables ; une Passive augmentant une capacité maximale ne modifie pas la jauge structurelle des autres créatures.

La documentation décrit les règles actuellement validées sans affirmer que toute mécanique future non mentionnée est impossible.

Une mécanique atypique future, comme un coût en PV, un sacrifice, un soin d’ennemi ou la copie d’un Skill, devra définir localement toutes les règles nécessaires avant son intégration. Aucune règle universelle n’est inventée tant que cette mécanique n’est pas réellement décidée.

Si une future capacité crée seulement une exception locale, sa fiche peut la documenter. Si elle introduit ou modifie une règle système réutilisable, les documents système concernés doivent être mis à jour.

## 16. Répartition documentaire

| Document | Responsabilité principale |
|---|---|
| [`02-COMBAT.md`](./02-COMBAT.md) | Timeline, opportunités d’action, ordre entre créatures, formules et résolution commune |
| [`03-CREATURES.md`](./03-CREATURES.md) | Identité familiale des capacités et propriétés structurelles des créatures |
| [`05-ELEMENTS.md`](./05-ELEMENTS.md) | Éléments des capacités et résistances élémentaires |
| [`06-COMBAT_EFFECTS.md`](./06-COMBAT_EFFECTS.md) | Lifecycle, durée, réapplication, snapshot, retrait et comportement des Effets de combat |
| [`07-EVOLUTIONS.md`](./07-EVOLUTIONS.md) | Transformations des versions de capacités entre les formes et branches |
| [`18-UI_FLOW.md`](./18-UI_FLOW.md) | Présentation et parcours de consultation ou de contrôle |

## 17. Éléments à préciser ultérieurement

* Les coefficients, durées, probabilités, nombres de hits, cycles et gains d’énergie propres aux capacités concrètes.
* Les seuils et modifications d’énergie propres aux capacités concrètes.
* Les conventions finales d’affichage de l’énergie, des Active prêtes et de leurs compteurs.
* Le schéma technique des données de capacités et l’outil de contenu associé.
* Les garde-fous techniques empêchant les boucles infinies de réactions.
* Les fiches et données des capacités de chaque famille et de chaque forme.
