# Project Awakening — Saisons

**Statut :** Draft de conception — à relire et valider

## 1. Rôle et périmètre du document

Ce document constitue la base du système transversal des Saisons de Project Awakening.

Les Saisons sont envisagées comme une structure importante après le lancement. Elles peuvent donner une trame périodique commune à plusieurs systèmes, modes, objectifs et contenus sans devenir elles-mêmes un mode de jeu.

Leur fonctionnement détaillé n’est pas encore cadré. Le présent draft rassemble uniquement les décisions déjà validées, définit les frontières documentaires et conserve explicitement les éléments restant à préciser.

## 2. Fonction transversale

Une Saison peut notamment :

* donner un thème général à une période du jeu ;
* renouveler des compétitions saisonnières ;
* influencer le PvP ;
* influencer des modes PvE compétitifs ;
* influencer de futures activités compétitives de guilde ;
* proposer des objectifs saisonniers individuels ;
* proposer de futurs objectifs saisonniers de guilde ;
* proposer de futurs Hauts Faits saisonniers ;
* être associée à certains contenus, équipements, sets, objets, skins ou autres récompenses ;
* porter éventuellement une dimension narrative ou visuelle commune.

Cette liste décrit des possibilités transversales validées. Elle n’impose pas que chaque Saison utilise tous ces domaines et ne définit encore aucune mécanique, récompense, source d’obtention ou règle de progression précise.

## 3. Progression durable et progression saisonnière

Une nouvelle Saison ne remet jamais à zéro la progression durable générale du joueur.

Cette protection concerne notamment la progression permanente du compte, des créatures et de la collection. Une Saison ne retire pas les niveaux, l’XP, les points de caractéristiques, les évolutions, les étoiles, les équipements, les objets, les créatures ou les éléments de collection durablement acquis selon leurs règles normales.

Une nouvelle Saison peut en revanche réinitialiser une progression, un classement, un score ou un compteur explicitement défini comme saisonnier par son référentiel propriétaire.

Les réinitialisations déjà validées restent locales aux modes concernés :

* la Tour infinie peut réinitialiser sa progression active et son classement selon [`13-PVE.md`](./13-PVE.md) ;
* le PvP conserve son MMR mais réinitialise sa cote saisonnière selon [`14-PVP.md`](./14-PVP.md).

Ces exemples n’établissent aucune règle universelle de reset pour les futurs systèmes saisonniers.

## 4. Relation avec les modes spécialisés

Une Saison peut coordonner une période, un thème ou plusieurs cycles saisonniers, mais elle ne récupère pas les règles internes des modes qu’elle influence.

Les responsabilités restent réparties ainsi :

* le fonctionnement saisonnier de la Tour infinie reste dans [`13-PVE.md`](./13-PVE.md) ;
* le fonctionnement des saisons compétitives du PvP reste dans [`14-PVP.md`](./14-PVP.md) ;
* les futures règles saisonnières de guilde resteront dans le futur `15-GUILDS.md` ;
* les futurs Hauts Faits saisonniers resteront dans le futur `19-ACHIEVEMENTS.md`.

Le présent document devra définir uniquement les règles réellement transversales lorsque celles-ci seront cadrées.

## 5. Objectifs, contenus et récompenses associés

Une Saison peut servir de cadre à des objectifs individuels, à de futurs objectifs de guilde ou à de futurs Hauts Faits. Leur structure, leurs conditions, leur progression et leurs récompenses ne sont pas encore définies.

Une association saisonnière avec un équipement, un set, un objet, un skin, un contenu ou une récompense ne modifie pas automatiquement :

* sa nature permanente ou temporaire ;
* sa source d’obtention ;
* ses règles fonctionnelles ;
* sa disponibilité après la Saison ;
* son appartenance aux systèmes de progression ou de collection.

Ces propriétés doivent rester définies par les référentiels spécialisés concernés et par le contenu concret.

## 6. Dimension thématique, visuelle et narrative

Une Saison peut porter un thème visuel, éditorial ou narratif commun à plusieurs systèmes. Cette possibilité reste facultative et ne valide encore aucun thème, calendrier ou format narratif.

Une Saison peut correspondre à des événements canoniques sans devoir être perçue comme une « saison » par les habitants de l’univers. Toute affirmation narrative concrète reste soumise au [référentiel Lore](../02-world/01-LORE.md).

## 7. Distinction entre Saison et Event

Une **Saison** constitue une grande trame périodique transversale susceptible de coordonner plusieurs systèmes et progressions explicitement saisonnières.

Un **Event** constitue une animation temporaire plus légère, généralement thématique, utilisant principalement les systèmes et modes existants selon [`17-EVENTS.md`](./17-EVENTS.md).

Un Event peut se dérouler pendant une Saison sans devenir la Saison elle-même. Réciproquement, une Saison n’a pas besoin de reposer sur une succession d’Events.

La temporalité commune ne fusionne donc pas ces deux concepts.

## 8. Contraintes de production

Le système de Saisons devra rester compatible avec le budget limité et l’équipe humaine de deux personnes.

La présence d’une trame saisonnière ne valide aucune cadence de production, aucun volume de contenu, aucune infrastructure supplémentaire, aucun passe et aucun abonnement.

## 9. Dépendances documentaires

| Document | Responsabilité liée |
| --- | --- |
| [`01-GAME_DESIGN_DOCUMENT.md`](./01-GAME_DESIGN_DOCUMENT.md) | Place des Saisons dans l’expérience de long terme |
| [`07-EVOLUTIONS.md`](./07-EVOLUTIONS.md) | Conditions saisonnières éventuelles et protection contre les blocages définitifs |
| [`08-ITEMS.md`](./08-ITEMS.md) | Équipements, sets et objets éventuellement associés à une Saison |
| [`10-PROGRESSION.md`](./10-PROGRESSION.md) | Progression durable du compte et des créatures |
| [`12-MODES.md`](./12-MODES.md) | Frontière entre cadre transversal et règles des modes |
| [`13-PVE.md`](./13-PVE.md) | Saisons et progression propres à la Tour infinie |
| [`14-PVP.md`](./14-PVP.md) | Saisons compétitives, cote et classement du PvP |
| [`17-EVENTS.md`](./17-EVENTS.md) | Animations temporaires légères distinctes des Saisons |
| [`18-QUESTS.md`](./18-QUESTS.md) | Quêtes journalières distinctes des futurs objectifs saisonniers |
| [`20-UI_FLOW.md`](./20-UI_FLOW.md) | Besoins fonctionnels de présentation et de navigation |
| [`04-MONETIZATION.md`](../00-foundation/04-MONETIZATION.md) | Garde-fous économiques et futurs passes ou abonnements non validés |
| [`01-LORE.md`](../02-world/01-LORE.md) | Canon et éventuelle dimension narrative des Saisons |

## 10. Éléments à préciser ultérieurement

* La durée, la cadence et le calendrier des Saisons.
* Leur structure exacte et leurs règles de transition.
* Les systèmes de progression saisonnière transversaux éventuels.
* La structure des objectifs saisonniers individuels ou de guilde.
* Les interactions entre les cycles saisonniers des différents modes.
* Les contenus, équipements, sets, objets, skins et récompenses associés à une Saison.
* Les règles de disponibilité ou de conservation de ces contenus après une Saison.
* La conservation des historiques, résultats et distinctions saisonniers.
* La portée des thèmes visuels, éditoriaux ou narratifs.
* Les besoins précis d’interface, de calendrier et de notification.

## 11. Questions ouvertes

* Une Saison possède-t-elle une progression transversale propre ou coordonne-t-elle uniquement les progressions de ses systèmes spécialisés ?
* Quels systèmes doivent obligatoirement partager le même calendrier saisonnier, s’il en existe ?
* Comment les objectifs saisonniers individuels, de guilde et les Hauts Faits doivent-ils rester distincts ?
* Quelles informations et distinctions saisonnières doivent rester visibles durablement sur le compte ?
