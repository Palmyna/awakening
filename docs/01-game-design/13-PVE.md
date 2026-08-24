# Project Awakening — Modes PvE

**Statut :** Draft de conception — à relire et valider

## 1. Rôle et périmètre du document

Ce document constitue le référentiel spécialisé des modes et activités PvE de Project Awakening.

Il recense les modes PvE confirmés ou envisagés, rassemble leurs décisions propres et documente leurs éventuelles exceptions au cadre transversal défini dans [`12-MODES.md`](./12-MODES.md).

Il ne redéfinit pas les règles communes des équipes, du combat, des résultats ou de la progression. Il ne valide pas non plus le fonctionnement détaillé d’un mode dont l’identité reste à cadrer.

Un mode PvE mineur peut être documenté ici. Un mode suffisamment complexe pourra recevoir ultérieurement son propre référentiel si cette séparation devient justifiée.

## 2. Statut des modes PvE

| Mode ou contenu | Statut actuel |
| --- | --- |
| Début représentatif du mode Histoire | Inclus dans la vertical slice |
| Mode Histoire | Colonne vertébrale PvE d’une première version jouable |
| Boss personnels | Direction PvE de long terme |
| Boss de serveur | Direction PvE de long terme |
| Tour infinie | Direction PvE de long terme |

La présence d’un mode dans ce tableau ne valide ni son fonctionnement détaillé, ni son ordre de production, ni sa date de disponibilité.

## 3. Application du cadre commun

Tout mode PvE applique par défaut le contrat transversal de [`12-MODES.md`](./12-MODES.md) et, lorsqu’il utilise le moteur de combat, les règles de [`02-COMBAT.md`](./02-COMBAT.md).

Une activité PvE individuelle utilise par défaut la réserve générale d’énergie définie dans [`10-PROGRESSION.md`](./10-PROGRESSION.md). Elle n’introduit une autre ressource d’entrée que si une exception est explicitement décidée et documentée pour ce mode.

Les coûts numériques, gains d’XP et quantités de récompenses relèvent du balancing et des données de contenu.

## 4. Mode Histoire

### 4.1. Place et structure

Le mode Histoire constitue la principale chaîne de progression PvE et la colonne vertébrale initiale du jeu.

Il est organisé en :

* mondes ;
* niveaux ;
* combats ;
* boss ou jalons réguliers.

Un niveau ordinaire correspond généralement à un combat court. Les séries de combats successifs peuvent être réservées aux boss, défis spéciaux, activités avancées ou modes dont l’identité le nécessite.

### 4.2. Progression et rejouabilité

Le mode Histoire doit :

* augmenter progressivement sa difficulté ;
* rester rejouable ;
* permettre de répéter certains niveaux pour leurs récompenses ;
* soutenir le farming de Sources d’énergie, de composants et d’autres récompenses pertinentes ;
* servir de principale source de déblocage des fonctionnalités ;
* accueillir de nouveaux mondes et niveaux au fil du développement ;
* soutenir une progression longue sans exiger une narration détaillée pour chaque niveau.

La puissance d’équipe peut servir d’indication de difficulté, mais ne constitue pas un verrou systématique.

### 4.3. Énergie et résultat

Le mode Histoire utilise la réserve générale d’énergie, consommée à l’entrée d’un niveau.

Lors d’une défaite standard, l’énergie utilisée reste normalement consommée. Une activité particulière ou une étape d’onboarding peut définir une exception explicite.

Les règles communes de victoire, défaite, XP, récompenses et résumé post-combat proviennent de [`12-MODES.md`](./12-MODES.md) et de [`10-PROGRESSION.md`](./10-PROGRESSION.md).

### 4.4. Onboarding et vertical slice

Le mode Histoire porte les principales étapes d’onboarding et les déblocages fonctionnels importants.

La vertical slice comprend uniquement un début représentatif du mode Histoire : plusieurs niveaux courts et un boss ou défi final.

Elle doit permettre de tester la boucle suivante :

> sélectionner une équipe → combattre → recevoir expérience et récompenses → développer les créatures → améliorer la composition → franchir un nouveau défi.

Les autres modes spécialisés, les événements, les guildes, les saisons et les systèmes sociaux sont exclus de cette vertical slice.

## 5. Boss personnels

Les boss personnels constituent une direction PvE de long terme.

Aucun fonctionnement interne supplémentaire n’est actuellement validé. Leur appellation ne détermine pas leur structure de combat, leur progression, leur répétition, leur fréquence, leurs récompenses ou une éventuelle logique de score.

S’ils sont joués individuellement, ils utilisent par défaut la réserve générale d’énergie. Toute autre régulation devra être explicitement décidée.

## 6. Boss de serveur

Les boss de serveur constituent une direction de long terme.

Cette appellation ne valide pas automatiquement une barre de PV globale, des contributions individuelles, un classement, des récompenses communautaires ou une durée limitée.

Leur structure de participation, leur dimension individuelle ou communautaire, la résolution de leur résultat et leur relation avec l’énergie restent à cadrer.

## 7. Tour infinie

La tour infinie constitue une direction PvE de long terme.

Son nom ne valide pas automatiquement un fonctionnement par étages, un reset quotidien, hebdomadaire ou saisonnier, un classement, des checkpoints ou des récompenses cumulatives.

Sa structure de progression, sa continuité, ses règles de répétition, ses récompenses et sa relation avec l’énergie restent à cadrer.

## 8. Futurs modes PvE

Les futurs modes ou activités PvE peuvent être ajoutés au présent document lorsqu’ils appliquent principalement le cadre commun et ne nécessitent qu’un nombre limité de règles propres.

Chaque ajout doit indiquer son statut de périmètre, ses objectifs, ses règles spécifiques et ses éventuelles exceptions aux contrats transversaux sans recopier intégralement ces derniers.

## 9. Dépendances

| Document | Responsabilité liée |
| --- | --- |
| [`01-GAME_DESIGN_DOCUMENT.md`](./01-GAME_DESIGN_DOCUMENT.md) | Boucles globales, mode Histoire, onboarding et vertical slice |
| [`02-COMBAT.md`](./02-COMBAT.md) | Moteur de combat et règles standards |
| [`10-PROGRESSION.md`](./10-PROGRESSION.md) | XP, déblocages et réserve générale d’énergie |
| [`12-MODES.md`](./12-MODES.md) | Contrats transversaux et statuts de périmètre |
| [`16-EVENTS.md`](./16-EVENTS.md) | Structure événementielle pouvant accueillir des activités PvE |
| [`17-QUESTS.md`](./17-QUESTS.md) | Objectifs pouvant utiliser les activités débloquées |
| [`19-UI_FLOW.md`](./19-UI_FLOW.md) | Sélection, préparation, parcours Histoire et résultats |

## 10. Éléments à préciser ultérieurement

* Les mondes, niveaux, boss, jalons et tables de loot concrets du mode Histoire.
* Les jalons exacts de l’onboarding et des déblocages.
* Les coûts en énergie, valeurs d’XP et quantités de récompenses de chaque activité.
* Les paramètres numériques de difficulté, répétition et progression.
* Les nombres précis d’étapes, de combats ou d’autres unités propres aux futurs modes.
* Les données exactes de la vertical slice.

## 11. Questions ouvertes

### 11.1. Mode Histoire

* Quelles règles structurelles distinguent les niveaux ordinaires, les boss, les défis spéciaux et les éventuelles séries de combats ?
* Comment les récompenses et la répétition distinguent-elles une première réussite du farming d’un niveau déjà terminé ?

### 11.2. Boss personnels

* Quelle identité de combat ou d’objectif distingue un boss personnel des niveaux et boss du mode Histoire ?
* Quelle structure d’accès, de progression, de répétition et de disponibilité doit être retenue ?
* Quelles règles de résultat et de récompense soutiennent ce mode sans le rendre obligatoire pour toute progression ?

### 11.3. Boss de serveur

* Quelle forme de participation et quelle dimension réellement partagée définissent un boss de serveur ?
* Comment son état, son résultat et les éventuelles contributions sont-ils résolus ?
* Quelle structure d’accès, de disponibilité et de récompense doit être retenue ?
* Quelle relation entretient-il avec la réserve générale d’énergie ou une éventuelle exception explicitement justifiée ?

### 11.4. Tour infinie

* Quelle structure de progression définit l’identité de la tour infinie ?
* Quelle continuité existe entre deux participations et quelles règles de reprise ou de réinitialisation sont nécessaires ?
* Quelles conditions de résultat, de répétition et de récompense doivent être retenues ?
* Quelle relation entretient-elle avec la réserve générale d’énergie ou une éventuelle exception explicitement justifiée ?
