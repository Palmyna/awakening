# Project Awakening — Direction artistique

**Statut :** Draft de conception — base initiale à compléter

## 1. Rôle et périmètre du document

Ce document rassemble les principes artistiques généraux actuellement validés pour **Project Awakening**.

Il définit la relation entre les illustrations, les cartes, l’interface, les animations et les VFX. Il ne fixe pas encore une direction artistique définitive, une palette, des typographies ou un style unique d’illustration.

## 2. Direction générale

Project Awakening est un jeu **2D** dont l’expérience visuelle est principalement centrée sur des créatures représentées sous forme de cartes.

Les illustrations occupent une place majeure dans l’identité des créatures et dans la mise en valeur de leur collection. La présentation générale doit cependant rester le résultat de plusieurs couches distinctes et complémentaires :

* l’illustration de la créature ;
* la structure fonctionnelle de la carte ;
* l’UI ;
* les animations de présentation ;
* les VFX.

Les principes propres aux cartes sont précisés dans le [draft Card Design](./03-CARD_DESIGN.md).

## 3. Illustrations et diversité artistique

Une forme possède une apparence de référence, principalement matérialisable par une illustration 2D.

Une même créature peut disposer de plusieurs illustrations grâce aux skins de carte. Ces illustrations peuvent employer des styles artistiques très différents, notamment manga, peinture, semi-réaliste ou 3D illustrée.

Le projet n’impose pas actuellement un style artistique unique à l’ensemble des skins. Cette diversité ne modifie ni l’identité fonctionnelle de la créature ni ses règles de gameplay.

## 4. Formats graphiques

La direction 2D n’impose pas un pipeline entièrement vectoriel.

Le vectoriel peut être pertinent pour l’UI, les icônes, les symboles d’éléments et de statuts, certains cadres, composants graphiques et VFX. Les illustrations de créatures peuvent employer des images 2D classiques.

Chaque catégorie d’asset doit pouvoir utiliser le format le plus pertinent selon son besoin. Aucune règle générale n’impose que tous les graphismes soient produits en SVG ou sous une autre forme vectorielle.

## 5. Dynamisme de la présentation

Une illustration statique ne signifie pas que l’expérience ou les combats doivent paraître statiques.

Le dynamisme peut être produit par la mise en scène des cartes, l’UI, les transitions, les animations et les VFX. Les responsabilités détaillées de ces deux derniers domaines sont réparties entre les drafts [VFX](./05-VFX.md) et [Animations](./06-ANIMATIONS.md).

## 6. Principes de production

La production artistique doit rester compatible avec le budget limité, l’équipe humaine de deux personnes et l’objectif d’autonomie avec les agents IA.

Autant que raisonnablement possible, les composants artistiques intégrés au jeu doivent pouvoir être lus, versionnés, modifiés, reproduits et vérifiés depuis le repository. Ce principe ne rend pas obligatoires la production par IA ou l’absence d’intervention humaine et n’exclut pas l’utilisation d’assets externes.

## 7. Éléments à préciser ultérieurement

* La direction artistique définitive des illustrations de base.
* La palette globale.
* Les typographies.
* Le style définitif des icônes et composants graphiques.
* Les formats, résolutions et règles de compression des illustrations.
* Le pipeline détaillé de création, de génération, de validation et d’intégration des assets.
* Les règles de cohérence entre les différents styles de skins.

