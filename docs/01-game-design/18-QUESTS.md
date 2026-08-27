# Project Awakening — Quêtes

**Statut :** Draft de conception — à relire et valider

## 1. Rôle et périmètre du document

Ce document définit le fonctionnement général actuellement validé :

* des trois quêtes journalières ;
* des quêtes saisonnières individuelles ;
* des quêtes saisonnières de Guilde.

Les autres catégories éventuelles de quêtes — narratives, hebdomadaires, événementielles ou propres à un autre mode — ne sont pas validées. Elles ne doivent pas être déduites du seul emploi générique du mot « quête ».

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

## 9. Quêtes saisonnières

Une Saison peut proposer des quêtes saisonnières individuelles et des quêtes saisonnières de Guilde. Elles restent totalement distinctes des trois quêtes journalières et ne modifient ni leur nombre, ni leur attribution aléatoire, ni leur renouvellement quotidien.

Les quêtes saisonnières :

* restent disponibles pendant la Saison concernée ;
* ne disparaissent pas selon une rotation hebdomadaire artificielle ;
* restent relativement légères ;
* ne doivent pas devenir nécessaires à la progression normale ;
* ne constituent ni un niveau de Saison, ni un parcours global de récompenses.

Une quête déjà disponible ne doit pas être retirée après quelques jours uniquement afin de créer de la pression.

### 9.1. Quêtes saisonnières de Guilde

Les quêtes saisonnières de Guilde apportent des objectifs collectifs supplémentaires. Elles restent légères, accessibles et non contraignantes.

Elles ne recréent aucun système général de quêtes quotidiennes ou hebdomadaires de Guilde. Leur application au contexte des Guildes reste cohérente avec [`15-GUILDS.md`](./15-GUILDS.md).

### 9.2. Récompenses

Les quêtes saisonnières donnent principalement de petites récompenses issues des systèmes normaux du jeu, par exemple de la monnaie générale, des ressources d’invocation, des composants ou de petites ressources de progression.

Ces familles illustrent l’échelle attendue sans imposer la liste de chaque Saison. Une simple quête saisonnière ne doit pas accorder directement un cosmétique exclusif important.

La complétion de l’ensemble des quêtes d’une Saison peut éventuellement accorder une récompense plus intéressante, notamment un paquet cosmétique. Cette possibilité n’est pas obligatoire et son contenu exact relève du content design et du balancing.

### 9.3. Clôture

À la clôture exacte de la Saison :

* une quête non terminée devient immédiatement indisponible ;
* elle ne peut plus progresser ;
* une quête terminée reste accomplie ;
* sa récompense déjà gagnée peut encore être récupérée pendant l’inter-saison selon les règles de disponibilité de [`10-PROGRESSION.md`](./10-PROGRESSION.md).

La même règle peut s’appliquer à une récompense globale déjà gagnée grâce à la complétion de toutes les quêtes de la Saison.

## 10. Relation avec les Saisons, les Events et les autres objectifs

Les Events peuvent proposer leurs propres objectifs, mais aucune relation structurelle entre ces objectifs et les trois quêtes journalières n’est validée.

Les quêtes saisonnières utilisent le calendrier global de [`16-SEASONS.md`](./16-SEASONS.md). Elles constituent un parcours distinct des quêtes journalières et des objectifs temporaires d’Event.

Toute interaction future entre ces catégories devra préserver :

* l’accessibilité des trois quêtes quotidiennes ;
* l’absence de dépendance à un Event temporaire ;
* la lisibilité des récompenses et des périodes ;
* la règle selon laquelle seules les fonctionnalités débloquées sont utilisées.

## 11. Dépendances

| Document | Responsabilité liée |
| --- | --- |
| [`01-GAME_DESIGN_DOCUMENT.md`](./01-GAME_DESIGN_DOCUMENT.md) | Session mobile et règles validées des trois quêtes |
| [`09-GACHA.md`](./09-GACHA.md) | Ressource générale d’invocation |
| [`10-PROGRESSION.md`](./10-PROGRESSION.md) | Récompenses ayant un effet sur la progression |
| [`12-MODES.md`](./12-MODES.md) | Cadre commun des activités pouvant servir d’objectif |
| [`15-GUILDS.md`](./15-GUILDS.md) | Application des quêtes saisonnières au contexte des Guildes |
| [`16-SEASONS.md`](./16-SEASONS.md) | Calendrier, inter-saison et cadre des quêtes saisonnières |
| [`17-EVENTS.md`](./17-EVENTS.md) | Éventuels objectifs temporaires distincts |
| [`20-UI_FLOW.md`](./20-UI_FLOW.md) | Présentation, suivi et récupération |
| [`04-MONETIZATION.md`](../00-foundation/04-MONETIZATION.md) | Paquets gratuits et séparation économique |

## 12. Éléments à préciser ultérieurement

* La liste concrète des quêtes.
* Leurs catégories, conditions et récompenses.
* Les pondérations et règles de sélection aléatoire.
* Les quantités de récompenses.
* L’heure de renouvellement.
* Le wording, les icônes et la présentation finale.
* Le moment exact de déblocage et le contenu du tutoriel.
* Les listes et conditions concrètes des quêtes saisonnières individuelles et de Guilde.
* Les petites récompenses saisonnières et leurs quantités.
* La présence et le contenu exacts d’une éventuelle récompense de complétion globale.

## 13. Questions ouvertes

* Quelles catégories d’objectifs doivent composer la liste prédéfinie ?
* Comment empêcher les répétitions indésirables ou les combinaisons de quêtes trop proches ?
* Le joueur peut-il remplacer une quête et, si oui, selon quelles limites sans paiement obligatoire ?
* Les récompenses sont-elles remises automatiquement ou réclamées manuellement ?
* Que devient une quête terminée mais non réclamée au renouvellement ?
* Les Events peuvent-ils modifier la liste journalière ou doivent-ils conserver des objectifs entièrement séparés ?
