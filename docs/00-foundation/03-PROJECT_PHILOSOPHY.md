# Project Awakening — Philosophie du projet

**Statut :** Rédigé — référence actuelle, à maintenir à jour

## 1. Rôle du document

Ce document définit la philosophie générale de conception de **Project Awakening**.

Il précise la manière dont la vision du projet doit guider les décisions de game design, de progression, d’expérience joueur, de monétisation et de production. Il ne remplace pas le **Game Design Document (GDD)** ni les documents spécialisés, qui devront décrire les mécaniques et leurs paramètres détaillés.

Cette philosophie repose en priorité sur la [vision du projet](./01-VISION.md) et s’appuie également sur les [piliers fondamentaux](./02-PILLARS.md). Ces documents constituent les fondations de référence actuelles du projet et doivent être maintenus à jour lorsque de nouvelles décisions validées les font évoluer.

## 2. Principe directeur

Project Awakening doit proposer une expérience mobile durable, accessible et équitable dans laquelle le joueur prend plaisir à faire grandir ses créatures, à les personnaliser et à construire des équipes adaptées aux contenus rencontrés.

La valeur de l’expérience ne doit pas reposer uniquement sur l’obtention des créatures les plus rares. Elle doit provenir de la progression dans le temps, des choix de build, des synergies et de l’attachement aux créatures développées par le joueur.

Chaque décision doit ainsi être examinée selon sa capacité à :

* renforcer la stratégie et la préparation des équipes ;
* offrir des choix de personnalisation réels ;
* valoriser la progression des créatures déjà possédées ;
* rester accessible sur mobile sans supprimer la profondeur ;
* préserver une relation équitable avec les joueurs ;
* rester compatible avec les moyens humains et financiers du projet ;
* contribuer à une licence originale capable d’évoluer pendant plusieurs années.

## 3. Philosophie du game design

### 3.1. Privilégier la préparation plutôt que les réflexes

Les combats doivent récompenser en priorité les décisions prises lors de la préparation : choix des créatures, composition de l’équipe, répartition des rôles, compétences, équipements, éléments, Effets de combat et synergies.

Le joueur doit gagner parce qu’il comprend ses créatures et construit une équipe pertinente, non parce qu’il exécute plus rapidement une série d’actions. L’automatisation principale des combats sert cette intention en déplaçant le centre de la stratégie vers la préparation et l’optimisation.

Les combats doivent néanmoins rester rapides et dynamiques. L’automatisation ne doit pas rendre les choix du joueur sans conséquence : la composition et le développement des créatures doivent rester déterminants dans le résultat.

Les attaques et les compétences ordinaires sont utilisées automatiquement. Le joueur peut déclencher manuellement les compétences ultimes ou activer leur déclenchement automatique. Cette possibilité d’intervention doit renforcer son implication sans déplacer le cœur de la réussite vers le timing ou les réflexes.

Les Effets de combat constituent un système central du combat. Ils doivent créer des styles de jeu variés, renforcer la profondeur des compétences et des éléments, et donner de l’importance à l’anticipation, aux résistances, aux immunités et aux possibilités de retrait. Ils contribuent ainsi aux piliers existants de stratégie et de personnalisation sans former un pilier fondamental indépendant.

Les décisions de conception doivent donc :

* donner une importance réelle à la composition d’une équipe pouvant réunir jusqu’à six créatures ;
* encourager l’étude des rôles, des compétences, des éléments, des Effets de combat et des synergies ;
* rendre perceptible l’effet des choix effectués avant le combat ;
* maintenir la priorité de la stratégie d’équipe sur l’exécution gestuelle.

Le projet doit éviter :

* de faire des réflexes ou de la précision manuelle le principal facteur de réussite ;
* de réduire les combats à une comparaison de puissance brute ;
* de rendre la préparation secondaire ou artificielle ;
* de proposer une automatisation qui efface l’influence des décisions du joueur ;
* de traiter les Effets de combat comme des effets accessoires sans rôle stratégique réel.

**Éléments à préciser ultérieurement :**

* les ajustements éventuels du taux actuel de résistance élémentaire pendant le balancing ;
* les paramètres exacts des courbes d’Agilité, de Crit et d’Esquive ainsi que les formules de dégâts ;
* la liste des Effets de combat et leurs règles détaillées d’application, de durée, de réapplication, de retrait, de snapshot et d’immunité.

### 3.2. Faire de la personnalisation le cœur de l’expérience

La personnalisation ne doit pas être un système périphérique. Elle constitue le cœur du gameplay et la principale source de diversité entre les joueurs.

Chaque créature possède exactement quatre Skills prédéfinis selon l’une des deux répartitions autorisées : une Active, deux Passive et une Ultimate ; ou deux Active, une Passive et une Ultimate. Le joueur ne choisit pas ces Skills, ne les remplace pas et ne construit pas son build en les sélectionnant dans une liste. Ils définissent l’identité fonctionnelle, le rôle et les synergies potentielles de la créature.

Le joueur développe la créature autour de cet ensemble fixe à travers la répartition de ses caractéristiques, son équipement, sa progression, son évolution, son niveau d’étoiles, ses interactions avec les Effets de combat et son rôle dans l’équipe. Les choix de composition et les synergies entre les membres d’une équipe participent également à cette différenciation.

Deux joueurs possédant les mêmes créatures doivent pouvoir aboutir à des builds et à des équipes différents. Les choix du joueur doivent donc conserver une influence réelle sur la manière dont ses créatures sont utilisées.

Le projet doit éviter :

* une progression entièrement linéaire et identique pour tous ;
* des choix de personnalisation sans effet significatif ;
* une conception dans laquelle la rareté détermine à elle seule la valeur d’une créature ;
* une situation où une seule manière de développer ou d’utiliser une créature rendrait les autres possibilités anecdotiques.

**Éléments à préciser ultérieurement :**

* les règles détaillées des caractéristiques, des compétences, des objets, des évolutions, des rôles, des Effets de combat et de leur équilibrage devront être définies dans le GDD et les documents spécialisés.

## 4. Philosophie de progression

### 4.1. Valoriser le développement dans le temps

Le joueur ne doit jamais obtenir directement la forme finale d’une créature. Une invocation donne accès à la forme de base d’une famille de créatures, que le joueur accompagne ensuite jusqu’à sa forme finale.

L’invocation constitue la voie principale d’obtention des créatures. Certaines créatures peuvent néanmoins être accordées directement par le gameplay, comme créature de départ ou comme récompense narrative, événementielle, de progression ou d’activité. Ces exceptions doivent être explicites et ne doivent pas remettre en cause le rôle central de l’invocation.

La progression individuelle, l’expérience gagnée en combat, les points de caractéristiques reçus par chaque créature lors de ses montées de niveau, leur répartition par le joueur et l’amélioration des étoiles doivent donner de la valeur au temps consacré à chaque créature.

La répartition des points de caractéristiques constitue un choix important et n’est pas librement réversible. Trois voies permettent néanmoins de modifier une répartition :

* une réinitialisation complète gratuite ramène la créature au niveau 1 et lui impose de regagner par le jeu les points liés à ses niveaux ;
* un objet rare obtenu en jouant permet de redistribuer les points déjà gagnés sans revenir au niveau 1 ;
* un service payant strictement limité peut fournir le même résultat immédiat que cet objet, sans accorder de point, d’expérience, de puissance ou de potentiel supplémentaire.

Le service payant ne doit jamais fournir un résultat impossible à obtenir gratuitement. La réinitialisation complète conserve notamment la forme, la branche, les étoiles, l’équipement, le surnom, les tags et les apparences déjà débloquées. La méthode d’obtention de l’objet ainsi que les limites exactes du service restent à définir dans les documents spécialisés.

Une nouvelle obtention d’une famille déjà découverte crée une nouvelle instance individuelle. Les instances d’une même famille peuvent servir de matériaux pour augmenter le niveau d’étoiles d’une autre instance. Ce système doit soutenir la continuité de l’instance améliorée, non annuler l’investissement déjà réalisé dans celle-ci.

### 4.2. Favoriser l’attachement aux créatures

Le plaisir doit venir de la croissance et de l’optimisation des créatures, pas seulement du renouvellement de la collection. Le joueur doit pouvoir conserver, développer et personnaliser ses créatures favorites au fil du temps.

Les illustrations et skins de carte participent également à cet attachement en permettant au joueur d’appliquer les skins de carte débloqués aux cartes des créatures qu’il préfère.

Le système de collection doit prolonger cet attachement en donnant au joueur un espace clair pour consulter ses créatures, parcourir les différentes apparences disponibles et mesurer sa progression de collection. Il doit valoriser les acquisitions déjà réalisées sans réduire l’expérience à la recherche permanente de nouveaux éléments.

Le projet doit éviter :

* de rendre rapidement inutiles les créatures déjà développées ;
* de pousser le joueur à abandonner constamment ses créatures au profit des plus rares ;
* de contourner le parcours d’évolution par l’obtention directe d’une forme finale ;
* d’effacer ou de faire recommencer la progression lors de l’amélioration d’une créature, en dehors d’une réinitialisation complète volontaire utilisée pour modifier sa répartition de caractéristiques.

**Éléments à préciser ultérieurement :**

* le rythme, les coûts, les ressources et l’équilibrage détaillé de la progression ne sont pas encore définis.

## 5. Philosophie de l’expérience joueur

### 5.1. Rester accessible sans devenir superficiel

Project Awakening s’adresse à un public large tout en visant une profondeur suffisante pour les joueurs les plus investis.

L’accessibilité doit permettre de comprendre et d’utiliser les systèmes essentiels sans supprimer les possibilités d’expérimentation. La profondeur doit provenir des interactions entre la progression, les builds, les objets, les compétences, les éléments, les Effets de combat et les compositions d’équipe, et non d’une complexité ajoutée sans bénéfice pour le joueur.

Le projet doit éviter deux extrêmes :

* une complexité inutile qui rendrait les systèmes difficiles à comprendre ;
* une simplification excessive qui supprimerait la créativité, l’optimisation et la diversité des builds.

### 5.2. Concevoir d’abord pour le mobile

Le projet est exclusivement destiné à Android et iOS. L’ensemble de l’expérience utilisateur doit être pensé pour une utilisation tactile.

Les interactions, la présentation des informations et le rythme général doivent rester cohérents avec les contraintes d’un appareil mobile. Le jeu ne doit pas être conçu comme une expérience pour ordinateur adaptée tardivement à un écran tactile.

L’interface doit favoriser des composants réutilisables. Une représentation de créature ou de carte doit pouvoir servir dans plusieurs contextes — notamment le combat, la composition d’équipe, la collection, l’encyclopédie, l’acquisition et la fiche d’une instance — en adaptant les informations visibles sans modifier l’identité fonctionnelle de la créature.

**Éléments à préciser ultérieurement :**

* les règles détaillées d’interface, d’ergonomie, d’accompagnement du joueur et de parcours utilisateur devront être définies dans les documents spécialisés.

### 5.3. Faire de la collection une expérience lisible et valorisante

Le système de collection doit réunir dans un même espace général deux parties clairement séparées : la collection de créatures et la collection de skins de carte. Ces deux catégories ne doivent pas être mélangées dans une liste unique.

Le joueur doit pouvoir consulter et organiser les instances qu’il possède, parcourir les séries de skins de carte et visualiser sa progression. Le système doit également permettre de rechercher et de filtrer les éléments, de consulter les skins disponibles pour une créature et d’appliquer un skin de carte débloqué.

L’encyclopédie des créatures doit rester distincte de la gestion des instances possédées. Elle présente uniquement les familles réellement obtenues, sans révéler leur nombre total, et enrichit progressivement les formes, branches et conditions d’évolution découvertes.

Les skins de carte non débloqués doivent rester consultables avec leur série, leur statut de disponibilité et leur mode général d’obtention lorsque celui-ci peut être communiqué. Certains skins secrets, surprises ou non encore officiellement révélés peuvent rester masqués.

Le système de collection doit rester distinct de l’inventaire : la collection sert à consulter, organiser et valoriser les éléments collectionnables, tandis que l’inventaire est consacré aux objets, aux ressources et aux autres éléments stockables.

**Éléments à préciser ultérieurement :**

* la navigation précise, les filtres et l’ergonomie de l’espace de collection ;
* les règles détaillées de présentation des skins secrets ;
* les règles exactes de calcul de la progression de collection et le traitement détaillé des contenus historiques ;
* la nature des éventuelles reconnaissances non compétitives accordées pour la complétion d’une collection ;
* le nom, la structure et les règles de complétion de la catégorie consacrée aux skins obtenus hors paquets.

**Question ouverte :**

* la compatibilité des skins de carte avec une créature, une forme précise ou plusieurs formes compatibles.

### 5.4. Distinguer les parcours cosmétiques et l’obtention des créatures

L’ouverture d’un paquet de skins de carte et l’invocation d’une créature constituent deux expériences indépendantes.

Le parcours cosmétique part d’une récompense de gameplay ou de la boutique cosmétique, conduit à l’ouverture d’un paquet de skins de carte et permet d’obtenir uniquement des skins de carte.

Le parcours des créatures part principalement de récompenses et de ressources obtenues en jouant, conduit à une invocation de créature et permet d’obtenir une créature jouable sous sa forme de base. Narrativement, l’invocation établit ou révèle un lien avec une manifestation vivante, puis la stabilise ; elle ne crée pas artificiellement une nouvelle forme de vie.

Certaines créatures peuvent être obtenues directement par le gameplay comme exceptions explicitement documentées. Un lien est également établi dans ce cas, sans que cette obtention directe devienne une invocation.

Ces parcours doivent employer des terminologies, des ressources, des interfaces, des animations et des règles économiques distinctes. Une ouverture cosmétique ne doit jamais donner de créature, et une invocation de créature ne doit pas être présentée comme l’ouverture d’un paquet cosmétique.

Une ressource générale principale d’invocation est utilisée dans le modèle initial. Elle doit être obtenue principalement grâce au mode Histoire, aux quêtes journalières, aux activités, aux récompenses de progression et aux événements. Elle reste entièrement séparée de l’économie cosmétique.

**Éléments à préciser ultérieurement :**

* la présentation artistique de l’invocation, qui pourra éventuellement utiliser un œuf, une éclosion, un rituel, un portail ou une autre représentation cohérente avec l’établissement, la révélation et la stabilisation du lien ;
* les écrans, animations et parcours détaillés des deux systèmes ;
* le nom, la représentation, les quantités et le rythme d’obtention de la ressource générale d’invocation.

## 6. Philosophie de monétisation

### 6.1. Financer le projet sans faire de l’achat la principale source de puissance

Project Awakening adopte un modèle Free-to-Play. Les créatures doivent s’obtenir principalement en jouant, et les invocations doivent être accessibles grâce aux quêtes quotidiennes, aux événements, aux récompenses et aux différentes activités.

La boutique est exclusivement consacrée aux contenus cosmétiques. Elle ne vend aucune créature, aucune invocation, aucun avantage de combat et aucune progression de puissance.

Les services de confort actuellement validés, strictement encadrés et distincts de la boutique cosmétique, sont :

* la redistribution payante des points de caractéristiques déjà gagnés par une créature sans la ramener au niveau 1 ; son utilisation doit être limitée et un objet rare obtenu en jouant doit permettre le même résultat ;
* les vitesses de visualisation accélérées ×2 et ×4 des combats, tandis que ×1 reste gratuit ;
* les extensions permanentes de capacité de créatures possédées ;
* la possibilité d’acheter des sacs augmentant uniquement la capacité de l’inventaire, également accessibles par le gameplay et sans puissance exclusive.

La réinitialisation complète depuis le niveau 1 reste accessible gratuitement sans objet. Les vitesses accélérées changent uniquement la restitution en temps réel : elles ne modifient ni les 120 secondes de simulation, ni les calculs, la seed RNG, les statistiques, les événements, le résultat, les récompenses ou le coût en énergie.

Ces services n’autorisent pas la vente de créatures, d’invocations, d’expérience, de points de caractéristiques, d’équipements, d’énergie, de ressources de progression ou de puissance. Leur liste n’est pas définitivement exhaustive : tout ajout futur exige une décision explicite et doit respecter les mêmes garde-fous.

Les skins appartenant aux séries distribuées par paquets sont principalement obtenus grâce à des paquets de skins de carte. Ces paquets peuvent être gagnés en jouant ou achetés directement contre de l’argent réel dans la boutique cosmétique.

Pour une même série, les paquets gratuits et payants utilisent le même ensemble de skins, les mêmes probabilités, le même nombre de skins, les mêmes règles de doublons et les mêmes règles d’ouverture. La méthode d’obtention du paquet constitue leur seule différence.

Chaque paquet contient un nombre fixe de plusieurs skins. Tous ses emplacements sont déterminés aléatoirement parmi les skins de la série, selon les probabilités associées à leurs niveaux de rareté visibles. Aucun emplacement, aucune rareté et aucun skin non possédé ne sont automatiquement garantis.

Avant l’achat, le joueur doit connaître la série concernée, le nombre de skins contenus, la liste des skins pouvant être obtenus, leurs probabilités, les règles de doublons et la durée de disponibilité éventuelle. Il ne connaît pas le résultat précis de l’ouverture.

L’achat direct d’un skin précis appartenant à une série distribuée par paquets ne fait pas partie du modèle principal. Certains skins peuvent cependant être accordés directement par le gameplay lorsqu’ils restent extérieurs à ces séries et sont clairement identifiés comme tels.

Les invocations et les ressources de progression ne sont pas vendues dans la boutique cosmétique. Une dépense cosmétique ne doit jamais permettre directement ou indirectement d’obtenir une créature, une invocation ou de la puissance.

Les doublons de skins de carte sont convertis en une monnaie permanente provisoirement nommée « monnaie de conversion des doublons ». Chaque rareté possède une valeur de conversion fixe différente. Cette monnaie donne accès uniquement à des récompenses cosmétiques.

### 6.2. Préserver l’équité et le respect des joueurs

Une décision économique doit être évaluée non seulement selon sa capacité à financer le développement, mais aussi selon son impact sur la progression, la transparence et l’environnement compétitif.

Aucun achat effectué dans la boutique cosmétique ne doit produire directement ou indirectement un avantage de progression ou de combat.

Le service payant de réinitialisation ne doit pas augmenter la puissance maximale accessible, accorder des points supplémentaires ni remplacer l’existence de méthodes gratuites. Les vitesses accélérées ne doivent jamais influencer la simulation, le résultat ou les récompenses d’un combat. Une extension de capacité ne doit modifier ni la puissance d’une créature ni la capacité gratuite attribuée à tous les comptes.

La présentation des séries de skins de carte doit permettre au joueur de comprendre et d’apprécier ce qu’il a obtenu sans transformer la complétion cosmétique en obligation de puissance. La complétion d’une série ne doit fournir aucun avantage automatique de puissance.

Le projet doit éviter :

* de rendre les achats indispensables à une progression normale ;
* de réserver principalement la puissance ou les créatures aux joueurs payants ;
* de créer un avantage compétitif reposant avant tout sur le paiement ;
* de supprimer la valeur d’une ouverture lorsqu’elle contient un doublon de skin de carte ;
* de différencier les probabilités, le contenu ou les règles fondamentales des paquets gratuits et payants d’une même série ;
* de masquer le coût réel d’un produit ;
* de masquer la nature aléatoire, les probabilités ou les règles de doublons d’un paquet ;
* de créer une pression artificielle ou ambiguë autour des offres temporaires ;
* de compromettre l’équité afin d’accélérer la monétisation.

**Éléments à préciser ultérieurement :**

* les prix, les probabilités exactes, le nombre de skins par paquet, les quantités, les rythmes d’obtention, les valeurs de conversion propres à chaque rareté et les seuils d’évaluation ;
* le contenu cosmétique détaillé du catalogue utilisant la monnaie de conversion des doublons.

### 6.3. Évolutions non validées

Les services de confort actuellement validés sont la redistribution limitée des points, les vitesses de visualisation ×2 et ×4, les extensions permanentes de capacité de créatures et la possibilité d’acheter des sacs d’inventaire également accessibles par le gameplay. Les publicités, les passes, les abonnements, la monnaie premium, l’achat direct d’invocations et tout autre service non explicitement validé ne font pas partie du modèle initial.

Leur éventuelle introduction après le lancement nécessitera une nouvelle décision explicite et une vérification de leur compatibilité avec les principes d’équité, de transparence et de respect des joueurs.

Une éventuelle décision future autorisant l’achat direct d’invocations devra en outre rester extérieure à la boutique cosmétique et préserver la séparation entre l’économie cosmétique et l’obtention des créatures.

**Questions ouvertes :**

* l’introduction éventuelle de publicités après le lancement ;
* la création éventuelle d’un passe ou d’un abonnement après la définition des saisons et des capacités de production ;
* l’introduction éventuelle d’une monnaie premium répondant à un besoin réel sans masquer le coût des produits ;
* l’autorisation future d’autres services de confort ou d’achats directs d’invocations après définition et équilibrage des systèmes concernés.

## 7. Philosophie de production

### 7.1. Adapter le périmètre aux moyens disponibles

Le projet est développé par une équipe humaine de deux personnes avec un budget volontairement très limité. Les décisions de conception, de contenu et de technologie doivent rester compatibles avec cette réalité.

L’ambition d’une licence durable doit être poursuivie par un enrichissement progressif du jeu. Les systèmes doivent pouvoir accueillir de nouvelles créatures, de nouveaux builds, de nouvelles illustrations et de nouveaux contenus au fil du développement sans imposer des coûts incompatibles avec les moyens disponibles.

Le projet doit privilégier :

* les solutions open source ;
* les services disposant d’un Free Tier ;
* les architectures limitant les coûts de développement et d’exploitation ;
* des choix dont la production et la maintenance peuvent être assumées dans la durée.

Le projet doit éviter :

* un périmètre dont la production régulière ne pourrait pas être soutenue par l’équipe ;
* des solutions trop coûteuses à développer, exploiter ou maintenir ;
* l’ajout de contenu sans cohérence avec les systèmes et l’univers existants ;
* des décisions à court terme qui compromettraient l’évolution du jeu sur plusieurs années.

**Éléments à préciser ultérieurement :**

* l’ordre de production, les priorités, les jalons et le rythme des mises à jour devront être définis dans les documents de production.

### 7.2. Utiliser l’intelligence artificielle comme outil de production

L’intelligence artificielle fait partie intégrante du processus de développement. Elle doit servir à accélérer la production, améliorer la qualité, faciliter la recherche et la conception, maintenir une documentation cohérente, et assister le développement et les tests.

Le projet cherche à maximiser l’autonomie de développement avec Codex et les autres agents IA utilisés sur le repository. Autant que raisonnablement possible, le code, les données, les configurations, les interfaces, les composants de cartes, les scènes, les shaders, les VFX, les animations et les logiques de gameplay et de présentation doivent pouvoir être lus, créés, modifiés, maintenus, versionnés, testés et vérifiés directement depuis le repository.

Les choix de production doivent éviter les dépendances inutiles à des workflows exigeant en permanence des compétences manuelles très spécialisées ou des opérations difficiles à reproduire depuis le repository. Cet objectif n’interdit ni les assets externes, ni l’intervention d’un artiste humain, ni une opération manuelle justifiée, et n’impose pas que tout soit produit par Codex.

Son utilisation ne remplace pas les responsabilités humaines déjà définies dans le projet. Le développeur principal reste responsable du développement, de la technique, du graphisme et de l’intégration. Le gestionnaire de projet et directeur artistique conserve ses responsabilités de gestion et de direction artistique.

Les résultats produits avec l’aide de l’IA doivent rester soumis à une vérification humaine et à la documentation du projet. Une suggestion générée par une IA ne constitue pas, à elle seule, une décision validée.

Le projet doit éviter :

* d’intégrer une proposition de l’IA comme une décision définitive sans validation ;
* d’utiliser l’IA pour contourner la vision, les piliers ou les contraintes documentées ;
* de confondre accélération de la production et extension incontrôlée du périmètre ;
* d’adopter sans nécessité un workflow dont les étapes essentielles ne peuvent pas être reproduites, testées ou vérifiées depuis le repository ;
* de déléguer à l’IA la responsabilité finale des choix de conception, de direction artistique ou de production.

**Éléments à préciser ultérieurement :**

* les responsabilités détaillées, les procédures de validation, les outils et les workflows liés à l’IA devront être définis dans la documentation spécialisée.

## 8. Choix contraires à la philosophie du projet

Une décision contredit la philosophie de Project Awakening si elle conduit notamment à :

* privilégier les réflexes au détriment de la préparation et de la stratégie d’équipe ;
* réduire les créatures à leur rareté ou à une progression identique pour tous ;
* rendre les choix de build sans conséquence réelle ;
* dévaloriser les créatures dans lesquelles le joueur a investi ;
* supprimer la profondeur au nom de l’accessibilité, ou rendre le jeu inutilement complexe ;
* concevoir une expérience qui ne serait pas adaptée au mobile et au tactile ;
* faire du paiement la principale voie d’accès à la puissance ;
* confondre la collection cosmétique avec une progression de puissance ;
* réduire le système de collection à un inventaire technique ou à une simple liste d’acquisitions ;
* reproduire directement les œuvres dont le projet s’inspire au lieu de construire une identité originale ;
* adopter un périmètre ou des coûts incompatibles avec la taille de l’équipe et le budget ;
* laisser un outil d’intelligence artificielle transformer une proposition en décision sans validation humaine.

Lorsqu’une décision semble renforcer un principe tout en en affaiblissant un autre, le conflit doit être signalé et documenté avant validation.
