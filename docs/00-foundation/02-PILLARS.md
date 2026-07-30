# Project Awakening — Piliers fondamentaux

**Statut :** Rédigé — référence actuelle, à maintenir à jour

## 1. Rôle du document

Ce document définit les piliers fondamentaux de **Project Awakening**.

Ces piliers traduisent la vision du projet en principes directeurs. Ils doivent servir de référence pour évaluer les futures décisions de conception, de développement et de production.

Ils ne définissent pas de nouvelles mécaniques et ne remplacent pas le **Game Design Document (GDD)** ni les documents spécialisés. En cas de doute, la vision du projet reste la référence principale.

## 2. Faire grandir ses créatures

### Ce que ce pilier signifie

Le plaisir de jeu doit venir autant, et surtout, du développement des créatures possédées que de l’obtention de nouvelles créatures.

Le joueur construit une relation durable avec ses créatures en les faisant progresser depuis leur forme de base, en développant leur potentiel et en les accompagnant jusqu’à leur forme finale.

### Conséquences sur la conception

* Les créatures doivent progresser individuellement en participant aux combats.
* Une invocation doit donner accès à la forme de base d’une famille, jamais directement à sa forme finale.
* La montée en niveau, les évolutions et l’amélioration des étoiles doivent renforcer progressivement une créature existante.
* Les nouvelles instances d’une famille déjà obtenue peuvent servir de matériaux d’étoiles sans obliger l’instance améliorée à recommencer son évolution.
* Les systèmes de progression doivent valoriser le temps investi dans les créatures déjà possédées.

### Ce que le projet doit éviter

* Réduire le plaisir de progression à l’acquisition répétée de créatures plus rares.
* Rendre rapidement inutiles les créatures dans lesquelles le joueur a investi.
* Permettre d’obtenir directement une forme finale et ainsi contourner le parcours d’évolution.
* Imposer la perte ou la reprise complète de la progression lors de l’amélioration d’une créature.

**Éléments à préciser ultérieurement :**

* Le rythme, les coûts, les ressources et l’équilibrage détaillé de la progression.

## 3. La personnalisation au cœur du gameplay

### Ce que ce pilier signifie

Chaque joueur doit pouvoir façonner ses créatures et ses équipes selon ses propres choix.

Deux joueurs possédant exactement les mêmes créatures doivent pouvoir créer des builds et des compositions différents. La créativité, l’expérimentation et l’optimisation constituent une part essentielle de l’expérience.

### Conséquences sur la conception

* Le joueur doit pouvoir répartir sur chaque créature les points de caractéristiques qu’elle reçoit lors de ses montées de niveau.
* Chaque créature doit posséder exactement quatre Skills prédéfinis : une Ultimate et trois autres Skills formant une combinaison fixe d’Active et de Passive.
* Le joueur ne doit ni choisir ni remplacer les compétences d’une créature. Il personnalise son fonctionnement à travers ses caractéristiques, son équipement, sa progression, son évolution, son niveau d’étoiles et son intégration dans une équipe.
* Les synergies entre les membres d’une équipe doivent encourager plusieurs compositions.
* La conception des créatures doit favoriser une diversité de builds et d’usages.
* La rareté d’une créature ne doit pas être son unique source de valeur.

### Ce que le projet doit éviter

* Proposer des créatures dont le développement ne laisse aucun choix significatif au joueur.
* Faire dépendre la valeur d’une équipe uniquement de la rareté de ses membres.
* Réduire l’optimisation à une progression linéaire identique pour tous.
* Concevoir les systèmes de manière à rendre les différentes possibilités de builds purement anecdotiques.

**Éléments à préciser ultérieurement :**

* Les règles détaillées des caractéristiques, des compétences, des objets, des évolutions, des rôles, des effets de statut et de leur équilibrage.

## 4. La stratégie avant les réflexes

### Ce que ce pilier signifie

La réussite doit récompenser en priorité la préparation de l’équipe, la compréhension des créatures, des éléments et des effets de statut, leurs synergies et les choix de composition.

Les combats sont principalement automatisés afin que la profondeur du jeu repose davantage sur les décisions prises avant et autour du combat que sur l’exécution gestuelle.

### Conséquences sur la conception

* Le joueur doit constituer et optimiser une équipe pouvant réunir jusqu’à six créatures.
* Les rôles, compétences, éléments, effets de statut, objets et synergies doivent influencer la pertinence d’une composition.
* Les effets de statut doivent soutenir des styles de jeu variés, renforcer certaines identités élémentaires et enrichir les interactions entre les créatures.
* Les combats doivent rester rapides et dynamiques, avec une durée moyenne visée de 30 à 60 secondes et un timeout standard de 120 secondes de simulation.
* Les attaques et compétences ordinaires doivent être utilisées automatiquement.
* Le joueur doit pouvoir déclencher manuellement les compétences ultimes ou activer leur déclenchement automatique.
* L’automatisation doit rendre visibles les conséquences des choix de préparation.
* Tout contrôle laissé au joueur pendant un combat doit rester cohérent avec la priorité donnée à la stratégie d’équipe.

### Ce que le projet doit éviter

* Faire des réflexes ou de la précision gestuelle le facteur principal de réussite.
* Transformer les combats en séquences longues qui affaiblissent le rythme recherché.
* Rendre la composition d’équipe secondaire face à la seule puissance brute.
* Concevoir une automatisation qui efface l’impact des choix effectués par le joueur.
* Réduire les effets de statut à des effets accessoires sans influence réelle sur la préparation ou le déroulement des combats.

**Éléments à préciser ultérieurement :**

* Les coefficients exacts de réduction des résistances élémentaires simples et doubles.
* Les valeurs, durées et probabilités des effets de statut, leurs règles individuelles de cumul et de renouvellement, les paramètres des diminishing returns des CC et le périmètre des immunités explicites.

## 5. Une expérience mobile accessible et profonde

### Ce que ce pilier signifie

Project Awakening est conçu exclusivement pour Android et iOS. L’expérience doit être naturelle sur un écran tactile, accessible à un large public et suffisamment profonde pour intéresser durablement les joueurs les plus investis.

L’accessibilité ne doit pas supprimer les possibilités d’optimisation, et la profondeur ne doit pas rendre le jeu inutilement difficile à comprendre ou à utiliser.

### Conséquences sur la conception

* L’ensemble de l’expérience utilisateur doit être pensé pour une utilisation tactile.
* Les interactions et la présentation des informations doivent être adaptées aux contraintes des appareils mobiles.
* Les principes essentiels du jeu doivent rester compréhensibles par un public large.
* Les systèmes de progression, de personnalisation et de composition doivent offrir une profondeur durable aux joueurs qui souhaitent les maîtriser.
* Le rythme des combats et des activités doit rester cohérent avec une expérience mobile.

### Ce que le projet doit éviter

* Concevoir d’abord une expérience destinée à un ordinateur, puis l’adapter superficiellement au mobile.
* Dépendre d’interactions peu adaptées à un écran tactile.
* Confondre profondeur et complexité inutile.
* Simplifier le jeu au point de supprimer l’expérimentation, l’optimisation ou la diversité des builds.

**Éléments à préciser ultérieurement :**

* Les règles détaillées d’interface, d’ergonomie, d’accompagnement du joueur et de parcours utilisateur.

## 6. Un modèle Free-to-Play équitable et respectueux

### Ce que ce pilier signifie

Le modèle économique doit financer le développement sans faire des achats la principale source de puissance.

Les joueurs doivent obtenir principalement les créatures et les invocations grâce au jeu. La boutique est exclusivement cosmétique, et la monétisation repose avant tout sur les skins de carte utilisant des illustrations alternatives, afin de préserver un environnement compétitif équitable.

Trois services de confort sont actuellement validés en dehors de la boutique cosmétique : la redistribution payante de points déjà gagnés sans recommencer la progression en niveaux, les vitesses de visualisation accélérées ×2 et ×4 des combats et les extensions permanentes de capacité de créatures possédées. Aucun ne doit accorder de puissance inaccessible gratuitement ni modifier le résultat ou les récompenses d’un combat.

### Conséquences sur la conception

* Les créatures doivent s’obtenir principalement en jouant.
* Les quêtes quotidiennes, les événements, les récompenses et les différentes activités doivent permettre d’obtenir des invocations.
* Les achats ne doivent jamais devenir la principale source de puissance.
* Les skins de carte et les illustrations alternatives qu’ils utilisent doivent constituer le cœur de la monétisation.
* Les séries de skins de carte doivent être distribuées principalement au moyen de paquets de skins de carte pouvant être gagnés en jouant ou achetés contre de l’argent réel.
* Les paquets gratuits et payants d’une même série doivent suivre les mêmes règles et donner accès aux mêmes skins avec les mêmes probabilités.
* Avant un achat, le joueur doit connaître la série, le nombre de skins contenus, les skins pouvant être obtenus, leurs probabilités, les règles concernant les doublons et la durée de disponibilité éventuelle.
* Les niveaux de rareté des skins de carte doivent rester visibles, strictement cosmétiques et associés à des probabilités clairement communiquées.
* Les ouvertures ne doivent comporter aucune protection contre les doublons ou la malchance.
* Les doublons de skins de carte doivent être convertis en une monnaie cosmétique permanente, chaque rareté possédant une valeur de conversion fixe différente.
* La monnaie issue des doublons doit donner accès uniquement à des récompenses cosmétiques.
* La complétion d’une série de skins de carte ne doit fournir aucun avantage automatique de puissance.
* L’obtention des créatures doit rester indépendante de la boutique cosmétique et des paquets de skins de carte.
* Le joueur doit pouvoir recommencer gratuitement la progression en niveaux d’une créature afin de modifier sa répartition de caractéristiques.
* Un objet rare obtenu en jouant doit permettre de redistribuer les points déjà gagnés sans ramener la créature au niveau 1.
* Un service payant distinct de la boutique cosmétique peut fournir le même résultat immédiat, à condition que son utilisation soit limitée et qu’il ne fournisse aucun avantage de potentiel par rapport aux méthodes gratuites.
* La visualisation des combats doit rester disponible gratuitement en ×1 ; ×2 et ×4 peuvent être achetés comme services de confort, sans modifier le temps de simulation, les calculs, la seed RNG, les statistiques, les événements, le résultat, les récompenses ou le coût en énergie.
* Le joueur doit pouvoir acheter directement ×4 ou payer seulement la différence après l’achat de ×2 ; les prix exacts restent à définir.
* Des extensions payantes peuvent augmenter définitivement la capacité de créatures possédées sans modifier la capacité gratuite calculée pour tous les comptes ni accorder de puissance de combat.
* Les services actuellement validés ne constituent pas une liste définitivement exhaustive ; tout nouveau service exige une décision explicite et le respect des garde-fous Free-to-Play et non-Pay-to-Win.
* La vente d’expérience, de points de caractéristiques, d’énergie, d’équipements ou de ressources de progression doit rester interdite.
* Les décisions économiques doivent préserver l’équité de l’environnement compétitif.

### Ce que le projet doit éviter

* Créer un avantage compétitif principalement accessible par le paiement.
* Rendre les achats indispensables à une progression normale.
* Limiter l’accès aux créatures principalement à des transactions payantes.
* Permettre à un service payant d’accorder des points de caractéristiques supplémentaires, d’augmenter le potentiel maximal ou d’influencer le résultat et les récompenses d’un combat.
* Concevoir des ouvertures cosmétiques dont les doublons seraient dépourvus de valeur.
* Réserver certains skins d’une série à la version payante de son paquet.
* Permettre à une dépense dans la boutique cosmétique de produire directement ou indirectement une créature, une invocation ou de la puissance.
* Présenter un paquet de skins de carte comme une invocation de créature, ou inversement.
* Masquer le coût réel d’un produit derrière une monnaie premium ou une présentation ambiguë.
* Masquer les probabilités, les règles de doublons ou la nature aléatoire d’un paquet payant.
* Sacrifier le respect des joueurs ou l’équité pour accélérer la monétisation.

**Éléments à préciser ultérieurement :**

* Les prix, les probabilités exactes, le nombre de skins par paquet, les quantités, les rythmes d’obtention, les valeurs de conversion propres à chaque rareté et les autres paramètres numériques nécessaires à l’équilibrage économique.
* Le contenu cosmétique détaillé du catalogue de conversion de la monnaie de conversion des doublons.
* Les limites exactes du service payant de réinitialisation, notamment leur portée par compte ou par créature.
* La méthode d’obtention et le rythme de distribution de l’objet rare permettant une réinitialisation sans retour au niveau 1.
* Les prix et la présentation des paliers de vitesse de visualisation ×2 et ×4.

## 7. Une identité originale portée par la collection

### Ce que ce pilier signifie

Project Awakening doit construire une licence originale, fondée sur un multivers riche et sur des familles de créatures inédites.

Les références issues de la culture populaire, des mythologies et des légendes servent de sources d’inspiration. Elles doivent être réinterprétées à travers des codes visuels, narratifs ou symboliques propres au projet, et non reproduites.

La représentation des créatures sous forme de cartes, la collection de créatures et la collection de skins de carte participent pleinement à cette identité.

Le système de collection doit valoriser les éléments obtenus et rendre visible la progression du joueur. Il peut permettre d’identifier les éléments manquants lorsque les règles de découverte du sous-système concerné l’autorisent ; l’encyclopédie des créatures ne révèle pas les familles encore inconnues. Il constitue une expérience à part entière et ne doit pas être réduit à un simple inventaire technique.

### Conséquences sur la conception

* Chaque famille de créatures doit être une création originale.
* Les inspirations doivent être transformées et intégrées à l’identité propre du projet.
* Une famille peut proposer plusieurs branches cohérentes, tandis que chaque instance progresse toujours entre un stade de base, un stade intermédiaire et un stade final.
* Les illustrations 2D de qualité doivent mettre en valeur les créatures sous forme de cartes.
* Le système de collection doit distinguer clairement la collection de créatures de la collection de skins de carte.
* L’encyclopédie des créatures doit valoriser les familles réellement obtenues et enrichir progressivement les formes et branches découvertes sans révéler le contenu encore secret.
* Les skins de carte doivent être organisés en séries cohérentes dont la progression peut être consultée.
* Les joueurs doivent pouvoir appliquer librement les skins de carte qu’ils ont débloqués aux cartes de leurs créatures favorites.

### Ce que le projet doit éviter

* Reproduire directement un personnage ou une créature existante.
* Se contenter d’imiter les œuvres et les jeux qui inspirent le projet.
* Créer des évolutions sans continuité visuelle, narrative ou symbolique au sein d’une famille.
* Traiter les illustrations comme un élément sans importance dans une expérience centrée sur les cartes et leur collection.
* Confondre le système de collection avec l’inventaire consacré aux objets et aux ressources.
* Limiter la collection à l’acquisition sans permettre au joueur de consulter et de valoriser ce qu’il possède.

## 8. Une expérience durable et capable d’évoluer

### Ce que ce pilier signifie

Le projet doit pouvoir s’enrichir pendant plusieurs années sans perdre sa cohérence ni devenir incompatible avec les moyens disponibles.

Sa longévité repose sur un univers riche, une progression profonde, une forte diversité de builds, des mises à jour régulières et l’ajout progressif de nouveaux contenus.

### Conséquences sur la conception

* Les systèmes doivent permettre l’ajout progressif de créatures, de contenus, de builds et d’illustrations.
* Les nouveaux contenus doivent renforcer la progression, la personnalisation et l’expérimentation.
* Les décisions doivent tenir compte d’un budget très limité et d’une équipe humaine de deux personnes.
* Les solutions open source, les services disposant d’un Free Tier et les architectures limitant les coûts doivent être privilégiés.
* L’intelligence artificielle doit soutenir la production, la qualité, la recherche, la conception, la documentation, le développement et les tests.

### Ce que le projet doit éviter

* Concevoir une expérience dépendante d’un renouvellement constant qui ne pourrait pas être soutenu par l’équipe.
* Choisir des solutions dont les coûts de développement ou d’exploitation sont incompatibles avec le budget.
* Ajouter du contenu sans préserver la cohérence de l’univers et des systèmes existants.
* Privilégier des gains à court terme qui compromettraient la capacité du projet à évoluer pendant plusieurs années.

**Éléments à préciser ultérieurement :**

* Le périmètre initial, l’ordre de production, les priorités, les jalons et le rythme des mises à jour.
* Les responsabilités détaillées, les procédures de validation, les outils et les workflows liés à l’intelligence artificielle.

## 9. Principe d’arbitrage

Une décision de conception est cohérente avec Project Awakening si elle renforce plusieurs de ces piliers sans en contredire un autre.

Lorsqu’une décision crée un conflit entre deux piliers, ce conflit doit être signalé et documenté avant validation. Aucune solution ne doit être considérée comme acquise tant qu’elle n’a pas été formalisée dans le document de conception approprié.
