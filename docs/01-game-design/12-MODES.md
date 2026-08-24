# Project Awakening — Modes de jeu

**Statut :** Draft de conception — à relire et valider

## 1. Rôle et périmètre du document

Ce document organise les modes de jeu actuellement confirmés ou envisagés et définit les contrats transversaux qu’un mode ou une activité doit respecter par défaut.

Il distingue le statut de périmètre d’un mode de ses règles détaillées. La présence d’un mode dans une liste de long terme ne valide ni son fonctionnement, ni son ordre de production, ni sa date de disponibilité.

Les règles internes des modes PvE, du PvP, des événements et des futurs systèmes de guilde appartiennent à leurs référentiels spécialisés. Le présent document définit leur cadre commun sans les redécrire individuellement.

## 2. Fonction des modes dans l’expérience

Un mode de jeu fournit un cadre d’activité dans lequel le joueur :

1. choisit un objectif ;
2. consulte les informations utiles ;
3. sélectionne une équipe préparée ;
4. combat ou accomplit l’activité ;
5. analyse le résultat ;
6. reçoit les récompenses prévues en cas de réussite ;
7. poursuit, retente ou retourne à la gestion.

Les modes doivent renforcer la progression, la personnalisation, la maîtrise des équipes et la découverte de nouveaux défis. Ils ne doivent pas réduire l’expérience à une simple comparaison de score de Puissance.

## 3. Statuts de périmètre

Les statuts utilisés sont :

* **inclus dans la vertical slice** ;
* **envisagé pour une première version jouable** ;
* **envisagé à long terme** ;
* **possibilité non validée**.

Ces statuts décrivent un périmètre fonctionnel, pas une roadmap.

| Mode ou contenu | Statut actuel |
| --- | --- |
| Début représentatif du mode Histoire | Inclus dans la vertical slice |
| Mode Histoire | Seul mode confirmé comme colonne vertébrale d’une première version jouable |
| Boss personnels | Envisagé à long terme |
| Boss de serveur | Envisagé à long terme |
| Tour infinie | Envisagé à long terme |
| PvP | Envisagé à long terme |
| Événements temporaires | Envisagé à long terme |
| Guildes | Envisagé à long terme |
| Contenus saisonniers | Envisagé à long terme |

Tout autre mode ou variante reste une possibilité non validée jusqu’à une décision explicite.

## 4. Contrat commun des équipes

Une équipe peut réunir jusqu’à six créatures. Une équipe complète en comporte six.

Deux instances d’une même famille peuvent cohabiter uniquement lorsque leurs chemins d’évolution ont réellement divergé. Une instance située sur le tronc commun reste incompatible avec toute autre instance de sa famille dans la même équipe.

Cette règle est globale pour tous les modes.

Un mode peut ajouter une restriction de composition uniquement si elle est explicitement définie. Les rôles suggérés et profils offensifs ne constituent pas des restrictions par défaut.

Le joueur doit pouvoir sélectionner rapidement une équipe enregistrée avant une activité et modifier sa composition lorsque le mode l’autorise.

## 5. Contrat commun du combat

Les modes utilisant le moteur de combat héritent des règles du [référentiel Combat](./02-COMBAT.md), notamment :

* une simulation mathématique en temps continu ;
* un résultat reproductible à partir des mêmes conditions initiales et de la même seed RNG ;
* des équipes présentes simultanément dans une formation de trois lignes ;
* des Basic Attacks et Active automatiques ;
* un contrôle global Auto ou Manuel pour les Ultimate ;
* un timeout standard de 120 secondes de simulation ;
* une représentation visuelle indépendante de la simulation ;
* les vitesses de visualisation ×1, ×2 et ×4 sans effet sur les calculs, le résultat ou les récompenses.

Un mode à objectif peut définir sa propre condition de victoire, de défaite ou de score. Il peut utiliser une durée différente uniquement si cette exception est explicitement documentée.

Sans exception de mode, le timeout départage un combat standard selon :

1. le nombre de créatures vivantes ;
2. le ratio global de PV restants parmi les survivants ;
3. en cas d’égalité parfaite, la victoire de l’équipe attaquante.

## 6. Informations avant une activité

Pour un contenu ordinaire, le joueur doit connaître suffisamment d’informations pour sélectionner une équipe pertinente, notamment :

* les éléments des adversaires qui en possèdent ;
* les principales menaces ;
* les Effets de combat importants ;
* les conditions particulières ;
* les récompenses principales ;
* les restrictions éventuelles ;
* le coût d’entrée lorsqu’il existe.

Un boss ou défi peut conserver une mécanique secrète. Le jeu doit alors signaler qu’une mécanique inconnue est présente. La première défaite ne doit pas devenir une étape systématiquement obligatoire pour comprendre un niveau.

## 7. Énergie des modes individuels

Les modes joués individuellement utilisent par défaut la réserve générale d’énergie définie dans [`10-PROGRESSION.md`](./10-PROGRESSION.md).

Cette règle s’applique notamment au mode Histoire, aux modes PvE individuels, au farming, aux défis individuels et au PvP. Le joueur choisit librement les activités dans lesquelles il investit sa réserve et peut consacrer toute l’énergie disponible à un même mode.

Un mode individuel ne crée pas automatiquement une énergie distincte, un ticket, une clé ou une autre ressource d’entrée parallèle. Il peut déroger à la réserve commune uniquement lorsqu’une exception est explicitement justifiée et documentée dans son propre référentiel.

Certains événements, contenus de guilde, activités communautaires ou systèmes saisonniers pourront définir une régulation particulière lors de leur cadrage. L’existence de cette possibilité ne valide encore aucune exception concrète.

## 8. Résultats et récompenses

Dans le fonctionnement standard, une victoire :

* accorde l’XP prévue aux créatures participantes ;
* accorde de l’XP au compte ;
* remet les récompenses annoncées ;
* distingue les récompenses de première réussite et de répétition lorsque nécessaire ;
* applique les déblocages liés à un jalon ;
* permet de poursuivre ou de retourner à la gestion.

Une défaite standard n’accorde aucune XP aux créatures ou au compte, aucune récompense principale et aucune progression de niveau. Elle ne retire aucune progression déjà acquise et ne provoque aucune pénalité durable.

Un mode fondé sur un score, un objectif partiel ou une participation doit définir explicitement ses propres règles de résultat et de récompense.

Après un combat, un résumé statistique simple des deux équipes doit être accessible. Il reste agrégé par créature plutôt que par Skill et aide le joueur à adapter sa préparation.

## 9. Articulation avec les référentiels spécialisés

Les règles propres à chaque domaine sont réparties ainsi :

* [`13-PVE.md`](./13-PVE.md) rassemble le mode Histoire et les autres directions PvE ne disposant pas de leur propre référentiel ;
* [`14-PVP.md`](./14-PVP.md) porte les contraintes et décisions propres au PvP ;
* le futur `15-GUILDS.md` portera les fonctions de guilde lorsqu’un cadrage suffisant permettra sa création ;
* [`16-EVENTS.md`](./16-EVENTS.md) porte la structure des événements et contenus saisonniers, qu’ils contiennent du PvE, du PvP, du communautaire ou une autre activité ;
* [`17-QUESTS.md`](./17-QUESTS.md) porte les objectifs journaliers ;
* le futur `18-ACHIEVEMENTS.md` portera les hauts faits lorsqu’un cadrage suffisant permettra sa création ;
* [`19-UI_FLOW.md`](./19-UI_FLOW.md) traduit les besoins fonctionnels des modes dans les parcours et écrans.

Un référentiel spécialisé hérite des contrats du présent document. Il décrit uniquement ses règles propres et les exceptions explicitement justifiées.

## 10. Dépendances

| Document | Responsabilité liée |
| --- | --- |
| [`01-GAME_DESIGN_DOCUMENT.md`](./01-GAME_DESIGN_DOCUMENT.md) | Boucles globales et statuts de périmètre |
| [`02-COMBAT.md`](./02-COMBAT.md) | Contrat du moteur et exceptions de mode |
| [`10-PROGRESSION.md`](./10-PROGRESSION.md) | XP, compte, énergie et résultats |
| [`13-PVE.md`](./13-PVE.md) | Modes PvE et règles propres au mode Histoire |
| [`14-PVP.md`](./14-PVP.md) | Contraintes et décisions propres au PvP |
| [`16-EVENTS.md`](./16-EVENTS.md) | Contenus temporaires et saisonniers |
| [`17-QUESTS.md`](./17-QUESTS.md) | Objectifs journaliers liés aux fonctionnalités débloquées |
| [`19-UI_FLOW.md`](./19-UI_FLOW.md) | Sélection, préparation, combat et résultats |

## 11. Éléments à préciser ultérieurement

* Les récompenses, coûts d’entrée et paramètres numériques de chaque activité.
* Les exceptions locales à la réserve générale d’énergie qui seront justifiées par le design d’un mode particulier.
