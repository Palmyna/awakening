# AGENTS.md

## Projet

Ce dépôt contient la documentation et, à terme, le code source de **Project Awakening**.

Project Awakening est un jeu mobile Free-to-Play centré sur la collection, la progression et la personnalisation de créatures représentées sous forme de cartes.

## Instructions obligatoires

Avant toute intervention :

1. Lire le fichier [`README.md`](./README.md).
2. Lire le document de vision [`docs/00-foundation/01-VISION.md`](./docs/00-foundation/01-VISION.md).
3. Consulter les documents existants liés à la demande.
4. Respecter la vision, la philosophie et les contraintes du projet.
5. Vérifier l’état actuel du projet avant de proposer ou d’effectuer une modification.

## Règles de travail

* Ne jamais inventer une décision de conception importante sans la signaler.
* Ne jamais présenter une hypothèse comme une décision validée.
* Ne jamais contredire un document existant sans expliquer clairement le conflit.
* Modifier uniquement les fichiers nécessaires à la demande.
* Ne pas créer de nouveau fichier sans raison claire.
* Conserver une documentation structurée, lisible et cohérente.
* Signaler les informations manquantes, les ambiguïtés et les questions ouvertes.
* Respecter les noms, chemins et conventions déjà présents dans le dépôt.
* Ne pas anticiper inutilement des fonctionnalités ou des systèmes qui n’ont pas encore été décidés.
* Préférer une modification limitée, claire et vérifiable à une intervention trop large.

## Synchronisation permanente de la documentation

La documentation doit toujours refléter l’état réel du projet.

Toute modification du projet doit inclure une vérification de son impact sur la documentation existante.

Pour chaque tâche, l’agent doit :

1. Identifier les documents liés aux éléments modifiés.
2. Vérifier si leur contenu reste exact après la modification.
3. Mettre à jour les documents devenus incomplets, incorrects ou obsolètes.
4. Mettre à jour le statut des documents dans [`README.md`](./README.md) lorsqu’un fichier est créé ou change réellement d’état.
5. Vérifier que les liens, noms de fichiers, chemins et références restent valides.
6. Signaler explicitement dans son résumé final les documents mis à jour.
7. Indiquer explicitement lorsqu’aucune mise à jour documentaire n’était nécessaire.

Une tâche ne doit pas être considérée comme terminée si le code, les données, les décisions de conception et la documentation se contredisent.

La documentation décrit les règles et décisions actuellement validées ; elle ne constitue pas une liste fermée de toutes les mécaniques futures. Une exception propre à un contenu particulier doit rester explicitement locale. Toute nouvelle règle système réutilisable, ou toute modification d’une règle commune, doit entraîner la mise à jour des documents de référence concernés.

## Documentation liée au développement

Lorsqu’une modification concerne le code ou l’architecture technique, l’agent doit vérifier si elle nécessite une mise à jour de la documentation, notamment pour :

* l’architecture générale ;
* la base de données ;
* le backend ;
* les API ;
* le système de sauvegarde ;
* la sécurité ;
* les analytics ;
* les procédures d’installation, de configuration ou de déploiement.

Lorsqu’une modification concerne le gameplay ou les données du jeu, l’agent doit vérifier si elle nécessite une mise à jour de la documentation, notamment pour :

* les combats ;
* les créatures jouables et les monstres ennemis ;
* les compétences ;
* les éléments ;
* les évolutions ;
* les objets ;
* les invocations ;
* la progression ;
* les modes de jeu ;
* l’économie et la monétisation ;
* l’interface et les parcours utilisateur.

## Décisions et hypothèses

Toute nouvelle proposition doit être clairement classée comme l’un des éléments suivants :

* **Décision validée** : décision déjà confirmée par le responsable du projet.
* **Proposition** : idée soumise à validation.
* **Hypothèse** : supposition temporaire utilisée pour avancer.
* **Question ouverte** : point nécessitant une décision ultérieure.

Une proposition ou une hypothèse ne doit jamais être intégrée comme une règle définitive sans validation explicite.

## Résumé obligatoire après intervention

À la fin de chaque intervention, l’agent doit fournir un résumé concis contenant :

* les fichiers créés ;
* les fichiers modifiés ;
* les principales modifications effectuées ;
* les documents mis à jour ;
* les hypothèses ou questions ouvertes ;
* les vérifications réalisées ;
* la confirmation qu’aucun autre fichier n’a été modifié.

## Langue

La documentation du projet doit être rédigée en français, sauf demande contraire explicite.

Le code, les noms techniques et les conventions propres aux outils utilisés peuvent rester en anglais lorsqu’il est plus pertinent de le faire.

## Priorité des documents

En cas de contradiction, l’ordre de priorité est le suivant :

1. Les documents du dossier `docs/00-foundation/`.
2. Les documents spécialisés correspondant au domaine concerné.
3. Le fichier [`README.md`](./README.md).
4. Les commentaires présents dans le code.
5. Les hypothèses formulées pendant une intervention.

En cas de conflit entre deux documents de même niveau, l’agent doit signaler le conflit et demander une validation avant de modifier une décision importante.
