# Project Awakening — Événements et contenus saisonniers

**Statut :** Draft de conception — à relire et valider

## 1. Rôle et périmètre du document

Ce document consolide les décisions existantes concernant les événements temporaires, les rotations et les contenus saisonniers.

Les événements sont envisagés à long terme et exclus de la vertical slice. Leur calendrier, leur cadence, leurs formats, leurs récompenses et leur ordre de production ne sont pas encore validés.

## 2. Fonction dans l’expérience

Les événements peuvent :

* proposer de nouveaux défis ;
* mettre en valeur certaines équipes ou certains éléments ;
* offrir des récompenses particulières ;
* renouveler les objectifs ;
* introduire temporairement de nouveaux contenus.

Ils prolongent les motivations de développement des créatures, d’expérimentation des compositions, de découverte et de collection. Ils ne doivent pas devenir la seule source d’une progression normale ou imposer un rythme incompatible avec une équipe de production de deux personnes.

## 3. Statut et relation avec les modes

Un événement peut s’appuyer sur un mode existant, proposer une variante explicitement documentée ou introduire un contenu temporaire particulier.

Lorsqu’il utilise le moteur de combat, il hérite des règles communes définies dans [`02-COMBAT.md`](./02-COMBAT.md) et [`12-MODES.md`](./12-MODES.md). Toute exception de durée, victoire, score, composition ou récompense doit être explicitement décrite.

La présence d’événements temporaires et de contenus saisonniers dans la vision de long terme ne valide aucun format précis, classement, coopération, ressource événementielle ou passe.

## 4. Contenu, accès et rejouabilité

Chaque événement devra définir au minimum :

* sa période d’accès ;
* les fonctionnalités prérequises ;
* ses activités ou objectifs ;
* ses règles de réussite, de score ou de répétition ;
* ses éventuels coûts d’entrée ;
* ses récompenses ;
* les informations conservées après sa fin ;
* sa politique de retour lorsqu’elle existe.

Une activité événementielle jouée individuellement utilise par défaut la réserve générale d’énergie. Un événement peut définir une régulation différente uniquement lorsqu’une exception est explicitement justifiée et documentée par son design. Cette possibilité ne valide actuellement aucune énergie, aucun ticket, aucune clé ou aucune ressource événementielle d’entrée particulière.

Une fonctionnalité temporaire ne doit pas contredire les règles communes des créatures, du combat, des éléments, des Effets de combat, des évolutions, des objets ou de la collection.

## 5. Récompenses de gameplay

Les événements constituent une source validée possible :

* de la ressource générale d’invocation ;
* de paquets de skins de carte obtenus gratuitement en jouant ;
* de créatures accordées directement lorsque cette exception est explicitement documentée ;
* de skins de carte accordés directement hors des séries distribuées par paquets ;
* d’autres récompenses de gameplay compatibles avec les systèmes existants.

Une créature accordée directement reste une nouvelle instance dans la forme de base de sa famille et ne devient pas une invocation.

Un skin accordé directement par un événement ne doit appartenir à aucune série distribuée par paquets. Sa méthode d’obtention doit être indiquée dans le système de collection.

Les quantités, conditions et fréquences de toutes ces récompenses restent à équilibrer.

## 6. Événements et progression durable

Une condition d’évolution ne doit jamais devenir définitivement impossible parce qu’un événement unique est terminé.

Lorsqu’un contexte saisonnier ou événementiel intervient dans une évolution, son occasion doit rester accessible ou revenir dans un délai raisonnable. Une instance ne doit jamais être condamnée à ne plus pouvoir progresser après une mise à jour.

Plus généralement, un événement peut accélérer, concentrer ou mettre en valeur une boucle existante sans rendre indispensable un contenu temporaire passé pour accéder durablement aux règles fondamentales du jeu.

## 7. Événements cosmétiques et offres temporaires

Une série de skins de carte et ses paquets peuvent être proposés temporairement à l’occasion d’un événement.

Pour une même série, les paquets gagnés en jouant et les paquets achetés utilisent :

* le même ensemble de skins ;
* les mêmes probabilités ;
* le même nombre de skins ;
* les mêmes règles de doublons ;
* les mêmes règles d’ouverture.

Les règles de disponibilité et de retour doivent être annoncées clairement. Une série temporaire doit normalement revenir selon une rotation annoncée ou être intégrée ultérieurement au catalogue permanent.

Un skin temporairement indisponible reste visible dans sa série avec son statut. Pour un skin Secret appartenant à un pool, seule son illustration ou son identité esthétique détaillée peut rester masquée : son existence et sa probabilité restent déclarées.

Les événements et offres doivent éviter les comptes à rebours artificiels, les rotations excessivement fréquentes, les informations ambiguës et les exclusivités non annoncées.

Certaines récompenses commémoratives ou événementielles peuvent exceptionnellement rester exclusives si cette exclusivité est annoncée dès le départ.

## 8. Saisons et canon narratif

Les saisons constituent avant tout une structure éditoriale et de contenu. Elles peuvent correspondre à des événements canoniques sans devoir être perçues comme des « saisons » par les habitants du multivers.

Les nouveaux mondes, régions et événements importants doivent recevoir une justification narrative explicite.

Une région événementielle peut rester dans le canon, devenir inaccessible, être transformée ou exceptionnellement disparaître lorsque le récit le justifie. Aucune règle universelle ne lui impose de disparaître à la fin de l’événement.

La relation exacte entre événements, saisons, régions et progression du mode Histoire reste à définir.

## 9. Production et cadence

La cadence des événements doit rester compatible avec :

* la roadmap ;
* le budget ;
* les capacités de l’équipe ;
* le temps de production des règles, récompenses, illustrations, UI, animations et VFX ;
* la maintenance des contenus permanents.

Aucune cadence fixe ne doit être annoncée avant cette évaluation.

La décision concernant d’éventuels passes ou abonnements est reportée jusqu’à la définition des saisons, des événements et des capacités réelles de production. Aucun passe ou abonnement ne fait partie du modèle initial.

## 10. Interface et transparence

Avant de participer, le joueur doit pouvoir connaître les informations nécessaires à l’activité : durée d’accès, objectifs, règles particulières, coûts éventuels et récompenses principales.

La collection doit indiquer la disponibilité actuelle et le mode général d’obtention des skins événementiels lorsque ces informations peuvent être communiquées.

Une offre cosmétique temporaire doit conserver les obligations de transparence du cadre de monétisation : prix réel, contenu possible, probabilités, doublons, durée et politique de retour.

La navigation, le calendrier, les notifications et la présentation détaillée restent à définir.

## 11. Dépendances

| Document | Responsabilité liée |
| --- | --- |
| [`09-GACHA.md`](./09-GACHA.md) | Invocations et acquisitions directes événementielles |
| [`10-PROGRESSION.md`](./10-PROGRESSION.md) | Progression et paramètres de récompense |
| [`11-COLLECTION.md`](./11-COLLECTION.md) | Disponibilité et skins obtenus hors paquets |
| [`12-MODES.md`](./12-MODES.md) | Contrat des activités et statut long terme |
| [`13-PVE.md`](./13-PVE.md) | Règles propres aux activités PvE utilisées par un événement |
| [`17-QUESTS.md`](./17-QUESTS.md) | Objectifs journaliers et éventuelles interactions futures |
| [`19-UI_FLOW.md`](./19-UI_FLOW.md) | Accès, information, résultat et calendrier |
| [`04-MONETIZATION.md`](../00-foundation/04-MONETIZATION.md) | Paquets, offres temporaires et protection des joueurs |
| [`01-LORE.md`](../02-world/01-LORE.md) | Canon des événements, saisons et régions |

## 12. Éléments à préciser ultérieurement

* La durée et la cadence des événements.
* Les quantités, taux, coûts et paliers de récompenses.
* Les calendriers de retour des séries cosmétiques.
* Les contenus, assets, textes et données propres à chaque événement.
* Les capacités de production nécessaires à une cadence soutenable.

## 13. Questions ouvertes

* Quels formats d’événements doivent être retenus en premier ?
* Quels événements sont récurrents, rotatifs, saisonniers ou uniques ?
* Quelle relation fonctionnelle doit exister entre événements et mode Histoire ?
* Des objectifs communautaires, coopératifs ou compétitifs doivent-ils exister dans certains événements ?
* Comment traiter les récompenses de gameplay devenues indisponibles après la fin d’un événement ?
* Une saison doit-elle structurer uniquement le calendrier éditorial ou également une progression propre ?
* Des ressources ou objets événementiels dédiés sont-ils nécessaires, et que deviennent-ils après l’événement ?
