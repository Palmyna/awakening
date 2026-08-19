# Project Awakening — Card Design

**Statut :** Draft de conception — base initiale à compléter

## 1. Rôle et périmètre du document

Ce document rassemble les principes validés concernant la représentation des créatures sous forme de cartes.

Il ne définit pas encore le design visuel exact, les dimensions, le ratio, la hiérarchie graphique ou le contenu obligatoire de chaque variante de carte.

## 2. Fonction de la carte

La carte de créature est la représentation visuelle et fonctionnelle d’une créature dans l’interface.

La carte et la créature ne sont pas deux entités de progression distinctes. En combat, la carte représente visuellement la créature déjà présente dans la simulation ; elle ne crée aucune nouvelle entité mécanique et ne modifie aucune règle de combat.

L’illustration utilisée par la carte reste distincte :

* de la structure fonctionnelle de la carte ;
* de la créature représentée ;
* du skin de carte possédé par le joueur.

## 3. Contextes d’utilisation

Une représentation de créature ou un composant de carte doit pouvoir être réutilisé dans plusieurs contextes, notamment :

* le combat ;
* la gestion des créatures ;
* la composition d’équipe ;
* la collection ;
* l’encyclopédie ;
* l’acquisition ;
* la fiche d’une instance ;
* la sélection dans d’autres interfaces concernées.

Les informations visibles peuvent varier selon le contexte sans modifier l’identité fonctionnelle de la créature.

## 4. Contenu contextuel

Selon son contexte, une carte peut notamment présenter :

* l’illustration de la créature ;
* son identité ;
* ses éléments ;
* des caractéristiques utiles ;
* ses PV ;
* son énergie ;
* ses effets de statut ;
* les informations contextuelles nécessaires à l’action du joueur.

Cette liste décrit des possibilités. Elle ne valide pas la présence simultanée ou permanente de toutes ces informations dans chaque contexte.

## 5. Présentation des combats

La présentation visuelle générale d’un combat prend pour référence conceptuelle un plateau d’auto-battler reposant sur des cartes, dans un esprit comparable à *Hearthstone Battlegrounds*.

Cette référence explique le type de représentation recherché. Elle n’autorise pas la copie de son identité visuelle, de ses cartes, de son interface, de son layout, de ses assets ou de ses animations.

Une position logique occupée par une créature peut être représentée visuellement par sa carte. La créature n’a pas besoin d’être affichée comme un personnage indépendant se déplaçant librement sur un terrain 2D ou 3D.

Les règles de simulation, de formation et de ciblage restent définies par le [document Combat](../01-game-design/02-COMBAT.md).

## 6. Skins de carte

Un skin de carte utilise une illustration spécifique pour modifier la représentation visuelle de la carte sans modifier la créature ni ses capacités.

Les éléments exacts de la carte affectés par un skin ne sont pas encore validés.

## 7. Éléments à préciser ultérieurement

* Le design visuel exact des cartes.
* Leur ratio et leurs dimensions.
* Leur cadre définitif.
* La disposition et la hiérarchie exactes des informations.
* Les informations obligatoirement visibles dans chaque contexte, notamment pendant un combat.
* Les états, transitions et adaptations définitifs du composant.
* Les éléments exacts modifiés par un skin, notamment le cadre, les VFX ou certains composants UI.

