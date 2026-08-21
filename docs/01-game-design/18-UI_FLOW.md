# Project Awakening — UI Flow

**Statut :** Draft de conception — base initiale à compléter

## 1. Rôle et périmètre du document

Ce document rassemble les besoins fonctionnels validés concernant les écrans, les informations et les parcours liés aux créatures.

Il ne fixe aucune mise en page, navigation finale, quantité d’onglets, grammaire de recherche ou direction visuelle.

## 2. Principes

L’interface est conçue d’abord pour Android et iOS et doit rester adaptée au tactile.

Elle doit favoriser des composants réutilisables. Une représentation de créature ou de carte doit pouvoir servir dans le combat, la composition d’équipe, la gestion des instances, la collection, l’encyclopédie, la sélection et l’acquisition. Les informations visibles peuvent varier selon le contexte sans modifier l’identité fonctionnelle de la créature.

Elle doit :

* distinguer clairement gestion des instances, encyclopédie, inventaire et collection de skins ;
* rendre lisibles les conséquences des actions irréversibles ;
* présenter les informations nécessaires sans révéler les branches et conditions encore secrètes ;
* privilégier des tooltips contextuels accessibles directement depuis les termes de gameplay affichés ;
* accompagner chaque fonctionnalité par un tutoriel court lors de son déblocage.

Lorsqu’un élément, une caractéristique, un Effet de combat, un statut contextuel ou un autre mot-clé nécessite une explication, le joueur doit pouvoir appuyer directement sur le terme concerné afin d’obtenir une définition concise. La présentation graphique et le contenu rédactionnel exact de ces tooltips restent à définir.

Les principes visuels et de production de l’interface sont précisés dans les drafts [Card Design](../03-art/03-CARD_DESIGN.md) et [UI Guide](../03-art/04-UI_GUIDE.md).

## 3. Fiche d’une instance

Le joueur doit pouvoir accéder aux informations pertinentes de l’instance, notamment :

* numéro de famille ;
* nom officiel de la forme et surnom éventuel ;
* lore ;
* rareté ;
* niveau, XP et étoiles ;
* stade et branche ;
* éléments de la forme, rôles suggérés et profil offensif ;
* score de Puissance ;
* caractéristiques principales et secondaires ;
* points disponibles ;
* Basic Attack et quatre Skills, consultables directement avec leur description et leur élément propre ;
* ensemble d'équipement, avec distinction entre Artefacts et Sources d'énergie ;
* tags et verrouillage ;
* apparences de formes débloquées ;
* informations d’évolution déjà découvertes.

La disposition et les regroupements restent à définir.

Le sélecteur d’apparence doit distinguer clairement la forme mécanique actuelle de l’apparence affichée. Il propose uniquement les formes réellement parcourues par l’instance et, pour chacune, les skins déjà débloqués qui lui sont compatibles. Ce changement est gratuit, limité au hors-combat et ne modifie aucune propriété mécanique.

Une fiche de Skill indépendante de la fiche de la créature n’est pas obligatoire. La consultation principale des capacités s’effectue depuis la fiche de l’instance.

Les descriptions de la Basic Attack, des Skills et des Effets de combat affichent autant que possible les valeurs concrètes déjà calculées pour l’instance possédée : dégâts, soins, durée effective d’un DoT ou HoT, Bouclier accordé et autres valeurs calculables.

Ces valeurs suivent automatiquement le niveau, les caractéristiques, le build, l’équipement, la forme et les autres données permanentes de l’instance. Lorsqu’une valeur dépend d’une cible future et ne peut pas être calculée honnêtement, la formule relative reste visible. L’interface ne présente jamais un faux montant final obtenu sans les informations nécessaires.

## 4. Lisibilité pendant le combat

Le combat affiche principalement les résultats utiles de la simulation, sans exposer constamment les calculs, compteurs internes ou modificateurs intermédiaires.

Les Effets de combat importants actifs sur une cible sont représentés par des icônes :

* un effet à stacks utilise une seule icône accompagnée de son compteur ;
* deux instances indépendantes du même effet utilisent deux icônes distinctes afin de préserver leurs durées propres ;
* la durée peut être représentée par un remplissage radial de l’icône, sans afficher constamment une valeur textuelle.

Une application réussie normale ou l’ajout d’une stack n’affiche aucun texte supplémentaire : l’apparition ou la mise à jour de l’icône suffit. Le combat ne doit pas devenir un combat log visuel.

Le joueur doit pouvoir distinguer, au moyen d’un feedback court :

* une Esquive ;
* une Immunité ;
* l’échec probabiliste d’un effet explicitement tenté.

Une résistance élémentaire ne produit pas de feedback spécifique : seule la valeur finale est affichée. Ces feedbacks peuvent notamment communiquer `Esquivé`, `Immunisé` ou l’échec du contrôle contextuel concerné. Le wording exact, le rendu graphique de ces feedbacks, le timer radial et le traitement visuel des Critiques restent à définir.

### 4.1. Résumé de fin de combat

Un résumé statistique simple doit être accessible après le combat pour l’équipe du joueur comme pour l’équipe adverse.

Les statistiques sont agrégées par créature, pas par Skill. Elles peuvent notamment couvrir :

* les dégâts infligés et reçus ;
* les soins effectués ;
* le Bouclier accordé ;
* les Cleanse et Dispel effectués ;
* le nombre de contrôles appliqués ;
* d’autres statistiques globales pertinentes à définir ultérieurement.

Ce résumé doit notamment aider le joueur à analyser une défaite et à adapter son équipe. Il ne nécessite pas un rapport technique détaillé ni un combat log destiné au joueur.

## 5. Parcours de gestion d’une instance

L’interface doit permettre d’accéder aux actions validées :

* attribuer des points ;
* gérer l’équipement ;
* modifier le surnom et les tags ;
* verrouiller ou déverrouiller l’instance ;
* choisir une apparence de forme déjà débloquée ;
* consulter les conditions d’évolution découvertes ;
* effectuer une réinitialisation ou une redistribution ;
* utiliser des instances non verrouillées comme matériaux d’étoiles.

Les actions irréversibles ou destructives doivent disposer d’une présentation et de confirmations adaptées. Le détail de ces protections reste à définir.

La gestion des équipements s'effectue depuis la fiche de l'instance. La disposition des catégories et le nombre exact d'emplacements restent à définir.

## 6. Liste des instances

La liste doit prendre en charge :

* la recherche dynamique sensible aux formes ;
* les tris validés ;
* l’identification de la forme, du stade et de la branche ;
* le score de Puissance recalculé ;
* l’état verrouillé ;
* l’état inutilisable pour dépassement de capacité.

## 7. Encyclopédie

L’encyclopédie doit :

* afficher uniquement les familles découvertes ;
* utiliser leurs numéros permanents sans zéro superflu ;
* ne jamais révéler le nombre total de familles ;
* distinguer lore familial et lore de forme ;
* présenter progressivement les formes et branches découvertes ;
* masquer le nombre et l’identité des branches encore inconnues.

## 8. Arbre d’évolution

Avant toute découverte complète, l’arbre peut afficher :

> Forme de base → ??? → ???

Les nouvelles branches et conditions connues enrichissent la vue du compte. L’existence ou l’apparence d’une forme rencontrée peut être révélée sans afficher sa condition. Le nombre et l’identité des branches encore inconnues restent masqués.

Lorsqu’exactement une évolution standard est valide, elle est automatique et ne demande ni choix ni confirmation. Lorsque plusieurs branches concurrentes sont valides, aucune évolution ne se produit et l’interface ne présente aucun écran de choix manuel. Un objet consommable d’évolution peut en revanche demander une confirmation avant sa consommation volontaire.

Une suite de plusieurs évolutions obtenues après une même récompense d’XP doit être présentée dans l’ordre.

## 9. Capacité et file d’attente

L’interface doit distinguer :

* la capacité gratuite ;
* les extensions permanentes ;
* la capacité totale ;
* le nombre d’instances actuellement possédées ;
* les instances grisées et inutilisables ;
* leur ordre dans la file de déblocage.

Elle doit indiquer qu’une créature obtenue au-delà de la capacité n’est jamais perdue et que la plus ancienne instance bloquée redevient automatiquement utilisable lorsqu’une place se libère.

## 10. Acquisition

Le parcours d’invocation doit rester clairement distinct de l’ouverture d’un paquet de skins de carte.

L’obtention d’une instance doit permettre d’identifier sa famille, sa rareté et son ajout éventuel à la file de dépassement de capacité, sans révéler les branches encore secrètes.

## 11. Fabrication et recettes

Le système d'établi, ou équivalent, doit permettre de sélectionner des composants et de fabriquer des Artefacts. Une bibliothèque ou un registre de plans conserve les recettes découvertes et permet de reproduire le même type d'Artefact, dont les caractéristiques finales peuvent varier.

La disposition, le nombre d'ingrédients, le traitement d'une combinaison invalide, les confirmations et la présentation des rolls restent à définir.

## 12. Éléments à préciser ultérieurement

* L’architecture de navigation.
* La disposition et le nombre d’écrans ou d’onglets.
* La grammaire et les contrôles exacts de recherche.
* La présentation des tris et filtres.
* Les confirmations des actions irréversibles.
* Les règles détaillées d’accessibilité.
* Les informations visibles dans chaque variante contextuelle de carte.
* La présentation graphique et le contenu rédactionnel final des tooltips contextuels.
* Le wording et le rendu graphique exacts des icônes, compteurs, timers, feedbacks de combat et Critiques.
* La liste définitive des statistiques du résumé post-combat.
* Les tutoriels et leur ordre exact.
* Les animations d’invocation, d’évolution et de montée d’étoile.
* La présentation commerciale des extensions de capacité.
