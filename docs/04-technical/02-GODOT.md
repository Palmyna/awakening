# Project Awakening — Godot

**Statut :** Draft de conception — base initiale à compléter

## 1. Rôle et périmètre du document

Ce document constitue la référence spécialisée pour les décisions et conventions propres à l’utilisation de **Godot** dans **Project Awakening**.

Le [document d’architecture générale](./01-ARCHITECTURE.md) répond principalement à la question : **« Comment Project Awakening est-il architecturé ? »** Il définit les principes techniques globaux indépendamment de leur traduction détaillée dans le moteur.

Le présent document répond principalement à la question : **« Comment cette architecture est-elle implémentée et organisée dans Godot ? »** Il accueillera progressivement les choix concrets propres au moteur à mesure qu’ils seront validés.

Il ne remplace pas :

* le document d’architecture générale ;
* le [document Combat](../01-game-design/02-COMBAT.md), responsable des règles de simulation et de gameplay ;
* les documents du dossier [`03-art`](../03-art/), responsables des décisions artistiques et visuelles.

## 2. Contexte technique validé

**Godot est le moteur actuellement retenu pour Project Awakening.**

Le projet est principalement conçu comme un jeu :

* mobile ;
* 2D ;
* centré sur des interfaces et des cartes ;
* destiné à Android et iOS.

Cette décision ne fixe pas encore la version de Godot, le ou les langages, la structure du projet ou les conventions d’implémentation.

## 3. Compatibilité avec la représentation 2D

La réalisation dans Godot doit rester compatible avec les principes artistiques déjà validés :

* les créatures sont principalement représentées sous forme de cartes ;
* leurs illustrations peuvent rester statiques ;
* le dynamisme repose largement sur la mise en scène des cartes, l’UI, les animations et les VFX ;
* aucune production systématique de modèles 3D n’est imposée ;
* aucun rig 2D complexe n’est obligatoire pour chaque créature ;
* aucun pipeline entièrement vectoriel n’est imposé.

Ces principes ne déterminent pas encore leur implémentation technique dans Godot. Les décisions artistiques restent définies par les drafts de [direction artistique](../03-art/01-ART_DIRECTION.md), de [style des créatures](../03-art/02-CREATURE_STYLE.md), de [Card Design](../03-art/03-CARD_DESIGN.md), d’[UI](../03-art/04-UI_GUIDE.md), de [VFX](../03-art/05-VFX.md) et d’[animations](../03-art/06-ANIMATIONS.md).

## 4. Séparation entre simulation et représentation

La simulation du combat doit rester indépendante de sa représentation visuelle dans Godot.

La couche chargée de l’affichage doit restituer les événements issus de la simulation sans modifier leurs résultats. Les responsabilités exactes de cette couche, ses interfaces et son organisation dans Godot ne sont pas encore définies.

Cette séparation doit rester compatible avec :

* les replays ;
* les différentes vitesses de visualisation ;
* les tests automatisés ;
* les simulations de balancing ;
* le debugging déterministe ;
* une future validation serveur.

Les principes généraux sont définis dans le [document d’architecture](./01-ARCHITECTURE.md) et les règles fonctionnelles de simulation dans le [document Combat](../01-game-design/02-COMBAT.md).

## 5. Autonomie avec les agents IA et reproductibilité

L’utilisation de Godot doit, autant que raisonnablement possible, privilégier des éléments que Codex et les autres agents IA peuvent créer, lire, modifier, versionner, maintenir, tester et vérifier directement depuis le repository.

Ce principe pourra notamment concerner :

* les scripts ;
* les scènes ;
* les ressources ;
* les configurations ;
* l’UI et les composants de cartes ;
* les shaders et VFX ;
* les données ;
* les autres fichiers du projet Godot.

Aucun format, mécanisme ou type de fichier Godot n’est rendu obligatoire par cette liste.

L’objectif est de maximiser la reproductibilité depuis le repository et d’éviter les dépendances inutiles à des manipulations manuelles impossibles ou difficiles à reproduire. Ce principe n’interdit pas l’utilisation manuelle de l’éditeur Godot lorsqu’elle est pertinente.

## 6. Éléments à préciser ultérieurement

### 6.1. Version et langages

* La version exacte de Godot.
* La politique de mise à jour du moteur.
* Le langage principal.
* L’éventuelle utilisation de plusieurs langages.

### 6.2. Structure du projet

* L’arborescence du projet Godot.
* Les conventions de dossiers.
* Les conventions de noms.
* La séparation entre gameplay, UI, données et assets.

### 6.3. Scènes et nodes

* L’architecture des scènes.
* Les responsabilités des différents types de scènes.
* La politique d’instanciation.
* La composition des cartes et composants UI.
* L’utilisation éventuelle des Autoloads.
* La communication entre les systèmes.

### 6.4. Resources et données

* L’utilisation éventuelle des Resources Godot.
* L’utilisation éventuelle de JSON ou d’autres formats.
* La représentation des données statiques et des données runtime.
* La séparation entre données de contenu et logique.

### 6.5. UI

* L’architecture technique des interfaces.
* La gestion des thèmes.
* L’adaptation responsive aux appareils mobiles.
* L’adaptation aux différentes résolutions et ratios d’écran.
* L’organisation technique des composants réutilisables.

### 6.6. Assets

* Le pipeline d’import.
* Les formats d’images.
* Les règles de compression.
* La gestion des illustrations.
* L’utilisation éventuelle de SVG.
* La gestion de l’audio.
* L’organisation technique des shaders et VFX.

### 6.7. Addons et dépendances

* La politique concernant les addons Godot.
* Les dépendances tierces.
* Leurs critères d’acceptation.
* Leur stratégie de maintenance.

### 6.8. Tests

* Les tests unitaires.
* Les tests d’intégration.
* Les tests de simulation.
* Les éventuels tests UI.
* Leur exécution automatisée.

### 6.9. Builds et plateformes

* La configuration des exports Android et iOS.
* L’automatisation des builds.
* La gestion des signatures.
* Les environnements de développement et de production.

### 6.10. Performances

* Les budgets mémoire.
* Les budgets CPU et GPU.
* Le nombre de cartes et d’effets simultanés.
* Les appareils mobiles cibles et leurs critères de performance.

### 6.11. Workflow IA

* Les règles permettant à Codex et aux autres agents IA de créer ou modifier des scènes et ressources.
* Les éléments pouvant nécessiter une intervention manuelle.
* La validation automatique des fichiers Godot.
* Les conventions facilitant les modifications par les agents IA.

## 7. Décisions non prises

Ce draft ne valide notamment pas :

* GDScript ou C# comme langage principal ;
* une version précise de Godot ;
* une structure définitive des dossiers ;
* l’utilisation obligatoire de `.tscn` ou d’un autre format ;
* une architecture exacte des nodes ;
* des Autoloads précis ;
* un pattern ECS, MVC ou une autre architecture particulière ;
* des addons ;
* un système exact d’événements ;
* l’architecture exacte du combat côté code ;
* un pipeline d’import définitif ;
* un système de build final.

Ces sujets nécessitent une validation explicite avant de devenir des conventions du projet.

