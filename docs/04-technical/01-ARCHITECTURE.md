# Project Awakening — Architecture technique

**Statut :** Draft de conception — base initiale à compléter

## 1. Rôle et périmètre du document

Ce document rassemble les décisions et principes techniques actuellement validés pour **Project Awakening**.

Il constitue une première base d’architecture. Il ne fixe pas encore la version du moteur, le langage, l’arborescence du projet, l’architecture des scènes, le modèle de données ou les conventions d’implémentation.

Il répond principalement à la question : **« Comment Project Awakening est-il architecturé ? »**

La traduction progressive de ces principes dans le moteur appartient au [draft spécialisé Godot](./02-GODOT.md), qui répond principalement à la question : **« Comment cette architecture est-elle implémentée et organisée dans Godot ? »**

## 2. Moteur et représentation

**Godot est le moteur actuellement retenu pour Project Awakening.**

Le jeu est conçu en 2D et son expérience visuelle est principalement centrée sur des créatures représentées sous forme de cartes.

Cette décision ne fixe pas encore :

* la version précise de Godot ;
* le langage de programmation ;
* l’organisation des scènes ;
* la structure exacte du projet ;
* les conventions de code.

Les décisions et conventions propres à l’utilisation du moteur doivent être centralisées dans le [draft Godot](./02-GODOT.md) plutôt que détaillées dans le présent document d’architecture générale.

## 3. Séparation entre simulation et représentation

La simulation de combat doit être indépendante de sa représentation visuelle.

Les cartes, animations, VFX et composants UI restituent les événements de la simulation sans modifier :

* la timeline ;
* les positions logiques et la formation ;
* les ciblages ;
* les calculs et dégâts ;
* les Skills et statuts ;
* le RNG et ses priorités ;
* les conditions de victoire ;
* les autres règles définies dans le [document Combat](../01-game-design/02-COMBAT.md).

La carte affichée en combat représente la créature simulée. Elle n’est pas une entité mécanique distincte.

## 4. Reproductibilité de la simulation

La séparation entre simulation et représentation doit préserver la possibilité de :

* reproduire un résultat à partir des mêmes conditions initiales et de la même seed RNG ;
* produire des replays ;
* utiliser différentes vitesses de visualisation ;
* exécuter des simulations de balancing ;
* automatiser les tests ;
* effectuer une validation serveur ;
* debugger un résultat déterministe.

Les responsabilités exactes du client, du backend et d’un éventuel service de validation restent à définir.

## 5. Autonomie et production depuis le repository

L’architecture doit favoriser, autant que raisonnablement possible, des systèmes que l’équipe et les agents IA peuvent lire, créer, modifier, maintenir, versionner, tester et vérifier directement depuis le repository.

Ce principe concerne particulièrement :

* le code ;
* les données et configurations ;
* les interfaces et composants de cartes ;
* les scènes ;
* les shaders et VFX ;
* les animations de présentation ;
* la logique de gameplay ;
* la logique de présentation.

Le projet doit éviter les dépendances inutiles à des opérations manuelles impossibles ou difficiles à reproduire depuis le repository.

Cette direction vise à maximiser l’autonomie et la reproductibilité. Elle n’interdit ni les assets externes, ni l’intervention d’un artiste humain, ni une opération manuelle justifiée, et n’impose pas que tous les éléments soient produits par Codex.

## 6. Contraintes générales

Les choix techniques doivent rester compatibles avec :

* les plateformes mobiles Android et iOS ;
* le budget volontairement limité ;
* l’équipe humaine de deux personnes ;
* la préférence du projet pour l’open source et les Free Tiers ;
* la maintenance et l’évolution du jeu sur plusieurs années.

## 7. Éléments à préciser ultérieurement

* La version de Godot.
* Le langage de programmation.
* Les conventions de code.
* L’arborescence du projet.
* L’architecture détaillée des scènes et composants.
* L’architecture et les formats des données.
* Les dépendances et addons.
* Le système de build et de déploiement.
* La stratégie de tests.
* La répartition des responsabilités entre client et backend.
* La sauvegarde, la sécurité, les API et les services en ligne.
* Les objectifs et budgets de performance.
* Le pipeline d’assets.
* Les autres choix d’implémentation.
