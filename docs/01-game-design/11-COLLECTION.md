# Project Awakening — Collection et encyclopédie

**Statut :** Draft de conception — base initiale à compléter

## 1. Rôle et périmètre du document

Ce document rassemble les décisions validées concernant la gestion des instances possédées, l’encyclopédie, la recherche, les tris et la capacité de créatures.

Il ne définit pas encore la mise en page finale, la grammaire complète de recherche ni les paramètres commerciaux des extensions de capacité.

## 2. Espaces distincts

Le système de collection comprend deux parties séparées :

* les créatures ;
* les skins de carte.

Ces catégories appartiennent au même espace général sans être mélangées dans une liste unique.

La gestion des instances possédées, l’encyclopédie des créatures et l’inventaire d’objets remplissent des fonctions distinctes.

Dans ces espaces, les créatures sont principalement représentées sous forme de cartes. Une base de composant peut être réutilisée entre la gestion, la collection et l’encyclopédie en adaptant les informations visibles au contexte, conformément aux drafts [Card Design](../03-art/03-CARD_DESIGN.md) et [UI Guide](../03-art/04-UI_GUIDE.md).

## 3. Gestion des instances possédées

Plusieurs instances d’une même famille peuvent être possédées.

Chaque instance conserve notamment :

* son niveau, son XP et ses points ;
* ses étoiles ;
* sa forme, son stade et sa branche ;
* son équipement ;
* son surnom facultatif ;
* ses tags personnalisés ;
* son verrouillage ;
* ses apparences de formes débloquées.

Les apparences de formes sont débloquées par instance et uniquement pour les formes qu’elle a réellement parcourues. Une ancienne forme accessible peut être affichée librement hors combat sans modifier la forme mécanique, les caractéristiques, les éléments, les capacités, les rôles ou l’équipement de l’instance. Les skins déjà débloqués peuvent être utilisés lorsqu’ils sont compatibles avec la forme affichée.

Le surnom est facultatif, modifiable et supprimable. Il ne remplace jamais le nom officiel de la forme et peut être utilisé par la recherche.

Les tags peuvent être créés librement par le joueur et n’ont aucun effet de gameplay. Ils servent à l’organisation, à la recherche et au filtrage et restent distincts des rôles suggérés par le jeu.

Aucun système spécifique de Favoris n’est retenu actuellement.

## 4. Verrouillage

Le verrouillage empêche :

* la consommation comme matériau d’étoiles ;
* la suppression ;
* la réinitialisation complète ;
* la redistribution de caractéristiques, gratuite ou payante.

Il ne bloque pas :

* l’XP et les niveaux ;
* l’évolution ;
* la montée d’étoile de l’instance cible ;
* l’équipement ;
* la modification du surnom et des tags ;
* le changement d’apparence cosmétique ;
* l’utilisation normale.

## 5. Encyclopédie des créatures

L’encyclopédie est un répertoire de compte distinct de la liste des instances possédées.

Une famille est découverte lorsque le joueur obtient réellement l’une de ses instances. Une forme devient découverte lorsque le compte l’obtient ou l’atteint, ainsi que lorsque le joueur la rencontre ou l’affronte et que son existence et son apparence sont révélées.

La rencontre d’une forme évoluée ne compte pas comme l’obtention d’une instance et ne révèle pas automatiquement sa condition d’évolution. La connaissance de l’existence d’une forme et celle de sa méthode d’évolution sont distinctes.

La découverte est permanente pour le compte, même si l’instance concernée évolue ensuite, est consommée ou n’est plus possédée sous cette forme.

Chaque famille possède :

* un numéro permanent affiché sans zéro superflu, par exemple `#1` ou `#42` ;
* un lore général ;
* un lore propre à chacune de ses formes.

Un numéro déjà attribué n’est jamais modifié ou réorganisé lorsque de nouvelles familles sont ajoutées.

L’encyclopédie affiche uniquement les familles découvertes et ne révèle jamais combien de familles existent au total. Les nombres absents peuvent signaler des découvertes manquantes sans annoncer une taille totale.

Elle présente les informations intrinsèques connues de la famille et de ses formes sans se substituer à la fiche de progression d’une instance possédée. Ces informations peuvent notamment comprendre :

* le numéro ;
* le nom de la famille ou de la forme ;
* le lore familial et le lore de forme ;
* la rareté ;
* les éléments ;
* les rôles suggérés ;
* le profil offensif ;
* les caractéristiques de base ;
* la Basic Attack et les Skills de la forme ;
* les informations d’évolution déjà découvertes.

## 6. Arbres partiellement connus

Une famille nouvellement obtenue peut apparaître ainsi :

> Forme de base → ??? → ???

Les formes et branches découvertes enrichissent progressivement l’arbre connu. Le nombre de branches possibles reste caché avant leur découverte.

Les conditions d’évolution découvertes deviennent des connaissances permanentes du compte et restent explicitement consultables. Elles ne doivent pas être redécouvertes pour chaque nouvelle instance de la même famille.

Une forme révélée par une rencontre n’expose pas automatiquement les autres branches de sa famille. Plus généralement, aucune découverte ciblée ne révèle le catalogue ou le nombre total des familles encore inconnues.

## 7. Recherche et tri des instances

La recherche est unifiée, dynamique et sensible aux formes.

Elle peut exploiter notamment :

* les noms de famille et de formes ;
* les surnoms ;
* les rôles suggérés ;
* les profils offensifs ;
* les éléments ;
* la rareté ;
* les tags personnalisés ;
* les autres propriétés pertinentes explicitement documentées.

Rechercher une forme de base doit retrouver toutes les instances de sa famille. Rechercher une forme évoluée doit retrouver les instances actuellement sous cette forme ainsi que celles dont le chemin antérieur est compatible, sans inclure une branche incompatible.

Les tris prévus comprennent :

* le score de Puissance ;
* la rareté ;
* le niveau ;
* les étoiles ;
* le nom ;
* le rôle ;
* le profil offensif ;
* l’élément ;
* le stade.

La grammaire exacte reste à définir.

## 8. Capacité gratuite

La capacité gratuite suit actuellement :

> **CapacitéGratuite = arrondi(1,30 × NombreBranchesDisponibles)**

L’arrondi est effectué à l’entier le plus proche.

Une branche correspond à un chemin d’évolution distinct, quel que soit le stade de divergence. Une famille linéaire compte pour une branche.

Lorsque de nouvelles branches deviennent disponibles dans le jeu, la capacité gratuite est recalculée automatiquement pour tous les comptes.

## 9. Extensions permanentes

La capacité totale suit :

> **CapacitéTotale = CapacitéGratuite + ExtensionsPayantes**

Une extension achetée ajoute définitivement sa valeur fixe. Elle ne modifie pas la formule de capacité gratuite, n’est jamais absorbée par une augmentation ultérieure de celle-ci et n’accorde aucune puissance de combat.

Les tailles et prix exacts restent à définir.

## 10. Dépassement de capacité

Une instance obtenue au-delà de la capacité :

* n’est jamais perdue ;
* reste possédée ;
* compte comme découverte ;
* devient grisée et inutilisable ;
* rejoint une file selon son ordre d’obtention.

Tant qu’elle reste bloquée, elle ne peut notamment pas être utilisée dans une équipe, développée, équipée, consommée comme matériau ou manipulée normalement.

Lorsqu’une place se libère, la plus ancienne instance bloquée selon cet ordre d’acquisition devient automatiquement utilisable.

Le joueur peut continuer à obtenir de nouvelles créatures au-delà de sa capacité.

## 11. Composition d’équipe

Deux instances d’une même famille peuvent cohabiter dans une équipe uniquement lorsque leurs chemins d’évolution ont réellement divergé.

Une forme du tronc commun reste incompatible avec toute autre instance de sa famille. Cette règle est globale pour tous les modes.

## 12. Éléments à préciser ultérieurement

* La grammaire exacte de recherche.
* Les filtres complémentaires.
* La présentation finale de la liste d’instances et de l’encyclopédie.
* Les informations affichées par chaque variante contextuelle de carte.
* La présentation des arbres partiellement connus.
* Les confirmations de verrouillage et d’actions irréversibles.
* Les tailles et prix des extensions de capacité.
* Les règles détaillées d’affichage et d’usage des instances bloquées.
* Les règles de calcul de la progression des collections de skins de carte.
