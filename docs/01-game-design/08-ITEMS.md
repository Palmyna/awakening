# Project Awakening — Objets et équipements

**Statut :** Rédigé — référence actuelle, à maintenir à jour

## 1. Rôle et périmètre du document

Ce document constitue la référence fonctionnelle du système d’objets, d’équipements, de fabrication et d’inventaire.

Il définit les catégories d’équipement, les règles d’attribution et de génération, les loadouts, le rôle du niveau d’objet et de l’iLvl, les principes de loot et de recyclage, les sets, la capacité d’inventaire et les sacs.

Il ne constitue ni une table de loot, ni un catalogue d’objets concrets, ni un document d’équilibrage. Les valeurs, probabilités, pools, recettes et contenus précis appartiendront aux données de production correspondantes.

## 2. Terminologie et espaces de stockage

Un **objet** est un élément pouvant être obtenu, stocké ou utilisé par un système du jeu.

Un **équipement** est un objet pouvant être équipé sur une instance de créature. Lorsqu’il ne figure dans aucun loadout, il est disponible dans l’inventaire principal.

L’inventaire d’objets reste distinct :

* de la gestion des instances de créatures ;
* de l’encyclopédie des créatures ;
* de la collection des skins de carte.

Les composants de fabrication utilisent un stockage séparé de l’inventaire principal, selon les règles de la section 12.

## 3. Loadouts d’équipement d’une instance

Chaque instance peut posséder plusieurs loadouts d’équipement enregistrés. Chaque loadout est composé exactement de :

* **3 emplacements d’Artefacts** ;
* **2 emplacements de Sources d’énergie**.

Il n’existe pas actuellement de sous-types d’emplacements supplémentaires.

Les loadouts appartiennent à l’instance, non à sa famille, à sa forme mécanique, à son skin ou à l’apparence affichée. Deux instances d’une même famille peuvent utiliser des équipements entièrement différents.

Lors d’une évolution, les loadouts et leurs équipements restent associés à la même instance. Afficher ensuite une ancienne forme comme apparence cosmétique ne modifie pas ces configurations.

Les équipements ne sont pas automatiquement représentés sur l’illustration ou la carte de la créature.

## 4. Catégories d’équipement

Les deux catégories d’équipement sont :

* les **Artefacts** ;
* les **Sources d’énergie**.

Les Sources d’énergie sont principalement orientées vers les caractéristiques principales et les effets directement liés au fonctionnement fondamental de la créature.

Les Artefacts sont principalement orientés vers les caractéristiques secondaires et des effets plus spécialisés ou spécifiques.

Cette répartition définit l’identité dominante des catégories. Un objet concret peut créer une exception locale lorsque son design le justifie explicitement, sans modifier la direction générale du système.

## 5. Règles d’équipement

### 5.1. Compatibilité universelle

Toutes les créatures peuvent équiper tous les équipements correspondant à un emplacement disponible. Il n’existe aucune restriction générale fondée sur l’élément, la famille, la forme ou l’identité de la créature.

Un effet d’équipement peut néanmoins posséder sa propre condition d’activation. Cette condition peut notamment dépendre du mode, du type d’adversaire, du contexte de combat ou d’une autre propriété explicitement documentée. Une créature ou une situation ne satisfaisant pas cette condition peut utiliser l’objet, mais ne bénéficie pas de l’effet concerné.

La possibilité d’équiper un objet et l’éligibilité à chacun de ses effets sont donc deux vérifications distinctes.

Cette capacité ne crée aucune catégorie structurelle séparée d’équipement PvP ou PvE. Les objets restent des Artefacts et des Sources d’énergie, et leur contexte d’efficacité ne leur impose aucune source d’obtention particulière. Un effet contextuel concret, sa condition et sa valeur doivent être définis explicitement par le contenu concerné.

### 5.2. Gestion et transfert

Un même exemplaire d’équipement peut être utilisé dans plusieurs loadouts de la même instance.

Dès qu’un équipement figure dans au moins un loadout d’une instance, il lui est réservé et ne peut pas être utilisé dans le loadout d’une autre instance. Pour le transférer, le joueur doit le retirer de tous les loadouts de l’instance actuelle. Lorsqu’il n’apparaît plus dans aucun loadout, il redevient disponible.

Hors combat, cette gestion et ce transfert n’appliquent aucun coût ni pénalité. La réservation n’est pas une liaison permanente de type *bind on equip*.

### 5.3. Exemplaires identiques

Plusieurs exemplaires identiques d’un équipement standard peuvent occuper simultanément plusieurs emplacements d’un même loadout si le joueur les possède réellement.

Une pièce précise appartenant à un set constitue une exception : la même pièce ne peut pas occuper plusieurs emplacements d’un même loadout. Le même exemplaire peut néanmoins figurer dans plusieurs loadouts de la même instance selon la règle de réservation. Des pièces différentes d’un même set peuvent naturellement être réunies.

## 6. Sources d’énergie

Les Sources d’énergie sont principalement obtenues comme :

* loot de combat ;
* récompenses d’activité ;
* autres récompenses pertinentes du jeu.

Elles participent à la boucle de farming et à la recherche de meilleurs exemplaires et rolls.

Une Source d’énergie inutilisée peut notamment :

* être équipée ;
* être vendue contre une petite quantité de monnaie soft ;
* servir de composant dans une recette d’Artefact lorsque cette recette le prévoit.

Une recette peut demander une Source précise, un type de Source ou aucune Source. Toutes les recettes d’Artefacts n’en nécessitent donc pas.

## 7. Artefacts et fabrication

### 7.1. Recettes et bibliothèque de compte

Les Artefacts sont principalement obtenus par fabrication dans un établi ou un système équivalent.

Le joueur place plusieurs composants. Certaines combinaisons correspondent à une recette valide. Une recette découverte est mémorisée dans une bibliothèque commune au compte, consultable et réutilisable.

Une même recette valide produit toujours le même **type d’Artefact**. Chaque fabrication crée néanmoins un nouvel exemplaire dont les propriétés variables sont générées immédiatement. La recette peut influencer ou limiter les raretés, caractéristiques, effets et rolls accessibles.

### 7.2. Résolution d’une combinaison

Si la combinaison ne correspond à aucune recette valide :

* aucun objet n’est créé ;
* aucun composant n’est consommé ;
* un feedback signale l’absence de recette valide correspondante.

Le wording et la présentation exacts de ce feedback appartiennent à l’UI.

Si la combinaison correspond à une recette valide :

1. les composants sont consommés ;
2. l’Artefact est généré ;
3. toutes ses propriétés variables sont fixées immédiatement.

### 7.3. Dissolution

Un Artefact inutile peut être dissous. Cette action :

* détruit définitivement l’Artefact ;
* fournit exactement **un composant** ;
* ne fournit jamais une Source d’énergie ;
* ne garantit jamais la récupération complète ou équivalente de ses matériaux de fabrication.

Une Source d’énergie utilisée comme composant ne peut donc pas être récupérée par la dissolution de l’Artefact obtenu. Les règles déterminant le composant récupéré restent à définir.

## 8. Génération et puissance d’un équipement

### 8.1. Niveau d’objet

Lorsqu’un équipement est généré ou fabriqué, son **niveau d’objet** correspond au niveau du compte à cet instant.

Ce niveau est fixé définitivement. Il ne progresse pas lorsque le compte gagne ensuite des niveaux et ne peut pas être amélioré. Obtenir le potentiel des niveaux de compte plus élevés demande de looter ou fabriquer de nouveaux équipements.

Le niveau d’objet ne fixe pas directement les valeurs obtenues. Il définit les plages de valeurs accessibles lors de la génération. Deux objets de même niveau peuvent donc obtenir des rolls différents.

Les bornes minimales et maximales peuvent évoluer par paliers : plusieurs niveaux de compte peuvent partager les mêmes plages avant une nouvelle progression.

### 8.2. Courbe de potentiel

La progression du potentiel des futurs équipements doit rester :

* très lente aux faibles niveaux, lorsque les niveaux de compte sont fréquents ;
* progressivement plus perceptible aux niveaux élevés, lorsque chaque niveau demande davantage d’investissement.

Cette direction ne valide aucune formule ni aucun palier numérique et ne doit pas provoquer une inflation incontrôlée de la puissance.

### 8.3. Déblocage progressif de la complexité

Le niveau de compte peut débloquer progressivement des couches de génération :

* les premiers équipements peuvent principalement fournir des caractéristiques simples ;
* des effets plus complexes peuvent devenir accessibles pendant la progression intermédiaire ;
* les objets de set peuvent apparaître dans la progression avancée.

Les niveaux parfois utilisés pour illustrer ces étapes, notamment `20` ou `50`, ne constituent pas des seuils validés.

## 9. Rareté, propriétés et rolls

### 9.1. Équipements standards

Pour un équipement standard, la rareté est générée lors de la création de chaque exemplaire. Un même type d’Artefact ou de Source d’énergie peut donc exister sous plusieurs raretés.

La rareté représente principalement :

* la difficulté ou la fréquence d’obtention ;
* le potentiel global de l’objet ;
* l’accès possible à davantage de propriétés ou d’effets ;
* des effets ou niveaux d’effets potentiellement plus intéressants.

Une rareté élevée ne garantit pas une bonne adéquation au build ni de bons rolls. Un objet moins rare peut rester préférable pour un usage donné.

Il n’existe aucune propriété distincte de **qualité d’objet**. La valeur réelle d’un exemplaire résulte déjà de son niveau, de sa rareté, de ses caractéristiques, de ses effets, de ses rolls et de son iLvl.

### 9.2. Caractéristiques et effets

Les caractéristiques d’un équipement peuvent être générées parmi un pool explicitement autorisé pour cet objet. La rareté peut notamment influencer le nombre de propriétés et les possibilités accessibles.

Un équipement peut également fournir des effets plus complexes. Certains effets sont fixes ; d’autres contiennent une valeur variable, qui constitue alors un roll soumis aux règles de génération de l’objet.

Les pools, incompatibilités éventuelles, valeurs et effets disponibles doivent être définis par le design de l’objet, de la recette ou du set concerné.

### 9.3. Cumul des bonus

Les bonus compatibles fournis par plusieurs équipements se cumulent de manière additive. Cette règle s’applique aux caractéristiques et aux effets numériques compatibles.

Il n’existe pas de règle générique neutralisant silencieusement deux effets identiques. Les objets doivent être conçus et équilibrés en tenant compte de leur cumul possible. Une exception propre à un effet doit être explicitement définie.

### 9.4. Propriétés définitives

Une fois l’équipement généré, son niveau, sa rareté, ses caractéristiques, ses rolls, ses effets et les valeurs de ces effets sont définitifs.

Le système de base ne comporte :

* aucun reroll ;
* aucun reforging ;
* aucune montée de niveau d’un équipement ;
* aucune transformation progressive d’un mauvais exemplaire en objet parfait.

Obtenir un meilleur équipement demande d’en looter ou d’en fabriquer un nouveau. Aucun système supplémentaire de modification d’objet n’est actuellement validé.

### 9.5. Absence de durabilité

Les équipements n’ont aucune durabilité. Ils ne s’usent pas, ne cassent pas, ne demandent aucune réparation et n’imposent aucun coût d’entretien.

## 10. iLvl

Chaque équipement possède un **iLvl visible**, distinct de son niveau d’objet et de sa rareté.

Le niveau d’objet décrit le contexte de génération et les plages accessibles. L’iLvl fournit une estimation normalisée de la puissance réelle de l’exemplaire précis afin de faciliter la comparaison rapide entre objets différents.

Son calcul doit prendre en compte la contribution réelle de l’objet, notamment ses caractéristiques, leurs valeurs, ses effets et leurs rolls. La formule et les pondérations exactes restent à définir.

L’iLvl est un indicateur comparatif. Il ne garantit pas qu’un équipement est adapté au build du joueur.

## 11. Objets de set

Tous les équipements n’appartiennent pas à un set. Les sets constituent une couche avancée et un objectif important de la recherche d’équipement à haut niveau.

### 11.1. Structure libre

Un set peut réunir :

* deux ou trois Artefacts ;
* deux Sources d’énergie ;
* plusieurs Artefacts et Sources d’énergie dans un set mixte.

Sa structure, son nombre de pièces et ses seuils sont définis par le set concret. La limite de deux Sources correspond aux deux emplacements disponibles dans un loadout.

Une pièce précise de set possède une rareté fixe liée à son identité. La même pièce n’existe pas sous plusieurs raretés aléatoires. Ses caractéristiques autorisées et leurs rolls peuvent néanmoins varier entre les exemplaires.

### 11.2. Effets de set

Les effets sont définis explicitement par chaque set. Ils peuvent être génériques, soutenir un style de jeu ou être associés à une famille, une créature, un Skill ou une autre condition de design cohérente.

Les sets concrets, leurs pièces, leurs seuils et leurs effets appartiennent au contenu de production.

## 12. Inventaire

### 12.1. Inventaire principal limité

L’inventaire principal possède actuellement une capacité de référence de :

> **40 emplacements de base**

Cette valeur reste ajustable pendant le balancing et les tests. La limitation soutient la gestion régulière du loot sans modifier les règles structurelles des objets.

L’inventaire principal accueille notamment :

* les Artefacts et Sources d’énergie non équipés ;
* les objets consommables, dont les consommables d’évolution ;
* certains objets ou monnaies d’événement lorsqu’ils existent comme objets stockables ;
* les sacs non équipés ;
* les autres objets individuels nécessitant une gestion d’inventaire.

### 12.2. Stockage des composants

Les composants de fabrication utilisent un stockage séparé et illimité. Ils ne consomment jamais de place dans l’inventaire principal et restent consultables depuis un espace ou onglet dédié.

## 13. Sacs et capacité d’inventaire

Le compte possède exactement **6 emplacements dédiés aux sacs**.

Un sac est un objet réel dont la capacité propre augmente la capacité de l’inventaire principal lorsqu’il est équipé.

Lorsqu’un sac est obtenu :

* si un emplacement de sac est libre, il y est automatiquement équipé et n’occupe plus de case dans l’inventaire principal ;
* si les six emplacements sont occupés, il rejoint l’inventaire principal et y occupe une case.

Un sac non équipé peut être conservé, vendu ou utilisé pour remplacer un sac équipé. Un sac déséquipé retourne dans l’inventaire principal et nécessite donc une place disponible.

Les sacs peuvent posséder différentes capacités et être obtenus par le loot, les récompenses, certaines progressions ou un service de confort payant. Les tailles, raretés éventuelles, sources, probabilités et prix restent à définir.

L’achat possible de sacs reste distinct de la boutique cosmétique. Il n’accorde aucune caractéristique, aucun équipement de combat exclusif ni aucune puissance inaccessible gratuitement. Les sacs existent également par le gameplay et un joueur Free-to-Play doit pouvoir progresser normalement sans achat.

## 14. Boucle de loot et de farming

Le système suit une philosophie inspirée des Hack’n Slash :

> obtenir → comparer → équiper → farmer → fabriquer → rechercher de meilleurs rolls → recycler les objets inutiles

Le joueur peut rejouer des combats pour obtenir des Sources d’énergie et des composants, fabriquer plusieurs exemplaires d’un Artefact et rechercher de meilleures raretés, propriétés, combinaisons et rolls.

Les combats du mode Histoire peuvent participer à cette boucle. Les activités plus avancées pourront utiliser leurs propres tables de loot, probabilités, récompenses et possibilités de farming ciblé lorsque leur contenu sera défini.

Les Boss personnels peuvent notamment devenir une source importante d’éléments liés aux sets, de composants permettant de former ou fabriquer des sets, de composants de craft spécialisés et de ressources propres à certains boss. Leurs contenus, taux et tables de loot exacts restent définis par le mode et les données de production correspondantes.

Un équipement peu intéressant conserve une utilité potentielle : une Source peut être vendue ou servir de composant, tandis qu’un Artefact peut être dissous.

## 15. Objets liés à d’autres systèmes

### 15.1. Évolutions

Un objet intervient dans une évolution uniquement de deux manières :

1. un équipement précis réellement équipé dans le loadout actif de l’instance constitue une condition standard évaluée lors d’une montée de niveau et n’est pas consommé ;
2. un objet consommable d’évolution est utilisé volontairement sur une instance éligible et déclenche immédiatement l’évolution correspondante.

Dans le second cas, les autres conditions doivent être satisfaites. L’objet est consommé volontairement et ne disparaît jamais automatiquement lors d’un level up. La simple possession dans l’inventaire ne constitue jamais une condition.

Les règles complètes appartiennent au [référentiel Évolutions](./07-EVOLUTIONS.md).

### 15.2. Consommation d’une instance comme matériau

Lorsqu’une instance est consommée comme matériau d’étoiles :

1. tous ses loadouts sont vidés ;
2. tous les équipements qui lui étaient réservés redeviennent disponibles dans l’inventaire ;
3. aucun équipement n’est détruit avec l’instance.

Cette protection est systématique.

### 15.3. Objet de réinitialisation des caractéristiques

Un objet rare obtenu en jouant permet de redistribuer les points de caractéristiques déjà gagnés sans modifier le niveau ni l’XP.

Il n’accorde aucun niveau, aucune expérience, aucun point supplémentaire et fournit le même résultat fonctionnel que le service payant limité correspondant.

## 16. Dépendances documentaires

| Document | Responsabilité liée |
| --- | --- |
| [`03-CREATURES.md`](./03-CREATURES.md) | Propriété et conservation de l’équipement par instance |
| [`07-EVOLUTIONS.md`](./07-EVOLUTIONS.md) | Conditions et déclenchements d’évolution liés aux objets |
| [`10-PROGRESSION.md`](./10-PROGRESSION.md) | Niveau du compte, étoiles et redistribution des caractéristiques |
| [`11-COLLECTION.md`](./11-COLLECTION.md) | Séparation entre collection et inventaire |
| [`13-PVE.md`](./13-PVE.md) | Sources de loot et de composants propres aux modes PvE |
| [`14-PVP.md`](./14-PVP.md) | Effets contextuels, loadouts et contraintes d’équité du PvP |
| [`16-SEASONS.md`](./16-SEASONS.md) | Associations saisonnières possibles sans modification automatique des règles d’objet |
| [`20-UI_FLOW.md`](./20-UI_FLOW.md) | Parcours de gestion, comparaison, fabrication et inventaire |
| [`04-MONETIZATION.md`](../00-foundation/04-MONETIZATION.md) | Service de confort payant lié aux sacs |

## 17. Éléments à préciser ultérieurement

Le cadrage fonctionnel du système est établi. Restent volontairement ouverts ou réservés au balancing, au contenu et à la production :

* la validation finale par les tests des `40` emplacements de base ;
* les tailles, raretés éventuelles, sources, probabilités, prix et valeurs de vente des sacs ;
* les protections UI contre le déséquipement d’un sac lorsqu’aucune place n’est disponible ;
* les noms, le nombre, la présentation et les probabilités des raretés d’équipement ;
* les pools, incompatibilités, nombres de propriétés et plages exactes des rolls ;
* les effets disponibles et leurs valeurs ;
* les effets contextuels concrets, leurs conditions et leurs coefficients ;
* le nombre, les noms, l’ergonomie et la méthode de sélection des loadouts ;
* la formule de progression des plages selon le niveau de compte et ses éventuels caps techniques ;
* les seuils exacts de déblocage des effets complexes et des objets de set ;
* la formule et les pondérations exactes de l’iLvl ;
* les tables, taux, quantités et possibilités de farming ciblé du loot ;
* les composants et recettes concrets, leurs coûts éventuels et leurs règles de découverte ;
* les règles exactes de récupération d’un composant lors de la dissolution ;
* les sets concrets, leurs pièces, seuils, propriétés et effets ;
* les valeurs de vente des Sources d’énergie et les paramètres de monnaie soft ;
* les objets consommables, équipements d’évolution et objets d’événement concrets ;
* la méthode d’obtention, la rareté et le rythme de distribution de l’objet de réinitialisation.
