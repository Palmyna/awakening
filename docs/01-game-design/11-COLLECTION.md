# Project Awakening — Collection et encyclopédie

**Statut :** Draft de conception — à relire et valider

## 1. Rôle et périmètre du document

Ce document définit le système de collection, la gestion des instances possédées, l’encyclopédie des créatures, la collection de skins de carte et la capacité de créatures.

Il formalise les distinctions entre propriété, découverte, progression, apparence et stockage. Il ne définit pas la mise en page finale, la grammaire complète de recherche, les paramètres commerciaux des extensions ou les règles encore ouvertes de compatibilité des skins.

## 2. Fonction du système de collection

Le système de collection permet de consulter, organiser et valoriser les éléments collectionnables du joueur.

Il soutient :

* l’attachement aux créatures ;
* la découverte de nouvelles familles et formes ;
* la gestion de plusieurs instances ;
* la compréhension des possibilités d’évolution ;
* la mise en valeur des skins de carte ;
* des objectifs de complétion lorsque le périmètre de la collection concernée est connu.

Il ne remplace ni la progression des créatures, ni la composition d’équipe, ni l’inventaire d’objets.

## 3. Espaces distincts

Le système de collection comprend deux parties séparées :

* les créatures ;
* les skins de carte.

Ces catégories appartiennent au même espace général sans être mélangées dans une liste unique.

Quatre fonctions restent distinctes :

* la **gestion des instances possédées**, consacrée aux individus réellement disponibles sur le compte ;
* l’**encyclopédie des créatures**, consacrée aux connaissances permanentes découvertes sur les familles et leurs formes ;
* la **collection de skins de carte**, consacrée aux apparences cosmétiques débloquées ou consultables ;
* l’**inventaire**, consacré aux objets, équipements, ressources et autres éléments stockables.

Une base de composant de carte peut être réutilisée entre ces espaces en adaptant les informations visibles au contexte.

## 4. Gestion des instances possédées

Plusieurs instances d’une même famille peuvent être possédées et développées séparément.

Chaque instance conserve notamment :

* son niveau, son XP et ses points ;
* ses étoiles ;
* sa forme, son stade et sa branche ;
* son équipement ;
* son surnom facultatif ;
* ses tags personnalisés ;
* son verrouillage ;
* ses apparences de formes débloquées.

Les apparences de formes sont débloquées par instance et uniquement pour les formes qu’elle a réellement parcourues. Une ancienne forme accessible peut être affichée librement hors combat sans modifier la forme mécanique, les caractéristiques, les éléments, les capacités, les rôles ou l’équipement de l’instance.

Le surnom est facultatif, modifiable et supprimable. Il ne remplace jamais le nom officiel de la forme et peut être utilisé par la recherche.

Les tags peuvent être créés librement par le joueur. Ils n’ont aucun effet de gameplay et restent distincts des rôles suggérés par le jeu.

Aucun système spécifique de Favoris n’est retenu actuellement.

## 5. Verrouillage et actions protégées

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

Le verrouillage protège les actions destructives ou irréversibles sans geler la progression ordinaire de l’instance.

## 6. Encyclopédie des créatures

L’encyclopédie est un répertoire permanent du compte, distinct de la liste des instances actuellement possédées.

Une famille est découverte lorsque le joueur obtient réellement l’une de ses instances.

Une forme devient découverte lorsque :

* le compte l’obtient ou l’atteint par évolution ;
* le joueur la rencontre ou l’affronte et que son existence et son apparence sont révélées.

La rencontre d’une forme évoluée ne compte pas comme l’obtention d’une instance et ne révèle pas automatiquement sa condition d’évolution. La connaissance de l’existence d’une forme et celle de sa méthode d’évolution restent distinctes.

La découverte est permanente pour le compte, même si l’instance concernée évolue ensuite, est consommée ou n’est plus possédée sous cette forme.

Chaque famille possède :

* un numéro permanent affiché sans zéro superflu, par exemple `#1` ou `#42` ;
* un lore général ;
* un lore propre à chacune de ses formes.

Un numéro déjà attribué n’est jamais modifié ou réorganisé lorsque de nouvelles familles sont ajoutées.

L’encyclopédie affiche uniquement les familles découvertes et ne révèle jamais combien de familles existent au total. Les nombres absents peuvent signaler des découvertes manquantes sans annoncer une taille totale.

Elle présente les informations intrinsèques connues sans se substituer à la fiche de progression d’une instance. Ces informations peuvent notamment comprendre le numéro, les noms, les lores, la rareté, les éléments, les rôles suggérés, le profil offensif, les caractéristiques de base, les capacités et les informations d’évolution découvertes.

## 7. Arbres partiellement connus

Une famille nouvellement obtenue peut apparaître ainsi :

> Forme de base → ??? → ???

Les formes et branches découvertes enrichissent progressivement l’arbre connu. Le nombre de branches possibles reste caché avant leur découverte.

Les conditions d’évolution découvertes deviennent des connaissances permanentes du compte et restent explicitement consultables. Elles ne doivent pas être redécouvertes pour chaque nouvelle instance de la même famille.

Une forme révélée par une rencontre n’expose pas automatiquement sa condition, les autres branches de sa famille ou le catalogue des familles encore inconnues.

## 8. Recherche, filtres et tris des instances

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

La grammaire exacte, les combinaisons de filtres et leurs contrôles tactiles restent à définir.

## 9. Capacité de créatures

La capacité gratuite suit actuellement :

> **CapacitéGratuite = arrondi(1,30 × NombreBranchesDisponibles)**

L’arrondi est effectué à l’entier le plus proche.

Une branche correspond à un chemin d’évolution distinct, quel que soit le stade de divergence. Une famille linéaire compte pour une branche.

Lorsque de nouvelles branches deviennent disponibles dans le jeu, la capacité gratuite est recalculée automatiquement pour tous les comptes.

La capacité totale suit :

> **CapacitéTotale = CapacitéGratuite + ExtensionsPayantes**

Une extension achetée ajoute définitivement sa valeur fixe. Elle ne modifie pas la formule de capacité gratuite, n’est jamais absorbée par une augmentation ultérieure de celle-ci et n’accorde aucune puissance de combat.

## 10. Dépassement de capacité

Une instance obtenue au-delà de la capacité :

* n’est jamais perdue ;
* reste possédée ;
* compte comme découverte ;
* devient grisée et inutilisable ;
* rejoint une file selon son ordre d’obtention.

Tant qu’elle reste bloquée, elle ne peut notamment pas être utilisée dans une équipe, développée, équipée, consommée comme matériau ou manipulée normalement.

Lorsqu’une place se libère, la plus ancienne instance bloquée selon l’ordre d’acquisition devient automatiquement utilisable.

Le joueur peut continuer à obtenir de nouvelles créatures au-delà de sa capacité. Le dépassement ne crée donc ni perte d’acquisition ni obligation d’achat.

## 11. Collection de skins de carte

La collection de skins permet :

* de consulter les skins débloqués et non débloqués ;
* de parcourir les séries de skins de carte ;
* de visualiser la progression au sein de chaque série ;
* de consulter les skins disponibles pour une créature ;
* d’appliquer un skin débloqué à une carte compatible.

Un skin de carte modifie uniquement la représentation visuelle. Il ne modifie ni la créature, ni ses caractéristiques, ni ses capacités.

Les skins non débloqués restent consultables avec leur série, leur statut de disponibilité et leur mode général d’obtention lorsque ces informations peuvent être communiquées. Certains skins secrets, surprises ou non encore officiellement révélés peuvent rester masqués.

Une série temporairement indisponible reste normalement visible avec une indication claire de son indisponibilité actuelle et de sa politique de retour connue.

La progression de collection est principalement suivie par série, car leur périmètre est connu. La complétion d’une série ne fournit aucun avantage automatique de puissance.

## 12. Skins obtenus hors paquets

Certains skins peuvent être accordés directement comme récompenses événementielles, de haut fait, narratives, de progression, commémoratives ou liées à une opération spéciale.

Ces skins :

* n’appartiennent à aucune série distribuée par paquets ;
* ne peuvent pas être obtenus aléatoirement dans ces séries ;
* doivent afficher leur méthode générale d’obtention dans la collection lorsque celle-ci peut être communiquée.

Ils seront regroupés dans une catégorie dédiée dont le nom, la structure et les règles de complétion ne sont pas encore validés.

## 13. Apparences de formes et skins

Le sélecteur d’apparence d’une instance distingue :

* sa forme mécanique actuelle ;
* les anciennes formes réellement parcourues et débloquées comme apparences ;
* les skins de carte débloqués compatibles avec la forme affichée.

Le changement d’apparence est gratuit, limité au hors-combat et sans effet mécanique.

La compatibilité d’un skin avec une créature indépendamment de sa forme, une forme précise ou plusieurs formes compatibles reste une décision ouverte. Les données concrètes d’un futur skin devront respecter la règle retenue.

## 14. Composition d’équipe

Deux instances d’une même famille peuvent cohabiter dans une équipe uniquement lorsque leurs chemins d’évolution ont réellement divergé.

Une forme du tronc commun reste incompatible avec toute autre instance de sa famille. Cette règle est globale pour tous les modes.

La liste des instances doit permettre d’identifier celles qui sont indisponibles pour dépassement de capacité et ne peuvent donc pas être sélectionnées.

## 15. Interactions et dépendances

| Document | Responsabilité liée |
| --- | --- |
| [`03-CREATURES.md`](./03-CREATURES.md) | Propriétés de famille, forme et instance |
| [`07-EVOLUTIONS.md`](./07-EVOLUTIONS.md) | Branches, apparences parcourues et conditions découvertes |
| [`09-GACHA.md`](./09-GACHA.md) | Nouvelles instances et acquisition au-delà de la capacité |
| [`10-PROGRESSION.md`](./10-PROGRESSION.md) | Étoiles, réinitialisations et score de Puissance |
| [`15-EVENTS.md`](./15-EVENTS.md) | Disponibilité et récompenses cosmétiques événementielles |
| [`18-UI_FLOW.md`](./18-UI_FLOW.md) | Parcours de consultation, recherche et actions protégées |
| [`04-MONETIZATION.md`](../00-foundation/04-MONETIZATION.md) | Séries, paquets, doublons et extensions de capacité |
| [`03-CARD_DESIGN.md`](../03-art/03-CARD_DESIGN.md) | Composants de carte selon le contexte |

## 16. Éléments à préciser ultérieurement

* La grammaire exacte de recherche et les filtres complémentaires.
* La présentation finale de la liste d’instances et de l’encyclopédie.
* Les informations affichées par chaque variante contextuelle de carte.
* La présentation des arbres partiellement connus.
* Les confirmations de verrouillage et d’actions irréversibles.
* Les tailles et prix des extensions de capacité.
* Les règles détaillées d’affichage des instances bloquées.
* Le calcul détaillé de la progression des séries de skins.
* Le traitement des contenus historiques dans les indicateurs de collection.

## 17. Questions ouvertes

* Quelle règle de compatibilité doit relier un skin de carte aux formes d’une créature ?
* Quelle reconnaissance non compétitive, s’il en existe une, doit accompagner la complétion d’une série ?
* Quel nom, quelle structure et quelles règles de complétion doit utiliser la catégorie des skins obtenus hors paquets ?
* Quels skins secrets peuvent rester masqués et à quel moment doivent-ils devenir visibles ?
