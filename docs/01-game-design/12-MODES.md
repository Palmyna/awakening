# Project Awakening — Modes de jeu

**Statut :** Draft de conception — à relire et valider

## 1. Rôle et périmètre du document

Ce document organise les modes de jeu actuellement confirmés ou envisagés et définit les contrats communs qu’un futur mode doit respecter.

Il distingue le statut de périmètre d’un mode de ses règles détaillées. La présence d’un mode dans une liste de long terme ne valide ni son fonctionnement, ni son ordre de production, ni sa date de disponibilité.

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

## 7. Résultats et récompenses

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

## 8. Mode Histoire

Le mode Histoire constitue la principale chaîne de progression PvE et la colonne vertébrale initiale du jeu.

Il est organisé en :

* mondes ;
* niveaux ;
* combats ;
* boss ou jalons réguliers.

Un niveau ordinaire correspond généralement à un combat court. Les séries de combats successifs peuvent être réservées aux boss, défis spéciaux, activités avancées ou modes dont l’identité le nécessite.

Le mode Histoire doit :

* augmenter progressivement sa difficulté ;
* rester rejouable ;
* permettre de répéter certains niveaux pour leurs récompenses ;
* soutenir le farming de Sources d’énergie, de composants et d’autres récompenses pertinentes ;
* servir de principale source de déblocage des fonctionnalités ;
* accueillir de nouveaux mondes et niveaux au fil du développement ;
* soutenir une progression longue sans exiger une narration détaillée pour chaque niveau.

La puissance d’équipe peut servir d’indication de difficulté, mais ne constitue pas un verrou systématique.

Le mode Histoire utilise une énergie consommée à l’entrée du niveau. Lors d’une défaite, cette énergie reste normalement consommée, sauf exception explicite propre à une activité ou à l’onboarding.

## 9. Onboarding et vertical slice

La vertical slice comprend uniquement un début représentatif du mode Histoire : plusieurs niveaux courts et un boss ou défi final.

Elle doit permettre de tester la boucle suivante :

> sélectionner une équipe → combattre → recevoir expérience et récompenses → développer les créatures → améliorer la composition → franchir un nouveau défi.

Le PvP, les guildes, les boss de serveur, les événements temporaires, les saisons et les systèmes sociaux sont exclus de cette vertical slice.

## 10. Modes et contenus de long terme

Les boss personnels, boss de serveur, tour infinie, PvP, événements temporaires, guildes et contenus saisonniers constituent des directions de long terme.

Les documents existants ne permettent pas encore de déduire :

* leur structure d’accès ;
* leur format de combat ;
* leurs conditions de victoire ou de score ;
* leurs règles de répétition ;
* leurs coûts d’entrée ;
* leurs récompenses ;
* leur calendrier ;
* leur dimension individuelle, compétitive ou coopérative détaillée.

Ces choix doivent rester locaux aux documents spécialisés correspondants.

## 11. Dépendances

| Document | Responsabilité liée |
| --- | --- |
| [`01-GAME_DESIGN_DOCUMENT.md`](./01-GAME_DESIGN_DOCUMENT.md) | Boucles globales et statuts de périmètre |
| [`02-COMBAT.md`](./02-COMBAT.md) | Contrat du moteur et exceptions de mode |
| [`10-PROGRESSION.md`](./10-PROGRESSION.md) | XP, compte, énergie et résultats |
| [`13-PVP.md`](./13-PVP.md) | Contraintes et décisions propres au PvP |
| [`15-EVENTS.md`](./15-EVENTS.md) | Contenus temporaires et saisonniers |
| [`16-QUESTS.md`](./16-QUESTS.md) | Objectifs journaliers liés aux fonctionnalités débloquées |
| [`18-UI_FLOW.md`](./18-UI_FLOW.md) | Sélection, préparation, combat et résultats |

## 12. Éléments à préciser ultérieurement

* Les récompenses, coûts d’entrée et paramètres numériques de chaque activité.
* Les niveaux, mondes, tables de loot et jalons concrets du mode Histoire.
* Les quantités et données exactes de la vertical slice.

## 13. Questions ouvertes

* Quel ordre de conception et de production doit être retenu pour les modes de long terme ?
* Quels modes utilisent le combat standard, un objectif de score, plusieurs combats successifs ou une autre structure ?
* Quelles activités utilisent l’énergie du mode Histoire, une autre régulation ou aucun coût d’entrée ?
* Quelles récompenses et règles de répétition distinguent chaque mode sans rendre un contenu unique obligatoire pour toute progression ?
* Quels modes doivent être permanents, rotatifs, temporaires ou saisonniers ?
