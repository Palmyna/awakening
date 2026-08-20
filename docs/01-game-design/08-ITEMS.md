# Project Awakening — Objets et équipements

**Statut :** Draft de conception — base initiale à compléter

## 1. Rôle et périmètre du document

Ce document rassemble les décisions validées concernant les objets, l’inventaire et les équipements des créatures.

Il ne définit pas encore les tables de loot, les affixes, les valeurs, les raretés, les emplacements exacts ni les règles d'amélioration et de sets.

## 2. Objets et inventaire

Un objet est un élément pouvant être obtenu et généralement stocké dans l’inventaire ou utilisé par un système du jeu.

Un objet d’équipement est un objet individuel. Lorsqu’il n’est pas équipé, il appartient à l’inventaire.

L’inventaire reste distinct du système de collection des créatures et des skins de carte.

## 3. Ensemble d’équipement d’une instance

Chaque instance possède son propre ensemble d’équipement actif.

Cet ensemble :

* comporte plusieurs objets ;
* utilise plusieurs emplacements ;
* appartient à l’instance, non à sa famille ou à sa forme ;
* est conservé lors d’une évolution ;
* n’est pas modifié par le choix d’une ancienne apparence cosmétique.

Deux instances d’une même famille peuvent utiliser des équipements entièrement différents.

Les équipements sont gérés depuis la fiche de la créature. Ils ne sont pas automatiquement représentés sur son illustration ou sa carte.

## 4. Catégories principales envisagées

La direction actuelle envisage deux catégories principales d'équipement :

* les **Artefacts** ;
* les **Sources d'énergie**.

La répartition envisagée est d'environ trois Artefacts et deux Sources d'énergie par instance. Cette direction ne valide ni le nombre exact ni la nature définitive des emplacements.

Chaque catégorie utilise ses propres sets. Un set appartient à une seule catégorie et ne mélange pas Artefacts et Sources d'énergie. Les effets, seuils et règles exactes de ces sets restent à définir.

## 5. Sources d'énergie

Les Sources d'énergie sont obtenues directement comme loot ou récompenses de combat et d'activité. Leur acquisition soutient une boucle de farming et la recherche de meilleurs rolls.

Leur lien fonctionnel éventuel avec l'énergie probablement utilisée pour l'invocation n'est pas décidé.

## 6. Artefacts et fabrication

Les Artefacts sont principalement fabriqués dans un établi ou un système équivalent en combinant des composants.

Les recettes sont à découvrir en jeu. Une recette découverte est mémorisée dans une bibliothèque ou un registre de plans du compte. Réutiliser une même recette permet de produire le même type d'Artefact, tandis que ses caractéristiques finales peuvent varier entre plusieurs fabrications.

Le nombre exact d'ingrédients, le traitement d'une combinaison invalide et la consommation éventuelle de composants lors d'un échec restent ouverts.

## 7. Philosophie de loot et farming

Le système vise une philosophie de loot inspirée des Hack'n Slash : rejouer des combats pour obtenir des composants et des Sources d'énergie, fabriquer des Artefacts et rechercher de meilleurs rolls.

Les combats du mode Histoire peuvent être rejoués et participent à cette boucle de farming avec les autres activités pertinentes. Les tables, quantités et rythmes de récompenses restent à définir.

## 8. iLvl

Chaque objet d’équipement possède un iLvl visible représentant son niveau de puissance propre.

L’iLvl possède un cap. Sa valeur exacte, ses caps et sa relation avec les autres propriétés d’un objet restent à définir.

## 9. Objets et évolutions

Une évolution peut demander qu’un objet soit possédé, porté ou équipé.

Dans ces cas, l’objet n’est pas consommé. Une évolution peut exceptionnellement déclarer explicitement la consommation d’un objet ; elle seule provoque alors sa disparition.

Les objets éventuellement liés aux évolutions doivent rester cohérents avec la progression et pouvoir être compris grâce aux informations disponibles en jeu.

## 10. Objet de réinitialisation des points de caractéristiques

Un objet rare obtenu en jouant permet de redistribuer les points de caractéristiques déjà gagnés sans modifier le niveau ni l’XP.

Il n’accorde aucun point supplémentaire et fournit le même résultat fonctionnel que le service payant limité correspondant.

## 11. Protection de l’équipement lors de la consommation d’une instance

Lorsqu’une instance est consommée comme matériau d’étoiles :

1. tous ses objets équipés sont automatiquement déséquipés ;
2. ces objets sont replacés dans l’inventaire ;
3. aucun équipement n’est détruit avec l’instance.

## 12. Dépendances

* Le [référentiel Créatures](./03-CREATURES.md) définit la propriété et la conservation de l’équipement par instance.
* Le [draft Évolutions](./07-EVOLUTIONS.md) définit le rôle des objets dans les conditions d’évolution.
* Le [draft Progression](./10-PROGRESSION.md) définit la redistribution de caractéristiques.
* Le [draft UI Flow](./18-UI_FLOW.md) définira les parcours de gestion et de comparaison.

## 13. Éléments à préciser ultérieurement

* Le nombre et les types définitifs d'emplacements.
* Les restrictions d’équipement.
* Les statistiques, affixes, raretés et qualités.
* Les règles d'amélioration et les effets, seuils et combinaisons exacts des sets.
* Les caps et valeurs exactes d’iLvl.
* Les sources, tables et règles de loot.
* Le nombre exact d'ingrédients d'une recette.
* Le comportement d'une combinaison invalide et la consommation éventuelle des composants en cas d'échec.
* Les règles de génération et de variation des rolls.
* La relation éventuelle entre les Sources d'énergie équipables et l'énergie d'invocation.
* La méthode d’obtention, la rareté et le rythme de distribution de l’objet de réinitialisation.
* Les éventuels objets consommés par des évolutions concrètes.
