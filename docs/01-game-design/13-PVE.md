# Project Awakening — Modes PvE

**Statut :** Rédigé — référence actuelle, à maintenir à jour

## 1. Rôle et périmètre du document

Ce document constitue le référentiel spécialisé des modes et activités PvE de Project Awakening.

Il définit les identités, progressions, résultats, récompenses et exceptions propres au mode Histoire, aux Boss personnels, aux World Boss et à la Tour infinie. Il peut également accueillir de futurs modes PvE ne justifiant pas leur propre référentiel.

Tous les modes PvE héritent par défaut des contrats transversaux de [`12-MODES.md`](./12-MODES.md) et, lorsqu’ils utilisent le moteur de combat, des règles de [`02-COMBAT.md`](./02-COMBAT.md). Une exception au combat standard, à l’énergie, aux récompenses, à l’XP, à la victoire ou à la défaite reste explicitement locale au mode concerné.

Le présent document ne fixe pas les valeurs numériques, les tables de loot concrètes, les courbes de difficulté ni les paramètres économiques réservés au balancing, au content design et aux données de production.

## 2. Statut et identité des modes PvE

| Mode ou contenu | Statut actuel | Fonction principale |
| --- | --- | --- |
| Début représentatif du mode Histoire | Inclus dans la vertical slice | Prouver la boucle PvE initiale et l’onboarding |
| Mode Histoire | Colonne vertébrale PvE d’une première version jouable | Progression générale, déblocages et farming de base |
| Boss personnels | Direction PvE de long terme | Challenge individuel spécialisé, progression propre et loot ciblé |
| World Boss | Direction PvE de long terme | Objectif communautaire temporaire fondé sur une réserve globale de PV |
| Tour infinie | Direction PvE de long terme | Challenge saisonnier, mesure de progression, classement et prestige |

La présence d’un mode dans ce tableau ne fixe ni son ordre de production, ni sa date de disponibilité, ni ses paramètres de balancing.

## 3. Application du cadre commun

Une activité PvE individuelle utilise par défaut la réserve générale d’énergie définie dans [`10-PROGRESSION.md`](./10-PROGRESSION.md). Elle n’introduit une autre ressource d’entrée que si une exception est explicitement décidée et documentée pour ce mode.

Les règles standards de composition, de préparation, de combat, de victoire, de défaite et de résumé post-combat restent applicables sauf exception locale définie ci-dessous.

Deux exceptions d’XP en cas de défaite sont actuellement validées :

* une défaite dans le mode Histoire accorde une petite quantité d’XP aux créatures participantes ;
* une défaite dans la Tour infinie peut accorder une petite quantité d’XP aux créatures participantes.

Ces exceptions ne rendent pas l’XP de défaite universelle. Elles n’accordent pas d’XP au compte, qui reste liée à la réussite de l’activité sauf future exception explicite.

Les Artefacts et Sources d’énergie peuvent posséder des effets dont l’activation dépend d’un contexte PvE documenté, notamment d’un type d’adversaire ou d’un mode. Cette capacité structurelle ne crée aucune catégorie séparée d’équipement PvE et ne valide aucun effet concret, coefficient ou mode d’obtention particulier.

## 4. Mode Histoire

### 4.1. Rôle et structure

Le mode Histoire constitue :

* la principale chaîne de progression PvE ;
* la colonne vertébrale initiale du jeu ;
* la principale structure de déblocage des fonctionnalités ;
* le principal support de l’onboarding ;
* le contenu principal de la vertical slice.

Il est organisé en :

* mondes ;
* niveaux ;
* combats ;
* boss ou jalons.

Un niveau ordinaire correspond généralement à un combat court.

Les boss d’Histoire constituent des combats plus importants pouvant posséder leur propre identité, leurs propres Skills, des mécaniques particulières et des contraintes spécifiques.

Il n’existe pas de catégorie structurelle distincte appelée « défi spécial ». Une future activité nécessitant plusieurs combats successifs ou une règle particulière devra être définie explicitement sans ajouter artificiellement cette catégorie à la structure de base du mode Histoire.

### 4.2. Progression, onboarding et rejouabilité

Le mode Histoire doit :

* augmenter progressivement sa difficulté ;
* rester rejouable ;
* soutenir le farming de Sources d’énergie, de composants et d’autres récompenses pertinentes ;
* servir de principale source de déblocage des fonctionnalités ;
* accueillir de nouveaux mondes et niveaux au fil du développement ;
* soutenir une progression longue sans exiger une narration détaillée pour chaque niveau.

La puissance d’équipe peut servir d’indication de difficulté, mais ne constitue pas un verrou systématique.

La vertical slice comprend uniquement un début représentatif du mode Histoire : plusieurs niveaux courts et un boss ou jalon final. Elle doit permettre de tester la boucle suivante :

> sélectionner une équipe → combattre → recevoir expérience et récompenses → développer les créatures → améliorer la composition → franchir un nouveau jalon.

Les autres modes spécialisés, les événements, les guildes, les saisons et les systèmes sociaux sont exclus de cette vertical slice.

### 4.3. XP en cas de victoire

Lorsqu’un niveau est réussi, les créatures participantes reçoivent la quantité normale d’XP prévue pour l’activité selon les règles de [`10-PROGRESSION.md`](./10-PROGRESSION.md).

Cette XP normale est identique pour une première réussite et pour le rejeu ultérieur du même niveau. La première réussite n’accorde pas davantage d’XP du seul fait qu’elle est la première.

La réussite accorde également l’XP du compte prévue pour l’activité.

### 4.4. XP en cas de défaite

Une défaite dans le mode Histoire accorde une petite quantité d’XP aux créatures participantes. Cette quantité reste nettement inférieure à l’XP normale d’une victoire et sa valeur exacte relève du balancing.

Cette exception locale ne donne aucune XP au compte et ne transforme pas la défaite en réussite.

### 4.5. Première réussite et farming

Une première réussite peut accorder :

* des récompenses uniques ;
* des déblocages ;
* des éléments de progression ;
* d’autres récompenses de première complétion.

Une réussite ultérieure du même niveau :

* conserve l’XP normale de l’activité ;
* accorde les récompenses répétables prévues par sa table de loot ;
* ne redonne aucune récompense unique déjà obtenue.

Le mode Histoire reste ainsi rejouable et utilisable pour le farming sans multiplier les récompenses de première réussite.

### 4.6. Énergie et résultat

Le mode Histoire utilise la réserve générale d’énergie, consommée à l’entrée d’un niveau.

Lors d’une défaite, l’énergie utilisée reste normalement consommée. Une activité particulière ou une étape d’onboarding peut définir une exception explicite.

## 5. Boss personnels

### 5.1. Identité et diversité

Les Boss personnels constituent un mode PvE individuel de long terme, distinct des boss du mode Histoire.

Ils proposent :

* un challenge individuel spécialisé ;
* une progression propre à chaque boss ;
* une incitation à développer plusieurs équipes et builds ;
* des sources de loot spécialisées.

Plusieurs Boss personnels différents peuvent exister. Chaque boss possède sa propre identité, notamment son apparence, ses Skills, ses mécaniques, ses éléments, son comportement, ses forces et faiblesses, ses besoins stratégiques et sa table de loot.

Une équipe excellente contre un boss ne doit donc pas nécessairement être optimale contre un autre.

### 5.2. Rotations et persistance

Les Boss personnels peuvent apparaître selon une rotation. Le rythme exact de cette rotation et la durée de disponibilité de chaque boss relèvent du content design.

La progression est indépendante pour chaque boss et persiste à l’échelle du compte. Lorsqu’un boss quitte la rotation puis revient, le joueur retrouve la progression précédemment atteinte contre ce boss.

### 5.3. Progression et paliers jouables

Chaque Boss personnel possède une progression sans limite théorique prédéfinie. Battre le palier actuel :

* valide ce palier ;
* débloque le palier suivant ;
* augmente progressivement la difficulté accessible.

Le joueur peut uniquement jouer :

* son palier actuel afin de progresser ;
* le palier immédiatement précédent déjà réussi afin de farmer un niveau maîtrisé.

Il ne peut pas redescendre librement vers tous les anciens paliers. Les numéros de paliers utilisés pendant le cadrage servent uniquement à illustrer ce contrat et ne constituent aucun seuil de contenu validé.

### 5.4. Loot spécialisé

Les Boss personnels peuvent devenir une source importante de loot spécialisé, notamment :

* d’éléments liés aux sets ;
* de composants permettant de former ou fabriquer des sets ;
* de composants de craft spécifiques ;
* de ressources ou composants propres à certains boss ;
* d’autres récompenses spécialisées.

Chaque boss peut posséder sa propre table de loot. La qualité, la richesse ou le potentiel de cette table doit progresser avec les paliers.

Les taux, recettes, courbes, paliers exacts, composants précis et règles de farming du palier précédent restent réservés au balancing et au content design.

### 5.5. Énergie

Les Boss personnels utilisent la réserve générale d’énergie. Leur coût exact reste à équilibrer et aucune énergie spécifique n’est validée.

## 6. World Boss

### 6.1. Identité et fenêtre d’activité

Le World Boss est un objectif communautaire temporaire dans lequel l’ensemble des joueurs contribue à réduire une réserve globale de PV à zéro avant la fin d’une fenêtre limitée.

La référence actuelle de cette fenêtre est d’environ une semaine. Sa durée exacte reste ajustable pendant le content design.

### 6.2. Victoire ou échec collectif

Si les PV globaux atteignent zéro avant l’expiration de la fenêtre :

* le World Boss est vaincu ;
* chaque joueur éligible obtient la récompense finale une seule fois pour cette apparition.

Si le World Boss possède encore des PV à l’expiration :

* le World Boss n’est pas vaincu ;
* aucune récompense finale n’est distribuée ;
* aucun joueur ne reçoit cette récompense.

Le résultat suit donc un principe de victoire collective ou d’échec collectif.

### 6.3. Tentative individuelle

Une tentative est un combat individuel contre le World Boss. Sa durée de référence est d’environ deux minutes et reste compatible avec le timeout standard de 120 secondes de simulation.

La tentative se termine :

* à l’expiration de son timer individuel ;
* plus tôt si toutes les créatures du joueur sont mortes ;
* ou selon une autre condition locale explicitement documentée.

Tant que le World Boss est vivant, les dégâts infligés pendant chaque tentative sont réellement soustraits à sa réserve globale de PV.

Le résumé expose les informations utiles à la compréhension du résultat personnel et collectif, notamment la contribution du joueur et l’état restant du World Boss. Le layout final appartient à [`19-UI_FLOW.md`](./19-UI_FLOW.md).

### 6.4. Fréquence et coût de participation

Le joueur peut participer autant de fois qu’il le souhaite tant que le World Boss est vivant et qu’il peut payer le coût de la tentative. Il n’existe aucune limite fixe de tentatives pendant cette phase collective.

Chaque tentative normale possède un coût élevé en énergie générale. Ce coût constitue la principale régulation individuelle et son montant exact relève du balancing.

Le World Boss ne crée aucun ticket, aucune clé, aucune monnaie d’entrée ni aucune énergie spécifique.

### 6.5. Éligibilité à la récompense finale

Pour être éligible à la récompense finale, le joueur doit avoir effectué au moins une participation valide pendant l’apparition concernée.

Les participations supplémentaires augmentent la contribution collective sans permettre de recevoir plusieurs fois la récompense finale.

### 6.6. Participation après la victoire collective

Si le World Boss est déjà vaincu mais qu’un joueur n’a encore effectué aucune participation, ce joueur peut toujours combattre une représentation du boss.

Ce combat se déroule normalement et ses dégâts sont simulés, mais ils ne modifient plus les PV globaux. Une participation tardive valide rend le joueur éligible à la récompense finale de l’apparition, reçue une seule fois.

Une tentative tardive coûte davantage qu’une tentative effectuée pendant que le World Boss est vivant. La référence actuelle est :

> coût tardif = `×1,5` le coût normal du World Boss

Cette valeur reste ajustable pendant le balancing. Le principe validé est que participer après la victoire collective reste possible, mais moins avantageux que contribuer pendant que le World Boss est encore vivant.

Si le World Boss échoue collectivement à l’expiration de sa fenêtre, aucune participation tardive n’existe et aucune récompense finale n’est accordée.

### 6.7. Scaling entre les apparitions

La difficulté d’une nouvelle apparition de World Boss doit suivre l’évolution globale de la population. Son calibrage peut notamment prendre en compte :

* la progression des joueurs actifs ;
* la puissance globale disponible ;
* les performances des précédentes apparitions ;
* la population active ;
* d’autres données pertinentes.

Les indicateurs et formules exacts restent à définir.

Une fois une apparition commencée, ses paramètres sont figés pour toute cette apparition. Ses PV ne sont pas augmentés dynamiquement pendant la fenêtre en fonction des performances observées.

## 7. Tour infinie

### 7.1. Identité et difficulté

La Tour infinie constitue un challenge PvE de long terme volontairement plus difficile que le mode Histoire.

Elle sert à :

* mesurer la progression et la maîtrise stratégique du joueur ;
* proposer une difficulté croissante sans limite théorique prédéfinie à l’intérieur d’une saison ;
* soutenir un classement saisonnier et le prestige ;
* encourager l’adaptation des équipes et des builds.

Elle n’est pas conçue comme une boucle de farming des anciens étages.

### 7.2. Progression dans une saison

Pendant une saison, le joueur possède un étage actuel.

Lorsqu’il remporte cet étage :

* il obtient la récompense unique de l’étage ;
* l’étage suivant devient son nouvel étage actuel ;
* l’étage terminé ne peut plus être rejoué pendant cette progression.

Le joueur ne peut pas revenir librement aux anciens étages. Contrairement aux Boss personnels, aucun palier précédent n’est farmable.

### 7.3. Défaite

Une défaite dans la Tour infinie :

* ne valide pas l’étage ;
* n’accorde pas sa récompense ;
* ne fait pas progresser vers l’étage suivant ;
* laisse le joueur sur son étage actuel ;
* peut accorder une petite quantité d’XP aux créatures participantes.

Cette XP constitue une exception locale à la règle standard. Elle n’accorde aucune XP au compte et sa valeur exacte relève du balancing.

### 7.4. Saisons et réinitialisation

La Tour infinie peut fonctionner avec de véritables saisons. Une nouvelle saison peut :

* réinitialiser la progression active ;
* placer les joueurs sur une nouvelle progression ;
* renouveler le classement.

Ce reset évite un avantage permanent des joueurs historiquement les plus avancés, demande aux joueurs souhaitant être classés de rejouer le mode et permet de renouveler régulièrement le challenge. La Tour n’est donc pas documentée comme une progression obligatoirement permanente entre toutes les saisons.

### 7.5. Renouvellement saisonnier

Une saison peut renouveler :

* les adversaires et compositions ennemies ;
* la courbe et la vitesse de montée en difficulté ;
* les modificateurs ;
* certaines règles locales ;
* la table de loot ;
* le thème artistique ou narratif.

Le thème visuel ou narratif reste distinct des règles de gameplay. Une saison thématique ne doit pas se réduire à imposer automatiquement l’équipe d’un élément correspondant.

Les saisons peuvent utiliser des malus, contraintes, comportements ennemis particuliers, modificateurs ou autres variations stratégiques. Les exemples envisagés pendant le cadrage restent purement illustratifs et ne valident aucune mécanique permanente.

### 7.6. Diversité stratégique

Une équipe optimale pendant une saison ne doit pas nécessairement rester optimale la saison suivante.

Le renouvellement doit encourager :

* l’entretien de plusieurs équipes ;
* la diversité des builds et des créatures utilisées ;
* l’adaptation aux règles et adversaires de la saison ;
* l’absence d’une composition universelle reproduite à chaque saison.

### 7.7. Classement, historique et prestige

La Tour peut posséder un classement saisonnier principalement consacré à la comparaison, au prestige et à la reconnaissance. L’étage atteint peut constituer son critère principal ; les règles précises de départage restent à cadrer.

Le classement ne doit pas produire directement une puissance obligatoire.

Malgré un reset de la progression jouable, des performances importantes peuvent rester enregistrées sur le compte, notamment un rang final ou un étage remarquable. Elles pourront alimenter le futur `18-ACHIEVEMENTS.md`, sans définir ici le fonctionnement complet des hauts faits.

Certains hauts faits ou éléments de prestige pourront éventuellement accorder des récompenses strictement cosmétiques ou honorifiques. Les contours ou bordures de carte constituent une piste privilégiée ; des titres, badges ou autres éléments visuels restent également possibles. Aucune récompense précise n’est obligatoire ou validée à ce stade et aucun bonus de puissance ne peut en résulter.

### 7.8. Loot et énergie

Une saison peut proposer une table de loot différente afin de renouveler l’intérêt du mode. Elle peut également inclure des paquets de skins ou d’autres récompenses cosmétiques ; lorsqu’un paquet appartient à une série également distribuée commercialement, il suit les mêmes règles que les autres paquets de cette série conformément au cadre de monétisation.

Les récompenses précises restent à définir et la Tour ne doit pas devenir une source exclusive de puissance imposant sa participation à la progression normale.

La Tour utilise la réserve générale d’énergie. Aucune ressource d’entrée spécifique n’est validée et le coût exact d’une tentative relève du balancing.

## 8. Futurs modes PvE

Un futur mode ou une activité PvE mineure peut être ajouté au présent document lorsqu’il applique principalement le cadre commun et ne nécessite qu’un nombre limité de règles propres.

Chaque ajout doit indiquer son statut de périmètre, son identité, sa progression, ses résultats, ses récompenses et ses éventuelles exceptions sans recopier intégralement les contrats transversaux.

## 9. Frontières documentaires

Le fonctionnement d’un mode PvE reste défini ici même lorsqu’il utilise une rotation, une fenêtre temporaire ou une saison. [`16-EVENTS.md`](./16-EVENTS.md) porte uniquement les règles événementielles ou éditoriales transversales qui s’appliquent lorsqu’un événement s’appuie sur ce mode.

Les parcours et informations nécessaires sont définis fonctionnellement dans [`19-UI_FLOW.md`](./19-UI_FLOW.md), sans imposer ici leur layout final.

Le futur `18-ACHIEVEMENTS.md` devra définir les hauts faits, leur structure et leurs récompenses éventuelles. Le présent document se limite aux performances PvE susceptibles de les alimenter.

## 10. Dépendances

| Document | Responsabilité liée |
| --- | --- |
| [`01-GAME_DESIGN_DOCUMENT.md`](./01-GAME_DESIGN_DOCUMENT.md) | Boucles globales, mode Histoire, onboarding et vertical slice |
| [`02-COMBAT.md`](./02-COMBAT.md) | Moteur de combat, timeout standard et objectifs propres aux modes |
| [`08-ITEMS.md`](./08-ITEMS.md) | Sets, composants, fabrication et principes des tables de loot |
| [`10-PROGRESSION.md`](./10-PROGRESSION.md) | XP, déblocages, énergie générale et exceptions locales de défaite |
| [`12-MODES.md`](./12-MODES.md) | Contrats transversaux et statuts de périmètre |
| [`16-EVENTS.md`](./16-EVENTS.md) | Enveloppes événementielles et éditoriales pouvant utiliser un mode PvE |
| [`17-QUESTS.md`](./17-QUESTS.md) | Objectifs pouvant utiliser les activités débloquées |
| [`19-UI_FLOW.md`](./19-UI_FLOW.md) | Sélection, préparation, progression, contribution et résultats |
| [`04-MONETIZATION.md`](../00-foundation/04-MONETIZATION.md) | Absence de puissance obligatoire liée au paiement ou aux cosmétiques |

## 11. Éléments à préciser ultérieurement

### 11.1. Mode Histoire

* Les valeurs exactes d’XP de victoire et de défaite.
* Les coûts en énergie, tables de loot et récompenses de première réussite.
* Le contenu précis des mondes, niveaux, boss et jalons.
* Les jalons exacts de l’onboarding et des déblocages.
* Les données exactes de la vertical slice.

### 11.2. Boss personnels

* La liste des boss, leurs contenus concrets, leurs rotations et leurs durées de disponibilité.
* Leur courbe de difficulté et leurs coûts en énergie.
* Leurs tables de loot, taux, composants, recettes et récompenses de palier.
* La progression précise du loot et les règles chiffrées du farming du palier précédent.

### 11.3. World Boss

* La fréquence, la durée et les paramètres exacts de chaque apparition.
* Le coût normal en énergie et l’ajustement éventuel du multiplicateur tardif `×1,5`.
* La formule de scaling, les PV, la puissance et les tables de récompenses.
* Les éventuelles conditions d’éligibilité supplémentaires à la participation minimale.
* La présentation exacte du résumé et les indicateurs communautaires supplémentaires.

### 11.4. Tour infinie

* La durée des saisons et la courbe de difficulté.
* Le coût d’une tentative et la valeur de l’XP de défaite.
* Les adversaires, compositions, thèmes et modificateurs concrets.
* Les tables de loot saisonnières.
* Les critères de départage du classement.
* Les hauts faits, récompenses cosmétiques et contours ou bordures de carte éventuels.

Ces éléments relèvent du balancing, du content design, de la production saisonnière, de l’UI, de l’Art ou de futurs référentiels. Ils ne constituent pas des questions structurelles bloquant le statut actuel du document.
