# Project Awakening — PvP

**Statut :** Rédigé — référence actuelle, à maintenir à jour

## 1. Rôle et périmètre du document

Ce document constitue le référentiel spécialisé du PvP de Project Awakening.

Le PvP est une direction de long terme, exclue de la vertical slice et non nécessaire à la première version jouable. Il permet aux joueurs de mesurer leurs compositions, builds, équipements et stratégies face aux défenses d’autres comptes, puis de progresser dans une compétition saisonnière.

Sa fonction principale repose sur la compétition, l’évaluation stratégique, le classement, le prestige et des récompenses attractives qui ne doivent pas rendre ce mode obligatoire pour la progression normale.

Le format principal validé est un PvP asynchrone, entièrement automatique et utilisant la puissance mécanique réelle des créatures. Les valeurs numériques, contenus saisonniers, tables de récompenses et paramètres de matchmaking restent réservés au balancing et au content design.

## 2. Format asynchrone

Le joueur enregistre une équipe de défense qui peut être affrontée lorsqu’il est hors ligne. Lorsqu’il initie un combat, le matchmaking lui assigne automatiquement la défense enregistrée d’un autre compte.

Le PvP synchrone ou live n’appartient pas au périmètre actuel. Il reste une possibilité hypothétique de très long terme et ne doit pas complexifier l’implémentation du format asynchrone.

Le PvP valorise la préparation, la compréhension des systèmes, les synergies et l’adaptation à la saison plutôt que les réflexes ou la rapidité d’exécution.

## 3. Équipes d’attaque et de défense

### 3.1. Contrat commun de composition

Le PvP hérite de [`02-COMBAT.md`](./02-COMBAT.md) et de [`12-MODES.md`](./12-MODES.md), notamment :

* une équipe pouvant réunir jusqu’à six créatures ;
* les règles globales de coexistence des instances d’une même famille ;
* la formation standard sur trois lignes ;
* le moteur, le ciblage, les Skills et les Effets de combat standards ;
* le timeout standard de 120 secondes de simulation ;
* le départage standard au timeout.

Sans future exception explicitement documentée, le départage compare le nombre de créatures vivantes, puis le ratio global de PV restants et applique enfin la règle standard donnant l’égalité parfaite à l’équipe attaquante.

### 3.2. Défense enregistrée

L’équipe de défense enregistre :

* les instances sélectionnées ;
* leurs positions ;
* la composition de l’équipe.

Elle ne conserve pas un snapshot figé de la puissance passée de ces instances.

### 3.3. Données live de la défense

Lorsqu’un adversaire lance le combat, la défense utilise l’état mécanique actuel de ses instances, notamment :

* leur niveau et leurs points actuellement attribués ;
* leurs étoiles et leur forme actuelle ;
* leur équipement ou loadout actuellement applicable ;
* leurs Skills ;
* leurs effets permanents actifs ;
* leurs autres propriétés mécaniques live.

Le joueur n’a pas besoin de réenregistrer sa défense après chaque amélioration. Modifier la progression, la forme, les points, l’équipement ou le build d’une instance modifie son état lors des futurs combats de défense.

La méthode exacte de sélection d’un loadout selon l’activité reste à définir dans le système d’équipement et l’UI ; elle ne transforme pas la défense en snapshot.

## 4. Combat full Auto

Le PvP asynchrone classé fonctionne entièrement en Auto pour les deux équipes :

* les Basic Attacks sont automatiques ;
* les Active sont automatiques ;
* les Ultimate sont automatiques ;
* aucun joueur n’intervient manuellement pendant la simulation.

Le mode Manuel des Ultimate n’est pas utilisé. Cette exception locale au contrôle commun évite un avantage structurel de l’attaquant contre une défense hors ligne.

Les thèmes, modificateurs ou autres règles saisonnières s’appliquent selon les mêmes conditions annoncées aux deux équipes.

## 5. Résolution, fermeture et Skip

### 5.1. Résolution dès le lancement

La simulation complète d’un combat PvP peut être calculée dès son lancement. La séquence visible constitue uniquement la restitution du résultat déterminé.

Une fois le combat lancé :

* fermer l’application ne l’annule pas ;
* perdre la connexion ne l’annule pas ;
* quitter la visualisation ne constitue pas un abandon ;
* le résultat reste conservé et peut être consulté ultérieurement.

Aucune pénalité de déconnexion supplémentaire n’est nécessaire après le lancement.

### 5.2. Skip PvP

Le confort associé au déblocage de la vitesse de visualisation `×4` peut également donner accès à un bouton `Skip` dans le PvP.

Le Skip passe directement au résumé. Il ne modifie jamais :

* la simulation ;
* la seed RNG ;
* les calculs ou statistiques ;
* le résultat ;
* les récompenses ;
* le coût en énergie ;
* le MMR ou la cote appliqués à ce résultat.

Il constitue uniquement un confort de visualisation et ne confère aucun avantage compétitif ou économique.

## 6. Puissance réelle et équipement

### 6.1. Absence de normalisation générale

Le format principal utilise l’état mécanique réel des créatures, notamment :

* niveau ;
* points attribués ;
* forme et évolution ;
* étoiles ;
* équipement ;
* Skills ;
* effets permanents actifs ;
* autres propriétés normalement applicables.

Il ne comporte aucune normalisation générale, suppression des étoiles, désactivation des équipements, statistique PvP standardisée ni catégorie de puissance artificiellement égalisée.

Une éventuelle activité PvP future utilisant une normalisation constituerait un format distinct et ne modifierait pas le contrat du format principal.

### 6.2. Effets contextuels

Un équipement peut posséder un effet dont l’activation dépend d’un mode, d’un type d’adversaire, d’un contexte de combat ou d’une autre condition explicitement documentée.

Cette capacité ne valide aucun effet concret et ne crée aucune catégorie structurelle d’équipement PvP ou PvE. Les objets restent les mêmes Artefacts et Sources d’énergie ; ils peuvent simplement convenir davantage à certains contextes.

La fonction contextuelle d’un objet ne détermine pas automatiquement son origine. Il peut provenir des sources générales de loot, de craft, de boss, d’événements ou d’autres activités prévues sans imposer une boucle fermée où le PvP serait nécessaire pour obtenir l’équipement permettant d’y être compétitif.

### 6.3. Loadouts

Une instance peut posséder plusieurs loadouts d’équipement destinés à différents builds ou activités.

Le même objet réel peut apparaître dans plusieurs loadouts de la même instance. Dès qu’il est utilisé dans au moins un de ses loadouts, il est réservé à cette instance et ne peut pas être utilisé dans les loadouts d’une autre créature.

Pour transférer l’objet vers une autre instance, le joueur doit d’abord le retirer de tous les loadouts de sa créature actuelle. Il redevient alors disponible.

Le nombre, les noms, l’ergonomie et la méthode de sélection des loadouts restent à définir dans [`08-ITEMS.md`](./08-ITEMS.md) et [`19-UI_FLOW.md`](./19-UI_FLOW.md).

## 7. Énergie, XP et absence de progression passive

### 7.1. Énergie générale

Le PvP utilise la réserve générale d’énergie. Le joueur peut consacrer une grande partie ou la totalité de sa réserve à ce mode.

Aucune énergie, aucun ticket et aucune clé propres au PvP ne sont validés. Le coût exact d’un combat relève du balancing.

### 7.2. Combat initié par le joueur

Un combat PvP initié par le joueur peut accorder de l’XP au compte. Il n’accorde aucune XP aux créatures, quelle que soit son issue.

La quantité d’XP du compte reste à équilibrer. Le MMR et la cote constituent des progressions compétitives distinctes du niveau du compte.

### 7.3. Défense hors ligne

Une défense jouée pendant l’absence du joueur n’accorde :

* aucune XP au compte ;
* aucune XP aux créatures ;
* aucun loot ;
* aucune récompense directe ;
* aucune cote saisonnière.

Elle peut uniquement influencer le MMR. Elle ne constitue donc aucune progression passive du compte ou des créatures.

## 8. Saisons et méta

Le PvP fonctionne avec des saisons. Une saison peut comporter :

* une cote propre à la saison ;
* un classement ;
* des jalons ;
* des récompenses ;
* un thème ;
* des modificateurs ou malus ;
* des contraintes et règles locales annoncées.

Le système ne repose pas sur des divisions obligatoires Bronze, Argent, Or ou équivalentes. La progression compétitive visible utilise directement la cote saisonnière et ses jalons.

Une saison ne doit pas se réduire à une rotation élémentaire imposant automatiquement un seul élément ou une seule équipe optimale. Les variations saisonnières doivent renouveler la méta, les compositions, les builds, les équipements, les synergies et les stratégies.

Une équipe optimale pendant une saison ne doit pas nécessairement rester optimale pendant la suivante. Les thèmes concrets et modificateurs précis relèvent du content design ; les exemples étudiés pendant le cadrage restent illustratifs.

## 9. MMR et cote saisonnière

### 9.1. MMR

Le MMR constitue une estimation interne du niveau compétitif réel du compte. Il sert principalement au matchmaking et peut évoluer après :

* un combat initié par le joueur ;
* une victoire de défense ;
* une défaite de défense.

Les défenses contribuent ainsi à l’évaluation du niveau réel sans modifier la progression compétitive visible pendant l’absence du joueur.

### 9.2. Cote saisonnière

La cote saisonnière constitue la progression compétitive visible. Elle sert :

* au classement ;
* aux jalons de récompenses ;
* à la comparaison entre joueurs.

Elle ne change que lorsque le joueur initie lui-même un combat :

* une victoire augmente la cote ;
* une défaite réduit la cote.

Une victoire ou une défaite de défense ne modifie jamais directement la cote.

Les gains et pertes peuvent varier selon le niveau compétitif estimé de l’adversaire. Le sens et l’amplitude de cette variation relèvent de la formule de balancing ; les exemples du cadrage ne définissent aucun coefficient.

### 9.3. Calibration initiale du MMR

Un nouveau joueur commence avec une valeur initiale de MMR de référence.

Ses premiers combats utilisent une volatilité plus importante afin de converger rapidement vers son niveau réel. La référence actuelle est d’environ dix combats, mais leur nombre exact et les coefficients restent ajustables.

Après cette phase, les variations deviennent progressivement plus normales.

### 9.4. Nouvelle saison

Lorsqu’une nouvelle saison commence :

* le MMR est conservé ;
* la cote saisonnière est réinitialisée.

Les joueurs déjà connus du système ne doivent pas refaire obligatoirement une phase complète de placement. Leur MMR continue de permettre un matchmaking pertinent, tandis que la nouvelle cote crée une progression visible propre à la saison.

## 10. Matchmaking

### 10.1. Recherche automatique

Le joueur ne choisit pas librement son adversaire. Le système sélectionne automatiquement une défense, principalement selon le MMR. La cote visible n’est pas le critère principal d’appariement.

La recherche commence dans une fenêtre de MMR proche. Elle peut s’élargir progressivement lorsque la population disponible ne permet pas de trouver rapidement un adversaire approprié. Les largeurs, seuils et rythmes d’élargissement relèvent du balancing.

### 10.2. Garde-fou contre les rematchs

Le système évite de proposer trop souvent le même compte. La référence actuelle demande normalement environ cinq autres combats ou adversaires avant de pouvoir rencontrer de nouveau un compte récent.

Cette valeur reste ajustable et le garde-fou peut être relâché lorsque la population disponible est insuffisante.

### 10.3. Adversaire caché

La composition exacte de l’adversaire n’est pas révélée avant le lancement. Cette règle conserve la surprise, empêche la préparation systématique d’un counter parfait et valorise les compositions solides dans la méta générale.

Après le combat, la composition adverse et les informations utiles à l’analyse peuvent être affichées dans le résumé.

## 11. Jalons, activité et classement

### 11.1. Jalons de cote

Une saison peut comporter des jalons numériques de cote.

Lorsqu’un joueur atteint un jalon pour la première fois pendant la saison :

* il obtient sa récompense une seule fois ;
* cette récompense reste acquise si sa cote redescend ensuite ;
* le jalon ne peut pas être farmé en oscillant autour de son seuil.

Les seuils et récompenses exacts restent à définir.

### 11.2. Éligibilité par activité régulière

Pour rester éligible au classement officiel, le joueur doit avoir initié au moins `X` combats PvP au cours des quatorze derniers jours.

La valeur `X` relève du balancing. Cette fenêtre glissante doit exiger une activité régulière tout en permettant une absence raisonnable, notamment d’environ une semaine, sans imposer une présence quotidienne.

Si la condition n’est plus remplie :

* la cote n’est ni détruite ni automatiquement réduite ;
* le joueur devient temporairement inéligible au classement officiel ;
* il redevient éligible lorsqu’il accomplit de nouveau l’activité requise.

Aucun decay agressif ou perte quotidienne automatique de cote n’est validé.

### 11.3. Classement final

À la clôture d’une saison, seuls les joueurs éligibles participent au classement final officiel.

Le classement applique successivement :

1. la cote saisonnière la plus élevée ;
2. à cote égale, le plus grand nombre de victoires en attaque ;
3. à cote et nombre de victoires identiques, le meilleur ratio de victoires en attaque.

Les victoires de défense ne servent pas à ces départages. Le ratio intervient uniquement après le nombre brut de victoires.

En cas d’égalité sur les trois critères, les joueurs partagent le même rang. Le classement utilise des rangs de compétition avec saut des positions suivantes correspondantes. Aucun quatrième critère arbitraire n’est appliqué.

## 12. Récompenses et prestige

### 12.1. Philosophie

Les récompenses PvP doivent être attractives, mais le mode ne doit pas devenir obligatoire pour la progression normale ni fournir une puissance essentielle exclusive.

Sa finalité principale reste :

* la compétition ;
* le prestige ;
* les hauts faits ;
* les cosmétiques ;
* l’évaluation stratégique.

### 12.2. Paquets cosmétiques

Les récompenses de jalons, de saison, de classement final ou d’autres objectifs compétitifs validés peuvent inclure des paquets de skins de carte.

Lorsqu’un paquet appartient à une série également distribuée commercialement, il utilise le même pool, les mêmes probabilités, le même nombre de skins, les mêmes règles de doublons et les mêmes règles RNG que le paquet acheté correspondant. Son obtention gratuite ne crée aucune version avantagée.

### 12.3. Classement final et hauts faits

Le classement final peut alimenter de futurs hauts faits, titres, badges, contours ou bordures de carte, cosmétiques prestigieux, paquets cosmétiques et autres récompenses cohérentes.

Les récompenses les plus prestigieuses doivent rester principalement honorifiques ou cosmétiques et ne conférer aucune puissance exclusive indispensable.

Le futur `18-ACHIEVEMENTS.md` devra définir les critères et récompenses propres aux hauts faits sans être créé artificiellement pendant la présente intervention.

## 13. Historique et analyse

### 13.1. Historique de la saison en cours

Le joueur peut consulter l’historique de ses matchs de la saison en cours, comprenant :

* les attaques lancées ;
* les défenses subies.

Chaque entrée doit permettre d’identifier au minimum :

* l’adversaire ;
* le résultat ;
* le type attaque ou défense ;
* la date ou l’ordre du combat ;
* les informations compétitives pertinentes.

### 13.2. Résumé d’un match

Ouvrir une entrée donne accès au même type de résumé fonctionnel que l’écran final du combat concerné. Il présente l’équipe, le résultat, les performances agrégées par créature et les informations utiles à l’analyse sans créer un second système analytique.

L’historique détaillé n’a pas besoin d’être conservé indéfiniment après la fin de la saison. Les performances importantes peuvent persister par le classement final, les hauts faits, le prestige ou des statistiques globales.

### 13.3. Replays

Les replays complets et leur partage ne font pas partie du périmètre actuel. Ils sont repoussés à très long terme ; le résumé suffit à la première implémentation.

La reproductibilité du moteur ne doit pas conduire à imposer dès maintenant une infrastructure de stockage, de compatibilité entre versions ou de partage de replays.

## 14. Frontières documentaires

Les règles d’équipement contextuel, de loadouts et de réservation appartiennent à [`08-ITEMS.md`](./08-ITEMS.md). Le PvP définit uniquement leur usage compétitif.

La progression générale du compte et l’énergie restent définies dans [`10-PROGRESSION.md`](./10-PROGRESSION.md). Le MMR, la cote, les jalons et le classement sont des progressions compétitives propres au présent mode.

Une saison PvP conserve son fonctionnement ici même lorsqu’elle possède un thème ou une durée limitée. [`16-EVENTS.md`](./16-EVENTS.md) porte uniquement une éventuelle enveloppe événementielle ou éditoriale transversale.

Les besoins fonctionnels des écrans et parcours appartiennent à [`19-UI_FLOW.md`](./19-UI_FLOW.md), sans imposer leur layout final.

## 15. Dépendances

| Document | Responsabilité liée |
| --- | --- |
| [`01-GAME_DESIGN_DOCUMENT.md`](./01-GAME_DESIGN_DOCUMENT.md) | Place du PvP dans l’expérience et périmètre de long terme |
| [`02-COMBAT.md`](./02-COMBAT.md) | Simulation, formation, ciblage, timeout et départage standard |
| [`03-CREATURES.md`](./03-CREATURES.md) | Identité, puissance réelle et composition des équipes |
| [`08-ITEMS.md`](./08-ITEMS.md) | Effets contextuels, loadouts et réservation des équipements |
| [`10-PROGRESSION.md`](./10-PROGRESSION.md) | Énergie générale, XP du compte et absence de progression passive |
| [`12-MODES.md`](./12-MODES.md) | Statut de périmètre et contrats transversaux |
| [`13-PVE.md`](./13-PVE.md) | Philosophie saisonnière commune et usages PvE des effets contextuels |
| [`16-EVENTS.md`](./16-EVENTS.md) | Éventuelle enveloppe événementielle des saisons compétitives |
| [`19-UI_FLOW.md`](./19-UI_FLOW.md) | Préparation, matchmaking, combat, saison, classement et historique |
| [`04-MONETIZATION.md`](../00-foundation/04-MONETIZATION.md) | Skip lié à `×4`, paquets cosmétiques et équité compétitive |

## 16. Éléments à préciser ultérieurement

### 16.1. Matchmaking et MMR

* La valeur initiale du MMR et les coefficients de calibration.
* Le nombre exact de combats à forte volatilité autour de la référence actuelle d’environ dix.
* Les formules de variation du MMR.
* La largeur initiale de recherche et son élargissement progressif.
* La valeur exacte du garde-fou contre les rematchs autour de la référence actuelle d’environ cinq adversaires.

### 16.2. Cote, activité et classement

* La valeur initiale et l’échelle de cote.
* Les formules exactes de gains et pertes.
* Les seuils des jalons.
* La valeur `X` de combats initiés pendant quatorze jours.

### 16.3. Saisons et récompenses

* La durée, le calendrier, les thèmes et modificateurs concrets des saisons.
* Les tables, quantités, seuils et séries de paquets cosmétiques.
* Les récompenses de jalons, de classement et de rangs prestigieux.
* Les hauts faits, titres, badges et contours ou bordures exacts.

### 16.4. Énergie, XP et loadouts

* Le coût en énergie d’un combat initié.
* La quantité d’XP accordée au compte.
* Le nombre, les noms et l’ergonomie des loadouts.
* Leur méthode de sélection automatique ou manuelle selon les modes.

### 16.5. Content design et très long terme

* Les effets contextuels concrets, leurs coefficients et leurs conditions.
* Le PvP synchrone ou live.
* Les replays complets et leur partage.

Ces éléments relèvent du balancing, du content design, de l’UI ou d’hypothèses de très long terme. Ils ne constituent pas des questions structurelles bloquant le statut actuel du document.
