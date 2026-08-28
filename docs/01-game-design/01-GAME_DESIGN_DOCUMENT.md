# Project Awakening — Game Design Document

**Statut :** Rédigé — référence actuelle, à maintenir à jour

## 1. Rôle et périmètre du document

### 1.1. Rôle du GDD

Ce document constitue la vue d’ensemble centrale du fonctionnement de **Project Awakening**.

Il décrit :

* la fantasy principale vécue par le joueur ;
* son rôle fonctionnel dans l’expérience ;
* ses objectifs à différents horizons ;
* les principales boucles de gameplay ;
* l’enchaînement entre gestion, activité, combat, résultat, récompense et progression ;
* la fonction des grands systèmes et leurs relations ;
* le rythme général attendu sur mobile ;
* le périmètre fonctionnel d’une première vertical slice.

Le GDD explique ce que le joueur fait, pourquoi il le fait, dans quel ordre et comment les systèmes échangent leurs résultats.

Il ne remplace pas les documents spécialisés. Ceux-ci devront définir les règles internes, les paramètres, les données, les exceptions et l’équilibrage détaillé de chaque domaine.

### 1.2. Références de fondation

Le présent document applique en priorité :

* la [vision du projet](../00-foundation/01-VISION.md) ;
* les [piliers fondamentaux](../00-foundation/02-PILLARS.md) ;
* la [philosophie du projet](../00-foundation/03-PROJECT_PHILOSOPHY.md) ;
* le [cadre de monétisation](../00-foundation/04-MONETIZATION.md) ;
* le [glossaire officiel](../00-foundation/05-GLOSSARY.md).

Il ne répète pas l’intégralité de ces fondations. Il en traduit les décisions en une structure fonctionnelle globale.

Pour les aspects narratifs qui soutiennent le rôle du joueur et l’acquisition des créatures, il applique également les fondations définies dans le [document de lore](../02-world/01-LORE.md).

### 1.3. Répartition avec les documents spécialisés

Le GDD définit notamment :

* la promesse de gameplay ;
* les boucles globales ;
* le rôle de chaque grand système ;
* les entrées et sorties entre les systèmes ;
* les principes généraux d’accès, de progression, de victoire, de défaite et de récompense ;
* les statuts de périmètre des modes de jeu ;
* la cible fonctionnelle de la vertical slice.

Les futurs documents spécialisés définiront notamment :

* le déroulement et les règles détaillées du combat ;
* les modèles de créatures et d'adversaires ;
* les compétences, éléments et Effets de combat ;
* les évolutions et équipements ;
* les invocations de créatures ;
* les courbes, coûts, ressources et règles détaillées de progression ;
* la collection ;
* les modes de jeu, quêtes, événements, hauts faits et fonctions sociales ;
* les écrans et parcours UI.

Lorsqu’une décision spécialisée modifie une boucle ou une relation globale, le GDD doit être mis à jour. Lorsqu’une décision modifie un principe de fondation, les fondations concernées doivent également être synchronisées.

### 1.4. Éléments exclus du GDD

Ce document ne définit pas :

* les formules de dégâts ou de progression ;
* les coefficients et la table détaillée des résistances élémentaires ;
* les coûts en énergie ;
* les temps de régénération ;
* les valeurs d’expérience ;
* les probabilités d’invocation ou d’ouverture ;
* les quantités de récompenses ;
* les limites numériques précises ;
* les listes exhaustives de créatures, compétences, Effets de combat, équipements ou quêtes ;
* le détail des écrans ;
* l’architecture technique ;
* le calendrier de production.

## 2. Résumé de l’expérience

### 2.1. Fantasy principale

La fantasy principale de Project Awakening est :

> Faire grandir, développer et révéler le potentiel de ses créatures.

Elle est soutenue par deux fantasies secondaires :

1. construire et maîtriser plusieurs équipes spécialisées ;
2. découvrir de nouvelles créatures, de nouveaux mondes et de nouveaux défis.

La collection et les invocations apportent de nouvelles possibilités de composition. Elles servent le développement à long terme des créatures et la création d’équipes réfléchies plutôt qu’une recherche permanente de rareté.

### 2.2. Rôle du joueur

Le joueur possède un rôle fictionnel légèrement défini. Il fait partie des humains capables de créer un lien avec les créatures et de stabiliser leur existence. Fonctionnellement, il les accompagne, provoque les conditions permettant à leurs potentiels d'évolution de s'exprimer et dirige plusieurs équipes ; l'humain ne façonne pas directement ces potentiels dans le lore.

Le nom provisoire de ce rôle est **Éveilleur**. Ce nom ne constitue pas encore un terme définitif de l’univers.

Le joueur n’est ni le seul humain possédant cette aptitude ni l’élu unique de l’univers. Le maintien de l’équilibre entre les forces décrites par le lore constitue une direction narrative et ne valide aucun système de choix moraux, d’embranchements ou de fins multiples.

Il choisit personnellement d'agir comme protecteur et de protéger les autres sans appartenir obligatoirement à une faction. Le titre provisoire d'Éveilleur décrit une aptitude, pas un camp ou une supériorité morale.

Le rôle fonctionnel du joueur consiste à :

* obtenir des créatures ;
* les faire progresser ;
* répartir leurs points de caractéristiques ;
* gérer leurs équipements ;
* construire et enregistrer plusieurs équipes ;
* sélectionner l’équipe adaptée à une activité ;
* comprendre les défis rencontrés ;
* analyser les résultats ;
* améliorer ses créatures et ses compositions.

### 2.3. Promesse centrale

Le joueur doit avoir le sentiment que :

* le temps consacré à ses créatures conserve de la valeur ;
* ses choix de caractéristiques, d’équipement et de composition produisent des différences visibles ;
* une nouvelle créature ouvre des possibilités sans rendre automatiquement les précédentes inutiles ;
* plusieurs équipes peuvent répondre à des défis différents ;
* la préparation reste plus importante que les réflexes ;
* le jeu respecte les contraintes de sessions mobiles sans supprimer la profondeur.

## 3. Expérience joueur recherchée

### 3.1. Hiérarchie des motivations

Les motivations principales sont, par ordre de priorité :

1. l’attachement et la croissance des créatures ;
2. la création, la maîtrise et l’optimisation de plusieurs équipes ;
3. la progression dans les mondes et le déblocage de nouvelles fonctionnalités ;
4. la découverte de nouvelles créatures et de nouveaux défis ;
5. la collection et la complétion ;
6. la compétition, la reconnaissance et la dimension sociale.

La compétition et les systèmes sociaux sont des extensions ultérieures. Ils ne doivent pas définir la première expérience du jeu.

### 3.2. Stratégie avant les réflexes

La réussite doit provenir principalement :

* de la compréhension des créatures ;
* de la composition d’équipe ;
* de la répartition des rôles ;
* des caractéristiques ;
* des équipements ;
* des compétences fixes ;
* des éléments ;
* des Effets de combat ;
* des synergies.

Le contrôle laissé au joueur pendant le combat offre une implication limitée. Il ne doit pas transformer le timing ou la précision gestuelle en facteur principal de réussite.

### 3.3. Personnalisation autour d’identités fixes

Chaque créature possède une identité fonctionnelle déterminée notamment par :

* son ensemble fixe de quatre Skills, répartis en une Active, deux Passive et une Ultimate ou en deux Active, une Passive et une Ultimate ;
* son ou ses éléments ;
* son profil de caractéristiques ;
* son rôle et ses synergies potentielles.

Le joueur ne choisit ni ne remplace les compétences de la créature. Il construit son build autour de ce profil grâce :

* à la répartition des points de caractéristiques ;
* à l’équipement ;
* à la progression ;
* à l’amélioration du niveau d’étoiles ;
* à l’évolution ;
* au choix des partenaires ;
* au rôle attribué dans une composition.

Deux joueurs possédant les mêmes créatures doivent pouvoir obtenir des résultats et des usages différents grâce à ces choix.

### 3.4. Accessibilité et profondeur

Les règles essentielles doivent rester compréhensibles par un public large. La profondeur doit provenir des interactions entre les systèmes, non d’une multiplication inutile des opérations ou des ressources.

L’interface et l’accompagnement doivent :

* introduire les systèmes progressivement ;
* présenter les informations nécessaires à la préparation ;
* permettre des actions courtes sur écran tactile ;
* éviter d’imposer une gestion complète avant chaque combat ;
* laisser aux joueurs investis la possibilité d’optimiser plusieurs équipes.

## 4. Modèle fonctionnel global

### 4.1. Principaux ensembles

Le fonctionnement global repose sur les ensembles suivants :

* les créatures possédées ;
* leur progression et leur personnalisation ;
* les équipes enregistrées ;
* les activités et le mode Histoire ;
* les combats ;
* les résultats et récompenses ;
* la progression du compte ;
* l’énergie ;
* les invocations de créatures ;
* la collection ;
* les contenus cosmétiques.

### 4.2. Circulation générale

La circulation principale est la suivante :

> Activités et récompenses → progression des créatures et du compte → amélioration des builds et des équipes → accès ou progression dans de nouvelles activités → nouvelles récompenses.

L’invocation de créature alimente cette circulation en ouvrant de nouvelles possibilités de composition.

La collection valorise ce que le joueur possède et rend sa progression visible. L’identification des éléments manquants dépend des règles de découverte de chaque sous-système : l’encyclopédie des créatures ne révèle pas les familles encore inconnues. La collection ne remplace ni la gestion des créatures ni l’inventaire.

La personnalisation cosmétique renforce l’attachement et la collection sans produire de puissance.

### 4.3. Deux rythmes complémentaires

Le jeu alterne :

* des moments d’activité rapides, centrés sur la sélection d’une équipe et le combat ;
* des moments de gestion, centrés sur la progression, l’équipement et l’optimisation des équipes.

Le joueur ne doit pas être obligé d’ouvrir tous les systèmes de gestion entre deux niveaux.

### 4.4. Représentation des créatures

Project Awakening est un jeu 2D dans lequel les créatures sont principalement représentées sous forme de cartes.

Une même base de représentation doit pouvoir servir dans le combat, la gestion des créatures, la composition d’équipe, la collection, l’encyclopédie, l’acquisition et les fiches d’instance. Les informations visibles peuvent varier selon le contexte sans modifier l’identité fonctionnelle de la créature.

L’apparence d’une forme peut être principalement matérialisée par une illustration statique. Les règles artistiques et visuelles détaillées relèvent des documents du dossier [`03-art`](../03-art/).

## 5. Objectifs du joueur

### 5.1. Objectifs immédiats

Pendant une activité, le joueur cherche à :

* comprendre le défi ;
* choisir une équipe préparée adaptée ;
* remporter le combat ;
* obtenir les récompenses annoncées ;
* identifier les forces et faiblesses de sa composition.

### 5.2. Objectifs à court terme

À court terme, le joueur cherche à :

* faire progresser ses créatures actives ;
* répartir de nouveaux points de caractéristiques ;
* améliorer ou remplacer un équipement ;
* obtenir une nouvelle créature ;
* compléter progressivement son groupe initial ;
* franchir les prochains niveaux du mode Histoire ;
* accomplir éventuellement ses quêtes journalières.

### 5.3. Objectifs à moyen terme

À moyen terme, le joueur cherche à :

* disposer d’une équipe complète de six créatures ;
* créer plusieurs équipes enregistrées ;
* spécialiser ses compositions ;
* faire évoluer ses créatures ;
* améliorer leur niveau d’étoiles ;
* débloquer de nouvelles fonctionnalités et activités ;
* adapter ses équipes à des boss et contraintes différents.

### 5.4. Objectifs à long terme

À long terme, le joueur cherche à :

* développer ses créatures favorites sur une progression très longue ;
* maîtriser plusieurs équipes spécialisées ;
* progresser toujours plus loin dans les mondes du mode Histoire ;
* obtenir des créatures ouvrant de nouvelles synergies ;
* enrichir l’encyclopédie des créatures ;
* compléter des séries de skins de carte ;
* participer ultérieurement à des contenus compétitifs ou communautaires.

## 6. Boucles principales

### 6.1. Boucle de gestion et de préparation

> Obtenir ou développer des créatures → répartir leurs caractéristiques → gérer leurs équipements → construire et enregistrer plusieurs équipes spécialisées → améliorer ces équipes au fil du temps.

Cette boucle est réalisée en amont, entre les activités ou pendant une session consacrée à la progression.

Le joueur doit pouvoir :

* consulter ses créatures ;
* comprendre leurs compétences fixes et leur rôle ;
* répartir leurs points de caractéristiques ;
* attribuer ou remplacer leur équipement ;
* créer une équipe pouvant réunir jusqu’à six créatures ;
* modifier et supprimer une équipe ;
* nommer librement chaque équipe ;
* conserver plusieurs compositions préparées.

### 6.2. Boucle d’activité

> Choisir un objectif ou une activité → comprendre le défi → sélectionner une équipe déjà préparée → combattre → analyser le résultat → obtenir les récompenses → faire progresser ses créatures et son compte → poursuivre, retenter ou retourner à la gestion.

Le joueur peut modifier sa composition avant le combat. Cette modification reste facultative et ne doit pas être imposée avant chaque niveau.

### 6.3. Boucle d’amélioration après un résultat

Après une victoire ou une défaite, le joueur peut :

* poursuivre avec la même équipe ;
* sélectionner une autre équipe enregistrée ;
* retourner à la gestion ;
* modifier un équipement ;
* modifier une composition ;
* investir de nouveaux points de caractéristiques lorsqu’il en possède ;
* retenter le défi afin d’observer l’impact de ses choix.

## 7. Boucle d’une session mobile

### 7.1. Structure hybride

Une session ne suit pas une liste d’actions obligatoire.

Le joueur peut librement :

* progresser dans le mode Histoire ;
* gérer ses créatures ;
* préparer ses équipes ;
* participer à une activité particulière ;
* accomplir une quête journalière ;
* poursuivre un objectif personnel.

### 7.2. Rythme visé

Une session normale vise environ **10 à 30 minutes**.

Le joueur doit également pouvoir :

* accomplir quelques actions utiles en moins de dix minutes ;
* répartir des points ou modifier un équipement lors d’une connexion courte ;
* jouer plus longtemps lorsqu’il possède de l’énergie accumulée ;
* participer à des activités dont la durée diffère du rythme ordinaire.

Cette cible décrit un rythme général et ne fixe pas la durée obligatoire de chaque activité.

### 7.3. Quêtes journalières

Chaque jour, le joueur reçoit trois quêtes journalières aléatoires tirées dans une liste prédéfinie.

Elles doivent :

* encourager le retour au jeu ;
* varier les activités ;
* utiliser uniquement des fonctionnalités déjà débloquées ;
* rester réalisables sans durée excessive ;
* accorder des récompenses ayant un effet sur la progression ;
* rester facultatives pour la progression normale.

Une journée manquée fait perdre l’occasion de réaliser les quêtes de cette journée, mais ne retire aucune progression générale et ne supprime pas l’énergie accumulée.

Aucune série de connexion punitive n’est prévue.

**Éléments à préciser ultérieurement :**

* La liste des quêtes possibles.
* Leurs catégories, conditions et récompenses.
* Leurs règles de sélection et de renouvellement.
* Les protections empêchant de proposer une quête inaccessible.

## 8. Mode Histoire

### 8.1. Colonne vertébrale initiale

Le mode Histoire constitue la principale chaîne de progression PvE du jeu.

Il ne repose pas sur une campagne scénarisée traditionnelle ni sur une longue narration entre chaque niveau.

Il est organisé en :

* mondes ;
* niveaux ;
* combats ;
* boss ou jalons réguliers.

### 8.2. Structure des niveaux

Un niveau ordinaire correspond généralement à un combat court.

Les séries de combats successifs peuvent être réservées :

* aux boss ;
* aux défis spéciaux ;
* aux activités avancées ;
* aux modes dont l’identité nécessite plusieurs combats.

### 8.3. Progression et rejouabilité

Le mode Histoire doit :

* augmenter progressivement sa difficulté ;
* rester rejouable ;
* permettre de répéter certains niveaux pour leurs récompenses ;
* soutenir le farming de Sources d'énergie, de composants et d'autres récompenses pertinentes ;
* servir de principale source de déblocage des fonctionnalités ;
* pouvoir recevoir de nouveaux mondes et niveaux au fil du développement ;
* soutenir une progression très longue sans exiger une narration détaillée pour chaque ajout.

La puissance d’équipe peut servir d’indication de difficulté. Elle ne constitue pas un verrou systématique.

### 8.4. Informations avant un niveau

Pour un contenu ordinaire, le joueur doit connaître suffisamment d’informations pour sélectionner une équipe pertinente :

* les éléments des adversaires qui en possèdent ;
* les principales menaces ;
* les Effets de combat importants ;
* les conditions particulières ;
* les récompenses principales ;
* les restrictions éventuelles.

Un boss ou défi peut conserver une mécanique secrète. Le jeu doit alors signaler qu’une mécanique inconnue est présente. La première défaite ne doit pas devenir une étape systématiquement obligatoire pour comprendre un niveau.

## 9. Onboarding et déblocages

### 9.1. Introduction

Le début du jeu comprend une courte introduction qui :

* présente le contexte général ;
* introduit le rôle du joueur ;
* fournit quelques éléments de lore ;
* permet de choisir une première créature parmi trois ;
* conduit rapidement au premier combat.

Le nom, l’identité et les caractéristiques exactes des trois créatures de départ restent à définir.

### 9.2. Progression du groupe initial

Le joueur commence avec une seule créature.

Pendant cette phase, il combat temporairement avec un groupe incomplet. Une équipe au sens complet du système comporte six créatures.

Les premières étapes accordent progressivement :

* de l’expérience ;
* des montées de niveau ;
* des points de caractéristiques ;
* une première ressource générale d’invocation ;
* une invocation contrôlée ou garantie ;
* de nouvelles créatures ;
* les emplacements et fonctions nécessaires à une équipe complète.

Le joueur doit atteindre suffisamment rapidement une équipe complète de six afin de découvrir le cœur stratégique du jeu.

### 9.3. Tutoriels contextualisés

Les fonctionnalités sont principalement débloquées par des jalons du mode Histoire.

Chaque nouvelle fonctionnalité doit être accompagnée d’un tutoriel court, présenté au moment où le joueur peut l’utiliser.

Les premiers jalons introduisent progressivement :

* le combat ;
* l’expérience des créatures ;
* les niveaux de créature ;
* la répartition des caractéristiques ;
* les invocations de créatures ;
* la composition d’équipe ;
* les synergies ;
* les équipements ;
* la gestion de plusieurs équipes ;
* les évolutions ;
* les activités spéciales.

Les niveaux exacts, l’ordre détaillé et les récompenses de ces jalons restent à définir.

## 10. Créatures, builds et équipes

### 10.1. Créatures

Chaque créature est une entité jouable représentée dans l’interface par une carte de créature.

Le système distingue :

* la **famille**, qui porte notamment la rareté, le numéro d’encyclopédie, le lore général et l’identité de la Basic Attack et des quatre Skills ;
* la **forme**, qui porte notamment l’apparence, les éléments, le profil de caractéristiques principales de base, les rôles suggérés, le profil offensif et les versions des capacités ;
* l’**instance possédée**, individu persistant développé par le joueur ;
* le **stade d’évolution**, parmi les trois stades parcourus par chaque instance ;
* la **branche d’évolution**, chemin définitif suivi par l’instance dans l’arbre de sa famille.

Une famille peut contenir de nombreuses formes et branches. Chaque instance parcourt cependant exactement trois stades et conserve sa progression individuelle à travers ses évolutions.

La rareté appartient à la famille et reste identique pour toutes ses formes et branches. Les raretés validées sont Rare, Épique, Légendaire et Mythique. Elles représentent principalement l’obtention et la collection, non une hiérarchie automatique de puissance.

Il n’existe aucun IV ni variation aléatoire cachée des valeurs intrinsèques : deux instances d’une même forme possèdent les mêmes valeurs de base avant les choix de progression du joueur.

### 10.2. Compétences fixes

L’ensemble de Skills comprend exactement :

* une Ultimate ;
* une Active et deux Passive, ou deux Active et une Passive.

Ces deux répartitions sont les seules autorisées. Chaque créature possède toujours au moins une Active et au moins une Passive.

Lorsqu’une créature est obtenue, cet ensemble est déjà déterminé.

Le joueur :

* ne choisit pas les compétences ;
* ne les remplace pas ;
* ne sélectionne pas un ensemble alternatif ;
* ne construit pas le build à partir d’une liste de compétences.

La Basic Attack et les quatre Skills définissent l’identité fonctionnelle de la famille et conservent leur continuité conceptuelle à travers ses évolutions. La catégorie de chaque Skill reste inchangée. Une nouvelle forme peut enrichir une capacité ou transformer fortement sa fonction lorsque cette transformation reste cohérente avec l’évolution de la créature.

### 10.3. Build de créature

Le build de créature est construit autour de ses compétences fixes grâce :

* à la répartition des caractéristiques ;
* à l’équipement ;
* à la progression ;
* à l’évolution ;
* au niveau d’étoiles ;
* à son usage dans différentes compositions.

La répartition des caractéristiques constitue un choix important et n’est pas librement réversible.

Trois voies permettent de modifier cette répartition :

1. une réinitialisation complète gratuite ramène la créature au niveau 1 et oblige à regagner les points liés aux niveaux ;
2. un objet rare obtenu en jouant redistribue les points déjà gagnés sans retour au niveau 1 ;
3. un service payant strictement limité fournit le même résultat immédiat que l’objet.

Le service payant n’accorde aucun point, aucune expérience, aucune ressource et aucun potentiel supplémentaire. Il doit rester facultatif et une méthode gratuite doit permettre d’obtenir le même résultat.

**Éléments à préciser ultérieurement :**

* La méthode d’obtention et le rythme de distribution de l’objet.
* La limite exacte du service payant, notamment par compte ou par créature.
* Le prix et la présentation du service.

La réinitialisation complète conserve la forme actuelle, la branche, le niveau d’étoiles, l’équipement, le surnom, les tags et les apparences déjà débloquées. Elle ne fait jamais régresser une évolution déjà obtenue.

### 10.4. Équipes enregistrées

Une équipe peut réunir jusqu’à six créatures. Une équipe complète en comporte six.

Deux instances d’une même famille peuvent cohabiter dans une équipe uniquement lorsque leurs chemins d’évolution ont réellement divergé. Une forme située sur leur tronc commun reste incompatible avec toute autre instance de cette famille. Cette règle s’applique globalement à tous les modes.

Le joueur peut :

* créer plusieurs équipes ;
* sélectionner jusqu’à six créatures dans chacune ;
* modifier une équipe ;
* supprimer une équipe ;
* nommer librement une équipe ;
* sélectionner rapidement une équipe avant une activité.

Les noms tels que « PvE », « PvP » ou « Boss » sont des exemples et ne constituent pas des catégories imposées.

**Éléments à préciser ultérieurement :**

* Le nombre exact d’équipes enregistrables.
* Les règles d’utilisation d’une même créature dans plusieurs équipes enregistrées.
* Les éventuelles restrictions propres à certains modes.

## 11. Combat — vue d’ensemble

### 11.1. Fonction du combat

Le combat met à l’épreuve :

* la pertinence de l’équipe sélectionnée ;
* le développement des créatures ;
* la répartition de leurs caractéristiques ;
* leurs équipements ;
* leurs compétences fixes ;
* les résistances élémentaires ;
* les Effets de combat ;
* les synergies de la composition.

### 11.2. Mode de contrôle

Les Basic Attacks et les Skills ordinaires sont utilisés automatiquement.

Le joueur peut :

* déclencher manuellement les compétences ultimes ;
* activer une option automatique qui gère également les compétences ultimes.

Une attaque peut comporter plusieurs composantes de dégâts dans un même hit hybride. Ce hit utilise un seul jet d’Esquive et un seul jet de Critique, tandis que ses composantes Physique et Spéciale sont calculées séparément selon leurs caractéristiques, défenses, résistances et modificateurs applicables.

Chaque Basic Attack et chaque Skill possède exactement un élément, indépendant du ou des éléments de sa créature. Le système élémentaire standard est défensif : il repose sur les résistances et les immunités explicitement accordées par des Skills, sans faiblesse ni bonus offensif automatique.

Le combat peut ainsi être semi-automatique ou entièrement automatique selon le choix du joueur. À chaque opportunité d’action valide, une Ultimate prête et autorisée est prioritaire sur une Active prête, elle-même prioritaire sur la Basic Attack. Une Ultimate ou une Active remplace la Basic Attack qui aurait normalement eu lieu.

Les contenus déjà maîtrisés doivent pouvoir être joués entièrement automatiquement.

### 11.3. Rythme et lisibilité

La durée moyenne visée d’un combat est de **30 à 60 secondes**. Le timeout standard est de **120 secondes de simulation**, sauf exception explicitement définie par un mode.

À ce timeout, un combat standard départage les équipes selon le nombre de créatures vivantes, puis selon le ratio entre les PV actuels et les PV maximum des survivants. Une égalité parfaite donne la victoire à l’attaquant. Une créature non vivante en attente d’une auto-résurrection ne compte pas comme survivante.

La visualisation est disponible gratuitement en ×1. Les paliers ×2 et ×4 sont des services de confort payants et peuvent être changés à tout moment, en Auto comme en Manuel. Le dernier choix est conservé pour le combat suivant. La vitesse ne modifie jamais la simulation, la seed RNG, les calculs, les statistiques, les événements, le résultat, les récompenses ou le coût en énergie. Dans le PvP asynchrone, le déblocage de ×4 peut également donner accès à un Skip qui passe directement au résumé sans modifier aucun de ces éléments.

Le combat doit rendre visibles :

* les actions importantes ;
* les Effets de combat ;
* les résultats utiles des interactions élémentaires, notamment les immunités ;
* les compétences ultimes ;
* les éliminations ;
* les changements majeurs dans l’équilibre du combat.

Le combat présente les résultats utiles de la simulation sans exposer constamment ses calculs internes. Les règles exactes d’ordre des actions, de ciblage, de dégâts, de Crit, d’Esquive et d’intelligence de combat sont définies dans [`02-COMBAT.md`](./02-COMBAT.md).

### 11.4. Présentation visuelle

La présentation générale prend pour référence conceptuelle un plateau d’auto-battler reposant sur des cartes, dans un esprit comparable à *Hearthstone Battlegrounds*, sans reprendre son identité visuelle, son interface, son layout, ses assets ou ses animations.

Une position logique occupée par une créature peut être représentée par sa carte. La créature n’a pas besoin d’être affichée comme un personnage indépendant se déplaçant librement sur un terrain 2D ou 3D.

Cette représentation ne modifie aucune règle de simulation. Les principes visuels des cartes et de leur mise en scène sont détaillés dans les drafts [Card Design](../03-art/03-CARD_DESIGN.md), [VFX](../03-art/05-VFX.md) et [Animations](../03-art/06-ANIMATIONS.md).

## 12. Résultats, victoire et défaite

### 12.1. Victoire

Une victoire :

* accorde l’expérience prévue aux créatures participantes ;
* accorde de l’expérience au compte ;
* remet les récompenses annoncées ;
* distingue les récompenses de première réussite et de répétition lorsque cela est nécessaire ;
* débloque l’étape ou la fonctionnalité suivante lorsqu’un jalon est atteint ;
* permet de poursuivre immédiatement ou de retourner à la gestion.

### 12.2. Défaite

Une défaite standard, sauf exception explicitement définie par un mode, n’accorde :

* aucune expérience aux créatures ;
* aucune expérience au compte ;
* aucune récompense principale ;
* aucune progression de niveau.

Elle ne provoque :

* aucune perte de progression déjà acquise ;
* aucune diminution permanente ;
* aucune suppression d’objet ;
* aucune autre pénalité durable.

L’énergie utilisée pour entrer dans le niveau est normalement consommée. Une exception peut être définie ultérieurement pour certaines activités ou étapes d’onboarding.

### 12.3. Analyse et actions suivantes

Après une défaite, le joueur peut :

* recommencer immédiatement avec la même équipe ;
* sélectionner une autre équipe préparée ;
* retourner à la gestion afin de modifier une composition ou un équipement ;
* quitter l’activité.

Le résultat doit donner accès à un résumé statistique simple des deux équipes, agrégé par créature plutôt que par Skill. Il présente notamment les dégâts infligés et reçus, les soins et Boucliers accordés ainsi que d’autres indicateurs globaux pertinents, dont la liste exacte reste à préciser dans le [document UI Flow](./20-UI_FLOW.md).

Ces informations doivent aider à comprendre les principales contributions, les Effets de combat importants et les créatures mises hors combat sans exposer un combat log technique détaillé.

Le jeu ne doit pas imposer automatiquement une solution ou un build unique.

## 13. Progression des créatures et du compte

### 13.1. Progression des créatures

Les créatures gagnent de l’expérience en participant aux combats remportés.

Lorsqu’une créature monte de niveau :

* sa progression individuelle augmente ;
* elle reçoit actuellement cinq points de caractéristiques ;
* le joueur répartit ces points sur cette même créature.

Le niveau ne possède pas de maximum et n’augmente aucune caractéristique automatiquement. Seuls les points attribués par le joueur aux six caractéristiques principales modifient alors le build ; les points non attribués peuvent être conservés indéfiniment.

L’XP d’une activité est attribuée individuellement après le combat à chaque créature participante et n’est jamais divisée entre les membres de l’équipe. Toutes les participantes reçoivent leur gain, y compris si elles sont mortes, contrôlées ou temporairement exclues à la fin du combat. Les règles de ratio liées aux niveaux et leurs valeurs actuelles sont définies dans le [draft Progression](./10-PROGRESSION.md).

### 13.2. Progression du compte

Le compte possède un niveau numérique.

Il gagne de l’expérience lorsque le joueur accomplit une activité.

La progression du compte :

* est beaucoup plus lente que celle des créatures ;
* représente la progression générale et l’ancienneté du joueur ;
* accorde une récompense à chaque niveau ;
* détermine le niveau d’objet des équipements nouvellement générés ou fabriqués ;
* participe à la progression du potentiel et de la complexité des équipements.

Les fonctionnalités, systèmes, modes, activités et principales étapes d’onboarding sont principalement débloqués par les jalons du mode Histoire. Le niveau de compte ne constitue pas par défaut un second système parallèle de déblocage. Des usages secondaires pourront être ajoutés ultérieurement s’ils sont explicitement justifiés sans concurrencer cette structure principale.

### 13.3. Absence de progression passive

Hors ligne, les créatures ne gagnent automatiquement :

* aucune expérience ;
* aucun niveau ;
* aucun point de caractéristique ;
* aucun équipement ;
* aucune ressource générale.

Le compte ne gagne pas non plus d’expérience automatiquement.

Le développement des créatures et du compte provient des activités réellement jouées.

### 13.4. Éléments à préciser ultérieurement

Les documents spécialisés devront définir :

* les courbes d’expérience ;
* les valeurs nécessaires à chaque niveau ;
* les règles d’arrondi de l’XP et la validation finale des paramètres actuels ;
* les multiplicateurs et exigences exacts des montées d’étoiles ;
* les récompenses du niveau de compte ;
* les éventuels usages secondaires du niveau de compte.

## 14. Énergie et régulation

### 14.1. Fonction

Le joueur possède une réserve générale d’énergie utilisée par défaut pour les activités individuelles, notamment le mode Histoire, les modes PvE individuels, le farming, les défis individuels et le PvP.

Cette énergie régule :

* le nombre d’activités jouées sur une période ;
* le gain d’expérience des créatures ;
* le gain d’expérience du compte ;
* la vitesse générale de progression.

Le joueur choisit librement les activités dans lesquelles il investit sa réserve disponible. Chaque activité définit son coût exact sans introduire automatiquement une énergie, un ticket, une clé ou une autre ressource d’entrée parallèle.

### 14.2. Régénération et accumulation

L’énergie :

* se régénère avec le temps ;
* continue à s’accumuler lorsque le joueur ne joue pas ;
* ne doit pas être perdue simplement parce que le joueur ne s’est pas connecté pendant une journée ;
* doit permettre d’utiliser ultérieurement une partie du temps de régénération accumulé.

La récupération d’énergie constitue la seule progression hors ligne validée.

Le système ne comporte aucun objet consommable de récupération d’énergie stocké dans l’inventaire. Une récompense ponctuelle de gameplay qui accorde de l’énergie l’ajoute immédiatement à la réserve générale, sans ticket ni ressource parallèle. Une activité répétable ne doit pas former une boucle remboursant structurellement autant ou davantage d’énergie que son coût d’entrée.

### 14.3. Garde-fous

L’énergie ne doit pas être vendue contre de l’argent réel.

Le système doit préserver :

* la possibilité de rattrapage ;
* la lisibilité ;
* l’équilibrage économique ;
* les contraintes techniques ;
* un rythme mobile qui ne bloque pas immédiatement un joueur absent.

Une activité peut utiliser une autre régulation uniquement lorsqu’une exception est explicitement justifiée et documentée localement. Certains événements, contenus de guilde, activités communautaires ou systèmes saisonniers pourront notamment définir une telle exception lors de leur propre cadrage.

### 14.4. Éléments à préciser ultérieurement

`10-PROGRESSION.md` devra définir :

* les coûts des activités ;
* le rythme de régénération ;
* la limite d’accumulation ou l’absence de limite stricte ;
* les quantités et fréquences des récompenses ajoutant directement de l’énergie ;
* les exceptions locales explicitement justifiées à la réserve commune ;
* les exceptions de consommation pendant l’onboarding.

## 15. Acquisition et invocation de créature

### 15.1. Voie principale

L’invocation de créature constitue la principale voie d’obtention des créatures.

Une invocation accorde toujours la forme de base d'une famille de créatures, jamais directement une forme évoluée. Cette règle reste valable lorsqu'une forme évoluée a déjà été rencontrée dans le monde.

Certaines créatures peuvent être accordées directement par le gameplay lorsqu'elles constituent une exception explicitement documentée à l'invocation comme voie principale. Une acquisition directe accorde elle aussi une nouvelle instance dans la forme de base de sa famille.

Narrativement, un dispositif lié à la Matrice entre en résonance avec un écho existant. Une nouvelle manifestation individuelle émerge dans sa forme de base et son Ancrage initial avec le joueur est établi. Le processus ordinaire n'est pas totalement contrôlable, ce qui peut justifier son aléatoire sans en fixer les règles ; les acquisitions contrôlées ou garanties déjà prévues peuvent l'encadrer exceptionnellement. Une obtention directe établit également un lien sans devenir une invocation.

Une nouvelle obtention d’une famille déjà possédée crée une nouvelle instance individuelle au stade 1, niveau 1, à 0 étoile et sans point attribué. Elle peut être développée séparément, suivre une autre branche ou servir ultérieurement de matériau d’étoiles pour une instance de la même famille.

### 15.2. Créature de départ

Le joueur choisit directement sa première créature parmi trois.

Cette obtention constitue une exception validée à l’invocation comme voie principale.

Un lien avec cette créature est établi lors de son obtention.

### 15.3. Ressource générale d’invocation

Une ressource générale principale permet d’effectuer les invocations de créatures.

Elle constitue une récompense de progression obtenue par le gameplay. Certaines activités, quêtes, récompenses uniques, jalons de progression et Events peuvent en distribuer de petites quantités maîtrisées, sans rendre sa présence obligatoire dans chaque récompense ni réserver son obtention à un mode particulier.

Elle est obtenue principalement grâce :

* au mode Histoire ;
* aux quêtes journalières ;
* aux activités ;
* aux récompenses de progression ;
* aux événements.

Elle reste entièrement séparée de l’économie cosmétique.

Sa distribution doit rester suffisamment limitée pour qu’aucune activité particulière ne devienne obligatoire afin de progresser normalement. Les classements finaux compétitifs saisonniers n’en distribuent jamais et n’accordent pas non plus d’invocations de créatures ; cette interdiction ne concerne pas les jalons personnels de progression des modes concernés.

### 15.4. Premières acquisitions

Les premières acquisitions sont encadrées afin de garantir une progression cohérente.

Après un premier jalon du mode Histoire, le joueur reçoit une invocation contrôlée ou garantie lui permettant d’obtenir une nouvelle créature.

Le nombre exact d’invocations garanties, les jalons concernés et les créatures accessibles restent à définir.

### 15.5. Séparation des parcours

L’invocation de créature et l’ouverture d’un paquet de skins de carte sont deux parcours distincts.

Une invocation :

* utilise une ressource de gameplay ;
* accorde une créature jouable ;
* ne doit pas être présentée comme une ouverture cosmétique.

Une ouverture de paquet :

* accorde uniquement des skins de carte ;
* n’utilise pas la ressource générale d’invocation ;
* n’accorde aucune créature ni puissance.

Les règles détaillées d’invocation seront définies dans `09-GACHA.md`. Le terme fonctionnel destiné au joueur et à la documentation reste **invocation de créature**.

## 16. Collection, cosmétique et économie

### 16.1. Système de collection

Le système de collection permet de consulter, organiser et valoriser les éléments collectionnables.

Il comprend deux parties séparées :

* la collection de créatures ;
* la collection de skins de carte.

Ces catégories appartiennent au même espace général sans être mélangées dans une liste unique.

Le système de collection reste distinct de l’inventaire consacré aux objets et ressources.

La gestion des instances possédées reste distincte de l’encyclopédie des créatures. L’encyclopédie conserve les découvertes du compte, affiche uniquement les familles réellement obtenues et enrichit progressivement les formes et branches connues sans révéler le nombre total de familles existantes.

### 16.2. Fonction dans la boucle globale

La collection :

* valorise les acquisitions ;
* rend visible la progression du joueur ;
* soutient la découverte ;
* renforce l’attachement aux créatures ;
* fournit des objectifs de complétion.

Elle soutient la boucle principale sans remplacer la progression et la maîtrise des équipes comme motivations prioritaires.

### 16.3. Monétisation principalement cosmétique

La boutique reste exclusivement consacrée aux contenus cosmétiques.

Elle ne vend :

* aucune créature ;
* aucune invocation ;
* aucune expérience ;
* aucun point de caractéristique ;
* aucun équipement ;
* aucune énergie ;
* aucune ressource de progression ;
* aucune augmentation du potentiel maximal.

Les services de confort actuellement validés en dehors de la boutique cosmétique sont :

* la réinitialisation payante des points de caractéristiques déjà gagnés sans retour au niveau 1, sans avantage de potentiel par rapport aux méthodes gratuites ;
* les vitesses de visualisation ×2 et ×4 des combats, ainsi que l’éventuel Skip PvP lié à ×4, qui agissent uniquement sur la restitution et n’influencent ni la simulation, ni le résultat, ni les récompenses ;
* les extensions permanentes de capacité de créatures possédées, qui n’accordent aucune puissance et ne remplacent pas la capacité gratuite ;
* la possibilité d’acheter des sacs augmentant uniquement la capacité de l’inventaire, également accessibles par le gameplay et sans puissance exclusive.

Cette liste décrit les services actuellement validés sans constituer une liste définitivement exhaustive. Tout nouveau service exige une décision explicite et doit respecter les garde-fous Free-to-Play et non-Pay-to-Win.

Les règles complètes de la boutique, des paquets de skins de carte, des doublons et de ces services sont définies par le [cadre de monétisation](../00-foundation/04-MONETIZATION.md).

## 17. Motivation et retour au jeu

### 17.1. Moteurs principaux

Les principaux moteurs de long terme sont :

1. développer les créatures favorites ;
2. créer et maîtriser plusieurs équipes spécialisées ;
3. progresser dans les mondes et niveaux du mode Histoire ;
4. débloquer de nouvelles fonctionnalités et activités ;
5. obtenir de nouvelles créatures et synergies ;
6. enrichir l’encyclopédie des créatures et découvrir de nouvelles branches ;
7. compléter les séries de skins de carte ;
8. progresser ultérieurement en PvP ;
9. participer ultérieurement à une guilde ou à des objectifs communautaires.

### 17.2. Régulation de la progression longue

La progression très longue est maîtrisée par :

* des rendements décroissants ;
* l’énergie ;
* l’augmentation progressive de la difficulté ;
* le besoin de diversifier les équipes et stratégies.

Le niveau des créatures ne possède pas de maximum. La formule exacte de la courbe d’XP reste cependant à définir.

### 17.3. Saisons et Events

Le jeu peut commencer sans Saison active. Lorsqu’elles sont lancées, les Saisons utilisent une période globale unique commune aux systèmes saisonniers, suivie d’une courte inter-saison pendant laquelle les modes concernés sont fermés et leurs résultats finalisés. Elles renouvellent certaines compétitions et influencent plusieurs systèmes spécialisés sans créer de niveau, d’XP ou de parcours de récompenses global.

Une nouvelle Saison peut réinitialiser uniquement les progressions, classements ou scores explicitement saisonniers ; elle ne remet jamais à zéro la progression durable générale du joueur.

Les Events restent totalement indépendants des Saisons et de l’inter-saison. Ils constituent de petites animations temporaires utilisant principalement les systèmes et modes existants pour proposer des missions thématiques et des récompenses adaptées. Plusieurs occurrences peuvent coexister ; elles ne possèdent aucune progression globale d’Event et ne doivent pas nécessiter un nouveau mode, une progression complexe ou une production lourde spécifique.

Les classements finaux compétitifs saisonniers privilégient le prestige, les Hauts Faits, les titres, badges, personnalisations et cosmétiques. Ils ne distribuent ni ressource générale d’invocation, ni invocations de créatures, ni énergie générale, contrairement aux jalons personnels de progression qui peuvent proposer ponctuellement ces ressources selon leur référentiel propriétaire.

Les dates, durées réelles, thèmes, contenus et récompenses exactes des Saisons et des Events ne sont pas définis dans le GDD.

## 18. Modes de jeu et statuts de périmètre

### 18.1. Catégories de statut

Le GDD utilise quatre statuts de périmètre :

* **inclus dans la vertical slice** ;
* **envisagé pour une première version jouable** ;
* **envisagé à long terme** ;
* **possibilité non validée**.

Ces statuts ne constituent pas une roadmap ni un calendrier de production.

### 18.2. Inclus dans la vertical slice

* Un début représentatif du mode Histoire.
* Plusieurs niveaux courts.
* Un boss ou défi final.

### 18.3. Envisagé pour une première version jouable

Le mode Histoire constitue le seul mode actuellement confirmé comme colonne vertébrale d’une première version jouable.

Aucun autre mode n’est encore validé dans ce périmètre.

### 18.4. Envisagé à long terme

Les fondations envisagent les modes et structures suivants :

* des boss personnels ;
* des World Boss ;
* une tour infinie ;
* du PvP ;
* des guildes ;
* des Saisons transversales ;
* des Events temporaires légers.

Leur présence dans cette liste ne valide ni leurs règles, ni leur ordre de production, ni leur date de disponibilité.

### 18.5. Possibilités non validées

Tout autre mode ou variante non explicitement validé doit rester présenté comme une possibilité.

Les contrats transversaux et les statuts de périmètre sont définis dans [`12-MODES.md`](./12-MODES.md). Les règles détaillées et les éventuelles exceptions de chaque mode relèvent des documents spécialisés associés.

## 19. Vertical slice fonctionnelle

### 19.1. Objectif

La vertical slice doit principalement prouver :

> Le plaisir de progresser dans plusieurs niveaux, sélectionner une équipe préparée, combattre, recevoir de l’expérience et des récompenses, développer ses créatures, améliorer ses compositions puis franchir un nouveau défi.

Elle doit également démontrer un onboarding simple et progressif.

Elle ne cherche pas à valider la monétisation, le cosmétique, les modes sociaux ou l’équilibrage final.

### 19.2. Parcours représentatif

La vertical slice comprend :

1. une courte introduction au contexte ;
2. le choix de la première créature parmi trois ;
3. un premier combat immédiat ;
4. une première montée de niveau ;
5. l’introduction de la répartition des caractéristiques ;
6. plusieurs niveaux courts ;
7. une acquisition contrôlée ou garantie ;
8. l’obtention progressive de plusieurs créatures ;
9. l’introduction de la composition d’équipe ;
10. la création ou la sélection d’une équipe préparée ;
11. la modification d’un équipement ou d’une composition ;
12. un nouveau combat permettant d’observer l’impact du changement ;
13. un boss ou défi final.

### 19.3. Systèmes obligatoires

La vertical slice doit inclure au minimum :

* une sélection limitée de créatures ;
* quatre Skills fixes par créature ;
* quelques éléments ;
* quelques Effets de combat ;
* plusieurs niveaux du mode Histoire ;
* un coût en énergie ;
* une régénération réelle ou simulée de l’énergie ;
* le choix de la première créature ;
* une acquisition contrôlée d’une nouvelle créature ;
* la progression graduelle du groupe initial ;
* au moins une équipe préparée ;
* des combats fonctionnels ;
* des résultats et récompenses ;
* de l’expérience pour les créatures ;
* de l’expérience pour le compte ;
* une montée de niveau de créature ;
* la répartition de points de caractéristiques ;
* au moins un équipement modifiable ;
* un ajustement dont l’impact peut être observé ;
* un boss ou défi final.

### 19.4. Éléments facultatifs

La vertical slice peut inclure si le périmètre le permet :

* une progression visible du niveau de compte ;
* un petit nombre de plusieurs équipes enregistrées ;
* une sauvegarde locale minimale entre plusieurs sessions.

### 19.5. Exclusions

La vertical slice exclut :

* le PvP ;
* les guildes ;
* les World Boss ;
* les événements temporaires ;
* les saisons ;
* la boutique ;
* les achats réels ;
* les paquets de skins de carte ;
* le catalogue cosmétique complet ;
* les systèmes sociaux ;
* les échanges entre joueurs ;
* la progression passive autre que la récupération d’énergie ;
* l’équilibrage définitif ;
* une progression infinie réellement déployée ;
* un catalogue étendu de créatures ;
* le backend et l’infrastructure de production finale.

### 19.6. Critères qualitatifs de validation

La vertical slice remplit son objectif si elle permet de vérifier que :

* la progression d’une créature produit un effet perceptible ;
* un choix de caractéristiques ou d’équipement modifie réellement son fonctionnement ;
* sélectionner une équipe adaptée améliore les chances de réussite ;
* les compétences fixes rendent les créatures compréhensibles et distinctes ;
* le passage entre activité, résultat et gestion reste fluide ;
* l’onboarding introduit les systèmes sans longues interruptions ;
* le rythme des combats et des niveaux est adapté au mobile ;
* le boss final exige une amélioration ou une adaptation compréhensible.

## 20. Dépendances et décisions ouvertes

### 20.1. Dépendances documentaires

Le GDD dépend des documents spécialisés suivants pour les détails :

* [`02-COMBAT.md`](./02-COMBAT.md) — déroulement, ordre des actions, ciblage, dégâts et contrôle ;
* [`03-CREATURES.md`](./03-CREATURES.md) — structure des créatures, caractéristiques, rôles et règles de progression propres ;
* [`04-SKILLS.md`](./04-SKILLS.md) — structure et règles des Skills fixes ;
* [`05-ELEMENTS.md`](./05-ELEMENTS.md) — éléments des formes et capacités, résistances, immunités et lisibilité élémentaire ;
* [`06-COMBAT_EFFECTS.md`](./06-COMBAT_EFFECTS.md) — lifecycle, application, réapplication, retrait, effets périodiques, contrôles et protections ;
* [`07-EVOLUTIONS.md`](./07-EVOLUTIONS.md) — conditions, branches et effets des évolutions ;
* [`08-ITEMS.md`](./08-ITEMS.md) — objets, équipements, génération, fabrication, inventaire et sacs ;
* [`09-GACHA.md`](./09-GACHA.md) — règles de l’invocation de créature ;
* [`10-PROGRESSION.md`](./10-PROGRESSION.md) — expérience, niveaux, étoiles, énergie, réinitialisations et progression du compte ;
* [`11-COLLECTION.md`](./11-COLLECTION.md) — gestion des instances, encyclopédie et capacité ;
* [`12-MODES.md`](./12-MODES.md) — contrats communs et statuts des modes ;
* [`13-PVE.md`](./13-PVE.md) — mode Histoire, Boss personnels, World Boss, Tour infinie et autres modes PvE sans référentiel propre ;
* [`14-PVP.md`](./14-PVP.md) — format asynchrone, matchmaking, saisons et classement du PvP ;
* [`15-GUILDS.md`](./15-GUILDS.md) — structure, fonctions et activités de guilde ;
* [`16-SEASONS.md`](./16-SEASONS.md) — trame transversale, progression durable et systèmes saisonniers ;
* [`17-EVENTS.md`](./17-EVENTS.md) — animations temporaires légères utilisant les systèmes existants ;
* [`18-QUESTS.md`](./18-QUESTS.md) — quêtes journalières et saisonnières ;
* `19-ACHIEVEMENTS.md` — hauts faits, lorsqu’un cadrage suffisant permettra sa création ;
* [`20-UI_FLOW.md`](./20-UI_FLOW.md) — écrans, navigation, tutoriels et parcours ;
* `21-SOCIAL_AND_COMMUNICATION.md` — fonctions sociales et de communication, document prévu mais non cadré et non créé ;
* [`01-ART_DIRECTION.md`](../03-art/01-ART_DIRECTION.md) à [`06-ANIMATIONS.md`](../03-art/06-ANIMATIONS.md) — direction artistique, représentation des créatures, cartes, UI, VFX et animations ;
* [`01-ARCHITECTURE.md`](../04-technical/01-ARCHITECTURE.md) — moteur retenu, séparation technique entre simulation et représentation et principes de reproductibilité.

### 20.2. Questions ouvertes conservées

Les questions suivantes ne bloquent pas le fonctionnement global décrit par le GDD :

* le nom définitif du rôle provisoirement appelé « Éveilleur » ;
* les paramètres exacts des courbes d’Agilité, de Crit et d’Esquive ;
* les valeurs et règles individuelles encore ouvertes des Effets de combat ;
* la méthode d’obtention et le rythme de distribution de l’objet de réinitialisation ;
* la limite et le prix du service payant de réinitialisation ;
* les prix et la présentation des vitesses de visualisation ×2 et ×4 ;
* la courbe d’expérience sans niveau maximal, les règles d’arrondi et la validation finale des paramètres actuels d’XP et de points par niveau ;
* les multiplicateurs et exigences exacts des quinze montées d’étoiles ;
* la formule exacte du score de Puissance ;
* les valeurs, pools, raretés, rolls, tables de loot, recettes, sets et formule d’iLvl des équipements ;
* les tailles, sources, probabilités et prix éventuels des sacs ;
* les prix et tailles des extensions permanentes de capacité ;
* les récompenses et usages secondaires du niveau de compte ;
* les coûts, la régénération et l’accumulation exacte de l’énergie ;
* le nom, la représentation et le rythme d’obtention de la ressource générale d’invocation ;
* les premières créatures, invocations garanties et jalons exacts de l’onboarding ;
* le nombre d’équipes enregistrables et leurs règles de partage des créatures ;
* les listes et récompenses des quêtes journalières ;
* les règles détaillées des modes envisagés ;
* les dates, durées réelles et contenus des Saisons, des Events et des mises à jour ;
* les quantités et données exactes de la vertical slice.

### 20.3. Principe de maintien

Une question ouverte ne doit pas être transformée en règle définitive sans validation.

Lorsqu’un futur document spécialisé répond à une question qui modifie le fonctionnement global, la réponse doit être reportée dans le GDD. Lorsqu’elle modifie un principe de fondation, les documents de fondation concernés doivent également être mis à jour.
