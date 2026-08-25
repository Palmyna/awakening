# Project Awakening — Events

**Statut :** Draft de conception — à relire et valider

## 1. Rôle et périmètre du document

Ce document constitue la base du système d’Events de Project Awakening.

Un Event est une petite animation temporaire utilisant principalement les systèmes et modes de jeu déjà existants. Il peut accompagner une occasion ponctuelle, proposer quelques objectifs thématiques et accorder de petites récompenses compatibles avec les systèmes permanents.

Les Events ne font pas partie de la vertical slice. Leur ordre de production, leur cadrage détaillé, leur calendrier et leur contenu concret restent à définir.

## 2. Identité d’un Event

Un Event doit rester :

* temporaire ;
* ciblé sur une occasion ou un thème identifiable ;
* simple à comprendre et à rejoindre ;
* principalement fondé sur le gameplay existant ;
* réaliste pour une équipe humaine de deux personnes.

Halloween, Noël, le Nouvel An ou l’anniversaire du jeu constituent des exemples d’intention. Ils ne forment ni une liste obligatoire, ni un calendrier validé.

La durée de référence peut être courte, par exemple quelques jours, mais aucune durée précise n’est encore validée.

## 3. Utilisation des systèmes existants

Un Event ne doit normalement pas nécessiter la création d’un nouveau mode de jeu.

Il peut s’appuyer sur des actions, règles ou activités déjà disponibles afin de proposer une variation thématique limitée. Le fonctionnement interne du mode ou du système utilisé reste défini dans son référentiel spécialisé.

Le modèle courant d’un Event ne doit pas demander :

* une nouvelle activité complète ;
* une progression complexe propre à l’Event ;
* une infrastructure lourde spécifique ;
* un volume important de contenu, d’UI, d’animations ou de VFX ;
* un nouveau mode conçu spécialement pour chaque occasion.

Une exception future à cette orientation nécessiterait une décision explicite distincte et ne serait pas déduite du présent draft.

## 4. Objectifs temporaires

Un Event peut proposer un petit ensemble d’objectifs thématiques accomplis dans le gameplay normal.

Ces objectifs peuvent, à titre purement illustratif, demander de vaincre certains adversaires dans un mode existant, d’utiliser certaines créatures ou certains éléments, ou d’accomplir des actions déjà suivies par le jeu. Aucun de ces exemples ne constitue une catégorie obligatoire ou une mécanique validée individuellement.

Chaque objectif concret devra préciser clairement :

* sa condition mesurable ;
* sa période de disponibilité ;
* les fonctionnalités nécessaires ;
* sa progression visible ;
* sa récompense.

Les objectifs d’un Event restent distincts des trois quêtes journalières définies dans [`18-QUESTS.md`](./18-QUESTS.md). Aucune modification automatique de la liste journalière n’est actuellement validée.

## 5. Récompenses légères

Un Event peut accorder de petites récompenses adaptées à son ampleur, notamment :

* un skin thématique ;
* un paquet de skins de carte ;
* un autre cosmétique ;
* une petite quantité d’une récompense ou ressource déjà utilisée par les systèmes existants.

Les récompenses précises, leurs quantités et leurs conditions restent à définir.

Lorsqu’un paquet appartient à une série également distribuée commercialement, il utilise le même ensemble de skins, les mêmes probabilités, le même nombre de skins, les mêmes règles de doublons et les mêmes règles d’ouverture que les autres paquets de cette série.

Un skin accordé directement ne doit appartenir à aucune série distribuée par paquets. Sa méthode d’obtention reste indiquée dans le système de collection.

Les fondations permettent qu’une créature soit exceptionnellement accordée directement par une récompense événementielle explicitement documentée. Cette possibilité générale ne fait pas d’une créature une récompense courante des Events légers et ne valide aucun cas concret.

## 6. Progression durable

Un Event peut mettre en valeur ou accélérer ponctuellement une boucle existante, mais il ne doit pas rendre son contenu temporaire indispensable à la progression normale.

Une condition d’évolution ne doit jamais devenir définitivement impossible parce qu’un Event unique est terminé. Toute condition temporelle doit rester accessible ou revenir dans un délai raisonnable selon [`07-EVOLUTIONS.md`](./07-EVOLUTIONS.md).

Un Event ne remet pas à zéro la progression durable du compte, des créatures ou de la collection.

## 7. Temporalité et transparence

Avant de participer, le joueur doit pouvoir connaître :

* la période de disponibilité ;
* les objectifs et leurs conditions ;
* les fonctionnalités requises ;
* les récompenses principales ;
* les éventuelles règles particulières réellement applicables.

La présentation doit éviter les comptes à rebours artificiels, les informations ambiguës et les exclusivités non annoncées.

Lorsqu’une série de skins ou une offre cosmétique est temporairement associée à un Event, les règles de disponibilité, de retour, de prix, de probabilités et de doublons restent celles du cadre de monétisation.

## 8. Relation avec les Saisons

Un Event peut se dérouler pendant une Saison ou reprendre son thème, mais il reste une animation temporaire distincte.

Une Saison constitue une trame périodique transversale susceptible d’influencer plusieurs modes et progressions saisonnières selon [`16-SEASONS.md`](./16-SEASONS.md). Un Event ne devient pas une Saison du seul fait qu’il possède un thème ou une date de fin.

## 9. Cohérence narrative

Un thème festif ou commémoratif ne constitue pas automatiquement un événement canonique de l’univers.

Lorsqu’un Event affirme une conséquence narrative, introduit un élément canonique ou s’appuie sur un événement important du monde, cette dimension doit respecter le [référentiel Lore](../02-world/01-LORE.md).

## 10. Contraintes de production

La cadence et l’ampleur des Events doivent rester compatibles avec la roadmap, le budget et les capacités d’une équipe humaine de deux personnes.

Le système doit privilégier la réutilisation des modes, règles, objectifs mesurables, composants UI et récompenses existants. Aucune cadence fixe n’est validée.

## 11. Dépendances documentaires

| Document | Responsabilité liée |
| --- | --- |
| [`07-EVOLUTIONS.md`](./07-EVOLUTIONS.md) | Protection contre les conditions temporelles définitivement impossibles |
| [`09-GACHA.md`](./09-GACHA.md) | Ressource générale d’invocation et acquisitions directes exceptionnelles |
| [`10-PROGRESSION.md`](./10-PROGRESSION.md) | Récompenses et progression durable |
| [`11-COLLECTION.md`](./11-COLLECTION.md) | Disponibilité et skins obtenus hors paquets |
| [`12-MODES.md`](./12-MODES.md) | Utilisation des modes et activités existants |
| [`16-SEASONS.md`](./16-SEASONS.md) | Trame périodique transversale distincte des Events |
| [`18-QUESTS.md`](./18-QUESTS.md) | Quêtes journalières distinctes des objectifs temporaires |
| [`20-UI_FLOW.md`](./20-UI_FLOW.md) | Accès, suivi, information et transparence |
| [`04-MONETIZATION.md`](../00-foundation/04-MONETIZATION.md) | Paquets, offres temporaires et protection des joueurs |
| [`01-LORE.md`](../02-world/01-LORE.md) | Cohérence narrative des Events qui portent une dimension canonique |

## 12. Éléments à préciser ultérieurement

* La durée et la cadence des Events.
* Les premières occasions retenues.
* Les catégories, conditions et quantités d’objectifs temporaires.
* Les petites récompenses et quantités associées.
* Les règles de récurrence ou de retour d’un Event.
* Les interactions éventuelles avec les quêtes journalières.
* Les besoins précis d’interface, de calendrier et de notification.

## 13. Questions ouvertes

* Quel premier ensemble minimal d’objectifs temporaires doit être supporté ?
* Quels Events doivent être récurrents et lesquels doivent rester ponctuels ?
* Comment présenter un Event lié au thème d’une Saison sans confondre leurs progressions et leurs récompenses ?
