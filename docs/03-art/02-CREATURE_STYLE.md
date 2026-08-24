# Project Awakening — Style des créatures

**Statut :** Draft de conception — base initiale à compléter

## 1. Rôle et périmètre du document

Ce document rassemble les décisions validées concernant la représentation artistique des créatures.

Il complète le [document structurel des créatures](../01-game-design/03-CREATURES.md), qui reste responsable de leur identité fonctionnelle, et le [draft de direction artistique](./01-ART_DIRECTION.md), qui porte les principes artistiques généraux.

## 2. Représentation principale

Les créatures sont principalement représentées par des illustrations 2D intégrées à leurs cartes.

L’illustration d’une forme peut rester statique. Le projet n’impose pas actuellement :

* de modèle 3D de la créature ;
* de personnage 3D animé ;
* de rig ou d’animation squelettique 2D ;
* de découpage systématique de l’illustration en plusieurs parties ;
* de nombreuses frames dessinées à la main.

Une forme conserve une apparence de référence conformément aux règles fonctionnelles existantes. Cette apparence peut être principalement matérialisée par son illustration de carte.

Les équipements attribués à une instance ne sont pas automatiquement visibles sur cette illustration. Une représentation exceptionnelle d'un équipement doit relever d'une décision artistique explicitement documentée et ne modifie pas l'objet fonctionnel équipé.

## 3. Variantes par les skins de carte

Une même forme peut disposer de plusieurs illustrations grâce aux skins de carte.

Ces illustrations peuvent adopter des styles très différents, notamment manga, peinture, semi-réaliste ou 3D illustrée. Un skin reste cosmétique : l’illustration employée ne modifie ni la structure fonctionnelle de la créature, ni ses caractéristiques, ni ses capacités.

Chaque skin est conçu pour une forme précise. Un style artistique peut être décliné sur plusieurs formes d’une famille, mais chaque déclinaison constitue un skin et une illustration distincts.

L’illustration constitue un asset artistique distinct du skin de carte possédé par le joueur et de la structure fonctionnelle de la carte.

## 4. Relation avec l’animation

Le personnage représenté dans l’illustration n’a pas besoin d’être animé directement. Le dynamisme peut provenir de la carte, de l’UI, des transitions et des VFX conformément aux drafts [Animations](./06-ANIMATIONS.md) et [VFX](./05-VFX.md).

## 5. Éléments à préciser ultérieurement

* Le style définitif des illustrations de référence.
* Les règles de composition, de cadrage et de lisibilité propres aux créatures.
* Les formats, résolutions et règles de compression.
* Le pipeline de création ou de génération des illustrations.
* Les règles détaillées de cohérence entre les formes d’une famille.
* Les éléments exacts d’une carte affectés par un skin.
