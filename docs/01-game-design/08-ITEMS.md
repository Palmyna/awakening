# Project Awakening — Objets et équipements

**Statut :** Draft de conception — base initiale à compléter

## 1. Rôle et périmètre du document

Ce document rassemble les décisions validées concernant les objets, l’inventaire et les équipements des créatures.

Il ne définit pas encore les tables de loot, les affixes, les valeurs, les raretés, les emplacements exacts ni les règles d’amélioration.

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

## 4. iLvl

Chaque objet d’équipement possède un iLvl visible représentant son niveau de puissance propre.

L’iLvl possède un cap. Sa valeur exacte, ses caps et sa relation avec les autres propriétés d’un objet restent à définir.

## 5. Objets et évolutions

Une évolution peut demander qu’un objet soit possédé, porté ou équipé.

Dans ces cas, l’objet n’est pas consommé. Une évolution peut exceptionnellement déclarer explicitement la consommation d’un objet ; elle seule provoque alors sa disparition.

Les objets éventuellement liés aux évolutions doivent rester cohérents avec la progression et pouvoir être compris grâce aux informations disponibles en jeu.

## 6. Objet de réinitialisation des points de caractéristiques

Un objet rare obtenu en jouant permet de redistribuer les points de caractéristiques déjà gagnés sans modifier le niveau ni l’XP.

Il n’accorde aucun point supplémentaire et fournit le même résultat fonctionnel que le service payant limité correspondant.

## 7. Protection de l’équipement lors de la consommation d’une instance

Lorsqu’une instance est consommée comme matériau d’étoiles :

1. tous ses objets équipés sont automatiquement déséquipés ;
2. ces objets sont replacés dans l’inventaire ;
3. aucun équipement n’est détruit avec l’instance.

## 8. Dépendances

* Le [référentiel Créatures](./03-CREATURES.md) définit la propriété et la conservation de l’équipement par instance.
* Le [draft Évolutions](./07-EVOLUTIONS.md) définit le rôle des objets dans les conditions d’évolution.
* Le [draft Progression](./10-PROGRESSION.md) définit la redistribution de caractéristiques.
* Le [draft UI Flow](./18-UI_FLOW.md) définira les parcours de gestion et de comparaison.

## 9. Éléments à préciser ultérieurement

* Le nombre et les types d’emplacements.
* Les restrictions d’équipement.
* Les statistiques, affixes, raretés et qualités.
* Les règles d’amélioration et les sets.
* Les caps et valeurs exactes d’iLvl.
* Les sources, tables et règles de loot.
* La méthode d’obtention, la rareté et le rythme de distribution de l’objet de réinitialisation.
* Les éventuels objets consommés par des évolutions concrètes.
