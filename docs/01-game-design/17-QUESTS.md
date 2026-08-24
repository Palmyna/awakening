# Project Awakening — Quêtes

**Statut :** Draft de conception — à relire et valider

## 1. Rôle et périmètre du document

Ce document définit le fonctionnement général actuellement validé des quêtes journalières.

Les autres catégories éventuelles de quêtes — narratives, hebdomadaires, événementielles ou propres à un mode — ne sont pas validées. Elles ne doivent pas être déduites du seul emploi générique du mot « quête ».

## 2. Fonction des quêtes journalières

Les quêtes journalières encouragent le retour au jeu et la variation des activités sans devenir obligatoires pour progresser normalement.

Elles s’intègrent à une session mobile libre : le joueur peut les accomplir, progresser dans le mode Histoire, gérer ses créatures, préparer ses équipes ou poursuivre un autre objectif personnel sans suivre une liste d’actions obligatoire.

Les quêtes doivent rester compatibles avec des actions et activités réellement utiles à la boucle générale. Elles ne doivent pas pousser le joueur vers une fonctionnalité inaccessible ou une dépense.

## 3. Attribution quotidienne

Chaque jour, le joueur reçoit exactement trois quêtes journalières aléatoires tirées dans une liste prédéfinie.

Les trois quêtes proposées doivent :

* utiliser uniquement des fonctionnalités déjà débloquées ;
* rester réalisables sans durée excessive ;
* encourager une certaine variété d’activités ;
* accorder des récompenses ayant un effet sur la progression ;
* rester facultatives pour la progression normale.

Le système de sélection doit empêcher de proposer une quête inaccessible en raison de l’état réel du compte.

La liste concrète, les catégories, les pondérations et les protections contre des combinaisons inadaptées restent à définir.

## 4. Cycle journalier et absence de punition

Une journée manquée fait perdre l’occasion de réaliser les quêtes de cette journée.

Elle ne provoque :

* aucune perte de progression générale ;
* aucune suppression d’une récompense déjà obtenue ;
* aucune perte d’énergie accumulée ;
* aucune rupture d’une série de connexion punitive.

Aucune série de connexion punitive n’est prévue.

L’heure de renouvellement, le traitement d’une quête en cours au moment du renouvellement et les règles éventuelles de récupération d’une récompense non réclamée restent à définir.

## 5. Conditions de quête

Une condition doit être formulée de manière mesurable et compréhensible à partir d’un état ou d’une action réellement suivi par le jeu.

Elle doit préciser ce qui fait progresser la quête et ne doit pas dépendre d’une fonctionnalité non débloquée.

Les types concrets de conditions ne sont pas encore validés. La documentation existante ne permet donc pas d’imposer, par exemple, des objectifs de victoire, d’invocation, de fabrication, de progression ou de collection comme catégories obligatoires.

Les quêtes journalières ne constituent pas des conditions d’évolution. Le système d’évolution n’utilise pas de compteurs historiques comme un nombre de combats, de victoires ou d’actions déjà accomplies.

## 6. Progression et validation

L’interface doit permettre au joueur de connaître :

* l’objectif de chaque quête ;
* sa progression actuelle ;
* sa condition d’achèvement ;
* sa récompense ;
* le temps restant avant le renouvellement.

Les règles de validation automatique ou de récupération manuelle d’une récompense ne sont pas encore définies.

Une quête ne doit jamais demander au joueur d’effectuer un achat réel. Les ouvertures ou acquisitions cosmétiques payantes ne constituent pas un prérequis nécessaire à une progression journalière normale.

## 7. Récompenses

Les quêtes journalières accordent des récompenses ayant un effet sur la progression.

Elles constituent notamment une source validée de la ressource générale d’invocation.

Des paquets de skins de carte peuvent également être obtenus gratuitement grâce aux quêtes. Pour une même série, un paquet obtenu en jouant utilise les mêmes skins, probabilités, quantité de contenu, règles de doublons et règles d’ouverture que le paquet acheté correspondant.

La présence possible d’une récompense cosmétique ne transforme pas une quête en offre commerciale et ne permet aucune conversion de la boutique cosmétique vers la puissance.

Les types exacts de récompenses, leurs quantités et leur répartition entre les trois quêtes restent à définir et à équilibrer.

## 8. Déblocages et onboarding

Les fonctionnalités sont principalement débloquées par des jalons du mode Histoire et accompagnées d’un tutoriel court.

La liste de quêtes disponible pour un compte doit évoluer avec ces déblocages. Une quête utilisant une fonctionnalité nouvellement accessible peut apparaître uniquement lorsque le joueur est en mesure de comprendre et d’utiliser cette fonctionnalité.

Le moment exact du déblocage des quêtes journalières et leur tutoriel ne sont pas encore définis.

## 9. Relation avec les événements et autres objectifs

Les événements peuvent proposer leurs propres objectifs, mais aucune relation structurelle entre ces objectifs et les trois quêtes journalières n’est validée.

Un futur système peut choisir de garder ces parcours séparés ou d’autoriser certaines interactions. Une telle décision devra préserver :

* l’accessibilité des trois quêtes quotidiennes ;
* l’absence de dépendance à un événement temporaire ;
* la lisibilité des récompenses et des périodes ;
* la règle selon laquelle seules les fonctionnalités débloquées sont utilisées.

## 10. Dépendances

| Document | Responsabilité liée |
| --- | --- |
| [`01-GAME_DESIGN_DOCUMENT.md`](./01-GAME_DESIGN_DOCUMENT.md) | Session mobile et règles validées des trois quêtes |
| [`09-GACHA.md`](./09-GACHA.md) | Ressource générale d’invocation |
| [`10-PROGRESSION.md`](./10-PROGRESSION.md) | Récompenses ayant un effet sur la progression |
| [`12-MODES.md`](./12-MODES.md) | Fonctionnalités et activités débloquées |
| [`16-EVENTS.md`](./16-EVENTS.md) | Éventuels objectifs temporaires distincts |
| [`19-UI_FLOW.md`](./19-UI_FLOW.md) | Présentation, suivi et récupération |
| [`04-MONETIZATION.md`](../00-foundation/04-MONETIZATION.md) | Paquets gratuits et séparation économique |

## 11. Éléments à préciser ultérieurement

* La liste concrète des quêtes.
* Leurs catégories, conditions et récompenses.
* Les pondérations et règles de sélection aléatoire.
* Les quantités de récompenses.
* L’heure de renouvellement.
* Le wording, les icônes et la présentation finale.
* Le moment exact de déblocage et le contenu du tutoriel.

## 12. Questions ouvertes

* Quelles catégories d’objectifs doivent composer la liste prédéfinie ?
* Comment empêcher les répétitions indésirables ou les combinaisons de quêtes trop proches ?
* Le joueur peut-il remplacer une quête et, si oui, selon quelles limites sans paiement obligatoire ?
* Les récompenses sont-elles remises automatiquement ou réclamées manuellement ?
* Que devient une quête terminée mais non réclamée au renouvellement ?
* Les événements peuvent-ils modifier la liste journalière ou doivent-ils conserver des objectifs entièrement séparés ?
