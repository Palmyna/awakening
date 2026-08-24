# Project Awakening — Progression

**Statut :** Rédigé — référence actuelle, à maintenir à jour

## 1. Rôle et périmètre du document

Ce document définit les systèmes validés qui transforment les activités accomplies en développement durable du compte et des créatures.

Il rassemble :

* l’expérience et les niveaux des instances ;
* l’attribution des points de caractéristiques ;
* l’interaction entre XP et évolutions ;
* les quinze montées du niveau d’étoiles ;
* les réinitialisations ;
* le score de Puissance ;
* la progression du compte et son influence sur les équipements ;
* les déblocages principalement portés par le mode Histoire ;
* la réserve générale d’énergie des activités individuelles ;
* les garde-fous empêchant une progression passive ou payante de puissance.

Il ne fixe pas les courbes, coûts, multiplicateurs, quantités de récompenses ou autres valeurs réservées au balancing.

## 2. Couches de progression

La progression repose sur plusieurs couches complémentaires :

* la progression en niveaux de chaque instance ;
* la répartition de ses points de caractéristiques ;
* son évolution entre exactement trois stades ;
* son niveau d’étoiles ;
* son équipement ;
* le niveau du compte ;
* les déblocages principalement portés par le mode Histoire.

Ces couches ne sont pas interchangeables. Le niveau ne remplace pas les étoiles, les étoiles ne remplacent pas l’évolution et le niveau du compte ne remplace pas le développement individuel des créatures.

La progression doit valoriser le temps investi dans les instances déjà possédées et préserver la diversité des builds plutôt que produire une montée linéaire identique pour tous.

## 3. Niveau et points de caractéristiques

Le niveau d’une instance ne possède pas de maximum. Il reste affiché directement et aucun système de prestige ne le remplace ou ne le réinitialise automatiquement.

La quantité d’XP nécessaire augmente fortement avec les niveaux afin que chaque nouvelle montée devienne progressivement plus difficile. La courbe exacte reste à définir.

Une montée de niveau :

* n’augmente aucune caractéristique automatiquement ;
* accorde actuellement cinq points de caractéristiques ;
* permet de répartir ces points uniquement entre les six caractéristiques principales de l’instance.

La valeur de cinq points constitue la référence actuelle mais reste ajustable pendant le balancing.

Dépenser un point augmente toujours de `+1` la caractéristique principale choisie. Les six caractéristiques utilisent la même unité de budget et aucun coût différent n’est appliqué selon la caractéristique. Leur formule ou leur courbe doit être recalibrée si leur valeur relative devient déséquilibrée.

Les points non attribués peuvent être conservés indéfiniment. Ils ne produisent aucun effet et n’augmentent pas le score de Puissance tant qu’ils ne sont pas attribués.

## 4. Attribution de l’XP d’une activité

Par défaut, l’XP des créatures est attribuée après un combat remporté et une défaite standard n’accorde aucune XP aux créatures ou au compte.

Un mode peut définir explicitement une exception locale. Le mode Histoire accorde une petite quantité d’XP aux créatures participantes après une défaite, tandis que la Tour infinie peut en accorder une. Ces exceptions, définies dans [`13-PVE.md`](./13-PVE.md), n’accordent aucune XP au compte et ne modifient pas la règle des autres modes.

Un combat PvP initié par le joueur peut accorder de l’XP au compte selon les règles de [`14-PVP.md`](./14-PVP.md), mais n’accorde jamais d’XP aux créatures. Une défense PvP résolue hors ligne n’accorde aucune XP au compte ou aux créatures.

Chaque créature participante reçoit son propre gain ; l’XP n’est jamais divisée entre les membres de l’équipe.

Toutes les participantes reçoivent leur gain, y compris si elles sont mortes, contrôlées ou temporairement exclues à la fin du combat. Utiliser une équipe réduite n’augmente jamais le gain individuel d’une participante.

La ou les créatures du niveau le plus élevé parmi les participantes reçoivent 100 % de `XPActivité`.

Pour les autres :

> **RatioXP = RatioMinimum + (1 − RatioMinimum) × ((NiveauCréature − 1) / (NiveauMaxÉquipe − 1))**

Puis :

> **XPGagnée = XPActivité × RatioXP**

Avec :

* `RatioMinimum` : part minimale, actuellement fixée à 10 % mais ajustable pendant le balancing ;
* `NiveauCréature` : niveau de la participante avant la récompense ;
* `NiveauMaxÉquipe` : niveau le plus élevé parmi les participantes avant la récompense ;
* `XPActivité` : valeur d’XP de l’activité ;
* `XPGagnée` : gain individuel calculé.

Lorsque toutes les participantes sont niveau 1, elles reçoivent 100 % de l’XP.

Les niveaux et ratios sont calculés avant l’attribution et restent fixes pour toute la récompense. Une récompense peut accorder plusieurs niveaux. Tous les niveaux obtenus sont appliqués et accordent chacun les points correspondants ; aucune limite artificielle d’un niveau gagné par combat n’existe.

Ce ratio doit faciliter la remontée d’une créature récemment réinitialisée et permettre un power-leveling contrôlé, sans accorder immédiatement toute l’XP d’une activité avancée à une créature très peu développée.

## 5. Interaction avec les évolutions

Après l’attribution de l’XP, chaque montée de niveau pertinente peut déclencher une évolution standard.

* Si exactement une évolution est valide, elle est automatique.
* Si plusieurs évolutions concurrentes sont valides, aucune ne se produit.
* Une même récompense peut provoquer plusieurs évolutions successives.
* L’utilisation volontaire d’un objet consommable d’évolution constitue le seul déclenchement prévu hors montée de niveau.

Une évolution conserve le niveau, l’XP, les points, les étoiles, l’équipement et les autres propriétés persistantes de l’instance. Les règles de conditions, de branches et de résolution appartiennent au [référentiel Évolutions](./07-EVOLUTIONS.md).

## 6. Niveau d’étoiles

Une nouvelle instance commence à 0 étoile et peut obtenir quinze montées :

* Bronze ★1 à ★5 : étoiles globales 1 à 5 ;
* Argent ★1 à ★5 : étoiles globales 6 à 10 ;
* Or ★1 à ★5 : étoiles globales 11 à 15.

Les étoiles augmentent uniquement les six caractéristiques principales de base de la forme et du stade actuels.

Elles ne multiplient pas :

* les trois caractéristiques secondaires ;
* les points distribués ;
* l’équipement ;
* les buffs ;
* les autres bonus externes.

Les multiplicateurs totaux doivent progresser de manière non linéaire. Les étoiles avancées peuvent produire un gain marginal supérieur, sans multiplication successive incontrôlée des paliers précédents.

Le niveau d’étoiles est permanent. Il ne diminue pas volontairement et n’est pas perdu lors d’une évolution ou d’une réinitialisation en niveaux.

## 7. Matériaux d’étoiles

Une montée d’étoile consomme une ou plusieurs instances de la même famille que l’instance cible, quelle que soit leur forme ou leur branche.

Certains paliers peuvent exiger que les instances utilisées comme matériaux possèdent elles-mêmes un niveau d’étoiles minimum. Les seules conditions d’une montée d’étoile portent sur les étoiles de ces instances.

Une montée d’étoile ne demande pas de niveau, de forme, de branche, d’équipement ou d’autre condition de progression à l’instance cible.

L’opération est irréversible. Une instance consommée disparaît définitivement et sa progression individuelle est perdue. Tous ses équipements sont automatiquement replacés dans l’inventaire avant sa disparition.

Une instance verrouillée ne peut pas être utilisée comme matériau. Les instances consommées ne peuvent pas être récupérées.

## 8. Réinitialisations

### 8.1. Réinitialisation complète gratuite

La réinitialisation complète gratuite :

* remet l’instance au niveau 1 et à l’XP correspondante ;
* retire les points gagnés grâce aux niveaux ;
* impose de regagner ces points en jouant.

Elle conserve :

* la forme actuelle et la branche ;
* le niveau d’étoiles ;
* l’équipement ;
* le surnom et les tags ;
* les apparences déjà débloquées.

L’instance niveau 1 utilise donc les caractéristiques de base de sa forme évoluée actuelle. Une évolution déjà obtenue n’est jamais perdue. Une évolution non encore obtenue devra toujours satisfaire ses conditions après la réinitialisation.

### 8.2. Redistribution sans retour au niveau 1

Un objet rare obtenu en jouant et un service payant strictement limité fournissent le même résultat fonctionnel :

* le niveau et l’XP ne changent pas ;
* les points déjà gagnés redeviennent disponibles ;
* aucun point supplémentaire, aucune expérience et aucun potentiel supplémentaire ne sont accordés.

Le service payant reste distinct de la boutique cosmétique. Il ne doit jamais devenir nécessaire pour corriger un build ou rester compétitif, et une méthode gratuite permet d’atteindre le même résultat.

### 8.3. Protection par verrouillage

Une instance verrouillée ne peut subir ni réinitialisation complète ni redistribution de caractéristiques. Le joueur doit la déverrouiller volontairement avant l’une de ces actions.

## 9. Score de Puissance

Chaque instance possède un score de Puissance recalculé en temps réel lorsque sa puissance permanente active change.

Il reflète notamment :

* sa forme et son stade ;
* ses étoiles ;
* ses points attribués ;
* son équipement ;
* les autres sources permanentes actives.

Les points non attribués ne l’augmentent pas.

Le score facilite le tri, la comparaison générale et l’indication de difficulté. Il ne mesure pas absolument l’efficacité stratégique d’une créature ou d’une composition dans toutes les situations et ne doit pas devenir un verrou systématique d’accès aux contenus.

## 10. Progression du compte

Le compte possède un niveau numérique et gagne de l’expérience lorsqu’une activité est accomplie.

Cette progression :

* est beaucoup plus lente que celle des créatures ;
* représente l’avancement général et l’ancienneté du joueur ;
* accorde une récompense à chaque niveau ;
* détermine le niveau d’objet des équipements nouvellement générés ou fabriqués ;
* peut débloquer progressivement des couches de potentiel et de complexité des équipements selon les règles du référentiel correspondant.

Les fonctionnalités, systèmes, modes, activités et principales étapes d’onboarding sont débloqués principalement par les jalons du mode Histoire. Le niveau de compte ne constitue pas par défaut un second système parallèle imposant des seuils artificiels pour ces déblocages.

Des usages secondaires du niveau de compte pourront être ajoutés ultérieurement s’ils sont explicitement justifiés et ne concurrencent pas le mode Histoire comme structure principale de déblocage.

Lorsqu’un équipement est généré ou fabriqué, son niveau d’objet correspond au niveau du compte à cet instant et reste ensuite fixe. Il détermine les plages de génération accessibles sans garantir les rolls obtenus.

Le niveau du compte peut également débloquer progressivement des couches de complexité de l’équipement. Les seuils et la courbe concernés restent à définir dans le [référentiel Objets et équipements](./08-ITEMS.md).

## 11. Énergie générale

Le joueur possède une réserve générale d’énergie qu’il peut investir librement dans les activités individuelles disponibles.

Par défaut, cette même réserve est utilisée notamment par :

* le mode Histoire ;
* les modes PvE individuels ;
* le farming ;
* les défis individuels ;
* le PvP.

Le PvP appartient à cette règle parce qu’il constitue une activité individuelle du joueur, même lorsqu’il l’oppose à un autre joueur. Le joueur peut donc consacrer une grande partie ou la totalité de sa réserve disponible à une session PvP.

La réserve générale :

* régule le rythme de jeu et la vitesse générale de progression sans imposer l’activité choisie ;
* se régénère avec le temps ;
* continue à s’accumuler lorsque le joueur ne joue pas ;
* ne doit pas être perdue simplement parce que le joueur ne s’est pas connecté pendant une journée ;
* n’est pas vendue contre de l’argent réel.

Chaque activité individuelle définit son coût exact, mais n’introduit pas automatiquement une énergie, un ticket, une clé ou une autre ressource d’entrée parallèle. Une régulation différente reste possible uniquement lorsqu’une exception est explicitement décidée et documentée localement, notamment pour certains événements, contenus de guilde, activités communautaires ou systèmes saisonniers.

Dans le mode Histoire, l’énergie est consommée à l’entrée d’un niveau. Lors d’une défaite standard, l’énergie utilisée reste normalement consommée. Une activité particulière ou une étape d’onboarding peut définir une exception explicite.

Le système ne comporte aucun objet consommable de récupération d’énergie stocké dans l’inventaire. Lorsqu’une récompense de gameplay accorde de l’énergie, celle-ci est immédiatement ajoutée à la réserve générale du joueur. Les contenus concernés, les quantités et leur fréquence restent à définir et à équilibrer.

Une récompense directe d’énergie provenant du gameplay ne peut pas devenir indirectement un mécanisme permettant d’acheter de l’énergie contre de l’argent réel.

## 12. Absence de progression passive et payante

Hors ligne, seule la récupération de l’énergie générale est validée.

Les créatures ne gagnent automatiquement aucune XP, aucun niveau, aucun point de caractéristique, aucun équipement et aucune autre ressource générale. Le compte ne gagne pas non plus d’expérience automatiquement.

La résolution d’une défense PvP hors ligne ne constitue pas une progression passive : elle ne produit ni XP, ni loot, ni récompense directe, ni cote saisonnière. Elle peut uniquement ajuster le MMR compétitif interne selon le référentiel PvP ; ce MMR reste distinct de la progression du compte.

Le modèle de lancement interdit la vente directe :

* d’expérience ;
* de points de caractéristiques ;
* d’énergie ;
* d’équipements ;
* de ressources de progression ;
* d’une puissance ou d’un potentiel maximal supplémentaire.

Les services de confort validés ne modifient pas ce principe.

## 13. Interactions et dépendances

| Document | Responsabilité liée |
| --- | --- |
| [`01-GAME_DESIGN_DOCUMENT.md`](./01-GAME_DESIGN_DOCUMENT.md) | Boucle globale, victoire, défaite et déblocages |
| [`03-CREATURES.md`](./03-CREATURES.md) | Construction des caractéristiques et propriétés persistantes |
| [`07-EVOLUTIONS.md`](./07-EVOLUTIONS.md) | Conditions, déclenchements et conservation pendant l’évolution |
| [`08-ITEMS.md`](./08-ITEMS.md) | Niveau d’objet, génération et restitution des équipements |
| [`09-GACHA.md`](./09-GACHA.md) | État initial et nouvelles instances utilisées pour les étoiles |
| [`11-COLLECTION.md`](./11-COLLECTION.md) | Verrouillage et gestion des instances |
| [`12-MODES.md`](./12-MODES.md) | Résultats et cadre transversal de l’énergie commune aux activités |
| [`13-PVE.md`](./13-PVE.md) | Énergie générale et exceptions locales d’XP des activités PvE |
| [`14-PVP.md`](./14-PVP.md) | Énergie générale, XP de compte en attaque, absence d’XP des créatures et progression compétitive distincte |
| [`16-EVENTS.md`](./16-EVENTS.md) | Récompenses et éventuelles exceptions locales de régulation |
| [`17-QUESTS.md`](./17-QUESTS.md) | Objectifs journaliers et récompenses de progression |
| [`19-UI_FLOW.md`](./19-UI_FLOW.md) | Présentation et confirmations des actions de progression |

## 14. Éléments à préciser ultérieurement

* La courbe exacte d’XP sans niveau maximal.
* La validation finale des cinq points par niveau.
* La validation finale du ratio minimum actuellement fixé à 10 %.
* Les règles d’arrondi de l’XP.
* Les quinze multiplicateurs d’étoiles.
* Les quantités et niveaux d’étoiles exigés pour les matériaux.
* La formule exacte du score de Puissance.
* Les récompenses du niveau de compte.
* La courbe reliant le niveau du compte aux plages de génération des équipements.
* Les éventuels usages secondaires explicitement justifiés du niveau de compte.
* La méthode d’obtention, la rareté et le rythme de distribution de l’objet de redistribution des caractéristiques.
* La limite d’utilisation et le prix du service payant de redistribution.
* Les coûts des activités, la capacité éventuelle, la régénération et les règles exactes d’accumulation de l’énergie générale.
* Les contenus accordant directement de l’énergie ainsi que les quantités et fréquences concernées.
* Les exceptions locales à la réserve commune qui seront justifiées par le design d’un système particulier.
