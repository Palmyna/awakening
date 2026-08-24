# Project Awakening — Collection et encyclopédie

**Statut :** Rédigé — référence actuelle, à maintenir à jour

## 1. Rôle et périmètre du document

Ce document définit le système de collection, la gestion des instances possédées, l’encyclopédie des créatures, la collection de skins de carte et la capacité de créatures.

Il formalise les distinctions entre propriété, découverte, progression, apparence et stockage. Il ne définit pas la mise en page finale, la grammaire complète de recherche, les paramètres commerciaux des extensions ou les données concrètes des futurs contenus cosmétiques.

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

## 11. Collection et séries de skins de carte

La collection de skins permet :

* de consulter les skins débloqués et non débloqués ;
* de parcourir les séries de skins de carte ;
* de visualiser la progression au sein de chaque série ;
* de connaître la méthode générale d’obtention de chaque contenu lorsqu’elle peut être communiquée ;
* de consulter les skins disponibles pour une forme précise ;
* d’appliquer un skin débloqué à la forme avec laquelle il est compatible.

Un skin de carte modifie uniquement la représentation visuelle. Il ne modifie ni la créature, ni ses caractéristiques, ni ses capacités.

Une série constitue un regroupement artistique, thématique ou conceptuel cohérent de skins. L’appartenance à une série reste distincte de sa méthode d’acquisition.

Une série peut notamment être distribuée par paquets, directement skin par skin, par des récompenses de gameplay, dans le cadre d’une opération spéciale ou par une autre méthode explicitement définie. Le modèle de lancement repose principalement sur les séries distribuées par paquets ; cette structure de collection ne valide aucune nouvelle méthode commerciale au lancement.

Une série temporairement indisponible reste normalement visible avec une indication claire de son indisponibilité actuelle et de sa politique de retour connue.

## 12. Compatibilité avec les formes

Chaque skin de carte est lié à une forme précise. Ses données déclarent explicitement cette forme et le skin ne peut pas être appliqué aux autres formes de la même famille.

Un même style artistique ou thème visuel peut être décliné sur plusieurs formes. Chaque combinaison entre une forme et cette apparence cosmétique constitue alors un skin distinct, obtenu séparément, même lorsque ces déclinaisons appartiennent à la même série.

Le sélecteur d’apparence d’une instance distingue :

* sa forme mécanique actuelle ;
* les anciennes formes réellement parcourues et débloquées comme apparences ;
* les skins de carte débloqués liés à la forme affichée.

Le joueur choisit d’abord une forme accessible comme apparence, puis peut lui appliquer uniquement les skins débloqués associés à cette forme. Le changement d’apparence reste gratuit, limité au hors-combat et sans effet mécanique.

## 13. Progression et complétion d’une série

La progression de collection est principalement suivie par série, car son périmètre est connu. L’interface reconnaît clairement sa complétion, par exemple sous la forme `X / X — Série complétée` ou d’un indicateur fonctionnel équivalent.

La complétion d’une série n’accorde aucune récompense automatique de gameplay, notamment aucune puissance, statistique, ressource de progression, équipement, invocation ou autre avantage compétitif.

Une reconnaissance future strictement cosmétique ou honorifique reste possible, notamment sous la forme d’un haut fait, d’un badge, d’un titre, d’une bordure ou d’un autre effet visuel. Aucun de ces exemples ne constitue actuellement une récompense validée ou obligatoire. Une éventuelle interaction avec le futur référentiel des hauts faits devra être définie lors de son cadrage.

## 14. Skins obtenus hors paquets

Certains skins peuvent être accordés directement comme récompenses événementielles, de haut fait, narratives, de progression, commémoratives ou liées à une opération spéciale.

Ces skins :

* n’appartiennent à aucune série distribuée par paquets ;
* ne peuvent pas être obtenus aléatoirement dans ces séries ;
* doivent afficher leur méthode générale d’obtention dans la collection lorsque celle-ci peut être communiquée.

Ils peuvent être regroupés dans une série artistique non distribuée par paquets, une collection ou une catégorie dédiée lorsque leur cohérence le justifie. Le nom officiel, l’organisation et les règles détaillées de cette catégorie restent à préciser.

## 15. Skins Secrets

`Secret` constitue une rareté cosmétique identifiable. Certains pools de skins peuvent exceptionnellement contenir un ou plusieurs skins de cette rareté, qui doivent rester rares dans la structure du pool et ne pas représenter une part importante de son contenu.

Lorsqu’un pool contient des skins Secrets, le joueur doit connaître avant toute ouverture :

* leur existence ;
* leur nombre ;
* leur rareté `Secret` ;
* leur probabilité exacte d’obtention.

La créature concernée par un skin Secret peut également être indiquée. Son illustration réelle, son nom précis et certains détails esthétiques peuvent rester masqués avant son obtention.

Dans la collection personnelle, un skin Secret non possédé apparaît comme une entrée connue mais masquée. Le joueur peut connaître son existence, sa rareté, la créature concernée lorsqu’elle est communiquée et son mode général d’obtention. Une représentation neutre, telle que `???` ou une silhouette générique non identifiable, peut remplacer l’illustration ; le choix final appartient à l’UI et à l’Art.

L’illustration réelle est révélée lorsque le joueur obtient lui-même le skin. L’obtention par un autre joueur ne la révèle pas automatiquement dans sa collection personnelle, sauf future décision sociale explicite.

Les skins Secrets suivent les mêmes règles générales de RNG et de doublons que les autres skins du pool. Ils ne bénéficient automatiquement d’aucune *pity*, garantie après un nombre de paquets ou protection particulière contre la malchance et les doublons.

## 16. Composition d’équipe

Deux instances d’une même famille peuvent cohabiter dans une équipe uniquement lorsque leurs chemins d’évolution ont réellement divergé.

Une forme du tronc commun reste incompatible avec toute autre instance de sa famille. Cette règle est globale pour tous les modes.

La liste des instances doit permettre d’identifier celles qui sont indisponibles pour dépassement de capacité et ne peuvent donc pas être sélectionnées.

## 17. Interactions et dépendances

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

## 18. Éléments à préciser ultérieurement

* La grammaire exacte de recherche et les filtres complémentaires.
* La présentation finale de la liste d’instances et de l’encyclopédie.
* Les informations affichées par chaque variante contextuelle de carte.
* La présentation des arbres partiellement connus.
* Les confirmations de verrouillage et d’actions irréversibles.
* Les tailles et prix des extensions de capacité.
* Les règles détaillées d’affichage des instances bloquées.
* Le calcul détaillé de la progression des séries de skins.
* Le traitement des contenus historiques dans les indicateurs de collection.
* La représentation finale des skins Secrets non obtenus, le wording, la présentation de leur rareté et l’animation de révélation.
* L’affichage éventuel de la créature concernée par un skin Secret.
* Le nombre concret de skins Secrets, les séries concernées et l’identité de chaque contenu.
* Les probabilités exactes, les tailles des séries et la répartition des skins entre les raretés.
* Les thèmes et styles des futures séries ainsi que leurs méthodes d’acquisition concrètes.
* La présentation d’une série complétée et l’éventuelle reconnaissance strictement cosmétique ou honorifique associée.
* Le nom, l’organisation UI et le contenu précis de la catégorie consacrée aux skins spéciaux ou obtenus hors paquets.
* Les prix et modalités de futures méthodes commerciales uniquement si celles-ci sont validées ultérieurement.
