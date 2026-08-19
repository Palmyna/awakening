# Project Awakening — Créatures

**Statut :** Rédigé — référence actuelle, à maintenir à jour

## 1. Rôle et périmètre du document

Ce document définit la structure fonctionnelle des créatures jouables de **Project Awakening**.

Il constitue la référence actuelle pour comprendre :

* la distinction entre famille, forme et instance possédée ;
* les propriétés appartenant à chacun de ces niveaux ;
* l’identité fonctionnelle d’une créature ;
* la construction générale de ses caractéristiques ;
* les contrats communs de niveau, d’étoiles, d’évolution et d’équipement ;
* le cycle de vie d’une instance ;
* les règles générales de coexistence dans une équipe ;
* la relation d’une créature avec l’acquisition, la collection et l’encyclopédie.

Il complète la [Vision](../00-foundation/01-VISION.md), le [GDD central](./01-GAME_DESIGN_DOCUMENT.md) et les [règles de combat](./02-COMBAT.md).

Il ne remplace pas les documents spécialisés consacrés :

* aux [Skills](./04-SKILLS.md) ;
* aux [éléments](./05-ELEMENTS.md) ;
* aux [effets de statut](./06-STATUS_EFFECTS.md) ;
* aux [évolutions](./07-EVOLUTIONS.md) ;
* aux [objets et équipements](./08-ITEMS.md) ;
* à l’[invocation](./09-GACHA.md) ;
* à la [progression](./10-PROGRESSION.md) ;
* à la [collection et l’encyclopédie](./11-COLLECTION.md) ;
* aux [parcours d’interface](./18-UI_FLOW.md) ;
* au [style visuel des créatures](../03-art/02-CREATURE_STYLE.md) ;
* à la [représentation sous forme de cartes](../03-art/03-CARD_DESIGN.md) ;
* au [lore des créatures](../02-world/02-CREATURE_LORE.md).

Ces documents possèdent les règles opérationnelles, valeurs, interfaces et contenus détaillés de leur domaine. Le présent document conserve les contrats structurels qu’ils doivent respecter.

## 2. Modèle structurel

### 2.1. Famille

Une **famille de créatures** représente l’identité persistante d’une lignée.

La famille porte notamment :

* son identité générale ;
* sa rareté ;
* son numéro permanent d’encyclopédie ;
* son lore général ;
* l’ensemble de ses formes et branches ;
* l’identité de sa Basic Attack ;
* l’identité de ses quatre Skills prédéfinis.

Une famille peut contenir plus de trois formes lorsqu’elle possède plusieurs branches d’évolution.

### 2.2. Forme

Une **forme** représente un état fonctionnel et visuel précis d’une famille.

La forme porte notamment :

* son nom officiel ;
* son apparence de référence ;
* son lore propre ;
* son ou ses éléments ;
* son profil de caractéristiques de base ;
* un ou deux rôles suggérés ;
* son profil offensif suggéré ;
* les versions de la Basic Attack et des Skills utilisées sous cette forme.

Une forme peut modifier significativement l’orientation fonctionnelle de la créature. Deux branches d’une même famille peuvent ainsi proposer des profils différents tout en conservant une identité familiale commune.

Le ou les éléments de la forme restent fixes pendant tout un combat. Ils sont distincts des éléments de sa Basic Attack et de ses quatre Skills, qui peuvent employer d’autres éléments.

Son apparence de référence peut être principalement matérialisée par une illustration 2D statique. Cette représentation n’impose ni modèle 3D, ni personnage 3D animé, ni rig 2D.

### 2.3. Instance possédée

Une **instance possédée** est l’individu concret d’une famille appartenant au joueur.

Elle persiste à travers ses évolutions. Une évolution ne crée pas une nouvelle instance et ne remplace pas la créature possédée.

L’instance porte notamment :

* son niveau et son XP ;
* ses points de caractéristiques attribués et disponibles ;
* son niveau d’étoiles ;
* son ensemble d’équipement ;
* son surnom éventuel ;
* ses tags personnalisés ;
* son état verrouillé ou déverrouillé ;
* son chemin d’évolution ;
* ses apparences de formes débloquées.

Plusieurs instances d’une même famille peuvent être possédées et développées différemment.

### 2.4. Stades et branches d’évolution

Chaque instance parcourt exactement trois stades :

1. stade 1 — forme de base ;
2. stade 2 — forme intermédiaire ;
3. stade 3 — forme finale.

Une famille peut toutefois contenir de nombreuses formes grâce à ses branches et sous-branches.

Une divergence peut commencer au stade 2 ou au stade 3. Le nombre de chemins possibles pour une famille n’est pas limité structurellement, mais une instance individuelle ne traverse toujours que trois formes.

Le choix d’une branche est définitif pour l’instance.

## 3. Identité fonctionnelle

### 3.1. Propriétés fondamentales

Une créature possède notamment :

* une famille ;
* une forme mécanique actuelle ;
* une rareté de famille ;
* un ou deux éléments au maximum ;
* une Basic Attack ;
* exactement quatre Skills prédéfinis ;
* six caractéristiques principales ;
* trois caractéristiques secondaires système ;
* une progression individuelle ;
* un ensemble d’équipement ;
* un score de Puissance ;
* un ou deux rôles suggérés ;
* un profil offensif suggéré.

Le joueur personnalise l’instance principalement par :

* la répartition de ses points de caractéristiques ;
* son équipement ;
* sa progression en niveau et en étoiles ;
* son évolution et sa branche ;
* son utilisation dans différentes compositions.

### 3.2. Rareté

La rareté appartient à la famille et reste identique pour toutes ses formes et branches.

Les raretés validées sont :

1. Rare ;
2. Épique ;
3. Légendaire ;
4. Mythique.

La rareté représente principalement la difficulté d’obtention, la valeur de collection et le prestige. Elle ne constitue pas une hiérarchie automatique de puissance.

Une rareté élevée peut rendre indirectement la progression en étoiles plus difficile lorsque les nouvelles instances de cette famille sont plus rares à obtenir. Les probabilités et règles d’acquisition appartiennent au [document Invocation](./09-GACHA.md).

### 3.3. Numéro et lore

Chaque famille possède un numéro unique, permanent et jamais réorganisé après son attribution.

Il est affiché sans zéro superflu, par exemple `#1`, `#42` ou `#133`. Toutes les formes d’une famille partagent ce numéro.

Chaque famille possède un court lore général et chaque forme un court lore propre. Leur contenu narratif détaillé appartient au [Lore des créatures](../02-world/02-CREATURE_LORE.md).

### 3.4. Basic Attack et Skills

Chaque famille possède :

* une Basic Attack ;
* exactement quatre Skills prédéfinis ;
* parmi ces quatre Skills, exactement une Ultimate ;
* soit une Active et deux Passive, soit deux Active et une Passive.

Le joueur ne choisit pas ces capacités dans une liste et ne les remplace pas.

La Basic Attack et les quatre Skills conservent leur continuité conceptuelle à travers les évolutions, et la catégorie de chaque Skill reste inchangée. Une forme ou une branche peut enrichir une capacité ou transformer fortement sa fonction lorsque cette transformation reste cohérente avec l’évolution de la créature.

Chaque Basic Attack et chacun des quatre Skills possède exactement un élément. L’élément d’une capacité est indépendant du ou des éléments de la forme et peut évoluer séparément entre deux formes lorsque la continuité conceptuelle de la capacité est respectée.

Les coefficients, valeurs, durées, probabilités, nombres de hits, ciblages, effets et statuts appartiennent aux [documents Skills](./04-SKILLS.md) et [Effets de statut](./06-STATUS_EFFECTS.md). Les règles élémentaires des formes et capacités appartiennent au [document Éléments](./05-ELEMENTS.md).

### 3.5. Rôles et profil offensif

Chaque forme possède un ou deux rôles suggérés au maximum parmi :

* Dégâts ;
* Tank ;
* Support ;
* Contrôle.

Les rôles sont informatifs. Ils n’accordent aucun bonus, ne produisent aucun calcul, ne limitent pas l’équipement et n’empêchent pas un autre build.

Chaque forme possède également un profil offensif suggéré :

* Physique ;
* Spécial ;
* Hybride.

Ce profil est lui aussi informatif. Une forme Hybride peut répartir ses capacités entre plusieurs catégories ou utiliser un hit comportant plusieurs composantes de dégâts.

Les règles d’un hit hybride, dont son unique jet d’Esquive et son unique jet de Critique, appartiennent aux documents [Combat](./02-COMBAT.md) et [Skills](./04-SKILLS.md).

### 3.6. Représentation visuelle

Une créature est principalement représentée dans l’interface par une carte utilisant une illustration de sa forme.

La carte, l’illustration et la créature restent des notions distinctes :

* la créature est l’entité fonctionnelle et, lorsqu’elle est possédée, l’instance persistante ;
* la carte est sa représentation visuelle et fonctionnelle dans l’interface ;
* l’illustration est un asset artistique utilisé par cette représentation.

Une même créature peut disposer de plusieurs illustrations grâce aux skins de carte. Des styles artistiques différents peuvent coexister entre ces skins sans modifier la structure fonctionnelle, les caractéristiques ou les capacités de la créature.

## 4. Caractéristiques

### 4.1. Caractéristiques principales et secondaires

Les six caractéristiques principales sont :

1. PV ;
2. Attaque ;
3. Attaque spéciale ;
4. Défense ;
5. Défense spéciale ;
6. Agilité.

Seules ces six caractéristiques peuvent recevoir directement les points gagnés lors des montées de niveau.

Les trois caractéristiques secondaires système sont :

1. Crit ;
2. Dégâts critiques ;
3. Esquive.

Elles ne reçoivent pas directement les points gagnés par niveau. Elles peuvent provenir des valeurs de base de la forme, de l’équipement, des Skills, des Passive, des effets de combat ou d’autres systèmes explicitement documentés.

L’Agilité contrôle l’intervalle des Basic Attacks et n’augmente pas le Crit.

Les formules, caps, conversions et modifications en combat appartiennent au [document Combat](./02-COMBAT.md).

### 4.2. Valeurs intrinsèques

Chaque forme possède son propre profil de caractéristiques de base.

Une évolution remplace les valeurs de base de l’ancienne forme par celles de la nouvelle. Les points distribués, l’équipement et les autres bonus ne deviennent jamais de nouvelles valeurs de base.

Il n’existe aucun système d’IV ni aucune variation aléatoire cachée des caractéristiques intrinsèques. Deux instances d’une même forme possèdent les mêmes valeurs de base avant les choix de progression du joueur.

### 4.3. Multiplicateur de stade

Le stade applique aux caractéristiques principales et secondaires de base de la forme le multiplicateur suivant :

* stade 1 : ×1 ;
* stade 2 : ×2 ;
* stade 3 : ×3.

Le multiplicateur dépend uniquement du stade. Deux branches différentes situées au même stade utilisent le même multiplicateur.

### 4.4. Ordre de construction

Pour les caractéristiques principales, l’ordre conceptuel est :

> valeurs de base de la forme → multiplicateur de stade → multiplicateur d’étoiles → points distribués → équipement → autres bonus permanents → modifications de combat

Pour les caractéristiques secondaires :

> valeurs de base de la forme → multiplicateur de stade → équipement et autres sources → modifications de combat

Le multiplicateur d’étoiles ne s’applique pas aux caractéristiques secondaires. Les points distribués ne sont pas multipliés rétroactivement par l’évolution ou les étoiles.

## 5. Progression individuelle

### 5.1. Niveau et points de caractéristiques

Le niveau d’une instance ne possède pas de maximum.

Une montée de niveau n’augmente aucune caractéristique automatiquement. Elle accorde actuellement cinq points à répartir entre les six caractéristiques principales.

Cette valeur constitue la référence actuelle mais reste ajustable pendant le balancing.

Les points non attribués peuvent être conservés indéfiniment. Ils ne produisent aucun effet et n’augmentent pas le score de Puissance.

Le niveau réel de l’instance reste directement affiché. Aucun système de prestige ne le remplace ou ne le réinitialise automatiquement.

### 5.2. Participation à l’XP

L’XP d’une activité est attribuée après le combat et calculée individuellement pour chaque créature participante. Elle n’est jamais divisée entre les membres de l’équipe.

Toutes les participantes sont éligibles, y compris si elles sont mortes, contrôlées ou temporairement exclues à la fin du combat.

Une même récompense peut accorder plusieurs niveaux et tous les points correspondants.

Le ratio dépendant des niveaux de l’équipe, sa formule actuelle, son ratio minimum et ses règles d’arrondi appartiennent au [document Progression](./10-PROGRESSION.md).

### 5.3. Niveau d’étoiles

Une nouvelle instance commence à 0 étoile et peut obtenir quinze montées regroupées en :

* Bronze ★1 à ★5 ;
* Argent ★1 à ★5 ;
* Or ★1 à ★5.

Les étoiles augmentent uniquement les six caractéristiques principales de base de la forme et du stade actuels. Elles ne multiplient pas les caractéristiques secondaires, les points distribués, l’équipement ou les bonus externes.

La progression est permanente et non linéaire. Elle utilise comme matériaux d’autres instances de la même famille, quelle que soit leur branche.

Les multiplicateurs, quantités, exigences des matériaux et règles de consommation appartiennent au [document Progression](./10-PROGRESSION.md). La protection par verrouillage relève du [document Collection](./11-COLLECTION.md) et la restitution de l’équipement du [document Objets et équipements](./08-ITEMS.md).

### 5.4. Réinitialisation

Une réinitialisation complète gratuite remet l’instance au niveau 1 et retire les points gagnés grâce aux niveaux, que le joueur doit ensuite regagner.

Elle conserve notamment :

* la forme et la branche déjà obtenues ;
* le niveau d’étoiles ;
* l’équipement ;
* le surnom ;
* les tags ;
* les apparences débloquées.

Une évolution déjà obtenue n’est jamais perdue. Une évolution non encore obtenue doit toujours satisfaire ses conditions après la réinitialisation.

Un objet rare obtenu en jouant et un service payant strictement limité permettent de redistribuer uniquement les points déjà gagnés sans modifier le niveau ni l’XP.

Les règles opérationnelles de ces méthodes appartiennent au [document Progression](./10-PROGRESSION.md).

### 5.5. Score de Puissance

Chaque instance possède un score de Puissance représentant une estimation synthétique de sa puissance numérique actuelle.

Il est recalculé en temps réel lorsque sa forme, ses étoiles, ses points attribués, son équipement ou une autre source permanente active modifient réellement sa puissance.

Il sert au tri et à la comparaison générale sans mesurer absolument l’efficacité stratégique d’une créature. Les points non attribués ne l’augmentent pas.

Sa formule appartient au [document Progression](./10-PROGRESSION.md).

## 6. Contrat structurel de l’évolution

L’évolution transforme définitivement la même instance.

Elle peut modifier :

* l’apparence ;
* le ou les éléments ;
* le profil de caractéristiques de base ;
* les rôles suggérés ;
* le profil offensif ;
* les versions de la Basic Attack et des Skills.

Le changement du ou des éléments de la forme et le changement de l’élément d’une capacité sont deux décisions indépendantes. Une évolution peut modifier l’un sans modifier l’autre.

Elle conserve les investissements et choix déjà attachés à l’instance, notamment :

* son niveau et son XP ;
* ses étoiles ;
* ses points attribués et disponibles ;
* son équipement ;
* son surnom et ses tags ;
* son verrouillage.

Les points attribués restent dans les caractéristiques choisies, même si la nouvelle forme possède un autre profil naturel.

Une forme atteinte débloque définitivement son apparence pour cette instance. Les anciennes formes réellement parcourues sur son chemin peuvent être utilisées comme apparences cosmétiques, sans modifier sa forme mécanique actuelle. Une branche non empruntée ne débloque aucune apparence.

Les conditions, objets éventuels, indices, découvertes, déclenchements, évolutions successives et choix de branches sont centralisés dans le [document Évolutions](./07-EVOLUTIONS.md).

## 7. Équipement et gestion individuelle

### 7.1. Ensemble d’équipement

Chaque instance possède son propre ensemble d’équipement actif, composé de plusieurs objets répartis dans plusieurs emplacements.

Cet ensemble appartient à l’instance, non à sa famille ou à sa forme. Il est conservé lors d’une évolution et n’est pas modifié par le choix d’une ancienne apparence cosmétique.

Les emplacements, restrictions, statistiques, affixes, raretés, améliorations, sets, iLvl, caps et règles de loot appartiennent au [document Objets et équipements](./08-ITEMS.md).

### 7.2. Surnom, tags et verrouillage

Une instance peut recevoir :

* un surnom facultatif ;
* des tags personnalisés sans effet de gameplay.

Aucun système distinct de Favoris n’est retenu actuellement.

Le verrouillage protège l’instance contre les actions destructives ou irréversibles, notamment sa consommation comme matériau, sa suppression, sa réinitialisation complète et la redistribution de ses caractéristiques.

Il ne bloque pas sa progression normale, son évolution, ses étoiles, son équipement ou son utilisation dans une activité.

Les règles de gestion, de recherche et de présentation appartiennent au [document Collection](./11-COLLECTION.md) et au [document UI Flow](./18-UI_FLOW.md).

## 8. Acquisition et cycle de vie d’une instance

L’invocation constitue la voie principale d’acquisition.

Une nouvelle instance obtenue normalement commence :

* au stade 1, dans la forme de base de sa famille ;
* au niveau 1 ;
* à 0 étoile ;
* sans point de caractéristique attribué.

Certaines acquisitions directes par le gameplay peuvent constituer des exceptions explicitement documentées.

Obtenir de nouveau une famille déjà connue crée toujours une nouvelle instance individuelle. Cette instance peut être développée, suivre une autre branche ou servir de matériau d’étoiles pour une autre instance de la même famille.

Une instance utilisée comme matériau disparaît définitivement. Tous ses objets équipés sont automatiquement replacés dans l’inventaire avant sa disparition. Une instance verrouillée ne peut pas être consommée.

Les ensembles de familles disponibles, probabilités, garanties, ressources et parcours d’acquisition appartiennent au [document Invocation](./09-GACHA.md). L’interprétation narrative des manifestations multiples appartient au [Lore des créatures](../02-world/02-CREATURE_LORE.md).

## 9. Utilisation dans une équipe

Une équipe peut réunir jusqu’à six créatures.

Deux instances d’une même famille peuvent cohabiter uniquement lorsque leurs chemins d’évolution ont réellement divergé.

Une instance située sur le tronc commun reste incompatible avec toute autre instance de sa famille dans la même équipe.

Cette règle est globale et s’applique à tous les modes.

Les rôles et profils suggérés ne constituent pas des restrictions de composition.

## 10. Relation avec la collection et l’encyclopédie

La liste des instances possédées et l’encyclopédie remplissent des fonctions distinctes.

Obtenir réellement une instance découvre sa famille pour le compte. Voir ou affronter une créature ne suffit pas.

La découverte est permanente. L’encyclopédie conserve le numéro, le lore familial, les lores de formes et les informations intrinsèques déjà découvertes.

Elle ne révèle jamais le nombre total de familles. Les formes, branches et conditions d’évolution encore inconnues restent cachées jusqu’à leur découverte.

La capacité de créatures détermine combien d’instances possédées sont utilisables, sans limiter leur propriété ni leur découverte. Une instance obtenue au-delà de cette capacité n’est jamais perdue : elle reste possédée et découverte, mais devient temporairement inutilisable jusqu’à son déblocage.

La formule de capacité, les extensions permanentes, la file de déblocage, la recherche, les tris et la présentation de l’encyclopédie appartiennent au [document Collection](./11-COLLECTION.md).

## 11. Créatures jouables et monstres ennemis

Une **créature** est une entité jouable, possédée, collectionnée et développée par le joueur.

Un **monstre** est une entité ennemie rencontrée dans une activité.

Un monstre :

* n’est pas ajouté à la collection de créatures ;
* n’est pas développé comme une instance possédée ;
* ne fait pas partie d’une équipe possédée par le joueur.

Les deux termes ne sont pas interchangeables.

## 12. Répartition documentaire

| Document | Responsabilité principale |
|---|---|
| [`02-COMBAT.md`](./02-COMBAT.md) | Formules, caps, dégâts, timing, Esquive, Critique et résolution des hits |
| [`04-SKILLS.md`](./04-SKILLS.md) | Basic Attack, Active, Passive, Ultimate et variations des capacités selon les formes |
| [`05-ELEMENTS.md`](./05-ELEMENTS.md) | Éléments des formes et interactions élémentaires |
| [`06-STATUS_EFFECTS.md`](./06-STATUS_EFFECTS.md) | Effets de statut et leurs règles communes |
| [`07-EVOLUTIONS.md`](./07-EVOLUTIONS.md) | Conditions, indices, découvertes, déclenchements et choix de branches |
| [`08-ITEMS.md`](./08-ITEMS.md) | Objets, emplacements, équipement, iLvl et loot |
| [`09-GACHA.md`](./09-GACHA.md) | Invocation, raretés d’acquisition, ensembles de familles disponibles et acquisitions directes |
| [`10-PROGRESSION.md`](./10-PROGRESSION.md) | XP, niveaux, étoiles, réinitialisations et score de Puissance |
| [`11-COLLECTION.md`](./11-COLLECTION.md) | Gestion des instances, encyclopédie, recherche, tris et capacité |
| [`18-UI_FLOW.md`](./18-UI_FLOW.md) | Informations affichées, écrans, navigation et confirmations |
| [`02-CREATURE_STYLE.md`](../03-art/02-CREATURE_STYLE.md) | Représentation artistique et illustrations des créatures |
| [`03-CARD_DESIGN.md`](../03-art/03-CARD_DESIGN.md) | Structure visuelle et variantes contextuelles des cartes |
| [`02-CREATURE_LORE.md`](../02-world/02-CREATURE_LORE.md) | Lore des familles, des formes, des manifestations et des évolutions |

## 13. Éléments à préciser ultérieurement et maintenance

Les paramètres et contenus encore ouverts sont maintenus dans leurs documents spécialisés, notamment :

* la courbe et les règles numériques d’XP ;
* la validation finale des cinq points par niveau ;
* les multiplicateurs et exigences des étoiles ;
* la formule du score de Puissance ;
* les propriétés détaillées des équipements et les caps d’iLvl ;
* les probabilités et garanties d’invocation ;
* les conditions propres aux évolutions concrètes ;
* la grammaire de recherche et les parcours d’interface ;
* les valeurs de base et profils numériques des familles et formes.

Ce document demeure la référence structurelle des créatures jouables.

Les documents spécialisés peuvent préciser ses règles, valeurs et interfaces, mais ne doivent pas modifier silencieusement les contrats structurels établis ici.

Toute évolution d’un de ces contrats doit entraîner la mise à jour coordonnée de ce document, du GDD, des fondations concernées et des documents spécialisés associés.
