# Project Awakening — Vision du projet

**Statut :** Rédigé — référence actuelle, à maintenir à jour

**Nom de code :** Project Awakening

## 1. Présentation

Ce document définit la vision globale de **Project Awakening**.

Il décrit la philosophie du jeu, son ambition, son public cible ainsi que les grands principes qui guideront les décisions de conception, de développement et de production.

Il ne détaille pas les mécaniques du jeu. Celles-ci seront décrites dans le **Game Design Document (GDD)** et dans les documents spécialisés associés.

Ce document constitue la référence principale permettant de comprendre rapidement ce que le projet cherche à accomplir.

## 2. Vision

Créer un jeu mobile **Free-to-Play** de collection de créatures représentées sous forme de cartes, inspiré des jeux gacha modernes, dans lequel le plaisir de jeu repose avant tout sur :

* la stratégie ;
* la personnalisation ;
* la progression des créatures ;
* la création et l’optimisation d’équipes.

Le jeu souhaite proposer une expérience durable, accessible et équitable, dans laquelle les joueurs développent leurs propres créatures au fil du temps plutôt que de rechercher uniquement les créatures les plus rares.

L’objectif est de construire une licence originale capable d’évoluer pendant plusieurs années grâce à :

* un univers riche ;
* un système de progression profond ;
* une forte diversité de builds ;
* des mises à jour régulières ;
* l’ajout progressif de nouveaux contenus.

## 3. Public cible

Le jeu s’adresse principalement :

* aux joueurs mobiles sur Android et iOS ;
* aux amateurs de jeux de collection ;
* aux joueurs appréciant les jeux gacha ;
* aux personnes recherchant une progression sur le long terme ;
* aux joueurs aimant optimiser leurs équipes ;
* aux joueurs appréciant la création de différents builds.

Le jeu est conçu pour rester accessible à tout public, tout en proposant suffisamment de profondeur pour satisfaire les joueurs les plus investis.

## 4. Plateformes

Le projet est développé exclusivement pour les plateformes mobiles :

* Android ;
* iOS.

L’ensemble de l’expérience utilisateur est pensé pour une utilisation tactile.

## 5. Inspirations

Le projet s’inspire de plusieurs types de jeux sans chercher à les reproduire.

Les principales inspirations sont :

* *Saint Seiya: Legend of Justice* ;
* *Pokémon* ;
* les jeux de cartes à collectionner ;
* les Hack’n Slash, notamment pour le système d’objets ;
* les Auto Battlers.

Ces inspirations servent uniquement de base de réflexion afin de construire une identité originale.

## 6. Univers

Le jeu prend place dans un multivers composé de plusieurs mondes et régions.

La civilisation humaine d’origine a disparu, mais elle a laissé un immense héritage informationnel et culturel. Une intelligence cosmique consciente, provisoirement appelée **Matrice cosmique**, interprète ces traces et leur donne vie dans une nouvelle réalité.

Chaque famille de créatures est une création originale issue de cette interprétation. Elle peut être inspirée par différents éléments de la mémoire humaine, par exemple :

* le cinéma ;
* les mangas ;
* les jeux vidéo ;
* les mythologies ;
* les légendes ;
* les dessins animés.

Une créature constitue un écho vivant et original, jamais la copie directe d’un personnage, d’une œuvre ou d’un autre élément humain. Plusieurs influences peuvent être mélangées, mais un concept dominant peut également suffire à inspirer une famille.

Par exemple, un héros en armure futuriste pourrait inspirer une famille de scarabées mécaniques reprenant certains codes visuels emblématiques de cette armure : couleurs, cœur énergétique ou lignes du casque.

De la même manière, un chevalier associé au phénix pourrait inspirer une lignée de créatures évoluant d’un jeune oiseau de feu jusqu’à un majestueux phénix.

Une intelligence artificielle créée par l’ancienne civilisation humaine cherche à préserver ses archives et à corriger les interprétations de la Matrice. Le conflit oppose ainsi la création à la conservation sans présenter l’une de ces forces comme entièrement bonne ou mauvaise.

Certains humains, dont le joueur, peuvent établir avec les créatures un lien qui stabilise leur existence. Cette relation fournit le fondement narratif de l’acquisition, de la collection et de l’attachement aux créatures sans modifier automatiquement les règles de gameplay correspondantes.

Chaque famille de créatures possède généralement trois formes :

1. une forme de base ;
2. une forme intermédiaire ;
3. une forme finale.

Cette approche permet de créer un univers extrêmement varié tout en développant une identité propre.

Les fondations narratives détaillées sont définies dans le [document de lore](../02-world/01-LORE.md).

## 7. Concept général

Le joueur collectionne des créatures représentées sous forme de cartes.

Le système de collection doit permettre de consulter et de valoriser les éléments collectionnables du joueur. Il réunit un espace consacré aux créatures et un espace consacré aux skins de carte, sans mélanger ces deux catégories dans une liste unique.

Le catalogue des créatures présente les créatures disponibles ou connues dans le jeu, qu’elles soient possédées ou non, sous réserve des contenus qui doivent rester secrets pour des raisons narratives, événementielles ou de découverte.

La collection de skins de carte permet de consulter les skins débloqués et non débloqués, de les parcourir par série, de visualiser la progression de collection et d’appliquer les skins débloqués aux cartes des créatures concernées.

Chaque créature possède notamment :

* une rareté ;
* un ou deux éléments au maximum ;
* exactement quatre Skills :

  * exactement une Ultimate ;
  * trois autres Skills formant une combinaison fixe d’Active et de Passive ;
* six caractéristiques principales :

  * les points de vie (PV) ;
  * l’Attaque ;
  * l’Attaque spéciale ;
  * la Défense ;
  * la Défense spéciale ;
  * l’Agilité ;
* trois caractéristiques secondaires :

  * le Crit ;
  * les Dégâts critiques ;
  * l’Esquive ;
* une progression individuelle.

L’ensemble de quatre Skills d’une créature est prédéfini. Lorsqu’une créature est obtenue, le joueur ne choisit pas ses Skills, ne les remplace pas et ne construit pas son build en les sélectionnant dans une liste. Ces Skills définissent son identité fonctionnelle, son rôle et ses synergies potentielles.

La question de savoir si une nouvelle forme obtenue lors d’une évolution conserve les mêmes compétences ou possède un nouvel ensemble prédéfini reste à définir. Dans tous les cas, le joueur ne sélectionne pas librement les compétences de la forme obtenue.

Le joueur constitue une équipe pouvant réunir jusqu’à six créatures afin d’affronter les différents contenus du jeu.

Les combats sont principalement automatisés afin de mettre l’accent sur la préparation des équipes et la stratégie plutôt que sur les réflexes.

## 8. Philosophie du gameplay

Le cœur du jeu repose sur la personnalisation.

Le plaisir ne provient pas uniquement de l’obtention de nouvelles créatures, mais surtout de leur évolution et de leur optimisation.

Chaque joueur doit pouvoir développer des créatures uniques grâce à :

* la répartition des caractéristiques ;
* les équipements ;
* la progression et l’évolution ;
* l’amélioration du niveau d’étoiles ;
* le choix des créatures réunies dans une équipe ;
* les synergies entre les membres de l’équipe.

Les compétences fixes ne constituent pas un choix de personnalisation. Elles fournissent le profil fonctionnel autour duquel le joueur construit le développement et les usages de la créature.

Deux joueurs possédant exactement les mêmes créatures doivent pouvoir construire des équipes différentes.

## 9. Progression

Le joueur n’obtient jamais directement la forme finale d’une créature.

Chaque invocation permet d’obtenir la forme de base d’une famille de créatures.

Le joueur fait ensuite évoluer cette créature au fil de sa progression jusqu’à sa forme finale.

L’invocation constitue la voie principale d’obtention des créatures. Certaines créatures peuvent néanmoins être accordées directement par le gameplay, notamment comme créature de départ ou comme récompense narrative, événementielle, de progression ou d’activité. Ces exceptions doivent être explicitement documentées et ne remettent pas en cause le rôle central de l’invocation.

Les créatures gagnent de l’expérience en participant aux combats.

À chaque montée de niveau, la créature concernée reçoit des points de caractéristiques que le joueur peut répartir librement sur celle-ci selon le build souhaité.

Cette répartition constitue un choix important et n’est pas librement réversible. Le joueur peut recommencer gratuitement la progression en niveaux de la créature depuis le niveau 1 afin de modifier progressivement sa répartition. Un objet rare obtenu en jouant ou un service payant strictement limité peuvent également permettre de redistribuer les points déjà gagnés sans revenir au niveau 1.

Le service payant n’accorde aucun point supplémentaire, aucune expérience et aucune augmentation du potentiel maximal. Une méthode gratuite obtenue par le gameplay doit permettre d’atteindre le même résultat. Les règles de conservation de l’évolution, du niveau d’étoiles et des autres éléments ainsi que les limites exactes du service restent à définir.

Les doublons de créature servent à améliorer le niveau d’étoiles de la créature concernée et à augmenter progressivement son potentiel, sans nécessiter de recommencer son évolution.

## 10. Système de combat

Les combats sont conçus pour être rapides et dynamiques.

La durée moyenne recherchée d’un combat doit être comprise entre **30 et 60 secondes**. Tous les combats utilisent par défaut un timeout de **120 secondes de simulation**, sauf exception explicitement définie par un mode.

Les attaques et les compétences ordinaires sont utilisées automatiquement. Le joueur peut choisir le moment où déclencher les compétences ultimes ou activer une option qui les gère également de manière automatique.

Le joueur peut ainsi intervenir de manière limitée ou laisser le combat se dérouler entièrement automatiquement. Cette intervention ne doit pas remplacer la préparation de l’équipe comme principal facteur de réussite.

Par défaut, les dégâts sont physiques ou spéciaux. Chaque compétence offensive doit déclarer la catégorie de dégâts et la caractéristique offensive qu’elle utilise : Attaque, Attaque spéciale ou, exceptionnellement, aucune lorsqu’elle suit une formule particulière. Toute exception aux règles ordinaires de dégâts doit être explicite.

Les dégâts physiques et spéciaux peuvent produire des coups critiques par défaut. Le Crit est une caractéristique secondaire indépendante. L’Agilité contrôle l’intervalle des Basic Attacks et n’augmente pas le Crit.

Le jeu récompense avant tout la qualité de la préparation des équipes.

## 11. Éléments

Chaque forme d’une créature appartient à un ou deux éléments au maximum :

* une créature **mono-élément** possède un seul élément ;
* une créature **bi-élément** en possède deux, mécaniquement égaux et sans hiérarchie principale ou secondaire.

La liste officielle comprend neuf éléments :

1. Feu ;
2. Eau ;
3. Terre ;
4. Vent ;
5. Plante ;
6. Métal ;
7. Électricité ;
8. Lumineux ;
9. Ténèbres.

L’élément d’une créature représente principalement la nature de ses pouvoirs, de ses capacités, de ses résistances et de son style de combat. Il n’est pas déterminé uniquement par son apparence, son espèce, son habitat ou son histoire.

Chaque Basic Attack et chaque Skill offensif possède exactement un élément ou est explicitement sans élément. Une attaque ne possède pas deux éléments simultanément dans le système initial.

Le système élémentaire standard est défensif. Il n’accorde aucun bonus offensif automatique : un élément de la cible peut résister à l’élément de l’attaque, tandis qu’une relation non déclarée et le même élément contre lui-même restent neutres. La table élémentaire de base ne produit aucune immunité naturelle.

Pour une créature bi-élément, une résistance applicable sur un seul de ses éléments est appliquée une fois. Lorsque ses deux éléments résistent à l’attaque, les deux réductions sont appliquées successivement et de manière multiplicative. Les coefficients exacts restent à équilibrer.

Toutes les combinaisons de deux éléments sont autorisées par défaut. Chaque forme déclare explicitement son ou ses éléments, qui peuvent changer lors d’une évolution lorsque les pouvoirs, les capacités, les résistances ou le style de combat de la créature le justifient.

Une créature bi-élément ne reçoit aucun avantage ou désavantage global automatique, et une créature mono-élément aucune compensation systématique. Leur équilibre doit être évalué à partir de leur profil complet.

**Éléments à préciser ultérieurement :**

* Les coefficients de réduction applicables aux résistances élémentaires simples et doubles.

## 12. Effets de statut

Les effets de statut constituent un système central du combat. Ils contribuent à la profondeur stratégique, à la personnalisation des créatures, à la diversité des builds et aux interactions entre créatures, compétences et éléments.

Un effet de statut peut être positif, négatif ou, plus rarement, neutre. Ses fonctions sont cumulables : il peut notamment modifier des caractéristiques, limiter des actions, produire un effet continu, réagir à un événement ou modifier temporairement une règle du combat.

Les compétences constituent une source principale d’effets de statut sans être nécessairement leur seule source. L’association entre un effet et un élément est facultative et doit être déclarée explicitement lorsqu’elle existe.

Les applications répétées de CC totaux utilisent des diminishing returns centrés sur leur durée. Un Skill peut accorder explicitement une immunité à certains CC ou statuts. Ces mécanismes ne créent aucune caractéristique principale ou secondaire supplémentaire.

Des effets différents peuvent coexister sur une même créature. Le comportement de plusieurs applications d’un même effet doit être défini individuellement, sans imposer une règle universelle de cumul ou de renouvellement.

La liste des effets, leurs valeurs, leurs conditions d’application, leurs durées et leurs interactions détaillées sont organisées dans le [draft consacré aux effets de statut](../01-game-design/06-STATUS_EFFECTS.md).

## 13. Personnalisation

La personnalisation constitue l’élément central du projet.

Chaque créature peut être personnalisée grâce :

* à la répartition de ses caractéristiques ;
* à son équipement ;
* à sa progression ;
* à l’amélioration de son niveau d’étoiles ;
* à son évolution ;
* à son rôle dans l’équipe ;
* au choix de ses partenaires et aux synergies de la composition.

Chaque créature possède un ensemble fixe de quatre Skills. Ces Skills ne sont ni choisis ni remplacés par le joueur : ils définissent l’identité et les possibilités autour desquelles ses choix de personnalisation s’organisent.

L’objectif est de favoriser la créativité des joueurs et la diversité des builds.

## 14. Équipement

Chaque créature peut équiper un unique équipement.

Les équipements possèdent notamment :

* une qualité ;
* des statistiques générées selon leur qualité ;
* des valeurs aléatoires comprises dans une plage définie ;
* éventuellement un pouvoir spécial.

Le système est inspiré des jeux Hack’n Slash afin d’encourager la recherche d’équipements optimaux.

## 15. Direction artistique

Le style graphique principal repose sur des illustrations 2D de qualité représentant les créatures sous forme de cartes.

À terme, plusieurs styles d’illustrations pourront être proposés, par exemple :

* style classique ;
* style manga ;
* style peinture ;
* style semi-réaliste ;
* style 3D illustrée.

Ces différents styles pourront être organisés en séries de skins de carte.

Les joueurs pourront appliquer librement les skins de carte qu’ils auront débloqués aux cartes de leurs créatures favorites.

Certains skins de carte peuvent être accordés directement comme récompenses sans appartenir à une série distribuée par paquets. Ils doivent rester clairement distingués de ces séries et leur méthode d’obtention doit être indiquée dans le système de collection.

## 16. Modes de jeu envisagés

Le projet prévoit à long terme plusieurs modes de jeu, notamment :

* une histoire principale ;
* des boss personnels ;
* des boss de serveur ;
* une tour infinie ;
* du PvP ;
* des événements temporaires ;
* des guildes ;
* des contenus saisonniers.

Le contenu sera progressivement enrichi au fil du développement.

## 17. Modèle économique

Le projet adopte un modèle **Free-to-Play**.

Les principes fondamentaux sont les suivants :

* les créatures s’obtiennent principalement en jouant ;
* les invocations sont obtenues grâce aux quêtes quotidiennes, aux événements, aux récompenses de jeu et aux différentes activités ;
* aucun achat effectué dans la boutique cosmétique ne doit permettre directement ou indirectement d’obtenir une créature, une invocation ou de la puissance.

La monétisation repose principalement sur une boutique exclusivement consacrée aux contenus cosmétiques.

Deux services de confort limités sont validés en dehors de la boutique cosmétique :

* la redistribution payante des points de caractéristiques déjà gagnés par une créature, sans retour au niveau 1, avec une utilisation limitée et un objet rare obtenu en jouant fournissant le même résultat ;
* l’accès aux vitesses de visualisation accélérées des combats, avec ×1 gratuit, ×2 comme premier palier payant et ×4 comme palier supérieur payant.

Les vitesses accélérées modifient uniquement la restitution du combat en temps réel. Elles ne changent ni la simulation, ni sa seed RNG, ni ses calculs, ses statistiques, ses événements, son résultat, ses récompenses ou son coût en énergie. Le joueur peut acheter directement ×4 ou payer seulement la différence après ×2 ; les prix restent à définir.

Ces services n’autorisent pas la vente de créatures, d’invocations, d’expérience, de points de caractéristiques, d’équipements, d’énergie, de ressources de progression ni d’une augmentation du potentiel maximal d’une créature.

Les skins appartenant aux séries distribuées par paquets s’obtiennent principalement en ouvrant des **paquets de skins de carte**. Ces paquets peuvent être gagnés en jouant ou achetés directement contre de l’argent réel dans la boutique cosmétique.

Pour une même série, les paquets gratuits et payants donnent accès au même ensemble de skins, avec les mêmes probabilités, le même nombre de skins, les mêmes règles de doublons et les mêmes règles d’ouverture. Aucun skin ne doit être réservé exclusivement à la version payante d’un même paquet.

Un paquet contient un nombre fixe de plusieurs skins appartenant à une même série. Tous ses emplacements sont déterminés aléatoirement selon les probabilités associées aux différents niveaux de rareté cosmétique. Les raretés sont visibles et n’accordent aucun avantage de jeu.

Avant un achat, le joueur connaît la série concernée, le nombre de skins contenus, la liste des skins pouvant être obtenus, leurs probabilités, les règles concernant les doublons et, le cas échéant, la durée de disponibilité. Il ne connaît pas les skins précis qu’il recevra avant l’ouverture.

Les séries et leurs paquets peuvent être proposés de manière permanente ou temporaire à l’occasion d’événements. L’achat direct d’un skin précis appartenant à une série distribuée par paquets ne fait pas partie du modèle principal.

La complétion d’une série de skins de carte ne fournira aucun avantage automatique de puissance.

Les ouvertures ne comportent aucune protection contre les doublons ou la malchance. Les doublons de skins de carte sont convertis en une monnaie permanente, provisoirement nommée « monnaie de conversion des doublons ». Chaque rareté possède une valeur de conversion fixe, différente de celle des autres raretés.

Cette monnaie donne accès uniquement à des récompenses cosmétiques. Elle ne permet jamais d’obtenir une créature, une invocation, une ressource de progression, un équipement, un avantage de combat ou une autre forme de puissance.

L’objectif est de financer le développement du jeu tout en préservant un environnement compétitif équitable.

## 18. Contraintes du projet

### Budget

Le budget de développement est volontairement très limité.

Le projet privilégiera :

* les solutions open source ;
* les services disposant d’un Free Tier ;
* une architecture limitant les coûts de développement et d’exploitation.

### Équipe

Le développement est assuré par une équipe de deux personnes :

* un développeur principal responsable du développement, de la technique, du graphisme et de l’intégration ;
* un gestionnaire de projet et directeur artistique.

L’intelligence artificielle est considérée comme un membre à part entière du processus de développement.

Elle sera utilisée afin de :

* accélérer la production ;
* améliorer la qualité ;
* faciliter la recherche et la conception ;
* maintenir une documentation cohérente ;
* assister le développement et les tests.

## 19. Ambition

L’objectif n’est pas simplement de créer un nouveau jeu gacha.

Project Awakening souhaite construire une licence originale de collection de créatures dans laquelle les joueurs prennent plaisir à :

* faire grandir leurs créatures ;
* expérimenter de nouvelles stratégies ;
* créer des builds personnalisés ;
* collectionner des skins de carte ;
* découvrir régulièrement de nouveaux contenus.

Chaque décision prise durant le développement devra contribuer à renforcer cette vision :

> Proposer un jeu durable, riche en possibilités de personnalisation, respectueux de ses joueurs et capable d’évoluer pendant de nombreuses années.
