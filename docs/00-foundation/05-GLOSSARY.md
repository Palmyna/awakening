# Project Awakening — Glossaire officiel

**Statut :** Rédigé, en attente de validation finale

## 1. Rôle du document

Ce document définit le vocabulaire officiel de **Project Awakening**.

Il sert de référence commune pour :

* la documentation ;
* les échanges entre les membres du projet ;
* les agents IA ;
* le futur code source ;
* les données du jeu ;
* les interfaces et les textes destinés aux joueurs lorsque les termes concernés s’y appliquent.

Le glossaire fixe le sens et l’usage des termes. Il ne crée pas de mécanique et ne remplace pas les documents spécialisés chargés de définir les systèmes du jeu.

Il complète la [vision du projet](./01-VISION.md), les [piliers fondamentaux](./02-PILLARS.md), la [philosophie du projet](./03-PROJECT_PHILOSOPHY.md) et le [cadre de monétisation](./04-MONETIZATION.md).

## 2. Conventions générales

### 2.1. Statut des termes

Chaque entrée possède l’un des statuts suivants :

* **Validé** : le terme et la distinction qu’il exprime constituent la référence actuelle du projet.
* **Provisoire** : le terme ou le concept est conservé pour faciliter le travail, mais il devra encore être confirmé ou renommé.

Sauf indication contraire, une variante autorisée peut être employée dans le contexte précisé sans devenir un terme officiel supplémentaire.

### 2.2. Français et anglais

Les concepts liés au jeu, à son univers et à son interface utilisent en priorité un terme français officiel.

Les termes anglais conventionnels restent officiels pour le développement et la production lorsqu’ils correspondent aux usages habituels du secteur. Les phrases de la documentation restent néanmoins rédigées en français.

Les équivalents anglais destinés au futur code ou aux données ne sont pas imposés lorsqu’ils ne sont pas déjà établis. Ils devront être ajoutés au glossaire au moment de la conception technique, selon l’architecture, le modèle de données, les conventions de nommage, le langage et les frameworks retenus.

**Élément à préciser ultérieurement :**

* les équivalents anglais fonctionnels destinés au code et aux données, lorsque les choix techniques permettront de les valider.

### 2.3. Acronymes

Les acronymes internationaux courants peuvent être conservés. Leur signification doit être développée lors de leur première occurrence dans un document lorsque cela améliore la compréhension.

### 2.4. Qualification des termes

Un terme doit être qualifié lorsque son emploi isolé pourrait créer une ambiguïté. Cette règle concerne notamment les builds, les doublons, la rareté, la qualité, les catalogues et les différents sens du mot « licence ».

## 3. Identité et univers

### Project Awakening

**Statut :** Validé comme nom actuel et nom de code ; titre commercial non définitif  
**Domaine :** Projet

**Définition :** Nom officiel actuel et nom de code du projet. Il peut être utilisé uniformément dans la documentation, mais ne préjuge pas du futur titre commercial du jeu.

**Élément à préciser ultérieurement :**

* le titre commercial définitif du jeu.

### Licence originale

**Statut :** Validé  
**Domaine :** Identité du projet

**Définition :** Propriété créative globale construite autour de Project Awakening et susceptible de réunir plusieurs œuvres, jeux ou produits.

**Terme à éviter :** « licence » sans qualification lorsque le contexte pourrait être confondu avec une licence logicielle.

### Licence logicielle

**Statut :** Validé  
**Domaine :** Développement

**Définition :** Conditions juridiques encadrant l’utilisation, la modification et la distribution d’un logiciel ou de son code.

### Univers

**Statut :** Validé  
**Domaine :** Univers narratif

**Définition :** Cadre fictionnel général de Project Awakening.

### Multivers

**Statut :** Validé  
**Domaine :** Univers narratif

**Définition :** Structure interne de l’univers impliquant plusieurs mondes, réalités ou dimensions.

## 4. Créatures, monstres et cartes

### Créature

**Statut :** Validé  
**Domaine :** Game design, univers, interface

**Définition :** Entité jouable collectionnée, possédée, développée et utilisée par le joueur. Les créatures composent l’équipe du joueur.

**Terme à éviter :** « monstre » pour désigner une entité jouable ou collectionnée.

### Monstre

**Statut :** Validé  
**Domaine :** Game design, combats

**Définition :** Ennemi affronté par le joueur au cours des activités et des combats. Un monstre n’est pas une créature possédée par le joueur.

**Terme à éviter :** « monstre » pour désigner une créature jouable, y compris dans les expressions « carte de monstre », « famille de monstres » et « doublon de monstre ».

### Carte de créature

**Statut :** Validé  
**Domaine :** Interface, représentation visuelle

**Définition :** Représentation visuelle et fonctionnelle d’une créature dans l’interface. La carte et la créature ne sont pas deux objets de progression distincts : le joueur possède une créature, représentée sous la forme d’une carte.

**Variante autorisée :** « carte » lorsque le contexte ne laisse aucune ambiguïté.

**Terme à éviter :** « carte de monstre » pour une créature du joueur.

Une éventuelle représentation d’un monstre ennemi sous forme de carte devra être explicitement qualifiée.

### Famille de créatures

**Statut :** Validé  
**Domaine :** Game design, univers

**Définition :** Ensemble des formes appartenant à une même chaîne d’évolution.

**Variantes autorisées :**

* « famille » lorsque le contexte est explicite ;
* « lignée » ou « lignée évolutive » dans un contexte narratif.

**Terme à éviter :** « famille de monstres » pour les créatures collectionnées.

Les variantes narratives n’introduisent pas un niveau de regroupement supplémentaire.

### Forme de base

**Statut :** Validé  
**Domaine :** Progression des créatures

**Définition :** Première forme d’une famille de créatures. Une invocation de créature donne accès à cette forme, jamais directement à la forme finale.

### Forme intermédiaire

**Statut :** Validé  
**Domaine :** Progression des créatures

**Définition :** Forme située entre la forme de base et la forme finale dans une famille de créatures qui comporte trois formes.

**Terme à éviter :** « évolution intermédiaire » pour désigner la forme obtenue.

### Forme finale

**Statut :** Validé  
**Domaine :** Progression des créatures

**Définition :** Dernière forme actuellement prévue dans la chaîne d’évolution d’une famille de créatures.

**Terme à éviter :** « évolution finale » pour désigner la forme obtenue.

### Évolution

**Statut :** Validé  
**Domaine :** Progression des créatures

**Définition :** Processus permettant à une créature de passer d’une forme à la suivante.

**Terme à éviter :** « évolution » pour désigner une forme ou l’amélioration du niveau d’étoiles.

## 5. Progression, personnalisation et équipe

### Caractéristique

**Statut :** Validé  
**Domaine :** Progression des créatures

**Définition :** Valeur principale propre à une créature et susceptible d’être influencée par sa progression et sa personnalisation.

Les **points de caractéristiques** sont les points que le joueur répartit pour augmenter les caractéristiques d’une créature.

**Terme à éviter :** « statistique » comme synonyme direct d’une caractéristique principale.

### Statistique

**Statut :** Validé  
**Domaine :** Données, analyse, description générale

**Définition :** Terme général ou technique utilisé pour des valeurs calculées, des données, des résultats ou des statistiques globales. Il ne désigne pas les caractéristiques principales d’une créature.

### Niveau d’étoiles

**Statut :** Validé  
**Domaine :** Progression des créatures

**Définition :** État actuel d’une créature dans le système d’étoiles.

### Amélioration du niveau d’étoiles

**Statut :** Validé  
**Domaine :** Progression des créatures

**Définition :** Processus utilisant les doublons de créature afin d’augmenter progressivement le potentiel de la créature concernée.

**Termes à éviter :** « évolution d’étoiles » et « évolution des étoiles ».

### Objet

**Statut :** Validé  
**Domaine :** Systèmes de jeu

**Définition :** Terme générique désignant un élément pouvant être obtenu et généralement stocké dans l’inventaire ou utilisé par un système du jeu.

Un équipement est une catégorie d’objet. Tous les objets ne sont pas des équipements.

### Équipement

**Statut :** Validé  
**Domaine :** Progression, personnalisation

**Définition :** Catégorie d’objet pouvant être équipée par une créature afin de participer à sa personnalisation et à son fonctionnement.

**Variantes autorisées :**

* « équipement équipé » ;
* « équipement actuel » pour l’équipement actuellement attribué à une créature.

### Système d’équipement

**Statut :** Validé  
**Domaine :** Progression, personnalisation

**Définition :** Système permettant de gérer, d’attribuer, de remplacer ou de retirer les équipements des créatures.

### Coffre

**Statut :** Provisoire — proposition non validée  
**Domaine :** Objets

**Définition :** Objet qui pourrait être obtenu, stocké dans un inventaire puis ouvert afin de recevoir un contenu.

Cette entrée conserve une piste de conception sans valider l’existence des coffres dans le jeu ni une boucle d’acquisition.

**Éléments à préciser ultérieurement :**

* les modes, les activités et la fréquence d’acquisition ;
* les éventuelles raretés ;
* le contenu exact ;
* le caractère déterminé ou aléatoire du contenu ;
* le nombre d’éléments contenus ;
* la place des coffres dans la progression et l’économie.

La présence d’un équipement dans un coffre reste une possibilité non validée.

### Rareté

**Statut :** Validé  
**Domaine :** Créatures, illustrations et cosmétiques

**Définition :** Notion qui doit toujours être qualifiée selon son domaine : **rareté d’une créature**, **rareté d’une illustration** ou **rareté d’un cosmétique**.

La rareté n’est pas automatiquement équivalente à la qualité.

### Qualité

**Statut :** Validé  
**Domaine :** Équipements et objets

**Définition :** Notion utilisée pour qualifier un équipement et, si cela est validé ultérieurement, d’autres catégories d’objets. Elle doit rester qualifiée tant que ses échelles et ses effets ne sont pas entièrement définis.

La qualité n’est pas automatiquement équivalente à la rareté.

### Build de créature

**Statut :** Validé  
**Domaine :** Game design

**Définition :** Ensemble des choix de personnalisation qui déterminent la manière dont une créature fonctionne, notamment ses caractéristiques, ses compétences et son équipement.

**Variante autorisée :** « build » lorsque le contexte de game design est explicite et sans ambiguïté.

### Build d’équipe

**Statut :** Validé  
**Domaine :** Game design

**Définition :** Ensemble des choix de personnalisation et d’optimisation considérés à l’échelle d’une équipe.

Le terme doit rester qualifié. Une composition d’équipe ne doit pas être appelée simplement « build ».

### Équipe

**Statut :** Validé  
**Domaine :** Game design

**Définition :** Ensemble concret de six créatures sélectionnées ou utilisées par le joueur.

Les monstres ennemis ne font pas partie de l’équipe du joueur.

### Composition d’équipe

**Statut :** Validé  
**Domaine :** Game design, stratégie

**Définition :** Choix et organisation stratégique des créatures qui composent une équipe.

**Variante autorisée :** « composition » lorsque le contexte est explicite.

## 6. Acquisition, hasard et récompenses

### Invocation

**Statut :** Validé  
**Domaine :** Acquisition des créatures

**Définition :** Système d’acquisition aléatoire de créatures. Une invocation permet d’obtenir la forme de base d’une famille de créatures.

**Terme à éviter :** « invocation » pour l’ouverture d’un contenu cosmétique, d’un objet ou d’un coffre.

### Ouverture

**Statut :** Validé  
**Domaine :** Acquisition, cosmétiques, objets

**Définition :** Action qui révèle le contenu d’un pack d’illustrations ou, si cette proposition est validée ultérieurement, d’un coffre.

### Tirage

**Statut :** Validé  
**Domaine :** Conception interne, technique

**Définition :** Terme générique interne décrivant une sélection aléatoire.

**Terme à éviter :** « tirage » comme nom officiel d’une fonctionnalité destinée au joueur lorsqu’un terme fonctionnel plus précis, comme « invocation » ou « ouverture », s’applique.

### Gacha

**Statut :** Validé  
**Domaine :** Genre, description générale

**Définition :** Terme décrivant un type général de système d’acquisition aléatoire ou une référence au genre dont s’inspire Project Awakening.

**Terme à éviter :** « gacha » comme nom officiel d’une fonctionnalité destinée au joueur.

### Verbes d’acquisition et d’utilisation

Les entrées suivantes sont validées dans les domaines fonctionnels du jeu :

| Terme officiel | Définition |
| --- | --- |
| **Obtenir** | Recevoir un élément, quelle que soit la méthode. |
| **Acquérir** | Forme plus soutenue ou plus formelle d’« obtenir », adaptée aux documents de conception. |
| **Acheter** | Obtenir un produit en échange d’argent réel. |
| **Débloquer** | Rendre un élément définitivement disponible sur le compte. |
| **Ouvrir** | Révéler ou recevoir le contenu d’un pack d’illustrations ou d’un coffre éventuel. |
| **Invoquer** | Effectuer une invocation de créature. |
| **Équiper** | Attribuer un équipement à une créature. |
| **Appliquer** | Attribuer un skin de carte à la carte d’une créature. |
| **Récupérer** | Recevoir un objet ou une récompense afin de l’ajouter à l’inventaire ou au compte. |

Le verbe « sélectionner » peut décrire le choix effectué dans un menu, mais l’action fonctionnelle portant sur un skin de carte reste « appliquer ».

**Termes à éviter :**

* « équiper un skin de carte » ;
* « appliquer un équipement ».

### Récompense

**Statut :** Validé  
**Domaine :** Systèmes de jeu

**Définition :** Élément ou bénéfice remis au joueur à la suite d’une activité, d’un objectif, d’un événement ou d’un autre système prévu par le jeu.

La nature possible d’un élément ne valide pas son mode réel d’acquisition. Le glossaire ne confirme donc pas qu’une créature, un équipement ou un coffre puisse être remis directement comme récompense.

### Récompense ayant un effet sur la progression

**Statut :** Validé  
**Domaine :** Progression, économie

**Définition :** Récompense qui influence directement ou indirectement la progression du joueur.

**Terme à éviter :** « récompense utile », qui pourrait suggérer qu’une récompense cosmétique serait inutile.

### Récompense cosmétique

**Statut :** Validé  
**Domaine :** Cosmétiques, économie

**Définition :** Récompense qui modifie ou enrichit la présentation visuelle sans conférer d’effet sur la progression ou les caractéristiques de jeu.

### Gain

**Statut :** Validé  
**Domaine :** Description générale

**Définition :** Résultat générique obtenu par le joueur. Ce terme ne précise ni la nature du résultat ni son mode d’acquisition.

### Monnaie

**Statut :** Validé  
**Domaine :** Économie

**Définition :** Valeur échangeable contre des contenus ou des éléments définis.

Une monnaie peut être considérée techniquement comme une catégorie de ressource, mais « monnaie » et « ressource » ne sont pas synonymes dans la documentation fonctionnelle.

### Ressource

**Statut :** Validé  
**Domaine :** Progression, systèmes de jeu

**Définition :** Élément consommable utilisé par un système de progression ou de jeu.

## 7. Illustrations, cosmétiques et commerce

### Illustration

**Statut :** Validé  
**Domaine :** Direction artistique

**Définition :** Œuvre visuelle produite pour représenter une créature.

Une illustration est un asset artistique. Elle n’est pas, à elle seule, le contenu cosmétique possédé par le joueur.

### Skin de carte

**Statut :** Validé  
**Domaine :** Cosmétique, interface

**Définition :** Contenu cosmétique possédé par le joueur et utilisant une illustration spécifique pour modifier la représentation visuelle de la carte d’une créature.

Un skin de carte ne modifie ni la créature, ni ses caractéristiques, ni ses capacités. Le joueur **applique** un skin de carte ; il ne l’équipe pas.

**Variante autorisée :** « skin » lorsque le contexte ne laisse aucune ambiguïté.

**Élément à préciser ultérieurement :**

* un éventuel nom destiné au joueur, davantage lié à l’univers, pourra être défini lors de la conception de l’interface.

### Visuel

**Statut :** Validé  
**Domaine :** Description générale

**Définition :** Terme générique désignant un élément visuel sans lui attribuer de statut artistique, cosmétique ou fonctionnel précis.

### Collection d’illustrations

**Statut :** Validé  
**Domaine :** Cosmétique, monétisation

**Définition :** Ensemble cohérent d’illustrations ou de skins de carte partageant un thème. Dans le modèle économique initial, ce terme désigne également le contenu payant connu avant l’achat.

Une collection peut être vendue sous la forme d’un produit.

### Collection de créatures

**Statut :** Validé  
**Domaine :** Collection

**Définition :** Ensemble des créatures possédées par le joueur ou disponibles dans le jeu, selon le contexte.

Ce terme reste distinct de « collection d’illustrations ».

### Pack d’illustrations

**Statut :** Validé  
**Domaine :** Cosmétique, acquisition

**Définition :** Conteneur cosmétique gratuit et aléatoire obtenu en jouant, dont les éléments précis sont révélés lors de son ouverture.

**Variantes autorisées :** « pack » lorsque le contexte cosmétique est explicite.

**Termes à éviter :**

* « pack » pour un contenu payant connu à l’avance dans le modèle initial ;
* « coffre » comme synonyme d’un pack d’illustrations.

### Produit

**Statut :** Validé  
**Domaine :** Monétisation

**Définition :** Élément pouvant être acheté contre de l’argent réel.

### Offre

**Statut :** Validé  
**Domaine :** Monétisation

**Définition :** Présentation commerciale, temporaire ou permanente, d’un ou de plusieurs produits.

Une offre peut contenir un produit comprenant une collection d’illustrations entière ou une partie de celle-ci.

### Doublon de créature

**Statut :** Validé  
**Domaine :** Progression des créatures

**Définition :** Nouvelle obtention d’une créature déjà possédée, utilisée pour améliorer le niveau d’étoiles de cette créature.

**Terme à éviter :** « doublon de monstre ».

### Doublon de skin de carte

**Statut :** Validé  
**Domaine :** Cosmétique, économie

**Définition :** Nouvelle obtention d’un skin de carte déjà débloqué, convertie en monnaie de conversion des doublons.

**Variante autorisée :** « doublon » lorsque le contexte cosmétique ne laisse aucune ambiguïté.

### Monnaie de conversion des doublons

**Statut :** Provisoire — nom descriptif interne  
**Domaine :** Économie, cosmétiques

**Définition :** Monnaie permanente provenant de la conversion des doublons de skins de carte et utilisable dans le catalogue de conversion.

**Élément à préciser ultérieurement :**

* le nom définitif destiné au joueur sera choisi selon l’univers, l’identité visuelle et l’interface.

### Boutique

**Statut :** Validé  
**Domaine :** Interface, monétisation

**Définition :** Interface générale dans laquelle le joueur consulte les contenus et les produits disponibles.

### Catalogue commercial

**Statut :** Validé  
**Domaine :** Monétisation

**Définition :** Ensemble des produits proposés contre de l’argent réel.

### Catalogue de conversion

**Statut :** Validé  
**Domaine :** Économie, cosmétiques

**Définition :** Ensemble des contenus accessibles avec la monnaie de conversion des doublons.

Un catalogue désigne un ensemble de contenus disponibles ; la boutique désigne l’interface qui les présente.

## 8. Modes de jeu et combats

### Mode de jeu

**Statut :** Validé  
**Domaine :** Game design

**Définition :** Activité ou type de contenu proposé au joueur, par exemple l’histoire, un boss, une tour ou le PvP.

### Mode de contrôle du combat

**Statut :** Validé  
**Domaine :** Combat

**Définition :** Manière dont les actions sont contrôlées pendant un combat, notamment le combat automatique ou semi-automatique.

**Terme à éviter :** « mode de jeu » pour désigner le degré d’automatisation d’un combat.

## 9. Conception, expérience et intelligence artificielle

### Game design

**Statut :** Validé  
**Domaine :** Conception

**Définition :** Discipline et travail de conception des règles, des systèmes, des mécaniques, des équilibres et des interactions du jeu.

**Variante autorisée :** « conception de jeu » dans un passage explicatif.

### Gameplay

**Statut :** Validé  
**Domaine :** Conception

**Définition :** Manière dont le jeu fonctionne concrètement lorsqu’il est joué, à travers ses mécaniques et ses interactions.

**Terme à éviter :** « expérience de jeu » comme synonyme exact.

### Expérience de jeu

**Statut :** Validé  
**Domaine :** Expérience joueur

**Définition :** Ensemble plus large de ce que le joueur ressent et perçoit, au-delà du seul fonctionnement des mécaniques et des interactions.

### Intelligence artificielle

**Statut :** Validé  
**Domaine :** Production, technique

**Définition :** Technologie générale utilisée pour assister certaines activités de recherche, de conception, de documentation, de développement, de production et de test.

**Abréviation officielle :** IA

### Outil d’IA

**Statut :** Validé  
**Domaine :** Production, technique

**Définition :** Logiciel ou service utilisant l’intelligence artificielle.

### Agent IA

**Statut :** Validé  
**Domaine :** Production, technique

**Définition :** Système disposant d’un objectif, d’un contexte, de règles et d’une certaine capacité d’action dans un workflow.

Les assistants autorisés à intervenir sur le repository, à lire son contenu ou à modifier ses fichiers peuvent être désignés comme des agents IA.

## 10. Développement et production

Les termes de cette section conservent leur forme anglaise conventionnelle dans la documentation technique et de production.

### Analytics

**Statut :** Validé  
**Domaine :** Développement, exploitation

**Définition :** Collecte et analyse de données et d’indicateurs afin de comprendre l’utilisation du jeu et d’évaluer son fonctionnement.

### API

**Statut :** Validé  
**Domaine :** Développement

**Définition :** Interface permettant à des logiciels ou composants d’échanger selon des règles définies.

**Forme développée :** *Application Programming Interface*.

### Asset

**Statut :** Validé  
**Domaine :** Production, développement

**Définition :** Ressource numérique utilisée ou intégrée dans la production du jeu, par exemple une illustration, un son ou un fichier d’interface.

**Terme à éviter :** « ressource » lorsque cette traduction créerait une confusion avec une ressource de jeu.

### Backend

**Statut :** Validé  
**Domaine :** Développement

**Définition :** Partie technique chargée des traitements, services et données qui ne relèvent pas directement de l’interface visible par le joueur.

### Build logiciel

**Statut :** Validé  
**Domaine :** Développement

**Définition :** Version compilée ou assemblée du jeu ou d’une application, produite pour être exécutée, testée ou distribuée.

**Variantes autorisées :**

* build du jeu ;
* build de développement ;
* build de test ;
* build de production ;
* build, lorsque le contexte technique est explicite.

Ce sens doit rester distinct de « build de créature » et de « build d’équipe ».

### Framework

**Statut :** Validé  
**Domaine :** Développement

**Définition :** Cadre technique fournissant une structure, des conventions et des composants réutilisables pour développer une application ou une partie du jeu.

### Free Tier

**Statut :** Validé  
**Domaine :** Production, services techniques

**Définition :** Niveau d’utilisation gratuit proposé par un service, généralement soumis à des limites.

### Frontend

**Statut :** Validé  
**Domaine :** Développement

**Définition :** Partie d’un logiciel chargée de la présentation et des interactions directement accessibles à l’utilisateur.

### Open source

**Statut :** Validé  
**Domaine :** Développement, production

**Définition :** Qualifie un logiciel dont le code source est accessible et dont la licence logicielle encadre les possibilités d’utilisation, de modification et de distribution.

### Pipeline

**Statut :** Validé  
**Domaine :** Développement, production

**Définition :** Enchaînement organisé d’étapes permettant de transformer, vérifier, intégrer ou livrer des éléments du projet.

### Repository

**Statut :** Validé  
**Domaine :** Développement

**Définition :** Espace versionné contenant les fichiers, le code et la documentation du projet.

**Variante française autorisée :** « dépôt » dans le texte courant ou explicatif.

Le terme **repository** est prioritaire dans les définitions techniques, les conventions de développement, les contextes liés à Git ou GitHub, ainsi que dans les noms techniques, commandes, variables et concepts propres aux outils.

### Roadmap

**Statut :** Validé  
**Domaine :** Production

**Définition :** Vue d’ensemble planifiée des orientations, priorités et étapes du projet dans le temps.

### UI

**Statut :** Validé  
**Domaine :** Interface, développement

**Définition :** Ensemble des éléments d’interface permettant de présenter des informations et de recevoir les interactions de l’utilisateur.

**Forme développée :** *User Interface*.

### VFX

**Statut :** Validé  
**Domaine :** Art, développement

**Définition :** Effets visuels produits pour enrichir la présentation et la lisibilité du jeu.

**Forme développée :** *Visual Effects*.

### Workflow

**Statut :** Validé  
**Domaine :** Production, développement

**Définition :** Organisation d’une suite de tâches, d’interventions et de validations destinée à produire un résultat.

## 11. Modèles, documents et plateformes

### Free-to-Play

**Statut :** Validé  
**Domaine :** Modèle économique

**Définition :** Modèle dans lequel le jeu est accessible sans achat initial obligatoire et peut proposer des achats facultatifs.

**Abréviation officielle :** F2P

### Game Design Document

**Statut :** Validé  
**Domaine :** Documentation de conception

**Définition :** Document principal décrivant de manière structurée les règles, systèmes et mécaniques du jeu.

**Abréviation officielle :** GDD

### PvP

**Statut :** Validé  
**Domaine :** Mode de jeu

**Définition :** Type de contenu dans lequel des joueurs ou leurs équipes s’affrontent.

**Forme développée :** *Player versus Player*.

### iOS

**Statut :** Validé  
**Domaine :** Plateforme

**Définition :** Plateforme mobile d’Apple ciblée par Project Awakening.
