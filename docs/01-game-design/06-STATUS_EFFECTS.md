# Project Awakening — Effets de statut

**Statut :** Draft de conception — base initiale à compléter

## 1. Rôle et périmètre du document

Ce document rassemble les décisions validées concernant les effets de statut et leurs interactions communes.

Il complète les [règles de combat](./02-COMBAT.md). Il ne fixe pas les valeurs, durées, probabilités, limites de cumul ou formules encore ouvertes et ne constitue pas une liste définitive de tous les effets du jeu.

## 2. Définition générale

Un effet de statut est une modification temporaire appliquée pendant un combat afin d’influencer une créature ou une règle de combat.

Un effet peut être :

* positif ;
* négatif ;
* plus rarement neutre.

Il peut modifier des caractéristiques, limiter ou empêcher des actions, produire un effet périodique, réagir à un événement ou modifier temporairement une règle.

Tous les effets de statut prennent fin au plus tard avec le combat en cours. Le terme « permanent », lorsqu’il est utilisé pour un effet de combat, signifie « jusqu’à la fin du combat » et ne modifie jamais définitivement l’instance.

L’association d’un effet à un élément est facultative et doit être déclarée explicitement. Aucun élément ne confère naturellement une immunité à un statut.

Lorsqu’une évolution enrichit ou transforme la version d’un même Skill, elle peut notamment ajouter, retirer ou modifier un effet de statut. Cette variation doit maintenir une continuité conceptuelle cohérente et être déclarée explicitement pour la forme ou la branche concernée.

## 3. Application d’un statut

### 3.1. Statut directement lié à un hit

Lorsqu’un statut est directement lié à un hit :

* le hit est d’abord soumis à l’Esquive ;
* si le hit réussit, le statut s’applique ;
* aucun second jet d’application caché n’est effectué.

Un statut ou autre effet offensif ciblé reste soumis à l’Esquive de chaque cible même lorsqu’il n’inflige aucun dégât, sauf exception explicitement inesquivable.

### 3.2. Probabilité explicitement définie

Lorsqu’un statut possède une probabilité liée à un hit :

1. l’Esquive du hit est résolue ;
2. si le hit réussit, la probabilité déclarée est testée.

Un Skill inesquivable peut conserver une probabilité d’application indépendante.

Une probabilité peut également être globale, propre à chaque cible ou attachée à une autre unité de résolution explicitement nommée. Une probabilité globale peut être testée avant les Esquives individuelles. La fiche du Skill doit préciser cette nature ; aucun jet caché implicite n’est ajouté.

## 4. Réapplication, coexistence et cumul

La règle de réapplication appartient à chaque statut. Elle peut notamment :

* renouveler la durée ;
* ajouter de la durée ;
* ajouter une stack ;
* créer une nouvelle instance lorsque cette règle est explicite.

Des sources différentes appliquant le même type de DoT ou de HoT créent des effets indépendants.

Plusieurs buffs identiques provenant de sources différentes peuvent coexister. Lorsqu’une même source réapplique exactement le même buff, sa durée est renouvelée par défaut, sauf règle explicite de stacking.

## 5. DoT et HoT

Les DoT et HoT utilisent une fréquence de tick globale.

Ils :

* persistent après la mort de leur source ;
* continuent normalement pendant un CC classique ;
* voient leurs timers gelés pendant l’Exclusion de leur cible ;
* utilisent un snapshot de leur source au moment de l’application.

La mort de leur cible ou son passage dans un état non vivant lié à une auto-résurrection ne retire pas automatiquement ces statuts et ne gèle pas leurs timers. Un effet exigeant une cible vivante, comme les dégâts d’un DoT, ne produit toutefois pas son effet normal tant que la cible est non vivante.

L’état de la cible reste dynamique et est recalculé à chaque tick. Cela comprend notamment ses défenses, ses résistances élémentaires, ses réductions, son Absorption, ses Boucliers et sa réduction des soins.

### 5.1. DoT

L’application d’un DoT peut être esquivée lorsqu’elle dépend d’un hit. Ses ticks ne sont pas esquivables et chacun peut produire un Crit.

### 5.2. HoT

Chaque tick d’un HoT peut produire un Crit. Les soins excédant les PV maximum sont perdus, sauf mécanique explicite utilisant ce surplus.

## 6. DoT identifiés

### 6.1. Brûlure

La Brûlure :

* inflige un DoT ;
* réduit les soins reçus.

Ses valeurs et ses règles de stacks restent à définir.

### 6.2. Poison

Le Poison peut se cumuler afin de devenir plus puissant. Sa formule et ses limites de stacks restent à définir.

### 6.3. Saignement

Le Saignement utilise les PV de la cible dans sa formule afin de remplir une fonction anti-tank. Sa formule et ses caps restent à définir.

## 7. Crowd Control total

Les tags de CC total standards sont :

* Stun ;
* Glacé ;
* Peur.

Ils empêchent la créature d’agir et partagent les mêmes règles générales de diminishing returns, tout en restant des tags distincts pour les interactions de Skills.

Si un CC est appliqué avant le début réel d’une action, il peut l’empêcher. Les actions prévues au même timestamp sont ordonnées selon l’Agilité effective, puis l’équipe attaquante, puis la position ; une action déjà lancée n’est pas annulée sans interruption explicite.

### 7.1. Diminishing returns

Chaque créature possède son propre historique temporaire de CC. Les applications répétées réduisent prioritairement la durée du CC plutôt que sa chance d’application.

La durée de l’historique, les paliers et le temps de récupération restent à équilibrer.

### 7.2. Immunités

Une immunité explicitement accordée empêche l’application des CC ou statuts compris dans son périmètre. Il n’existe pas d’immunité naturelle permanente fondée uniquement sur un élément.

## 8. Silence

Pendant Silence :

* la Basic Attack reste disponible ;
* ses Basic Attacks réussies continuent à générer de l’énergie ;
* ses Basic Attacks réussies continuent à faire progresser les compteurs d’Active ;
* ses Active et son Ultimate ne peuvent pas être utilisées ;
* les Active prêtes et l’Ultimate ayant atteint son seuil restent prêtes.

Après la fin du Silence, les règles normales de priorité reprennent.

## 9. Exclusion

L’Exclusion retire temporairement une créature du combat.

Pendant l’Exclusion, la créature :

* ne peut ni agir ni être ciblée ;
* n’est pas considérée comme présente pour une AoE ;
* conserve sa position ;
* voit ses timers personnels, DoT, HoT, buffs et debuffs gelés.

Elle revient dans la même position et dans l’état où ses effets ont été gelés.

## 10. Buffs, debuffs et modifications de caractéristiques

Les buffs et debuffs sont des effets temporaires. Leurs modifications en pourcentage sont appliquées successivement et de manière multiplicative.

Ils restent distincts des modifications explicitement appliquées jusqu’à la fin du combat. Ces dernières peuvent ne pas avoir de timer, ne pas être dissipables et se cumuler indéfiniment lorsqu’un Skill le prévoit.

Slow et Haste ne constituent pas un système de vitesse séparé : ils modifient directement l’Agilité, qui détermine ensuite l’intervalle réel des Basic Attacks.

La réduction des soins peut exister comme debuff indépendant. Son cap reste à équilibrer.

## 11. Cleanse et Dispel

Par défaut :

* Cleanse retire un effet négatif aléatoire d’un allié, terme qui inclut le lanceur ;
* Dispel retire un effet positif aléatoire d’un ennemi.

La formulation « autre allié » exclut explicitement le lanceur.

Un Skill peut définir une autre quantité ou une règle de sélection particulière.

## 12. Boucliers et Absorption

Un Bouclier est une réserve universelle de dégâts flat. Les Boucliers peuvent coexister comme réserves séparées et sont consommés avant les PV, selon l’ordre défini par le document Combat.

L’Absorption réduit un pourcentage de dégâts avant les Boucliers. Deux applications du même effet d’Absorption ne se cumulent pas et renouvellent sa durée ; des effets d’Absorption différents peuvent coexister.

Les Boucliers et l’Absorption ne produisent pas de Crit.

## 13. Énergie

Des Skills peuvent :

* retirer de l’énergie ;
* voler de l’énergie ;
* modifier ou empêcher la quantité d’énergie générée par une Basic Attack ;
* modifier le seuil de l’Ultimate ou la capacité maximale effective de la jauge.

Pendant le combat, les autres Skills ne constituent pas des sources autonomes de gain direct d’énergie. Le gain normal provient des Basic Attacks réussies.

Il n’existe pas de statut général empêchant toute génération d’énergie. Une exception doit être explicitement définie.

## 14. Mécaniques générales absentes

Il n’existe pas de mécanique générale de Root ou de Taunt.

Un Skill peut modifier le ciblage ou interdire une catégorie de cibles uniquement si cette règle est explicitement définie. Une telle exception ne crée pas automatiquement un statut système partagé par les autres Skills.

## 15. Éléments à préciser ultérieurement

* Les valeurs, durées et probabilités de chaque statut.
* Les règles individuelles de stacks et de réapplication.
* Les paramètres des diminishing returns des CC.
* Les formules et caps de Brûlure, Poison et Saignement.
* Le cap de réduction des soins.
* Les règles détaillées d’interface, d’icônes et de lisibilité.
* La liste définitive des effets de statut.
