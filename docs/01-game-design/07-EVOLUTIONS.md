# Project Awakening — Évolutions

**Statut :** Rédigé — référence actuelle, à maintenir à jour

## 1. Rôle et périmètre du document

Ce document constitue la référence fonctionnelle du système d’évolution des créatures. Il définit la structure des parcours, les conditions, les déclenchements, la résolution des branches, la conservation de l’instance et la relation entre forme mécanique, apparence et découverte.

Il approfondit le [référentiel Créatures](./03-CREATURES.md) sans le remplacer. Les valeurs propres à chaque famille, les conditions des évolutions concrètes, les données des objets, les paramètres de balancing et la présentation finale appartiennent aux documents spécialisés ou aux données de production correspondantes.

## 2. Famille, formes et instance

Une famille peut contenir plusieurs formes et plusieurs branches d’évolution. Chaque instance possédée parcourt cependant exactement trois stades :

1. stade 1 — forme de base ;
2. stade 2 — forme intermédiaire ;
3. stade 3 — forme finale.

Une divergence peut commencer au stade 2 ou au stade 3. Une famille peut donc contenir plus de trois formes au total, mais une instance individuelle n’en parcourt que trois.

L’évolution transforme la même instance. Elle ne crée pas une nouvelle créature et ne remplace pas son identité individuelle. Le chemin parcouru est définitif pour cette instance ; suivre une autre branche demande de développer une autre instance de la même famille.

Toute nouvelle instance acquise commence sous la forme de base de sa famille. Des formes intermédiaires ou finales peuvent exister naturellement dans le monde et être rencontrées comme créatures ou adversaires, mais elles ne peuvent pas être obtenues directement comme nouvelles instances déjà évoluées.

## 3. Effets mécaniques d’une évolution

Une évolution peut modifier :

* l’apparence de référence ;
* le ou les éléments ;
* le profil de caractéristiques principales de base ;
* les rôles suggérés ;
* le profil offensif ;
* les versions de la Basic Attack et des Skills.

La Basic Attack et les quatre Skills conservent leur continuité conceptuelle, et la catégorie de chaque Skill reste inchangée. Une nouvelle forme peut enrichir une capacité ou transformer fortement sa fonction lorsque cette transformation reste cohérente avec l’évolution de la créature.

Le changement du ou des éléments de la forme et le changement de l’élément d’une capacité sont indépendants. Une évolution peut modifier l’un sans modifier l’autre. Chaque capacité possède toujours exactement un élément dans la version utilisée par la nouvelle forme.

### 3.1. Budget des caractéristiques principales

Toutes les familles utilisent le même budget total pour leurs six caractéristiques principales de base :

1. PV ;
2. Attaque ;
3. Attaque spéciale ;
4. Défense ;
5. Défense spéciale ;
6. Agilité.

Les familles peuvent répartir ce budget différemment. La rareté n’accorde pas automatiquement un budget supérieur. Le total numérique exact du budget reste à définir ; toute valeur utilisée dans un exemple de conception ne constitue pas une valeur de production.

Une évolution peut redistribuer ce budget afin d’orienter une branche. Toute augmentation d’une ou plusieurs caractéristiques doit être compensée par une diminution totale équivalente ailleurs :

> **Somme des modificateurs de redistribution = 0**

Une évolution ne crée donc aucun budget de caractéristiques principales supplémentaire. Le profil redistribué devient le profil de base de la nouvelle forme et reste utilisé pour la suite de ce chemin tant qu’une évolution ultérieure ne définit pas explicitement une nouvelle redistribution.

### 3.2. Multiplicateur de stade

Le multiplicateur de stade appliqué au profil de caractéristiques principales de la forme actuelle et aux caractéristiques secondaires de base de la famille est :

* stade 1 : ×1 ;
* stade 2 : ×2 ;
* stade 3 : ×3.

Ce multiplicateur augmente la puissance globale. Il reste distinct de la redistribution, qui oriente le profil sans modifier son budget total. Passer au stade suivant n’impose pas une nouvelle redistribution : en son absence, le profil de base déjà établi est simplement utilisé avec le nouveau multiplicateur.

### 3.3. Caractéristiques secondaires

Les valeurs de base de Crit, Dégâts critiques et Esquive appartiennent à l’identité intrinsèque de la famille. Elles restent identiques entre ses formes et ses branches et ne participent pas au budget de redistribution des caractéristiques principales.

Le multiplicateur de stade continue néanmoins de s’appliquer à ces valeurs de base.

## 4. Conditions d’évolution

Chaque transition possède ses propres conditions. Toute évolution exige obligatoirement un niveau minimum, propre à la famille et à la transition concernées. Il n’existe ni niveau universel commun à toutes les familles, ni évolution sans niveau minimum.

Le niveau demandé est toujours un minimum, jamais un niveau exact. En plus de ce niveau, une transition peut notamment dépendre :

* du moment de la journée ;
* d’une saison ;
* d’une région ou d’un environnement ;
* d’un équipement précis réellement équipé sur l’instance ;
* d’un objet consommable d’évolution utilisé volontairement ;
* d’une autre condition explicitement définie pour cette famille.

Cette liste décrit les besoins actuels sans constituer une liste fermée de toutes les mécaniques futures.

### 4.1. Combinaison des conditions

Lorsque plusieurs conditions sont définies pour une transition, elles utilisent une logique `ET` : elles doivent toutes être satisfaites simultanément. Le système ne prévoit pas de groupes complexes de conditions utilisant une logique `OU`.

### 4.2. Conditions exclues

Le niveau d’étoiles n’est jamais une condition d’évolution. L’évolution et les étoiles restent deux systèmes de progression séparés ; une évolution ne dépend donc ni de l’obtention ni de la consommation des doublons nécessaires aux étoiles.

Les évolutions n’utilisent pas non plus de compteurs historiques propres à l’instance, tels qu’un nombre de combats, de victoires, d’ennemis vaincus, d’Ultimates utilisées ou d’événements déjà produits. Les conditions sont évaluées à partir de l’état et du contexte pertinents au moment du déclenchement.

### 4.3. Conditions contextuelles et temporelles

Une condition de contexte — horaire, saison, région, environnement ou équipement — doit être valide au moment du déclenchement. Un contexte rencontré précédemment n’est pas mémorisé comme un historique.

Une condition temporelle ne doit jamais provoquer un blocage prolongé ou déraisonnable. Une fenêtre courte et régulièrement récurrente est acceptable. Plus les occasions sont espacées, plus la famille doit proposer des possibilités cohérentes pendant les autres périodes pertinentes.

Une condition ne doit jamais devenir définitivement impossible, dépendre d’un événement unique terminé, devenir obsolète après une mise à jour ou condamner définitivement une instance à ne plus pouvoir progresser. Son occasion doit rester accessible ou revenir dans un délai raisonnable.

## 5. Déclenchement et résolution

### 5.1. Déclenchement standard

En dehors de l’utilisation volontaire d’un objet consommable d’évolution, une évolution se déclenche uniquement lors d’une montée de niveau. Toutes les conditions sont évaluées à cet instant.

Dépasser le niveau minimum sans remplir une autre condition ne déclenche rien immédiatement lorsque cette condition devient valide plus tard. L’instance pourra évoluer lors d’une montée de niveau ultérieure si toutes les conditions sont alors réunies.

### 5.2. Résolution des évolutions valides

Lors d’un déclenchement standard :

* si exactement une évolution est valide, elle se produit automatiquement et ne peut pas être refusée ou retardée ;
* si plusieurs évolutions concurrentes sont valides, aucune évolution ne se produit ;
* si aucune évolution n’est valide, l’instance conserve sa forme actuelle.

Le système ne choisit jamais arbitrairement une branche et n’affiche aucun écran de sélection manuelle. Lorsque plusieurs branches étaient valides, le joueur doit modifier les conditions avant une future montée de niveau afin qu’une seule évolution reste valide.

Les conditions des branches concurrentes doivent permettre au joueur de contrôler raisonnablement la situation qu’il provoque, sans transformer la résolution en choix direct d’une branche dans l’interface.

### 5.3. Plusieurs niveaux et évolutions successives

Une attribution importante d’XP peut faire gagner plusieurs niveaux et permettre plusieurs évolutions successives, jusqu’à faire passer une instance du stade 1 au stade 3.

Chaque évolution est évaluée et présentée séparément. Les séquences ou animations correspondantes se succèdent ; elles ne sont pas fusionnées en une transformation unique.

## 6. Objets liés aux évolutions

Un objet intervient dans une évolution uniquement selon l’un des deux mécanismes suivants.

### 6.1. Équipement comme condition

Une transition peut exiger qu’un équipement précis soit réellement équipé sur l’instance. Cet équipement :

* doit occuper l’emplacement concerné au moment de la montée de niveau ;
* est évalué comme une condition standard ;
* n’est pas consommé par l’évolution.

Cette règle peut concerner un Artefact ou une Source d’énergie. Les équipements concrets restent à définir dans les données des familles et des objets.

### 6.2. Objet consommable comme déclencheur

Un objet consommable d’évolution est utilisé volontairement sur une instance éligible. Celle-ci doit déjà satisfaire le niveau minimum obligatoire et toutes les autres conditions de la transition.

L’objet utilisé correspond directement à l’évolution qu’il déclenche. Son utilisation :

1. cible une instance éligible ;
2. peut demander une confirmation de consommation selon les règles finales d’interface ;
3. consomme l’objet ;
4. déclenche immédiatement l’évolution, sans attendre une nouvelle montée de niveau.

Un objet ne disparaît jamais automatiquement à la suite d’une montée de niveau. Son utilisation ne mène pas à un écran demandant au joueur de choisir arbitrairement une branche.

Le simple fait de posséder un objet dans l’inventaire n’est jamais une condition d’évolution. « Porter » et « équiper » ne désignent pas deux mécanismes différents : seule la présence réelle d’un équipement dans l’ensemble actif de l’instance constitue la condition standard décrite ci-dessus.

## 7. Conservation de l’instance et de sa progression

Une évolution conserve notamment :

* le niveau et l’XP ;
* les étoiles ;
* les points de caractéristiques attribués et disponibles ;
* l’équipement ;
* le surnom ;
* les tags ;
* le verrouillage ;
* le chemin déjà parcouru ;
* les apparences de formes déjà débloquées.

Les points attribués restent dans les caractéristiques choisies, même lorsque la nouvelle forme utilise un profil intrinsèque redistribué. Une évolution ne réinitialise jamais la progression individuelle.

## 8. Forme mécanique et apparence affichée

La forme mécanique actuelle et l’apparence affichée sont deux notions distinctes.

Une instance peut afficher une ancienne forme réellement parcourue tout en conservant intégralement les propriétés de sa forme mécanique actuelle, notamment :

* ses caractéristiques et son stade ;
* ses éléments ;
* sa Basic Attack et ses quatre Skills ;
* ses rôles et son profil offensif ;
* son équipement ;
* toute autre propriété fonctionnelle.

Chaque forme réellement parcourue débloque définitivement son apparence pour cette instance uniquement. Une forme appartenant à une branche non parcourue n’est pas débloquée pour elle.

Le joueur peut changer gratuitement l’apparence affichée parmi celles de l’instance, hors combat et sans modifier sa forme mécanique. Pour chaque forme ainsi accessible, il peut employer les skins de carte déjà débloqués qui sont compatibles avec cette forme selon les règles de collection. La compatibilité concrète des futurs skins reste définie par leurs données propres.

## 9. Découverte des formes et des conditions

Les conditions exactes d’une évolution peuvent rester cachées avant leur découverte. Le jeu doit fournir des indices cohérents dans le lore, les descriptions, les objets, les régions, les environnements, les ennemis, les activités ou d’autres contenus du monde. Une association totalement arbitraire imposant le recours à une ressource externe est à éviter.

Une condition découverte devient une connaissance permanente du compte et reste consultable pour les futures instances de la famille.

L’arbre connu se complète progressivement. Une famille peut initialement présenter des emplacements inconnus, mais le nombre réel de branches reste caché tant qu’elles ne sont pas découvertes. Découvrir une branche ne révèle pas automatiquement les autres.

Voir ou affronter une forme évoluée peut révéler son existence et son apparence. Cette observation ne révèle pas automatiquement sa condition d’évolution ni la manière de l’obtenir. La connaissance d’une forme et celle de sa méthode d’évolution sont donc distinctes.

Cette découverte ciblée ne doit jamais révéler le catalogue complet des familles encore inconnues. Les règles de conservation et de présentation de ces connaissances appartiennent au [document Collection et encyclopédie](./11-COLLECTION.md).

## 10. Dépendances documentaires

| Document | Responsabilité liée |
| --- | --- |
| [`03-CREATURES.md`](./03-CREATURES.md) | Structure famille / forme / instance, caractéristiques et progression conservée |
| [`02-COMBAT.md`](./02-COMBAT.md) | Formules et valeur systémique des caractéristiques |
| [`04-SKILLS.md`](./04-SKILLS.md) | Continuité et versions des capacités entre formes |
| [`05-ELEMENTS.md`](./05-ELEMENTS.md) | Éléments des formes et des capacités |
| [`08-ITEMS.md`](./08-ITEMS.md) | Équipements et objets consommables liés aux évolutions |
| [`10-PROGRESSION.md`](./10-PROGRESSION.md) | Attribution d’XP, montées de niveau, points et étoiles |
| [`11-COLLECTION.md`](./11-COLLECTION.md) | Découverte, encyclopédie, apparences de formes et skins |
| [`18-UI_FLOW.md`](./18-UI_FLOW.md) | Présentation des conditions, séquences et actions du joueur |

## 11. Éléments à préciser ultérieurement

Le cadrage fonctionnel du système est établi. Restent volontairement ouverts ou réservés au balancing, au contenu et à la production :

* le budget numérique total exact des caractéristiques principales de base ;
* les valeurs de base concrètes des familles ;
* les redistributions propres aux branches ;
* les niveaux minimums et conditions concrètes de chaque transition ;
* les objets consommables et équipements concrets liés aux évolutions ;
* les conventions détaillées de conception des indices ;
* le cap défensif exact et les éventuels paramètres additionnels de la formule défensive ;
* les paramètres exacts de la courbe d’Agilité et l’intervalle minimum des Basic Attacks ;
* l’équilibrage relatif des caractéristiques ;
* les animations finales et l’enchaînement visuel des évolutions successives ;
* la présentation UI finale des conditions connues ou inconnues et des arbres partiellement découverts ;
* la compatibilité concrète des futurs skins avec les différentes formes.
