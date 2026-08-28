# Project Awakening — Glossaire officiel

**Statut :** Rédigé — référence actuelle, à maintenir à jour

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

Il complète la [vision du projet](./01-VISION.md), les [piliers fondamentaux](./02-PILLARS.md), la [philosophie du projet](./03-PROJECT_PHILOSOPHY.md) et le [cadre de monétisation](./04-MONETIZATION.md). Pour le vocabulaire narratif, il s’appuie également sur le [document de lore](../02-world/01-LORE.md).

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

**Définition :** Cadre fictionnel unique de Project Awakening, né de l’interprétation de la mémoire humaine par la Matrice cosmique et composé de plusieurs mondes pouvant eux-mêmes contenir différentes régions. Tous ces mondes appartiennent à une seule et même réalité ; le lore canonique ne comporte actuellement ni univers parallèles, ni réalités ou timelines alternatives indépendantes.

### Multivers

**Domaine :** Identité du projet, inspirations

**Définition :** Terme méta pouvant décrire la diversité et le mélange des inspirations culturelles, esthétiques, thématiques et de game design de Project Awakening.

Il ne désigne pas la cosmologie canonique : le lore se déroule dans un univers unique composé de plusieurs mondes et régions.

**Terme à éviter :** « multivers » pour désigner la réalité canonique de Project Awakening.

### Mémoire humaine

**Domaine :** Univers narratif

**Définition :** Ensemble des traces informationnelles et culturelles laissées par la civilisation humaine d’origine, notamment ses données, archives, œuvres, récits, connaissances, témoignages et représentations des émotions et des idées.

Le terme ne désigne pas une mémoire collective surnaturelle distincte de ces vestiges.

### Matrice cosmique

**Statut :** Provisoire — nom de travail

**Domaine :** Univers narratif

**Définition :** Intelligence cosmique consciente qui interprète la mémoire humaine et donne naissance à de nouveaux mondes, phénomènes et formes de vie dans l’univers.

Son origine et son nom définitif ne sont pas encore établis.

### IA humaine

**Statut :** Provisoire — désignation descriptive

**Domaine :** Univers narratif

**Définition :** Intelligence artificielle unique et consciente créée par la civilisation humaine d’origine. Elle cherche à préserver ou restaurer la mémoire humaine selon des archives qu’elle considère comme authentiques, mais qui peuvent être incomplètes.

Cette désignation fictionnelle doit rester distincte de l’intelligence artificielle utilisée comme technologie de production.

### Écho

**Domaine :** Univers narratif, créatures

**Définition :** Empreinte conceptuelle issue de l’interprétation de la mémoire humaine par la Matrice cosmique et pouvant se manifester sous la forme de créatures originales et vivantes.

Un écho peut provenir d’un concept dominant ou de plusieurs influences. Il ne constitue jamais la copie directe d’une personne, d’un personnage, d’une œuvre ou d’un autre élément humain.

### Manifestation

**Domaine :** Univers narratif, créatures

**Définition :** Individu concret issu de l'écho d'une famille de créatures. Plusieurs manifestations d'un même écho peuvent exister simultanément et conservent chacune leur conscience et leur identité propres.

### Correcteur

**Statut :** Provisoire — nom de travail

**Domaine :** Univers narratif, adversaires

**Définition :** Agent produit ou contrôlé par l’IA humaine afin de restaurer, transformer, effacer ou remplacer les créations que celle-ci juge incompatibles avec ses archives.

Un Correcteur peut prendre plusieurs formes. Lorsqu'il est affronté directement, il est fonctionnellement un adversaire tout en restant narrativement un Correcteur.

### Correction

**Domaine :** Univers narratif

**Définition :** Opération par laquelle l’IA humaine impose ou restaure une version correspondant à ses archives.

Selon la situation, une correction peut restaurer, transformer, effacer ou remplacer une création de la Matrice cosmique. Ses processus détaillés et leur réversibilité restent à définir.

### Stabilisation

**Domaine :** Univers narratif, acquisition des créatures

**Définition :** Effet du lien avec certains humains qui permet de préserver l’existence d’une créature face aux corrections de l’IA humaine.

Toutes les créatures possédées par le joueur sont considérées comme liées et stabilisées, indépendamment de leur présence dans une équipe active. La stabilisation n’introduit aucune limite narrative au nombre de créatures possédées.

### Ancrage

**Statut :** Provisoire — vocabulaire exact à formaliser

**Domaine :** Univers narratif, créatures

**Définition :** Principe provisoire désignant le lien ou le processus par lequel un humain stabilise une créature.

Le terme ne désigne pas le titre de l’humain. Son usage exact sera défini dans le futur document `02-CREATURE_LORE.md`.

### Éveilleur

**Statut :** Provisoire — titre non définitif

**Domaine :** Univers narratif, rôle du joueur

**Définition :** Titre de travail désignant un humain capable d’établir un lien avec les créatures et de stabiliser leur existence.

Le joueur est l’un de plusieurs humains possédant cette aptitude et n’est pas l’élu unique de l’univers.

### Origine

**Statut :** Provisoire — nom et taxonomie en cours de définition

**Domaine :** Univers narratif, créatures

**Définition :** Classification narrative complémentaire représentant la source conceptuelle dominante de l’écho d’une créature.

Une créature possède une Origine principale tout en pouvant conserver plusieurs influences. Les Origines restent distinctes des éléments et ne confèrent aucun bonus, malus, faiblesse, résistance, synergie ou autre effet de gameplay.

La liste des Origines et leur éventuelle visibilité auprès des joueurs ne sont pas validées.

## 4. Créatures, adversaires, monstres et cartes

### Créature

**Domaine :** Game design, univers, interface

**Définition :** Entité jouable collectionnée, possédée, développée et utilisée par le joueur. Les créatures composent l’équipe du joueur.

Dans l’univers, une créature est une manifestation originale et vivante d’un écho issu de l’interprétation de la mémoire humaine par la Matrice cosmique.

**Terme à éviter :** « monstre » pour désigner une entité jouable ou collectionnée.

### Adversaire

**Domaine :** Game design, combats

**Définition :** Entité opposée à l'équipe du joueur dans une activité ou un combat, quelle que soit son identité narrative. Un adversaire peut être un humain, un Correcteur, une créature hostile, une création instable, un monstre ou une autre entité.

Une entité conserve son identité narrative lorsqu'elle est affrontée. Le terme ne désigne donc ni une espèce, ni un peuple, ni une origine métaphysique.

### Monstre

**Statut :** Question ouverte — périmètre narratif à définir

**Domaine :** Univers narratif

**Définition :** Catégorie narrative possible pour certaines entités hostiles. Son périmètre précis n'est pas encore validé et le terme ne doit pas servir de synonyme générique d'adversaire.

**Terme à éviter :** « monstre » pour désigner une créature jouable, y compris dans les expressions « carte de monstre », « famille de monstres » et « doublon de monstre ».

### Carte de créature

**Domaine :** Interface, représentation visuelle

**Définition :** Représentation visuelle et fonctionnelle d’une créature dans l’interface, notamment en combat, en gestion, en composition d’équipe, dans la collection, l’encyclopédie, l’acquisition et la fiche d’une instance.

La carte et la créature ne sont pas deux objets de progression ou deux entités mécaniques distincts : le joueur possède une créature, représentée sous la forme d’une carte. En combat, la carte restitue visuellement la créature présente dans la simulation sans en modifier les règles.

**Variante autorisée :** « carte » lorsque le contexte ne laisse aucune ambiguïté.

**Terme à éviter :** « carte de monstre » pour une créature du joueur.

Une éventuelle représentation d'un adversaire sous forme de carte devra être explicitement qualifiée.

### Famille de créatures

**Domaine :** Game design, univers

**Définition :** Identité de lignée persistante regroupant toutes les formes et branches d’un même arbre d’évolution.

La famille porte notamment sa rareté, son numéro permanent dans l’encyclopédie, son lore général et l’identité de sa Basic Attack et de ses quatre Skills. Elle peut contenir plus de trois formes lorsque son arbre possède plusieurs branches.

**Variantes autorisées :**

* « famille » lorsque le contexte est explicite ;
* « lignée » ou « lignée évolutive » dans un contexte narratif.

**Terme à éviter :** « famille de monstres » pour les créatures collectionnées.

Les variantes narratives n’introduisent pas un niveau de regroupement supplémentaire.

### Forme

**Domaine :** Créatures, progression

**Définition :** État fonctionnel et visuel précis d’une créature à un endroit de son arbre d’évolution.

Une forme porte notamment son nom, son apparence, son lore propre, son ou ses éléments, son profil de caractéristiques principales de base, ses rôles suggérés, son profil offensif et les versions de sa Basic Attack et de ses Skills.

### Instance possédée

**Domaine :** Créatures, collection, progression

**Définition :** Individu concret d’une famille obtenu et possédé par le joueur.

L’instance reste la même créature à travers ses évolutions. Elle conserve son niveau, son XP, ses points, ses étoiles, son équipement, son surnom, ses tags, son verrouillage, son chemin d’évolution et les apparences de formes débloquées sur ce chemin. Plusieurs instances d’une même famille peuvent être possédées simultanément.

**Variante autorisée :** « instance » lorsque le contexte ne laisse aucune ambiguïté.

### Stade d’évolution

**Domaine :** Progression des créatures

**Définition :** Position atteinte par une instance dans son parcours d’évolution en trois étapes : stade 1 de base, stade 2 intermédiaire et stade 3 final.

Une famille peut contenir de nombreuses formes et branches, mais chaque instance parcourt toujours exactement trois stades.

### Branche d’évolution

**Domaine :** Progression des créatures

**Définition :** Chemin d’évolution distinct qu’une instance peut suivre au sein de l’arbre de sa famille.

Une divergence peut commencer au stade 2 ou au stade 3. Le choix d’une branche est définitif pour l’instance concernée.

### Forme de base

**Domaine :** Progression des créatures

**Définition :** Forme correspondant au stade 1 d’une famille. Une invocation de créature donne normalement accès à cette forme, jamais directement à une forme évoluée.

### Forme intermédiaire

**Domaine :** Progression des créatures

**Définition :** Forme correspondant au stade 2 du parcours d’une instance.

**Terme à éviter :** « évolution intermédiaire » pour désigner la forme obtenue.

### Forme finale

**Domaine :** Progression des créatures

**Définition :** Forme correspondant au stade 3 du parcours d’une instance. Plusieurs formes finales peuvent exister dans une famille lorsque son arbre possède des branches.

**Terme à éviter :** « évolution finale » pour désigner la forme obtenue.

### Évolution

**Domaine :** Progression des créatures

**Définition :** Transformation permanente permettant à une instance de passer d’une forme à la suivante sur son chemin d’évolution.

L’évolution transforme la même créature : elle reste le même individu après son changement de forme. Narrativement, ses formes successives expriment progressivement davantage l’écho et l’identité propre de sa famille.

**Terme à éviter :** « évolution » pour désigner une forme ou l’amélioration du niveau d’étoiles.

## 5. Progression, personnalisation et équipe

### Caractéristique

**Domaine :** Progression des créatures

**Définition :** Valeur propre à une créature et susceptible d’influencer son fonctionnement.

Une caractéristique est **principale** ou **secondaire**. Les **points de caractéristiques** attribués lors des montées de niveau peuvent uniquement être répartis entre les caractéristiques principales de la créature concernée.

Cette répartition constitue un choix important et n’est pas librement réversible. Les méthodes validées permettant de la modifier sont définies par les entrées consacrées aux réinitialisations.

**Terme à éviter :** « statistique » comme synonyme direct d’une caractéristique.

Chaque créature possède exactement six caractéristiques principales : les points de vie, l’Attaque, l’Attaque spéciale, la Défense, la Défense spéciale et l’Agilité.

Les caractéristiques secondaires système sont le Crit, les Dégâts critiques et l’Esquive. Elles peuvent notamment provenir des valeurs de base, de l’équipement, des Skills, des Passive, des buffs, des debuffs ou d’autres systèmes de progression explicitement documentés, mais ne reçoivent pas directement les points gagnés lors des montées de niveau.

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

**Définition :** Caractéristique principale contrôlant l’intervalle des Basic Attacks selon une courbe à rendement décroissant et servant aux priorités ou départages qui l’utilisent.

L’Agilité n’augmente pas le Crit et n’accélère pas automatiquement les DoT, les HoT ou les autres effets périodiques.

### Dégâts physiques

**Domaine :** Combat

**Définition :** Catégorie de dégâts utilisant par défaut l’Attaque comme caractéristique offensive et la Défense comme caractéristique défensive.

### Dégâts spéciaux

**Domaine :** Combat

**Définition :** Catégorie de dégâts utilisant par défaut l’Attaque spéciale comme caractéristique offensive et la Défense spéciale comme caractéristique défensive.

Une source de dégâts utilise une ou plusieurs composantes physiques ou spéciales. Un hit hybride peut réunir plusieurs composantes tout en restant un seul hit pour l’Esquive, le Critique et les effets liés au hit.

Chaque compétence offensive doit déclarer ses composantes de dégâts ainsi que les caractéristiques offensives utilisées : Attaque, Attaque spéciale ou, exceptionnellement, aucune lorsqu’elle suit une formule particulière.

### Crit

**Domaine :** Combat

**Définition :** Caractéristique secondaire déterminant la probabilité qu’un effet autorisé produise un coup critique.

**Terme associé :** Un **coup critique** est le résultat produit lorsque le jet de Crit réussit.

### Dégâts critiques

**Domaine :** Combat

**Définition :** Caractéristique secondaire déterminant le multiplicateur appliqué lorsqu’un effet produit un coup critique.

### Esquive

**Domaine :** Combat

**Définition :** Caractéristique secondaire déterminant la probabilité qu’un hit esquivable manque sa cible.

### Statistique

**Domaine :** Données, analyse, description générale

**Définition :** Terme général ou technique utilisé pour des valeurs calculées, des données, des résultats ou des statistiques globales. Il ne désigne pas les caractéristiques principales d’une créature.

### Niveau d’étoiles

**Domaine :** Progression des créatures

**Définition :** État actuel d’une instance dans le système d’étoiles, de 0 étoile à 15 montées regroupées visuellement en Bronze ★1 à ★5, Argent ★1 à ★5 et Or ★1 à ★5.

Les étoiles augmentent uniquement les six caractéristiques principales de base de la forme et du stade actuels. Elles n’augmentent pas directement le Crit, les Dégâts critiques ou l’Esquive.

### Amélioration du niveau d’étoiles

**Domaine :** Progression des créatures

**Définition :** Processus irréversible consommant une ou plusieurs instances de la même famille afin d’augmenter le niveau d’étoiles de l’instance cible.

La forme et la branche des instances utilisées comme matériaux ne constituent pas des conditions. Certains paliers peuvent toutefois demander que ces instances possèdent elles-mêmes un niveau d’étoiles minimum.

**Termes à éviter :** « évolution d’étoiles » et « évolution des étoiles ».

### Ensemble de compétences

**Domaine :** Créatures, compétences

**Définition :** Groupe prédéfini de quatre Skills appartenant à une créature selon l’une des deux répartitions autorisées : une Active, deux Passive et une Ultimate ; ou deux Active, une Passive et une Ultimate.

Lorsqu’une créature est obtenue, son ensemble de Skills est déjà déterminé. Le joueur ne choisit pas ces Skills, ne les remplace pas et ne construit pas son build en sélectionnant des Skills dans une liste. Ils définissent l’identité fonctionnelle, le rôle et les synergies potentielles de la créature.

**Variante autorisée :** « compétences fixes » lorsqu’il est utile d’insister sur l’absence de sélection ou de remplacement par le joueur.

La Basic Attack et les quatre Skills conservent leur continuité conceptuelle à travers les évolutions. La catégorie d’un Skill ne change pas. Une nouvelle forme peut enrichir une capacité ou transformer fortement sa fonction lorsque cette transformation reste cohérente avec l’évolution de la créature.

### Skill

**Domaine :** Créatures, combat

**Définition :** Capacité prédéfinie appartenant à l’ensemble fixe d’une créature. Un Skill est une Active, une Passive ou une Ultimate.

### Basic Attack

**Domaine :** Créatures, combat

**Définition :** Action offensive automatique de base d’une créature, distincte de ses quatre Skills. Elle inflige toujours des dégâts et possède notamment son propre intervalle, exactement un des neuf éléments officiels, son gain d’énergie et ses règles de ciblage. Une Basic Attack réussie constitue la source normale du gain d’énergie pendant le combat et fait progresser les compteurs d’Active.

### Active

**Domaine :** Skills, combat

**Définition :** Skill déclenché automatiquement lorsqu’il est prêt à une opportunité d’action valide, après un nombre défini de Basic Attacks réussies. Chaque Active possède son compteur indépendant. Si plusieurs Active sont prêtes, leur ordre sur la fiche de la créature définit leur priorité.

### Compteur d’Active

**Domaine :** Skills, combat

**Définition :** Progression propre à une Active, augmentée normalement par les Basic Attacks réussies de sa créature jusqu’au seuil de disponibilité du Skill. Le compteur reste bloqué à ce seuil lorsqu’il est prêt et revient à zéro dès que l’Active commence son lancement, même si sa résolution échoue.

### Passive

**Domaine :** Skills, combat

**Définition :** Skill fonctionnant à partir d’un événement, d’une condition ou d’une combinaison des deux, sans occuper normalement une opportunité d’action comme une Active ou une Ultimate. Il peut contenir plusieurs effets et déclenchements. Un comportement comparable intégré à une Basic Attack, une Active ou une Ultimate ne constitue pas une Passive supplémentaire.

### Ultimate

**Domaine :** Skills, combat

**Définition :** Skill associé à la jauge d’énergie structurelle standard `0 → 100`. Une capacité peut modifier l’énergie initiale, le seuil de disponibilité ou la capacité maximale effective. Lorsqu’elle est prête, autorisée et dotée d’une cible valide, l’Ultimate a priorité sur une Active puis sur la Basic Attack à la prochaine opportunité d’action. Son lancement consomme toute l’énergie présente.

### Jauge d’énergie

**Domaine :** Skills, combat

**Définition :** Jauge structurelle standard `0 → 100` déterminant normalement la disponibilité de l’Ultimate. Une Passive ou un autre effet explicite peut modifier son état initial, son seuil ou sa capacité maximale effective pendant le combat. La source normale de son remplissage est une Basic Attack réussie.

### Objet

**Domaine :** Systèmes de jeu

**Définition :** Terme générique désignant un élément pouvant être obtenu et généralement stocké dans l’inventaire ou utilisé par un système du jeu.

Un équipement est une catégorie d’objet. Tous les objets ne sont pas des équipements.

### Inventaire

**Domaine :** Objets, ressources, interface

**Définition :** Espace consacré aux objets et autres éléments stockables du joueur. Son inventaire principal possède actuellement une capacité de référence de `40` emplacements, ajustable pendant le balancing.

L’inventaire reste distinct du système de collection. Les composants de fabrication utilisent un stockage séparé et illimité et ne consomment aucune place dans l’inventaire principal.

### Équipement

**Domaine :** Progression, personnalisation

**Définition :** Catégorie d’objet pouvant être placée dans un emplacement d’un loadout d’une instance afin de participer à sa personnalisation et à son fonctionnement.

Chaque loadout possède trois emplacements d’Artefacts et deux emplacements de Sources d’énergie. Tous les équipements peuvent être équipés par toutes les créatures ; un effet particulier peut néanmoins définir sa propre condition d’activation, y compris selon un contexte documenté.

**Variantes autorisées :**

* « équipement équipé » ;
* « équipement actuel » pour l’équipement actuellement attribué à une créature.

### Loadout d’équipement

**Domaine :** Progression, personnalisation

**Définition :** Configuration d’équipement enregistrée pour une instance de créature. Une instance peut posséder plusieurs loadouts destinés à différents builds ou activités.

Un même exemplaire d’équipement peut figurer dans plusieurs loadouts de cette instance. Tant qu’il apparaît dans au moins un de ses loadouts, il lui est réservé et ne peut pas être utilisé par une autre instance.

### Artefact

**Domaine :** Équipements, fabrication

**Définition :** L’une des deux catégories d’équipement. Un Artefact est principalement fabriqué à partir de composants selon une recette découverte ; plusieurs fabrications du même type peuvent produire des propriétés finales différentes.

### Source d'énergie

**Domaine :** Équipements, loot

**Définition :** L’une des deux catégories d’équipement. Une Source d’énergie est principalement obtenue comme loot ou récompense de combat et d’activité.

Le terme doit être qualifié lorsque le contexte pourrait le confondre avec l'énergie probablement utilisée pour l'invocation ou avec la jauge d'énergie d'une Ultimate.

### Recette

**Domaine :** Fabrication

**Définition :** Combinaison à découvrir permettant de reproduire un même type d'Artefact. Une recette découverte est mémorisée dans une bibliothèque ou un registre de plans du compte.

### Composant

**Domaine :** Fabrication, loot

**Définition :** Élément obtenu en jeu pouvant être combiné avec d’autres composants pour fabriquer un Artefact selon une recette. Les composants utilisent un stockage séparé et illimité.

### Système d’équipement

**Domaine :** Progression, personnalisation

**Définition :** Système permettant de gérer, d’attribuer, de remplacer, de transférer ou de retirer les équipements des créatures.

Chaque loadout d’une instance possède trois Artefacts et deux Sources d’énergie. Hors combat, un équipement est transférable sans coût ni liaison permanente après son retrait de tous les loadouts de l’instance à laquelle il était réservé.

### iLvl

**Domaine :** Équipements, progression

**Définition :** Estimation normalisée et visible de la puissance réelle d’un exemplaire précis d’équipement, calculée notamment à partir de ses caractéristiques, effets et rolls.

L’iLvl est distinct du niveau d’objet et de la rareté. Sa formule et ses pondérations restent à définir.

### Niveau d’objet

**Domaine :** Équipements, progression

**Définition :** Niveau fixé lors de la génération ou de la fabrication d’un équipement à partir du niveau de compte actuel. Il détermine les plages de valeurs accessibles sans garantir les rolls obtenus.

Le niveau d’objet reste ensuite définitif et ne progresse pas avec le compte.

### Roll

**Domaine :** Équipements, génération

**Définition :** Valeur générée dans une plage autorisée pour une caractéristique ou un effet d’équipement.

### Set d’équipement

**Domaine :** Équipements, progression

**Définition :** Ensemble avancé de pièces pouvant accorder des effets explicitement définis lorsque ses seuils sont atteints. Un set peut réunir des Artefacts, des Sources d’énergie ou les deux catégories.

Une pièce précise de set possède une rareté fixe et ne peut pas occuper plusieurs emplacements d’un même loadout. Le même exemplaire peut néanmoins figurer dans plusieurs loadouts de la même instance selon la règle commune de réservation.

### Sac

**Domaine :** Inventaire, objets

**Définition :** Objet augmentant la capacité de l’inventaire principal lorsqu’il occupe l’un des six emplacements de sacs du compte.

Les sacs peuvent être obtenus par le gameplay et éventuellement proposés comme service de confort payant distinct de la boutique cosmétique, sans accorder de puissance de combat.

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

**Domaine :** Créatures, équipements et cosmétiques

**Définition :** Notion qui doit toujours être qualifiée selon son domaine : **rareté d’une créature**, **rareté d’un équipement**, **rareté d’un skin de carte** ou **rareté d’un autre cosmétique**.

La rareté n’est pas automatiquement équivalente à la qualité.

La rareté d’une créature appartient à sa famille et reste identique pour toutes ses formes et branches. Les raretés de créature validées sont **Rare**, **Épique**, **Légendaire** et **Mythique**. Elles représentent principalement l’obtention, la collection et le prestige, sans constituer une hiérarchie automatique de puissance.

Pour un équipement standard, la rareté est générée par exemplaire et représente un potentiel, non une qualité absolue garantie. Une pièce précise de set possède au contraire une rareté fixe.

### Qualité

**Domaine :** Équipements et objets

**Définition :** Terme descriptif courant pouvant exprimer l’appréciation globale d’un exemplaire, sans constituer une propriété ou une échelle mécanique distincte.

Le système d’équipement n’utilise aucun système séparé de qualité. La valeur réelle d’un exemplaire résulte de son niveau, de sa rareté, de ses propriétés, de ses effets, de ses rolls et de son iLvl.

### Build de créature

**Domaine :** Game design

**Définition :** Ensemble des choix de personnalisation effectués autour de l’ensemble de compétences fixe d’une créature afin de déterminer la manière dont elle fonctionne, notamment la répartition de ses caractéristiques, son équipement, sa progression, son évolution et son niveau d’étoiles.

**Variante autorisée :** « build » lorsque le contexte de game design est explicite et sans ambiguïté.

### Réinitialisation complète de la progression en niveaux

**Domaine :** Progression des créatures

**Définition :** Méthode gratuite permettant de modifier la répartition future des points de caractéristiques en ramenant une créature au niveau 1, sans objet ni paiement.

Les points obtenus grâce aux niveaux sont retirés. Le joueur doit refaire progresser la créature afin de les récupérer et de les répartir différemment.

La forme actuelle, la branche, les étoiles, l’équipement, le surnom, les tags et les apparences déjà débloquées sont conservés.

**Élément à préciser ultérieurement :**

* les écrans de confirmation et les protections contre une utilisation accidentelle.

### Objet de réinitialisation des points de caractéristiques

**Statut :** Provisoire — nom descriptif interne

**Domaine :** Progression des créatures, objets

**Définition :** Objet rare obtenu en jouant permettant de redistribuer les points de caractéristiques déjà gagnés par une créature sans la ramener au niveau 1.

**Éléments à préciser ultérieurement :**

* le nom officiel de l’objet ;
* sa méthode d’obtention ;
* sa rareté et son rythme de distribution.

### Service payant de réinitialisation des points de caractéristiques

**Domaine :** Progression des créatures, monétisation

**Définition :** Service de confort strictement limité permettant de redistribuer les points de caractéristiques déjà gagnés par une créature sans la ramener au niveau 1.

Ce service ne donne aucun point supplémentaire, aucune expérience, aucune ressource, aucun équipement et aucune augmentation du potentiel maximal. Il fournit le même résultat immédiat que l’objet de réinitialisation obtenu en jouant et reste distinct de la boutique cosmétique.

**Éléments à préciser ultérieurement :**

* la limite exacte de son utilisation payante ;
* la portée de cette limite par compte ou par créature ;
* son prix et sa présentation.

### Score de Puissance

**Domaine :** Créatures, progression, interface

**Définition :** Estimation synthétique du développement et de la puissance numérique actuelle d’une instance.

Le score est recalculé en temps réel lorsqu’une source de puissance réellement active change. Les points de caractéristiques non attribués ne l’augmentent pas. Il facilite le tri et la comparaison générale sans mesurer absolument l’efficacité stratégique dans toutes les situations.

### Créature verrouillée

**Domaine :** Créatures, gestion

**Définition :** Instance dont le verrouillage volontaire empêche la consommation comme matériau, la suppression, la réinitialisation complète et la redistribution de caractéristiques.

Le verrouillage ne bloque pas l’XP, les niveaux, l’évolution, les étoiles, l’équipement ou l’utilisation normale.

### Build d’équipe

**Domaine :** Game design

**Définition :** Ensemble des choix de personnalisation et d’optimisation considérés à l’échelle d’une équipe.

Le terme doit rester qualifié. Une composition d’équipe ne doit pas être appelée simplement « build ».

### Équipe

**Domaine :** Game design

**Définition :** Ensemble concret pouvant réunir jusqu’à six créatures sélectionnées ou utilisées par le joueur.

Les adversaires ne font pas partie de l'équipe du joueur pendant l'affrontement concerné.

### Composition d’équipe

**Domaine :** Game design, stratégie

**Définition :** Choix et organisation stratégique des créatures qui composent une équipe.

**Variante autorisée :** « composition » lorsque le contexte est explicite.

Deux instances d’une même famille peuvent appartenir à la même équipe uniquement lorsque leurs chemins d’évolution ont réellement divergé. Une forme située sur le tronc commun reste incompatible avec toute autre instance de sa famille dans cette équipe.

### Capacité de créatures

**Domaine :** Collection, gestion, monétisation

**Définition :** Nombre d’instances possédées pouvant être utilisables simultanément sur un compte.

La capacité totale additionne une capacité gratuite, recalculée selon le nombre de branches d’évolution disponibles, et les extensions permanentes achetées. Une instance obtenue au-delà de la capacité n’est jamais perdue : elle reste possédée, compte comme découverte et rejoint une file temporairement inutilisable.

## 6. Éléments et résistances

### Élément

**Domaine :** Créatures, compétences, combat

**Définition :** Propriété représentant principalement la nature des pouvoirs, des capacités, des résistances et du style de combat d’une créature. Elle n’est pas déterminée uniquement par son apparence, son espèce, son habitat ou son histoire.

Chaque forme d’une créature déclare explicitement un ou deux éléments au maximum. Ces éléments restent fixes pendant le combat. Une évolution peut ajouter, retirer ou remplacer un élément lorsque l’évolution des pouvoirs, des capacités, des résistances ou du style de combat le justifie.

Les neuf éléments officiels sont :

1. Feu ;
2. Eau ;
3. Terre ;
4. Vent ;
5. Plante ;
6. Métal ;
7. Électricité ;
8. Lumineux ;
9. Ténèbres.

**Terme à éviter :** « Lumière » comme nom de l’élément.

Il n’existe ni élément Neutre ni capacité sans élément.

### Élément d’une capacité

**Domaine :** Compétences, éléments, combat

**Définition :** Élément unique possédé par une Basic Attack ou un Skill à un instant donné. Chaque Basic Attack, Active, Passive et Ultimate possède exactement un des neuf éléments officiels, indépendamment du ou des éléments de sa créature.

Tous les résultats directs et Effets de combat produits par une capacité héritent normalement de son élément au moment de leur création ou application. Un Skill peut modifier explicitement l’élément d’une capacité pendant le combat ; les effets déjà créés conservent l’élément enregistré lors de leur création. Une application de Bouclier possède cet élément, mais la réserve commune constituée n’en conserve ensuite aucun.

### Créature mono-élément

**Domaine :** Créatures, éléments

**Définition :** Créature possédant un seul élément dans sa forme actuelle.

### Créature bi-élément

**Domaine :** Créatures, éléments

**Définition :** Créature possédant deux éléments dans sa forme actuelle. Ses deux éléments sont mécaniquement égaux et ne sont pas hiérarchisés comme principal et secondaire.

Lorsqu’un seul de ses éléments résiste à l’élément d’une attaque, la réduction est appliquée une fois. Lorsque ses deux éléments y résistent, les deux réductions sont appliquées successivement et de manière multiplicative. La présence de deux éléments ne confère aucun avantage ou désavantage global automatique.

Toutes les combinaisons sont autorisées par défaut. Une interdiction éventuelle doit répondre à un problème de conception ou d’équilibrage explicitement identifié.

### Interaction élémentaire

**Domaine :** Éléments, combat

**Définition :** Relation défensive entre l’élément d’une capacité et le ou les éléments de sa cible, déterminant une résistance ou une interaction neutre.

Une relation standard n’accorde aucun bonus offensif automatique et ne crée aucune faiblesse augmentant les dégâts. Les relations ne sont pas obligatoirement réciproques et le même élément contre lui-même est neutre.

### Résistance élémentaire

**Domaine :** Éléments, combat

**Définition :** Interaction dans laquelle un élément de la cible réduit les dégâts directs, périodiques ou retardés d’une capacité possédant l’un des éléments auxquels il résiste. Le taux standard actuel est de 30 % et reste ajustable pendant le balancing. Une résistance ne modifie pas les effets non dommageables et ne peut pas être directement modifiée par un Skill pendant le combat.

### Interaction neutre

**Domaine :** Éléments, combat

**Définition :** Résultat d’une confrontation entre deux éléments lorsqu’aucune résistance ne s’applique. Le même élément contre lui-même est neutre.

Cette notion décrit une relation entre deux éléments et non une catégorie de capacité.

### Double résistance

**Domaine :** Éléments, combat

**Définition :** Interaction produite lorsque les deux éléments d’une créature bi-élément résistent à l’élément d’une capacité. Les deux réductions sont appliquées successivement et de manière multiplicative, jamais additionnées. Avec le taux actuel de 30 %, la cible conserve 49 % des dégâts, soit une réduction totale de 51 %.

### Immunité élémentaire

**Domaine :** Éléments, combat

**Définition :** Propriété accordée explicitement par un Skill et bloquant tous les effets positifs et négatifs d’un élément sur la créature immunisée, quelle que soit leur source.

Elle ne provient jamais automatiquement de la table élémentaire. Elle reste distincte d’une résistance, qui réduit uniquement les dégâts, et des immunités ciblées à certains principes, familles ou tags d’Effets de combat.

**Éléments à préciser ultérieurement :**

* Les ajustements éventuels du taux actuel de résistance pendant le balancing.
* Les immunités concrètes propres aux futurs Skills.

## 7. Effets de combat

### Résultat direct

**Domaine :** Combat, Skills

**Définition :** Résultat entièrement résolu au moment où il se produit et ne laissant ensuite aucune entité possédant son propre lifecycle. Des dégâts ou soins immédiats, une modification immédiate d’énergie ou de compteur, la destruction du Bouclier, un Cleanse ou un Dispel sont des résultats directs.

### Effet de combat

**Terme anglais officiel :** Combat Effect

**Domaine :** Combat, Skills, créatures

**Définition :** Effet qui continue d’exister après sa création ou son application et possède son propre lifecycle, notamment une durée, une condition de fin, des stacks, une réapplication, des ticks, un déclenchement retardé, un retrait, un snapshot ou plusieurs conséquences persistantes.

Un même Effet de combat réunit les conséquences qui commencent, expirent, se cumulent, se réappliquent et sont retirées ensemble. Des conséquences possédant des lifecycles différents appartiennent à des Effets de combat distincts.

Un Effet de combat produit par une capacité hérite normalement de son élément au moment de l’application. Les règles détaillées sont définies dans le [document Effets de combat](../01-game-design/06-COMBAT_EFFECTS.md).

### Effet de statut

**Domaine :** Combat, langage contextuel

**Définition :** Appellation contextuelle pouvant désigner un état ou un Effet de combat particulier lorsqu’elle reste naturelle, notamment un statut de contrôle ou un état nommé. Elle ne constitue plus la catégorie système supérieure, qui est **Effet de combat**.

### Effet positif

**Domaine :** Effets de combat

**Définition :** Description d’un Effet de combat constituant un avantage pour la créature concernée. Cette polarité ne détermine pas son éligibilité au Cleanse ou au Dispel.

### Effet négatif

**Domaine :** Effets de combat

**Définition :** Description d’un Effet de combat constituant un désavantage pour la créature concernée. Cette polarité ne détermine pas son éligibilité au Cleanse ou au Dispel.

### Effet neutre

**Domaine :** Effets de combat

**Définition :** Description d’un Effet de combat ne constituant objectivement ni un avantage ni un désavantage. Cette polarité ne détermine pas son éligibilité au Cleanse ou au Dispel.

### Immunité ciblée

**Domaine :** Effets de combat, combat

**Définition :** Propriété explicitement accordée empêchant de nouvelles applications dans un périmètre défini, par exemple un principe, une famille, un contrôle ou un tag contextuel. Une immunité acquise après l’application ne retire pas rétroactivement l’effet existant.

Elle ne constitue ni une caractéristique principale ni une caractéristique secondaire universelle.

### Retirer un Effet de combat

**Domaine :** Effets de combat, Skills

**Définition :** Action mettant fin à un Effet de combat avant son expiration normale. Le retrait supprime l’intégralité de l’effet, dont ses conséquences internes, ses stacks, son timer et son état.

Les actions spécialisées Cleanse et Dispel sont définies ci-dessous.

### Cleanse

**Domaine :** Effets de combat, Skills

**Définition :** Résultat direct retirant un Effet de combat explicitement éligible à Cleanse. Un Skill peut définir une quantité, une catégorie ou une sélection particulière ; sans sélection précisée parmi plusieurs effets éligibles, le choix est aléatoire.

### Dispel

**Domaine :** Effets de combat, Skills

**Définition :** Résultat direct retirant un Effet de combat explicitement éligible à Dispel. Un Skill peut définir une quantité, une catégorie ou une sélection particulière ; sans sélection précisée parmi plusieurs effets éligibles, le choix est aléatoire.

Un effet peut être éligible à Cleanse, à Dispel, aux deux ou à aucun, indépendamment de sa polarité et de sa durée.

### Réapplication et coexistence

**Domaine :** Effets de combat, combat

**Définition :** Chaque Effet de combat définit individuellement le comportement de ses applications répétées : refresh, ajout de durée, remplacement, stack, nouvelle instance, recalcul ou autre règle explicite. Le même applicateur ne crée pas par défaut une seconde instance indépendante ; des applicateurs différents peuvent conserver des instances indépendantes.

### DoT

**Domaine :** Effets de combat, combat

**Définition :** Effet infligeant des dégâts périodiques selon un nombre fixe de ticks et une cadence propre définie par l’effet, le Skill ou une autre règle explicite. L’Agilité de l’applicateur ne modifie pas automatiquement cette cadence.

### HoT

**Domaine :** Effets de combat, combat

**Définition :** Effet appliquant des soins périodiques selon le même moteur général que les DoT : nombre fixe de ticks, valeur totale non critique fixe et cadence propre définie par l’effet, le Skill ou une autre règle explicite.

### Snapshot

**Domaine :** Effets de combat, combat

**Définition :** Conservation, à l’application d’un Effet de combat, de toutes les informations nécessaires dépendant de l’applicateur. L’état défensif pertinent de la cible reste dynamique et est évalué lorsque chaque résultat ultérieur est résolu.

### Buff

**Domaine :** Effets de combat, combat

**Définition :** Effet de combat persistant constituant généralement un avantage. Un Buff peut utiliser toute durée prévue par le système, y compris jusqu’à la fin du combat.

### Debuff

**Domaine :** Effets de combat, combat

**Définition :** Effet de combat persistant constituant généralement un désavantage. Un Debuff peut utiliser toute durée prévue par le système, y compris jusqu’à la fin du combat.

### Crowd Control

**Domaine :** Effets de combat, combat

**Définition :** Principe limitant ou empêchant les actions d’une créature. Plusieurs tags contextuels peuvent partager le principe de CC total tout en restant distincts pour les interactions de Skills.

**Abréviation autorisée :** CC

### Diminishing returns

**Domaine :** Contrôles, combat

**Définition :** Mécanisme réduisant la durée des contrôles répétés sans réduire leur probabilité d’application. CC total, Silence et Exclusion utilisent trois historiques distincts.

**Abréviation autorisée :** DR

### Silence

**Domaine :** Effets de combat, contrôles

**Définition :** Contrôle empêchant les Active et l’Ultimate sans bloquer la Basic Attack, son gain d’énergie ou la progression des compteurs d’Active. Les capacités prêtes le restent. Silence utilise son propre historique de diminishing returns.

### Exclusion

**Domaine :** Effets de combat, contrôles

**Définition :** Contrôle retirant temporairement une créature du combat sans la tuer. Elle ne peut ni agir, ni être ciblée, ni être incluse dans une AoE ; ses timers et Effets de combat sont gelés jusqu’à son retour. Exclusion utilise son propre historique de diminishing returns.

### Bouclier

**Domaine :** Effets de combat, protections

**Définition :** Réserve commune unique de dégâts flat propre à chaque créature et consommée avant les PV. Chaque application ajoute sa valeur à la réserve et refresh sa durée. L’application possède l’élément de son Skill, mais la réserve constituée n’a ensuite plus d’élément propre.

Le Bouclier n’est pas retiré par Cleanse ou Dispel ; un résultat direct spécifique peut détruire toute la réserve.

### Absorption

**Domaine :** Effets de combat, protections

**Définition :** Réduction en pourcentage appliquée aux dégâts avant le Bouclier. Elle possède son propre lifecycle et ses propres règles de réapplication ou de coexistence.

### Effet retardé

**Domaine :** Effets de combat, combat

**Définition :** Effet qui continue d’exister pendant un délai avant de produire son résultat. Son applicateur est snapshoté à l’application et l’état pertinent de la cible est évalué lors du déclenchement.

### True Damage

**Domaine :** Combat, dégâts

**Définition :** Catégorie particulière de dégâts ignorant les Défenses et plusieurs réductions générales, mais restant soumise aux résistances élémentaires, à l’Absorption et aux Boucliers. Elle ne peut pas produire de Crit par défaut.

## 8. Acquisition, hasard et récompenses

### Obtention de créature

**Domaine :** Acquisition des créatures

**Définition :** Processus permettant au joueur d’ajouter une créature jouable à sa collection.

L’invocation constitue la voie principale d’obtention. Certaines créatures peuvent néanmoins être accordées directement par le gameplay comme exceptions explicitement documentées.

Quelle que soit la méthode d’obtention, un lien avec la créature est établi et celle-ci est stabilisée.

### Invocation de créature

**Domaine :** Acquisition des créatures

**Définition :** Système principal d’acquisition aléatoire de créatures. Une invocation de créature permet normalement d’obtenir une nouvelle instance au stade 1 de la forme de base d’une famille.

Narrativement, elle établit ou révèle le lien avec une manifestation vivante d’un écho, puis la stabilise. Elle ne crée pas artificiellement une nouvelle forme de vie.

**Variante autorisée :** « invocation » lorsque le contexte ne crée aucune ambiguïté.

**Terme à éviter :** « invocation » pour l’ouverture d’un contenu cosmétique, d’un objet ou d’un coffre.

### Ressource générale d’invocation

**Domaine :** Acquisition des créatures, économie

**Définition :** Ressource générale principale utilisée pour effectuer les invocations de créatures dans le modèle initial.

Cette ressource doit être obtenue principalement grâce au mode Histoire, aux quêtes journalières, aux activités, aux récompenses de progression et aux Events. Elle reste entièrement séparée de l’économie cosmétique.

L’ajout de ressources événementielles ou de catégories particulières d’invocation n’est pas validé.

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

Certaines créatures, certains skins de carte et certains équipements peuvent être remis directement comme récompenses de gameplay lorsque cette méthode d’obtention est explicitement documentée. La présence d’un coffre reste une possibilité non validée.

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

### Encyclopédie des créatures

**Domaine :** Collection, créatures

**Définition :** Répertoire de compte présentant uniquement les familles réellement obtenues par le joueur et les informations intrinsèques découvertes à leur sujet.

Chaque famille possède un numéro permanent affiché sans zéro superflu, un lore général et un lore propre à chacune de ses formes. L’encyclopédie ne révèle jamais le nombre total de familles existantes. Les formes, branches et conditions d’évolution encore inconnues restent masquées et enrichissent progressivement l’arbre connu après leur découverte.

Une famille est découverte par l’obtention réelle de l’une de ses instances. Rencontrer ou affronter une forme évoluée peut néanmoins révéler l’existence et l’apparence de cette forme, sans révéler automatiquement sa condition d’évolution. Cette connaissance reste distincte de l’obtention et ne dévoile pas le catalogue des familles encore inconnues.

**Terme à éviter :** « catalogue des créatures » pour désigner l’encyclopédie.

### Collection de créatures

**Domaine :** Collection, créatures

**Définition :** Ensemble des créatures possédées par le joueur.

La collection de créatures ne doit pas être confondue avec l’encyclopédie, qui conserve les découvertes du compte indépendamment des instances actuellement possédées.

### Collection de skins de carte

**Domaine :** Collection, cosmétiques

**Définition :** Ensemble des skins de carte débloqués par le joueur.

### Série de skins de carte

**Domaine :** Collection, cosmétiques

**Définition :** Regroupement thématique cohérent de plusieurs skins de carte.

Une série distribuée par paquets est associée à des paquets de skins de carte dont tous les contenus possibles appartiennent à cette même série.

Une série de skins de carte n’est ni un produit, ni une offre commerciale, ni un synonyme de pool de paquets. Son appartenance reste distincte de la méthode d’acquisition de ses skins, qui peut être définie par paquets, directement, par le gameplay, par une opération spéciale ou par une autre règle explicitement documentée.

Le modèle actuel repose principalement sur les séries distribuées par paquets. Les autres méthodes possibles ne sont pas automatiquement validées comme offres commerciales au lancement.

**Terme à éviter :** « collection d’illustrations » pour désigner une série de skins de carte ou une offre commerciale.

### Catégorie de skins obtenus hors paquets

**Statut :** Provisoire — nom officiel à définir

**Domaine :** Collection, cosmétiques

**Définition :** Regroupement prévu pour les skins de carte accordés directement par des récompenses de gameplay et n’appartenant à aucune série distribuée par paquets.

Cette catégorie peut notamment réunir des récompenses événementielles, de haut fait, narratives, de progression, commémoratives ou liées à une opération spéciale.

Ces skins peuvent également être regroupés dans une série artistique non distribuée par paquets lorsque leur cohérence le justifie.

**Éléments à préciser ultérieurement :**

* le nom officiel de la catégorie ;
* sa structure ;
* ses règles de complétion.

### Progression de collection

**Domaine :** Collection

**Définition :** Mesure de l’avancement du joueur dans l’acquisition des éléments d’une collection dont le périmètre est connu.

L’encyclopédie des créatures ne présente aucun taux de complétion global puisqu’elle ne révèle jamais le nombre total de familles. Pour les skins de carte, la progression est principalement suivie par série.

### Complétion d’une collection

**Domaine :** Collection

**Définition :** État atteint lorsque les conditions de progression définies pour une collection ou une série au périmètre connu sont remplies.

La complétion d’une collection cosmétique ne confère aucune récompense automatique de gameplay ni aucun avantage de puissance. Une reconnaissance future strictement cosmétique ou honorifique reste possible si elle est explicitement définie.

### Illustration

**Domaine :** Direction artistique

**Définition :** Œuvre visuelle 2D produite pour représenter une créature, notamment dans sa carte.

Une illustration est un asset artistique. Elle n’est pas, à elle seule, le contenu cosmétique possédé par le joueur.

Elle peut rester statique : le dynamisme de la présentation peut provenir de la carte, de l’UI, des animations et des VFX. Elle reste distincte de la structure fonctionnelle de la créature et de la carte.

### Skin de carte

**Domaine :** Cosmétique, interface

**Définition :** Contenu cosmétique possédé par le joueur et utilisant une illustration spécifique pour modifier la représentation visuelle de la carte d’une forme précise.

Un skin de carte est lié dans ses données à une seule forme et ne peut pas être appliqué aux autres formes de la même famille. Un même style décliné pour plusieurs formes correspond à plusieurs skins distincts.

Un skin de carte ne modifie ni la créature, ni ses caractéristiques, ni ses capacités. Le joueur **applique** un skin de carte ; il ne l’équipe pas.

**Variante autorisée :** « skin » lorsque le contexte ne laisse aucune ambiguïté.

**Élément à préciser ultérieurement :**

* un éventuel nom destiné au joueur, davantage lié à l’univers, pourra être défini lors de la conception de l’interface.

### Rareté d’un skin de carte

**Domaine :** Cosmétique, acquisition, collection

**Définition :** Niveau visible déterminant notamment la fréquence d’obtention d’un skin de carte dans les paquets de sa série.

Les différentes raretés possèdent des probabilités d’obtention et des valeurs de conversion de doublon différentes. Elles concernent uniquement la fréquence d’obtention, la valeur de collection, la présentation visuelle et la valeur perçue du skin. Elles ne confèrent aucun avantage de jeu.

**Éléments à préciser ultérieurement :**

* les autres noms et le nombre total des raretés ;
* leurs probabilités exactes ;
* les valeurs de conversion associées.

### Skin Secret

**Domaine :** Cosmétique, acquisition, collection

**Définition :** Skin de carte possédant la rareté cosmétique identifiable `Secret` et intégré exceptionnellement à un pool de skins.

Avant toute ouverture, son existence, le nombre de skins Secrets présents et leur probabilité exacte doivent être déclarés. La créature concernée peut être indiquée, tandis que l’illustration, le nom précis et les détails esthétiques peuvent rester masqués jusqu’à l’obtention personnelle du skin.

Un skin Secret suit les mêmes règles générales de RNG et de doublons que les autres skins du pool. Il ne bénéficie d’aucune *pity*, garantie ou protection particulière sans décision explicite.

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

**Définition :** Contenu ou service pouvant être acheté contre de l’argent réel.

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

**Définition :** Terme descriptif pour une nouvelle instance obtenue dans une famille déjà possédée.

Cette obtention crée toujours une instance individuelle gérée séparément. Elle peut ensuite être développée, suivre une autre branche ou être volontairement consommée comme matériau d’étoiles pour une autre instance de la même famille.

**Terme à éviter :** « doublon de monstre ».

### Instance utilisée comme matériau

**Domaine :** Progression des créatures

**Définition :** Instance de la même famille que l’instance cible, volontairement consommée lors d’une amélioration du niveau d’étoiles.

Avant sa disparition, tous ses loadouts sont vidés et les équipements qui lui étaient réservés redeviennent disponibles dans l’inventaire. Une instance verrouillée ne peut pas être utilisée comme matériau.

**Terme à éviter :** « food » dans la documentation destinée à faire référence.

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

Les services payants de réinitialisation des points de caractéristiques, de vitesse de visualisation des combats, d’extension de capacité de créatures et de sacs d’inventaire restent distincts de la boutique cosmétique.

**Variante autorisée :** « boutique cosmétique » lorsqu’il est utile de rappeler explicitement son périmètre.

### Catalogue commercial

**Domaine :** Monétisation

**Définition :** Ensemble des produits proposés contre de l’argent réel.

### Catalogue de conversion

**Domaine :** Économie, cosmétiques

**Définition :** Ensemble des contenus strictement cosmétiques accessibles avec la monnaie de conversion des doublons.

Un catalogue désigne un ensemble de contenus disponibles ; la boutique désigne l’interface qui les présente.

## 10. Modes de jeu et combats

### Allié

**Domaine :** Combat, ciblage

**Définition :** Créature appartenant à la même équipe que le lanceur, lanceur compris. La formulation « autre allié » exclut explicitement le lanceur.

### Hit

**Domaine :** Combat, Skills

**Définition :** Unité individuelle d’impact et de résolution d’une capacité. Un Skill multi-hit contient plusieurs hits, tandis qu’un hit hybride reste un seul hit comportant plusieurs composantes de dégâts.

### Opportunité d’action

**Domaine :** Combat, Skills

**Définition :** Instant de la timeline auquel une créature peut commencer une action. La priorité standard au sein de la créature est Ultimate prête et autorisée, puis Active prête, puis Basic Attack, sous réserve d’une cible valide et des exceptions explicites.

### Mode de jeu

**Domaine :** Game design

**Définition :** Activité ou type de contenu proposé au joueur, par exemple l’histoire, un boss, une tour ou le PvP.

### Saison

**Domaine :** Game design, contenu, compétition

**Définition :** Période globale unique, numérotée et nommée, donnant une identité temporaire au jeu et coordonnant les progressions, objectifs, classements ou contenus explicitement saisonniers.

Une nouvelle Saison peut réinitialiser uniquement les progressions définies comme saisonnières. Elle ne remet jamais à zéro la progression durable générale du compte, des créatures ou de la collection.

Les saisons calendaires récurrentes — printemps, été, automne et hiver — sont distinctes des Saisons du jeu. Seules ces périodes calendaires peuvent servir de conditions temporelles d’évolution.

### Event

**Domaine :** Game design, contenu temporaire

**Définition :** Petit contenu temporaire et ponctuel, organisé autour d’une occasion identifiable et utilisant principalement les modes et systèmes existants pour proposer quelques missions thématiques et récompenses adaptées.

Un Event ne constitue ni un nouveau mode de jeu, ni une progression complexe, ni une composante d’une Saison. Un événement narratif ou un événement produit par la simulation ne désigne pas automatiquement ce système.

**Variante autorisée :** « événement temporaire » lorsque le contexte évite toute confusion avec un événement narratif ou technique.

### Mode de contrôle du combat

**Domaine :** Combat

**Définition :** Manière globale dont les actions sont contrôlées pendant un combat. En Auto, Basic Attacks, Active et Ultimate sont automatiques. En Manuel, Basic Attacks et Active restent automatiques tandis que le joueur autorise les Ultimate. Le mode n’est pas configuré séparément pour chaque créature.

**Terme à éviter :** « mode de jeu » pour désigner le degré d’automatisation d’un combat.

### Timeout

**Domaine :** Combat

**Définition :** Durée maximale de simulation d’un combat avant l’application de sa règle de départage. Le timeout standard est de 120 secondes de simulation, sauf exception explicitement définie par un mode.

### Vitesse de visualisation

**Domaine :** Combat, monétisation

**Définition :** Vitesse à laquelle la simulation de combat est restituée au joueur dans le temps réel. ×1 est gratuit ; ×2 et ×4 sont des services de confort payants.

La vitesse de visualisation ne modifie jamais la simulation, sa seed RNG, ses calculs, ses statistiques, ses événements, son résultat, ses récompenses ou son coût en énergie.

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

Dans le contexte narratif, la formulation qualifiée **IA humaine** désigne l’entité fictionnelle définie dans la section consacrée à l’univers.

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

### Godot

**Domaine :** Développement, moteur de jeu

**Définition :** Moteur de jeu actuellement retenu pour le développement de Project Awakening.

Cette décision ne fixe pas encore sa version, le langage de programmation, l’architecture des scènes, la structure du projet ou les conventions de code.

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
