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

Les termes validés ne comportent pas de champ de statut : leur présence dans le glossaire indique qu’ils constituent la référence actuelle du projet.

Le champ **Statut** est réservé aux termes provisoires, aux propositions et aux autres éléments qui ne sont pas encore validés. Il précise alors explicitement la nature de leur incertitude.

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

**Domaine :** Projet

**Définition :** Nom officiel actuel et nom de code du projet. Il peut être utilisé uniformément dans la documentation, mais ne préjuge pas du futur titre commercial du jeu.

**Élément à préciser ultérieurement :**

* le titre commercial définitif du jeu.

### Licence originale

**Domaine :** Identité du projet

**Définition :** Propriété créative globale construite autour de Project Awakening et susceptible de réunir plusieurs œuvres, jeux ou produits.

**Terme à éviter :** « licence » sans qualification lorsque le contexte pourrait être confondu avec une licence logicielle.

### Licence logicielle

**Domaine :** Développement

**Définition :** Conditions juridiques encadrant l’utilisation, la modification et la distribution d’un logiciel ou de son code.

### Univers

**Domaine :** Univers narratif

**Définition :** Cadre fictionnel général de Project Awakening.

### Multivers

**Domaine :** Univers narratif

**Définition :** Structure interne de l’univers impliquant plusieurs mondes, réalités ou dimensions.

## 4. Créatures, monstres et cartes

### Créature

**Domaine :** Game design, univers, interface

**Définition :** Entité jouable collectionnée, possédée, développée et utilisée par le joueur. Les créatures composent l’équipe du joueur.

**Terme à éviter :** « monstre » pour désigner une entité jouable ou collectionnée.

### Monstre

**Domaine :** Game design, combats

**Définition :** Ennemi affronté par le joueur au cours des activités et des combats. Un monstre n’est pas une créature possédée par le joueur.

**Terme à éviter :** « monstre » pour désigner une créature jouable, y compris dans les expressions « carte de monstre », « famille de monstres » et « doublon de monstre ».

### Carte de créature

**Domaine :** Interface, représentation visuelle

**Définition :** Représentation visuelle et fonctionnelle d’une créature dans l’interface. La carte et la créature ne sont pas deux objets de progression distincts : le joueur possède une créature, représentée sous la forme d’une carte.

**Variante autorisée :** « carte » lorsque le contexte ne laisse aucune ambiguïté.

**Terme à éviter :** « carte de monstre » pour une créature du joueur.

Une éventuelle représentation d’un monstre ennemi sous forme de carte devra être explicitement qualifiée.

### Famille de créatures

**Domaine :** Game design, univers

**Définition :** Ensemble des formes appartenant à une même chaîne d’évolution.

**Variantes autorisées :**

* « famille » lorsque le contexte est explicite ;
* « lignée » ou « lignée évolutive » dans un contexte narratif.

**Terme à éviter :** « famille de monstres » pour les créatures collectionnées.

Les variantes narratives n’introduisent pas un niveau de regroupement supplémentaire.

### Forme de base

**Domaine :** Progression des créatures

**Définition :** Première forme d’une famille de créatures. Une invocation de créature donne accès à cette forme, jamais directement à la forme finale.

### Forme intermédiaire

**Domaine :** Progression des créatures

**Définition :** Forme située entre la forme de base et la forme finale dans une famille de créatures qui comporte trois formes.

**Terme à éviter :** « évolution intermédiaire » pour désigner la forme obtenue.

### Forme finale

**Domaine :** Progression des créatures

**Définition :** Dernière forme actuellement prévue dans la chaîne d’évolution d’une famille de créatures.

**Terme à éviter :** « évolution finale » pour désigner la forme obtenue.

### Évolution

**Domaine :** Progression des créatures

**Définition :** Processus permettant à une créature de passer d’une forme à la suivante.

**Terme à éviter :** « évolution » pour désigner une forme ou l’amélioration du niveau d’étoiles.

## 5. Progression, personnalisation et équipe

### Caractéristique

**Domaine :** Progression des créatures

**Définition :** Valeur principale propre à une créature et susceptible d’être influencée par sa progression et sa personnalisation.

Les **points de caractéristiques** sont attribués à la créature concernée lors de ses montées de niveau. Le joueur les répartit librement sur cette même créature afin d’augmenter ses caractéristiques selon le build souhaité.

**Terme à éviter :** « statistique » comme synonyme direct d’une caractéristique principale.

Chaque créature possède exactement six caractéristiques principales : les points de vie, l’Attaque, l’Attaque spéciale, la Défense, la Défense spéciale et l’Agilité.

### Points de vie

**Domaine :** Combat, progression des créatures

**Définition :** Caractéristique représentant la quantité de dégâts qu’une créature peut subir avant d’être mise hors combat.

**Abréviation officielle :** PV

Lors de la première introduction de la notion dans un document, la formulation « points de vie (PV) » peut être employée. L’abréviation peut ensuite être utilisée dans l’interface, les tableaux et les contextes nécessitant une forme compacte.

### Attaque

**Domaine :** Combat, progression des créatures

**Définition :** Caractéristique offensive intervenant par défaut dans le calcul des dégâts physiques.

### Attaque spéciale

**Domaine :** Combat, progression des créatures

**Définition :** Caractéristique offensive intervenant par défaut dans le calcul des dégâts spéciaux.

Le terme « spécial » ne désigne pas uniquement la magie. Il peut couvrir des capacités élémentaires, énergétiques, psychiques, techniques ou reposant sur une autre forme de puissance non physique.

### Défense

**Domaine :** Combat, progression des créatures

**Définition :** Caractéristique défensive protégeant par défaut contre les dégâts physiques.

### Défense spéciale

**Domaine :** Combat, progression des créatures

**Définition :** Caractéristique défensive protégeant par défaut contre les dégâts spéciaux.

### Agilité

**Domaine :** Combat, progression des créatures

**Définition :** Caractéristique liée au minimum à la vitesse d’une créature et à ses chances de coup critique.

L’Agilité constitue une base du calcul des chances de coup critique, sans en être nécessairement l’unique source. Son influence exacte sur l’ordre et la fréquence des actions reste à définir dans la documentation du combat.

### Dégâts physiques

**Domaine :** Combat

**Définition :** Catégorie de dégâts utilisant par défaut l’Attaque comme caractéristique offensive et la Défense comme caractéristique défensive.

### Dégâts spéciaux

**Domaine :** Combat

**Définition :** Catégorie de dégâts utilisant par défaut l’Attaque spéciale comme caractéristique offensive et la Défense spéciale comme caractéristique défensive.

Par défaut, une source de dégâts est physique ou spéciale. Toute source ne dépendant d’aucune caractéristique offensive, ignorant une défense, appliquant une valeur fixe ou suivant une règle particulière doit être déclarée explicitement.

Chaque compétence offensive doit déclarer sa catégorie de dégâts ainsi que la caractéristique offensive utilisée : Attaque, Attaque spéciale ou, exceptionnellement, aucune lorsqu’elle suit une formule particulière.

### Coup critique

**Domaine :** Combat

**Définition :** Résultat particulier pouvant modifier les dégâts d’une attaque selon des règles qui restent à définir.

Les dégâts physiques et spéciaux peuvent produire des coups critiques par défaut. Une compétence peut exceptionnellement les interdire si cette propriété est explicite. Les compétences, les équipements, les effets de statut et d’autres effets documentés peuvent modifier les chances de coup critique.

### Statistique

**Domaine :** Données, analyse, description générale

**Définition :** Terme général ou technique utilisé pour des valeurs calculées, des données, des résultats ou des statistiques globales. Il ne désigne pas les caractéristiques principales d’une créature.

### Niveau d’étoiles

**Domaine :** Progression des créatures

**Définition :** État actuel d’une créature dans le système d’étoiles.

### Amélioration du niveau d’étoiles

**Domaine :** Progression des créatures

**Définition :** Processus utilisant les doublons de créature afin d’augmenter progressivement le potentiel de la créature concernée.

**Termes à éviter :** « évolution d’étoiles » et « évolution des étoiles ».

### Objet

**Domaine :** Systèmes de jeu

**Définition :** Terme générique désignant un élément pouvant être obtenu et généralement stocké dans l’inventaire ou utilisé par un système du jeu.

Un équipement est une catégorie d’objet. Tous les objets ne sont pas des équipements.

### Inventaire

**Domaine :** Objets, ressources, interface

**Définition :** Espace consacré aux objets, aux ressources et aux autres éléments stockables du joueur.

L’inventaire reste distinct du système de collection. Il ne constitue pas l’espace de consultation des créatures et des skins de carte collectionnés.

### Équipement

**Domaine :** Progression, personnalisation

**Définition :** Catégorie d’objet pouvant être équipée par une créature afin de participer à sa personnalisation et à son fonctionnement.

**Variantes autorisées :**

* « équipement équipé » ;
* « équipement actuel » pour l’équipement actuellement attribué à une créature.

### Système d’équipement

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

**Domaine :** Créatures et cosmétiques

**Définition :** Notion qui doit toujours être qualifiée selon son domaine : **rareté d’une créature**, **rareté d’un skin de carte** ou **rareté d’un autre cosmétique**.

La rareté n’est pas automatiquement équivalente à la qualité.

### Qualité

**Domaine :** Équipements et objets

**Définition :** Notion utilisée pour qualifier un équipement et, si cela est validé ultérieurement, d’autres catégories d’objets. Elle doit rester qualifiée tant que ses échelles et ses effets ne sont pas entièrement définis.

La qualité n’est pas automatiquement équivalente à la rareté.

### Build de créature

**Domaine :** Game design

**Définition :** Ensemble des choix de personnalisation qui déterminent la manière dont une créature fonctionne, notamment ses caractéristiques, ses compétences et son équipement.

**Variante autorisée :** « build » lorsque le contexte de game design est explicite et sans ambiguïté.

### Build d’équipe

**Domaine :** Game design

**Définition :** Ensemble des choix de personnalisation et d’optimisation considérés à l’échelle d’une équipe.

Le terme doit rester qualifié. Une composition d’équipe ne doit pas être appelée simplement « build ».

### Équipe

**Domaine :** Game design

**Définition :** Ensemble concret de six créatures sélectionnées ou utilisées par le joueur.

Les monstres ennemis ne font pas partie de l’équipe du joueur.

### Composition d’équipe

**Domaine :** Game design, stratégie

**Définition :** Choix et organisation stratégique des créatures qui composent une équipe.

**Variante autorisée :** « composition » lorsque le contexte est explicite.

## 6. Éléments et affinités

### Élément

**Domaine :** Créatures, compétences, combat

**Définition :** Propriété représentant principalement la nature des pouvoirs, des capacités, des résistances et du style de combat d’une créature. Elle n’est pas déterminée uniquement par son apparence, son espèce, son habitat ou son histoire.

Chaque forme d’une créature déclare explicitement un ou deux éléments au maximum. Une évolution peut ajouter, perdre ou remplacer un élément lorsque l’évolution des pouvoirs, des capacités, des résistances ou du style de combat le justifie.

Les neuf éléments officiels sont :

1. Feu ;
2. Eau ;
3. Terre ;
4. Vent ;
5. Plante ;
6. Métal ;
7. Électricité ;
8. Lumière ;
9. Ténèbres.

**Terme à éviter :** « Lumineux » comme nom de l’élément. Le mot reste autorisé comme adjectif.

### Créature mono-élément

**Domaine :** Créatures, éléments

**Définition :** Créature possédant un seul élément dans sa forme actuelle.

### Créature bi-élément

**Domaine :** Créatures, éléments

**Définition :** Créature possédant deux éléments dans sa forme actuelle. Ses deux éléments sont mécaniquement égaux et ne sont pas hiérarchisés comme principal et secondaire.

Les affinités des deux éléments se combinent de manière multiplicative. Deux faiblesses ou deux résistances peuvent produire une interaction renforcée ; une faiblesse et une résistance peuvent se neutraliser. La présence de deux éléments ne confère aucun avantage ou désavantage global automatique.

Toutes les combinaisons sont autorisées par défaut. Une interdiction éventuelle doit répondre à un problème de conception ou d’équilibrage explicitement identifié.

### Affinité élémentaire

**Domaine :** Éléments, combat

**Définition :** Relation entre l’élément d’une compétence offensive et le ou les éléments de sa cible, déterminant une faiblesse, une résistance ou une interaction neutre.

Les relations de la table élémentaire sont réciproques. Un élément résiste à lui-même. Le nombre exact de forces et de faiblesses de chaque élément doit respecter une plage commune qui reste à définir.

### Faiblesse élémentaire

**Domaine :** Éléments, combat

**Définition :** Affinité dans laquelle l’élément d’une compétence offensive est efficace contre un élément de la cible.

### Résistance élémentaire

**Domaine :** Éléments, combat

**Définition :** Affinité dans laquelle un élément de la cible réduit l’efficacité de l’élément d’une compétence offensive.

### Interaction neutre

**Domaine :** Éléments, combat

**Définition :** Résultat d’une confrontation entre deux éléments lorsqu’aucune faiblesse ni résistance ne s’applique.

Cette notion ne doit pas être confondue avec une compétence sans élément.

### Faiblesse renforcée

**Domaine :** Éléments, combat

**Définition :** Résultat pouvant être produit lorsqu’une compétence rencontre la même faiblesse sur les deux éléments d’une créature bi-élément.

### Résistance renforcée

**Domaine :** Éléments, combat

**Définition :** Résultat pouvant être produit lorsqu’une compétence rencontre la même résistance sur les deux éléments d’une créature bi-élément.

### Compétence sans élément

**Domaine :** Compétences, éléments

**Définition :** Compétence qui ne possède aucun élément. Une compétence offensive possède exactement un élément ou est explicitement déclarée sans élément ; elle ne possède pas deux éléments simultanément dans le système initial.

### Immunité élémentaire

**Domaine :** Éléments, combat

**Définition :** Propriété particulière empêchant explicitement une interaction ou ses effets. Elle ne provient pas automatiquement de la table élémentaire de base, qui ne contient aucune immunité générale.

Par défaut, une immunité explicitement déclarée domine une faiblesse élémentaire, sauf règle contraire elle aussi explicite.

**Question ouverte :**

* L’existence d’un bonus lorsqu’une compétence partage un élément avec la créature qui l’utilise.

**Éléments à préciser ultérieurement :**

* La table exacte des affinités, les plages communes de forces et de faiblesses et les coefficients applicables aux interactions simples ou renforcées.

## 7. Effets de statut

### Effet de statut

**Domaine :** Combat, compétences, créatures

**Définition :** Modification temporaire appliquée dans le cadre du combat afin d’influencer une créature ou une règle de combat.

Un effet de statut peut cumuler plusieurs fonctions : modifier des caractéristiques, limiter ou empêcher des actions, produire un effet continu, réagir à un événement ou modifier temporairement une règle. Les compétences en constituent une source principale, mais d’autres systèmes explicitement documentés peuvent en appliquer, modifier ou retirer.

L’association entre un effet de statut et un élément est facultative. Elle doit être déclarée explicitement et ne peut pas être déduite uniquement de son nom ou de son apparence.

### Effet positif

**Domaine :** Effets de statut

**Définition :** Effet de statut constituant un avantage pour la créature concernée.

### Effet négatif

**Domaine :** Effets de statut

**Définition :** Effet de statut constituant un désavantage pour la créature concernée.

### Effet neutre

**Domaine :** Effets de statut

**Définition :** Effet de statut ne constituant objectivement ni un avantage ni un désavantage. Cette polarité doit rester rare.

### Résistance à un effet de statut

**Domaine :** Effets de statut, combat

**Définition :** Propriété pouvant limiter l’application ou, si cela est défini ultérieurement, la durée ou l’intensité d’un effet de statut.

Cette propriété ne constitue pas une septième caractéristique principale. Les mécanismes portant sur l’application, la durée et l’intensité restent distincts et ne sont pas tous considérés comme validés.

### Immunité à un effet de statut

**Domaine :** Effets de statut, combat

**Définition :** Propriété empêchant totalement l’application d’un effet de statut dans le périmètre explicitement déclaré.

### Retirer un effet de statut

**Domaine :** Effets de statut, compétences

**Définition :** Action générique mettant fin à un effet avant son expiration normale. Chaque effet doit préciser s’il peut être retiré et, le cas échéant, selon quelles conditions générales.

Des termes spécialisés comme « dissiper », « purifier » ou « soigner » ne doivent être employés comme actions distinctes que si leur sens est défini dans la documentation spécialisée.

### Coexistence et cumul des effets de statut

**Domaine :** Effets de statut, combat

**Définition :** Des effets différents peuvent coexister sur une même créature. Chaque effet définit individuellement le comportement de plusieurs applications identiques, notamment leur absence d’accumulation, leur renouvellement, leur durée, leur intensité, leurs instances ou leur remplacement.

Des incompatibilités entre certains effets peuvent être déclarées lorsqu’elles sont explicitement documentées.

**Éléments à préciser ultérieurement :**

* La liste des effets de statut, leurs conditions et chances d’application, leurs durées, leurs valeurs, leurs règles individuelles de cumul et de renouvellement, leurs interactions, leur retrait ainsi que les mécanismes détaillés de résistance et d’immunité.

## 8. Acquisition, hasard et récompenses

### Obtention de créature

**Domaine :** Acquisition des créatures

**Définition :** Processus permettant au joueur d’ajouter une créature jouable à sa collection.

L’invocation constitue la voie principale d’obtention. Certaines créatures peuvent néanmoins être accordées directement par le gameplay comme exceptions explicitement documentées.

### Invocation de créature

**Domaine :** Acquisition des créatures

**Définition :** Système principal d’acquisition aléatoire de créatures. Une invocation de créature permet d’obtenir la forme de base d’une famille de créatures.

**Variante autorisée :** « invocation » lorsque le contexte ne crée aucune ambiguïté.

**Terme à éviter :** « invocation » pour l’ouverture d’un contenu cosmétique, d’un objet ou d’un coffre.

### Ressource générale d’invocation

**Statut :** Provisoire — modèle initial à confirmer

**Domaine :** Acquisition des créatures, économie

**Définition :** Ressource générale envisagée pour effectuer les invocations de créatures dans le modèle initial.

Cette ressource doit être obtenue principalement en jouant. L’ajout de ressources événementielles ou de catégories particulières d’invocation n’est pas validé.

### Œuf

**Statut :** Provisoire — présentation visuelle non validée

**Domaine :** Invocation de créature, interface, animation

**Définition :** Présentation visuelle qui pourrait précéder la révélation d’une créature lors d’une invocation.

Le terme ne remplace pas « invocation de créature » et ne doit pas être présenté comme le nom officiel du système.

### Éclosion

**Statut :** Provisoire — présentation visuelle non validée

**Domaine :** Invocation de créature, interface, animation

**Définition :** Animation ou étape de révélation qui pourrait être associée à un œuf dans une future présentation de l’invocation.

Le terme ne constitue pas un synonyme officiel d’« invocation de créature ».

### Ouverture d’un paquet de skins de carte

**Domaine :** Acquisition, cosmétiques

**Définition :** Action qui révèle les skins de carte contenus dans un paquet de skins de carte.

**Variante autorisée :** « ouverture » lorsque le contexte cosmétique ne crée aucune ambiguïté.

**Terme à éviter :** « ouverture de paquet » pour désigner une invocation de créature.

### Tirage

**Domaine :** Conception interne, technique

**Définition :** Terme générique interne décrivant une sélection aléatoire.

**Terme à éviter :** « tirage » comme nom officiel d’une fonctionnalité destinée au joueur lorsqu’un terme fonctionnel plus précis, comme « invocation de créature » ou « ouverture d’un paquet de skins de carte », s’applique.

### Gacha

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
| **Ouvrir** | Révéler les skins contenus dans un paquet de skins de carte ou le contenu d’un coffre éventuel. |
| **Invoquer** | Effectuer une invocation de créature. |
| **Équiper** | Attribuer un équipement à une créature. |
| **Appliquer** | Attribuer un skin de carte à la carte d’une créature. |
| **Récupérer** | Recevoir un objet ou une récompense afin de l’ajouter à l’inventaire ou au compte. |

Le verbe « sélectionner » peut décrire le choix effectué dans un menu, mais l’action fonctionnelle portant sur un skin de carte reste « appliquer ».

**Termes à éviter :**

* « équiper un skin de carte » ;
* « appliquer un équipement ».

### Récompense

**Domaine :** Systèmes de jeu

**Définition :** Élément ou bénéfice remis au joueur à la suite d’une activité, d’un objectif, d’un événement ou d’un autre système prévu par le jeu.

Certaines créatures et certains skins de carte peuvent être remis directement comme récompenses de gameplay lorsque cette méthode d’obtention est explicitement documentée. Cette possibilité ne confirme pas qu’un équipement ou un coffre puisse être remis directement comme récompense.

### Récompense ayant un effet sur la progression

**Domaine :** Progression, économie

**Définition :** Récompense qui influence directement ou indirectement la progression du joueur.

**Terme à éviter :** « récompense utile », qui pourrait suggérer qu’une récompense cosmétique serait inutile.

### Récompense cosmétique

**Domaine :** Cosmétiques, économie

**Définition :** Récompense qui modifie ou enrichit la présentation visuelle sans conférer d’effet sur la progression ou les caractéristiques de jeu.

### Gain

**Domaine :** Description générale

**Définition :** Résultat générique obtenu par le joueur. Ce terme ne précise ni la nature du résultat ni son mode d’acquisition.

### Monnaie

**Domaine :** Économie

**Définition :** Valeur échangeable contre des contenus ou des éléments définis.

Une monnaie peut être considérée techniquement comme une catégorie de ressource, mais « monnaie » et « ressource » ne sont pas synonymes dans la documentation fonctionnelle.

### Ressource

**Domaine :** Progression, systèmes de jeu

**Définition :** Élément consommable utilisé par un système de progression ou de jeu.

## 9. Collection, illustrations, cosmétiques et commerce

### Système de collection

**Domaine :** Collection, interface

**Définition :** Fonctionnalité globale permettant de consulter, d’organiser et de valoriser les éléments collectionnables.

Le système de collection comprend au minimum une partie consacrée aux créatures et une partie consacrée aux skins de carte. Ces deux catégories appartiennent au même espace général, mais ne sont pas mélangées dans une liste unique.

Le système de collection reste distinct de l’inventaire.

### Collection du joueur

**Domaine :** Collection

**Définition :** Ensemble des éléments collectionnables effectivement possédés ou débloqués par le joueur.

Ce terme n’inclut pas les objets, les ressources et les autres éléments stockables relevant de l’inventaire.

### Catalogue des créatures

**Domaine :** Collection, créatures

**Définition :** Ensemble des créatures disponibles ou connues dans le jeu, qu’elles soient possédées ou non par le joueur.

Les créatures qui doivent rester secrètes pour des raisons narratives, événementielles ou de découverte peuvent être masquées ou présentées sous forme de silhouette.

### Collection de créatures

**Domaine :** Collection, créatures

**Définition :** Ensemble des créatures possédées par le joueur.

La collection de créatures ne doit pas être confondue avec le catalogue des créatures, qui peut également comprendre des créatures non possédées.

### Collection de skins de carte

**Domaine :** Collection, cosmétiques

**Définition :** Ensemble des skins de carte débloqués par le joueur.

### Série de skins de carte

**Domaine :** Collection, cosmétiques

**Définition :** Regroupement thématique cohérent de plusieurs skins de carte.

Une série distribuée par paquets est associée à des paquets de skins de carte dont tous les contenus possibles appartiennent à cette même série.

Une série de skins de carte n’est ni un produit ni une offre commerciale, même si les paquets permettant d’obtenir ses skins peuvent être achetés dans la boutique cosmétique.

**Terme à éviter :** « collection d’illustrations » pour désigner une série de skins de carte ou une offre commerciale.

### Catégorie de skins obtenus hors paquets

**Statut :** Provisoire — nom officiel à définir

**Domaine :** Collection, cosmétiques

**Définition :** Regroupement prévu pour les skins de carte accordés directement par des récompenses de gameplay et n’appartenant à aucune série distribuée par paquets.

Cette catégorie peut notamment réunir des récompenses événementielles, de haut fait, narratives, de progression, commémoratives ou liées à une opération spéciale.

**Éléments à préciser ultérieurement :**

* le nom officiel de la catégorie ;
* sa structure ;
* ses règles de complétion.

### Progression de collection

**Domaine :** Collection

**Définition :** Mesure de l’avancement du joueur dans l’acquisition des éléments d’une collection ou d’un catalogue.

La progression de la collection de créatures et celle de la collection de skins de carte sont présentées séparément. Pour les skins de carte, elle est principalement suivie par série.

### Complétion d’une collection

**Domaine :** Collection

**Définition :** État atteint lorsque les conditions de progression définies pour une collection, un catalogue ou une série sont remplies.

La complétion d’une collection cosmétique ne confère aucun avantage automatique de puissance.

### Illustration

**Domaine :** Direction artistique

**Définition :** Œuvre visuelle produite pour représenter une créature.

Une illustration est un asset artistique. Elle n’est pas, à elle seule, le contenu cosmétique possédé par le joueur.

### Skin de carte

**Domaine :** Cosmétique, interface

**Définition :** Contenu cosmétique possédé par le joueur et utilisant une illustration spécifique pour modifier la représentation visuelle de la carte d’une créature.

Un skin de carte ne modifie ni la créature, ni ses caractéristiques, ni ses capacités. Le joueur **applique** un skin de carte ; il ne l’équipe pas.

**Variante autorisée :** « skin » lorsque le contexte ne laisse aucune ambiguïté.

**Élément à préciser ultérieurement :**

* un éventuel nom destiné au joueur, davantage lié à l’univers, pourra être défini lors de la conception de l’interface.

**Question ouverte :**

* La compatibilité d’un skin de carte avec une créature indépendamment de sa forme, avec une forme précise ou avec plusieurs formes compatibles.

### Rareté d’un skin de carte

**Domaine :** Cosmétique, acquisition, collection

**Définition :** Niveau visible déterminant notamment la fréquence d’obtention d’un skin de carte dans les paquets de sa série.

Les différentes raretés possèdent des probabilités d’obtention et des valeurs de conversion de doublon différentes. Elles concernent uniquement la fréquence d’obtention, la valeur de collection, la présentation visuelle et la valeur perçue du skin. Elles ne confèrent aucun avantage de jeu.

**Éléments à préciser ultérieurement :**

* les noms et le nombre des raretés ;
* leurs probabilités exactes ;
* les valeurs de conversion associées.

### Visuel

**Domaine :** Description générale

**Définition :** Terme générique désignant un élément visuel sans lui attribuer de statut artistique, cosmétique ou fonctionnel précis.

### Paquet de skins de carte

**Domaine :** Cosmétique, acquisition

**Définition :** Contenu cosmétique ouvrable permettant d’obtenir un nombre fixe de plusieurs skins de carte appartenant à une même série.

Un paquet peut être gagné en jouant ou acheté directement contre de l’argent réel dans la boutique cosmétique. Pour une même série, les paquets gratuits et payants possèdent le même ensemble de skins, les mêmes probabilités, le même nombre de skins, les mêmes règles de doublons et les mêmes règles d’ouverture.

Tous les emplacements sont déterminés aléatoirement selon les probabilités associées aux raretés. Aucun emplacement ne garantit automatiquement une rareté, un skin précis ou un skin non possédé.

**Variante autorisée :** « paquet » lorsque le contexte cosmétique ne crée aucune ambiguïté.

**Termes à éviter :**

* « pack d’illustrations » ;
* « coffre » comme synonyme d’un paquet de skins de carte ;
* « invocation » pour l’ouverture d’un paquet.

**Élément à préciser ultérieurement :**

* le nombre exact de skins contenus dans un paquet.

### Produit

**Domaine :** Monétisation

**Définition :** Élément pouvant être acheté contre de l’argent réel.

### Offre

**Domaine :** Monétisation

**Définition :** Présentation commerciale, temporaire ou permanente, d’un ou de plusieurs produits.

Une offre peut notamment présenter un ou plusieurs paquets de skins de carte appartenant à une même série.

### Offre commerciale

**Domaine :** Monétisation

**Définition :** Terme générique désignant un produit ou une offre permettant d’obtenir du contenu.

Les termes « produit » et « offre » restent prioritaires lorsque leur distinction est nécessaire. Une offre commerciale ne doit pas être appelée « collection ».

### Doublon de créature

**Domaine :** Progression des créatures

**Définition :** Nouvelle obtention d’une créature déjà possédée, utilisée pour améliorer le niveau d’étoiles de cette créature.

**Terme à éviter :** « doublon de monstre ».

### Doublon de skin de carte

**Domaine :** Cosmétique, économie

**Définition :** Nouvelle obtention d’un skin de carte déjà débloqué, convertie en monnaie de conversion des doublons selon la valeur fixe associée à sa rareté.

**Variante autorisée :** « doublon » lorsque le contexte cosmétique ne laisse aucune ambiguïté.

### Monnaie de conversion des doublons

**Statut :** Provisoire — nom descriptif interne  
**Domaine :** Économie, cosmétiques

**Définition :** Monnaie cosmétique permanente provenant de la conversion des doublons de skins de carte et utilisable dans le catalogue de conversion.

Chaque rareté possède une valeur de conversion fixe différente. Cette monnaie ne permet d’obtenir aucune créature, invocation, ressource de progression, équipement, récompense de combat ou autre forme de puissance.

**Élément à préciser ultérieurement :**

* le nom définitif destiné au joueur sera choisi selon l’univers, l’identité visuelle et l’interface.

### Boutique

**Domaine :** Interface, monétisation

**Définition :** Interface exclusivement consacrée à la consultation et à l’achat de contenus et de produits cosmétiques.

Dans le modèle initial, la boutique permet notamment d’acheter directement contre de l’argent réel des paquets de skins de carte. Elle ne vend aucune créature, invocation, ressource de progression, équipement, avantage de combat ou autre forme de puissance.

**Variante autorisée :** « boutique cosmétique » lorsqu’il est utile de rappeler explicitement son périmètre.

### Catalogue commercial

**Domaine :** Monétisation

**Définition :** Ensemble des produits proposés contre de l’argent réel.

### Catalogue de conversion

**Domaine :** Économie, cosmétiques

**Définition :** Ensemble des contenus strictement cosmétiques accessibles avec la monnaie de conversion des doublons.

Un catalogue désigne un ensemble de contenus disponibles ; la boutique désigne l’interface qui les présente.

## 10. Modes de jeu et combats

### Mode de jeu

**Domaine :** Game design

**Définition :** Activité ou type de contenu proposé au joueur, par exemple l’histoire, un boss, une tour ou le PvP.

### Mode de contrôle du combat

**Domaine :** Combat

**Définition :** Manière dont les actions sont contrôlées pendant un combat, notamment le combat automatique ou semi-automatique.

**Terme à éviter :** « mode de jeu » pour désigner le degré d’automatisation d’un combat.

## 11. Conception, expérience et intelligence artificielle

### Game design

**Domaine :** Conception

**Définition :** Discipline et travail de conception des règles, des systèmes, des mécaniques, des équilibres et des interactions du jeu.

**Variante autorisée :** « conception de jeu » dans un passage explicatif.

### Gameplay

**Domaine :** Conception

**Définition :** Manière dont le jeu fonctionne concrètement lorsqu’il est joué, à travers ses mécaniques et ses interactions.

**Terme à éviter :** « expérience de jeu » comme synonyme exact.

### Expérience de jeu

**Domaine :** Expérience joueur

**Définition :** Ensemble plus large de ce que le joueur ressent et perçoit, au-delà du seul fonctionnement des mécaniques et des interactions.

### Intelligence artificielle

**Domaine :** Production, technique

**Définition :** Technologie générale utilisée pour assister certaines activités de recherche, de conception, de documentation, de développement, de production et de test.

**Abréviation officielle :** IA

### Outil d’IA

**Domaine :** Production, technique

**Définition :** Logiciel ou service utilisant l’intelligence artificielle.

### Agent IA

**Domaine :** Production, technique

**Définition :** Système disposant d’un objectif, d’un contexte, de règles et d’une certaine capacité d’action dans un workflow.

Les assistants autorisés à intervenir sur le repository, à lire son contenu ou à modifier ses fichiers peuvent être désignés comme des agents IA.

## 12. Développement et production

Les termes de cette section conservent leur forme anglaise conventionnelle dans la documentation technique et de production.

### Analytics

**Domaine :** Développement, exploitation

**Définition :** Collecte et analyse de données et d’indicateurs afin de comprendre l’utilisation du jeu et d’évaluer son fonctionnement.

### API

**Domaine :** Développement

**Définition :** Interface permettant à des logiciels ou composants d’échanger selon des règles définies.

**Forme développée :** *Application Programming Interface*.

### Asset

**Domaine :** Production, développement

**Définition :** Ressource numérique utilisée ou intégrée dans la production du jeu, par exemple une illustration, un son ou un fichier d’interface.

**Terme à éviter :** « ressource » lorsque cette traduction créerait une confusion avec une ressource de jeu.

### Backend

**Domaine :** Développement

**Définition :** Partie technique chargée des traitements, services et données qui ne relèvent pas directement de l’interface visible par le joueur.

### Build logiciel

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

**Domaine :** Développement

**Définition :** Cadre technique fournissant une structure, des conventions et des composants réutilisables pour développer une application ou une partie du jeu.

### Free Tier

**Domaine :** Production, services techniques

**Définition :** Niveau d’utilisation gratuit proposé par un service, généralement soumis à des limites.

### Frontend

**Domaine :** Développement

**Définition :** Partie d’un logiciel chargée de la présentation et des interactions directement accessibles à l’utilisateur.

### Open source

**Domaine :** Développement, production

**Définition :** Qualifie un logiciel dont le code source est accessible et dont la licence logicielle encadre les possibilités d’utilisation, de modification et de distribution.

### Pipeline

**Domaine :** Développement, production

**Définition :** Enchaînement organisé d’étapes permettant de transformer, vérifier, intégrer ou livrer des éléments du projet.

### Repository

**Domaine :** Développement

**Définition :** Espace versionné contenant les fichiers, le code et la documentation du projet.

**Variante française autorisée :** « dépôt » dans le texte courant ou explicatif.

Le terme **repository** est prioritaire dans les définitions techniques, les conventions de développement, les contextes liés à Git ou GitHub, ainsi que dans les noms techniques, commandes, variables et concepts propres aux outils.

### Roadmap

**Domaine :** Production

**Définition :** Vue d’ensemble planifiée des orientations, priorités et étapes du projet dans le temps.

### UI

**Domaine :** Interface, développement

**Définition :** Ensemble des éléments d’interface permettant de présenter des informations et de recevoir les interactions de l’utilisateur.

**Forme développée :** *User Interface*.

### VFX

**Domaine :** Art, développement

**Définition :** Effets visuels produits pour enrichir la présentation et la lisibilité du jeu.

**Forme développée :** *Visual Effects*.

### Workflow

**Domaine :** Production, développement

**Définition :** Organisation d’une suite de tâches, d’interventions et de validations destinée à produire un résultat.

## 13. Modèles, documents et plateformes

### Free-to-Play

**Domaine :** Modèle économique

**Définition :** Modèle dans lequel le jeu est accessible sans achat initial obligatoire et peut proposer des achats facultatifs.

**Abréviation officielle :** F2P

### Game Design Document

**Domaine :** Documentation de conception

**Définition :** Document principal décrivant de manière structurée les règles, systèmes et mécaniques du jeu.

**Abréviation officielle :** GDD

### PvP

**Domaine :** Mode de jeu

**Définition :** Type de contenu dans lequel des joueurs ou leurs équipes s’affrontent.

**Forme développée :** *Player versus Player*.

### Android

**Domaine :** Plateforme

**Définition :** Plateforme mobile de Google ciblée par Project Awakening.

### iOS

**Domaine :** Plateforme

**Définition :** Plateforme mobile d’Apple ciblée par Project Awakening.
