# Project Awakening — Events

**Statut :** Rédigé — référence actuelle, à maintenir à jour

## 1. Rôle et périmètre du document

Ce document définit le fonctionnement commun actuellement validé des **Events** de Project Awakening.

Un Event est un petit contenu temporaire et ponctuel, organisé autour d’une occasion identifiable. Il utilise principalement les systèmes déjà existants pour proposer quelques missions thématiques et des récompenses adaptées.

Il ne constitue ni un mode majeur, ni une progression globale, ni une composante des Saisons. Les dates, contenus, valeurs et présentations concrètes de chaque occurrence relèvent du content design, du balancing, de l’UI et de la production.

## 2. Identité et contraintes de production

Un Event doit rester :

* léger ;
* simple à comprendre ;
* facile à rejoindre ;
* réaliste à produire pour une petite équipe ;
* principalement construit à partir de systèmes, modes, conditions mesurables, composants UI et récompenses existants.

Les Events ne sont pas destinés à accueillir de grands contenus temporaires exigeant un nouveau mode complet, une infrastructure spécifique importante, une progression complexe, de nombreuses mécaniques inédites ou une production lourde d’UI, d’animations, de VFX et de contenu.

Les Saisons et les mises à jour générales portent les renouvellements plus importants. Le système Events ne crée aucune obligation de produire régulièrement un volume élevé de contenu original.

## 3. Occasions et catégories éditoriales

Un Event accompagne une occasion concrète ou identifiable, par exemple une fête populaire, l’anniversaire du jeu, une mise à jour ou une commémoration. Noël, Halloween et le Nouvel An sont des exemples illustratifs, pas un calendrier obligatoire.

Des catégories éditoriales peuvent regrouper les occurrences — Event calendaire ou festif, anniversaire, mise à jour, commémoration ou autre occasion ponctuelle adaptée. Ces catégories sont uniquement des sur-thèmes : elles ne créent ni architecture, ni progression, ni règles fonctionnelles différentes.

## 4. Durée, cadence et coexistence

Chaque Event définit librement sa durée selon son occasion, son contenu, ses missions, le calendrier et les contraintes de production. Il peut durer quelques jours, environ une semaine ou davantage lorsque son contexte le justifie.

Il n’existe aucune cadence obligatoire. La fréquence réelle et le calendrier relèvent du content design et de la production.

Plusieurs Events peuvent être actifs simultanément. Aucune limite fonctionnelle n’impose une occurrence unique, même si le planning doit éviter une accumulation confuse ou excessivement exigeante.

## 5. Indépendance vis-à-vis des Saisons

Les Events et les Saisons sont deux systèmes totalement indépendants.

Un Event :

* n’utilise pas le calendrier d’une Saison ;
* n’a pas besoin de commencer ou de finir avec elle ;
* ne dépend pas de l’inter-saison ;
* peut se dérouler pendant une Saison ou une inter-saison ;
* peut commencer et finir à tout moment ;
* ne devient pas saisonnier parce que son thème ressemble à celui d’une Saison.

Une proximité thématique volontaire ou accidentelle ne crée aucune relation fonctionnelle. Le cadre transversal des Saisons reste défini dans [`16-SEASONS.md`](./16-SEASONS.md).

## 6. Accès et rubrique Events

Le jeu possède une rubrique dédiée qui liste chaque Event actuellement disponible et permet de les consulter individuellement. Lorsqu’aucun Event n’est actif ou en phase de fermeture, elle peut simplement indiquer qu’aucun Event n’est actuellement disponible, sans contenu artificiel de remplacement.

Le système Events est débloqué à un jalon cohérent de la progression. Une occurrence ne peut demander que des fonctionnalités déjà accessibles au joueur, sauf si elle lui fournit directement le contenu nécessaire.

Le jalon exact de déblocage appartient au cadrage de la progression et de l’onboarding.

## 7. Missions thématiques

Le cœur d’un Event repose sur de petites missions temporaires liées à son thème. Elles se distinguent des quêtes habituelles par leur contexte, les actions particulières proposées et leurs éventuels objets ou éléments spécifiques.

Une occurrence peut utiliser librement :

* une liste de missions indépendantes accessibles simultanément ;
* un ensemble de missions pouvant débloquer une récompense globale ;
* une chaîne progressive dans laquelle une mission débloque la suivante, un contenu nécessaire ou une récompense intermédiaire ;
* une structure mixte combinant plusieurs de ces modèles.

Aucun nombre minimal de missions, aucune catégorie obligatoire, aucune récompense globale systématique et aucune structure universelle ne sont imposés.

Les missions peuvent mesurer des actions réalisées dans les combats, les modes, l’invocation, la collection, les Skills, les équipements ou d’autres fonctionnalités existantes. Elles n’en modifient pas les règles permanentes et ne créent pas de dépendance structurelle avec les systèmes utilisés.

## 8. Progression et suivi

Un Event ne possède pas par défaut :

* de niveau ou d’XP d’Event ;
* de barre de progression globale ;
* de parcours global de récompenses ;
* de système comparable à un Battle Pass.

L’interface suit directement la progression utile de chaque mission. Une chaîne peut indiquer son étape courante, sans ajouter de jauge globale lorsqu’elle n’apporte aucune information.

Lorsqu’une mission est terminée, sa récompense récupérable est mise en évidence. Après récupération, son état devient `Récupéré` ou équivalent et ne demande plus d’interaction. Une liste entièrement accomplie et récupérée n’a pas besoin d’un indicateur artificiel de complétion à `100 %`.

Chaque Event définit localement sa fin fonctionnelle : accomplissement de missions indépendantes, dernière étape d’une chaîne ou déblocage d’une récompense globale éventuelle.

## 9. Non-rétroactivité

Une mission d’Event ne comptabilise jamais une action réalisée avant qu’elle soit active et accessible au joueur. Sa progression commence seulement à cet instant.

Cette application locale suit le principe transversal des missions, quêtes et objectifs comparables défini dans [`18-QUESTS.md`](./18-QUESTS.md). Toute exception future doit être explicitement documentée par le système concerné.

## 10. Accessibilité et contenus nécessaires

Une mission ne doit jamais être bloquée par l’absence d’un contenu spécifique obtenu aléatoirement ou pendant une ancienne période. Si elle exige une créature, un skin, un Artefact, un objet, une ressource ou une autre fonctionnalité précise, le jeu doit en garantir l’accès, par exemple parce que le joueur la possède déjà, parce que l’Event la fournit ou parce qu’une étape précédente la débloque.

Le joueur ne dépend donc pas d’une RNG antérieure pour participer normalement.

Lorsqu’une famille précise est réellement indispensable, l’Event peut exceptionnellement accorder directement une nouvelle instance au joueur qui ne la possède pas. Cette instance suit l’état standard d’une nouvelle acquisition : forme de base, stade 1, niveau 1, 0 étoile et aucun point de caractéristique attribué.

Cette remise est une acquisition directe exceptionnelle, pas une invocation. Un joueur possédant déjà la famille utilise normalement son instance existante et ne reçoit pas automatiquement un doublon. Les règles communes d’acquisition directe restent définies dans [`09-GACHA.md`](./09-GACHA.md).

Un autre contenu nécessaire peut être remis au lancement, à l’ouverture de la rubrique, par une action introductive évidente ou comme récompense d’une mission précédente.

## 11. Objets, effets locaux et possession durable

Un objet, un skin ou un autre contenu acquis pendant un Event reste définitivement possédé après sa fin. Sa provenance ne crée ni catégorie structurelle d’objet d’Event, ni skin temporaire, ni disparition automatique.

Un Event peut proposer des objets thématiques, utilitaires ou humoristiques, y compris des Artefacts destinés à soutenir ses missions sans présenter une puissance durable importante.

Un objet peut posséder un effet actif seulement pendant une période ou une occurrence explicitement définie. Après cette période, l’objet reste possédé ; son effet peut devenir inactif ou conserver un bénéfice permanent mineur si son contenu le prévoit et si l’équilibrage le permet. Un tel objet ne doit pas devenir indispensable aux builds ou à la progression.

Un gimmick purement contextuel, cosmétique ou humoristique peut rester local à l’Event, y compris lorsqu’une mission suit son utilisation. Il ne devient pas automatiquement un Effet de combat standard de [`06-COMBAT_EFFECTS.md`](./06-COMBAT_EFFECTS.md). Les exemples comme une boule de neige ou un état descriptif sans conséquence mécanique restent illustratifs.

## 12. Récompenses

Selon son contenu, un Event peut notamment accorder :

* de la monnaie générale ;
* des composants et ressources de progression ;
* de petites quantités de ressource générale d’invocation ;
* de l’énergie générale ;
* des paquets de skins, des skins directs ou d’autres cosmétiques ;
* des Artefacts et objets thématiques ou humoristiques ;
* d’autres récompenses compatibles avec les systèmes permanents.

Aucune catégorie n’est obligatoire et les quantités relèvent du balancing et du content design.

La ressource d’invocation reste la ressource générale définie dans [`09-GACHA.md`](./09-GACHA.md). Un Event ne crée ni ticket, ni monnaie, ni ressource événementielle d’invocation, ni nouvelle catégorie d’invocation.

Lorsqu’un Event accorde ponctuellement de l’énergie générale, celle-ci est ajoutée directement à la réserve commune selon [`10-PROGRESSION.md`](./10-PROGRESSION.md). Aucun consommable, ticket ou nouvelle ressource n’est créé. Cette récompense ne doit pas être distribuée à chaque petite mission ni créer une boucle répétable remboursant structurellement autant ou davantage d’énergie que l’activité n’en coûte.

Les paquets gratuits respectent les mêmes règles que les paquets payants correspondants. Un skin direct n’appartient à aucune série distribuée par paquets. Un Event ne peut pas réintroduire un ancien cosmétique saisonnier, dont le seul retour possible reste une offre temporaire de la boutique selon le cadre de monétisation.

## 13. Arrivée en cours d’Event

Un joueur qui commence le jeu, débloque le système Events ou revient pendant la phase active peut participer immédiatement. Il bénéficie uniquement du temps restant et ne reçoit aucune prolongation individuelle.

Une récompense de lancement peut être disponible dès le début de l’Event, notamment lorsqu’elle introduit son thème ou fournit un contenu nécessaire. Un joueur arrivant plus tard peut la récupérer tant que la phase active continue.

## 14. Fin active et phase de fermeture

À la fin exacte de la phase active :

* les missions cessent immédiatement de progresser ;
* aucune nouvelle mission ne peut être terminée ;
* aucune nouvelle récompense ne peut être débloquée ;
* les missions inachevées le restent ;
* aucune action ultérieure ne complète rétroactivement l’Event.

Tout contenu déjà obtenu reste définitivement possédé.

L’Event peut ensuite rester visible pendant une phase de fermeture d’environ une semaine, valeur ajustable. Il est clairement présenté comme terminé. Cette phase autorise uniquement la récupération de récompenses déjà débloquées avant la fin active ; elle ne permet aucune progression ni nouvelle éligibilité.

Un joueur qui devient éligible seulement pendant la fermeture ne peut ni participer, ni recevoir une récompense de lancement qu’il n’avait pas débloquée pendant la phase active.

À l’expiration de la fermeture, l’Event disparaît de la liste et ses récompenses temporelles non réclamées sont définitivement perdues, sans crédit ni récupération rétroactive automatique. Les règles transversales de disponibilité et d’expiration restent définies dans [`10-PROGRESSION.md`](./10-PROGRESSION.md).

## 15. Récurrence des thèmes

Un thème peut revenir librement lors d’une nouvelle occurrence. Celle-ci peut réutiliser, modifier, retirer ou ajouter des missions, objets et récompenses. Le retour d’un thème n’impose ni copie identique, ni calendrier fixe, ni farming des anciennes occurrences.

## 16. Frontière avec les quêtes

Les missions d’Event sont totalement distinctes :

* des trois quêtes journalières ;
* des quêtes saisonnières individuelles ;
* des quêtes saisonnières de Guilde.

Elles ne remplacent, ne réduisent et ne modifient pas la liste, la sélection ou le renouvellement des quêtes journalières. Elles ne deviennent pas des quêtes saisonnières et peuvent coexister avec toutes ces catégories.

Une mission d’Event peut demander une action dans une activité également utilisée par une quête sans créer de relation fonctionnelle entre les systèmes.

## 17. Notifications et interface

L’annonce d’un Event reste légère. Elle peut utiliser un indicateur dans l’interface, un badge sur la rubrique Events ou une petite présentation lors de la première connexion concernée. Elle ne nécessite ni calendrier complexe, ni pression permanente, ni notification téléphone spécifique.

Pour chaque occurrence, l’interface doit permettre de connaître au minimum :

* son nom ou son thème ;
* sa période active et le temps restant pertinent ;
* son état actif ou terminé ;
* ses missions et leurs dépendances visibles ;
* la progression utile de chaque mission ;
* les récompenses, leur disponibilité et leur état de récupération ;
* la phase de fermeture et ses restrictions.

La rubrique et les missions réutilisent autant que possible les composants existants. Le layout final appartient à [`20-UI_FLOW.md`](./20-UI_FLOW.md).

## 18. Hauts Faits et cohérence narrative

Les Events peuvent alimenter de futurs Hauts Faits conservant la mémoire durable d’une participation, d’une complétion ou d’une performance. Leur fonctionnement appartient au futur `19-ACHIEVEMENTS.md` ; aucun historique événementiel séparé n’est nécessaire.

Un Event festif, humoristique ou commémoratif n’est pas automatiquement canonique. Toute révélation, conséquence durable ou évolution narrative canonique doit être décidée explicitement et respecter le [référentiel Lore](../02-world/01-LORE.md).

## 19. Dépendances documentaires

| Document | Responsabilité liée |
| --- | --- |
| [`06-COMBAT_EFFECTS.md`](./06-COMBAT_EFFECTS.md) | Frontière entre Effet de combat standard et gimmick local |
| [`08-ITEMS.md`](./08-ITEMS.md) | Objets, Artefacts et effets contextuels |
| [`09-GACHA.md`](./09-GACHA.md) | Ressource générale d’invocation et acquisitions directes exceptionnelles |
| [`10-PROGRESSION.md`](./10-PROGRESSION.md) | Énergie générale, disponibilité, éligibilité et expiration des récompenses |
| [`11-COLLECTION.md`](./11-COLLECTION.md) | Skins directs et contenus définitivement possédés |
| [`12-MODES.md`](./12-MODES.md) | Règles des activités réutilisées par les missions |
| [`16-SEASONS.md`](./16-SEASONS.md) | Cadre saisonnier totalement indépendant |
| [`18-QUESTS.md`](./18-QUESTS.md) | Non-rétroactivité transversale et séparation des catégories de missions et quêtes |
| [`20-UI_FLOW.md`](./20-UI_FLOW.md) | Rubrique, suivi, états, notifications et fermeture |
| [`04-MONETIZATION.md`](../00-foundation/04-MONETIZATION.md) | Paquets, offres temporaires et garde-fous commerciaux |
| [`01-LORE.md`](../02-world/01-LORE.md) | Canon éventuel et cohérence narrative |

## 20. Éléments à préciser ultérieurement

Le cadrage fonctionnel est établi. Restent réservés au content design, au balancing, à l’UI, à la production ou à de futurs référentiels :

* le jalon exact de déblocage du système Events ;
* les premières occurrences, leur calendrier et leur fréquence réelle ;
* la durée concrète de chaque Event et de sa fermeture ;
* les missions, dépendances et récompenses exactes de chaque occurrence ;
* les quantités de ressources et autres valeurs de balancing ;
* les objets, effets locaux et habillages thématiques concrets ;
* les détails graphiques, animations, wording et layout final ;
* les Hauts Faits concrets ;
* les éventuelles utilisations narratives canoniques futures.

Aucune question fonctionnelle bloquante ne subsiste actuellement pour le système Events.
