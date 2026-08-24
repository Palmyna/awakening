# Project Awakening — UI Flow

**Statut :** Draft de conception — à relire et valider

## 1. Rôle et périmètre du document

Ce document définit les besoins fonctionnels et les principaux parcours déjà déductibles des systèmes validés.

Il couvre :

* l’entrée dans une session et l’accès progressif aux fonctionnalités ;
* le mode Histoire et la sélection d’une activité ;
* la préparation d’une équipe, le combat et le résultat ;
* la progression et la gestion des instances ;
* la collection, l’encyclopédie et les skins de carte ;
* l’invocation de créatures ;
* les quêtes journalières ;
* les objets, la fabrication et l’inventaire ;
* les parcours cosmétiques et les services de confort déjà validés.

Il ne fixe aucune architecture finale de navigation, mise en page, quantité d’onglets, grammaire de recherche, palette, typographie ou direction visuelle détaillée.

## 2. Principes transversaux

L’interface est conçue d’abord pour Android et iOS et doit rester adaptée au tactile.

Elle favorise des composants réutilisables. Une représentation de créature ou de carte doit pouvoir servir dans le combat, la composition d’équipe, la gestion des instances, la collection, l’encyclopédie, la sélection et l’acquisition. Les informations visibles peuvent varier selon le contexte sans modifier l’identité fonctionnelle de la créature.

L’interface doit :

* distinguer clairement gestion des instances, encyclopédie, inventaire et collection de skins ;
* distinguer l’invocation de créature de l’ouverture d’un paquet cosmétique ;
* rendre lisibles les conséquences des actions irréversibles ;
* présenter les informations nécessaires à la décision en cours ;
* masquer les branches et conditions encore secrètes ;
* éviter d’imposer une gestion complète entre deux activités ;
* permettre des actions courtes lors d’une connexion mobile ;
* préserver l’accès aux optimisations avancées pour les joueurs investis.

Les principes visuels et de production appartiennent aux drafts [Card Design](../03-art/03-CARD_DESIGN.md) et [UI Guide](../03-art/04-UI_GUIDE.md).

## 3. Tooltips et vocabulaire de gameplay

Lorsqu’un élément, une caractéristique, un Effet de combat, un statut contextuel ou un autre mot-clé nécessite une explication, le joueur doit pouvoir appuyer directement sur le terme concerné afin d’obtenir une définition concise.

Les tooltips doivent utiliser le vocabulaire du [glossaire officiel](../00-foundation/05-GLOSSARY.md) et rester cohérents entre la fiche d’une instance, la préparation d’équipe, les informations d’activité et le combat.

Un tooltip d’élément peut notamment présenter son rôle et les éléments de capacité auxquels il résiste. Une matrice globale des résistances n’est pas obligatoire.

La présentation graphique et le wording final restent à définir.

## 4. Entrée dans une session

Une session ne suit pas une liste d’actions obligatoire. Le joueur doit pouvoir accéder aux fonctions déjà débloquées pour :

* progresser dans le mode Histoire ;
* participer à une activité disponible ;
* consulter ses trois quêtes journalières ;
* gérer ses créatures ;
* préparer ses équipes ;
* consulter la collection ;
* gérer ses objets ;
* poursuivre un objectif personnel.

L’interface doit rendre visibles les informations de session qui influencent immédiatement ces choix, notamment la réserve générale d’énergie disponible, les quêtes en cours, les déblocages récents et les récompenses prêtes à être récupérées selon les règles futures de chaque système.

Cette exigence ne valide ni un écran d’accueil précis ni des badges, onglets ou notifications particuliers.

## 5. Onboarding et déblocages

Le début du jeu suit le parcours fonctionnel suivant :

1. courte introduction au contexte et au rôle du joueur ;
2. choix de la première créature parmi trois ;
3. premier combat rapide ;
4. première montée de niveau ;
5. introduction de la répartition des caractéristiques ;
6. progression à travers plusieurs niveaux ;
7. première ressource d’invocation ;
8. acquisition contrôlée ou garantie ;
9. obtention progressive de nouvelles créatures ;
10. introduction de la composition d’équipe ;
11. création ou sélection d’une équipe préparée ;
12. modification d’un équipement ou d’une composition ;
13. combat permettant d’observer l’impact du changement ;
14. boss ou défi final de la vertical slice.

Les fonctionnalités sont principalement débloquées par des jalons du mode Histoire. Chaque déblocage est accompagné d’un tutoriel court au moment où le joueur peut réellement utiliser la fonction.

Les jalons, l’ordre détaillé après les premières étapes et le contenu exact des tutoriels restent à définir.

## 6. Sélection d’une activité

Le parcours standard d’une activité est :

> choisir un objectif → consulter ses règles → sélectionner une équipe → combattre → consulter le résultat → poursuivre, retenter ou retourner à la gestion.

Avant un contenu ordinaire, l’interface présente suffisamment d’informations pour préparer une équipe pertinente :

* éléments des adversaires qui en possèdent ;
* principales menaces ;
* Effets de combat importants ;
* conditions particulières ;
* récompenses principales ;
* restrictions éventuelles ;
* coût d’entrée lorsqu’il existe.

Pour une activité individuelle, l’interface utilise par défaut la réserve générale d’énergie et indique le coût correspondant ainsi que l’énergie qui restera après l’entrée. Une régulation différente n’est présentée que lorsqu’une exception propre au mode a été explicitement définie.

Une mécanique secrète de boss ou de défi reste possible, mais sa présence doit être signalée.

## 7. Mode Histoire

Le mode Histoire doit permettre de parcourir les mondes, leurs niveaux et leurs boss ou jalons réguliers.

Le parcours doit distinguer :

* les niveaux accessibles ;
* les niveaux terminés ;
* les prochaines étapes ;
* les récompenses de première réussite et de répétition lorsqu’elles diffèrent ;
* le coût en énergie générale ;
* les déblocages associés à un jalon ;
* les informations nécessaires avant le combat.

La puissance d’équipe peut être présentée comme indication de difficulté sans constituer un verrou systématique.

La hiérarchie exacte entre multivers, mondes, régions et niveaux dans la navigation reste à définir. Les régions appartiennent au cadre narratif et ne doivent pas être inventées comme couche d’interface obligatoire lorsque le contenu ne les utilise pas.

## 8. Équipes enregistrées et préparation

Le joueur doit pouvoir :

* créer plusieurs équipes ;
* sélectionner jusqu’à six créatures dans chacune ;
* modifier et supprimer une équipe ;
* nommer librement une équipe ;
* sélectionner rapidement une équipe avant une activité ;
* organiser les créatures sur trois lignes.

Le joueur choisit les lignes, tandis que les colonnes et le regroupement contigu sont gérés automatiquement par les règles du combat.

L’interface doit empêcher ou expliquer les compositions invalides, notamment :

* plus de six créatures ;
* deux instances d’une même famille dont les chemins n’ont pas réellement divergé ;
* une instance temporairement inutilisable pour dépassement de capacité ;
* une restriction explicitement définie par un mode.

Le nombre d’équipes enregistrables et les règles d’utilisation d’une même instance dans plusieurs équipes enregistrées restent à définir.

## 9. Lisibilité pendant le combat

Le combat affiche principalement les résultats utiles de la simulation, sans exposer constamment les calculs, compteurs internes ou modificateurs intermédiaires.

Les Effets de combat importants actifs sur une cible sont représentés par des icônes :

* un effet à stacks utilise une seule icône accompagnée de son compteur ;
* deux instances indépendantes du même effet utilisent deux icônes distinctes ;
* la durée peut être représentée par un remplissage radial sans valeur textuelle permanente.

Une application réussie normale ou l’ajout d’une stack n’affiche aucun texte supplémentaire : l’apparition ou la mise à jour de l’icône suffit.

Le joueur doit pouvoir distinguer au moyen d’un feedback court :

* une Esquive ;
* une Immunité ;
* l’échec probabiliste d’un effet explicitement tenté.

Une résistance élémentaire ne produit pas de feedback spécifique : seule la valeur finale est affichée.

Le mode de contrôle est global au combat. En Auto, les Ultimate sont autorisées automatiquement ; en Manuel, le joueur peut demander leur déclenchement lorsqu’elles sont prêtes. Les Basic Attacks et Active restent automatiques.

La vitesse de visualisation peut être changée à tout moment. Le dernier choix est conservé pour le combat suivant. Cette vitesse ne modifie jamais la simulation, le résultat, les récompenses ou le coût en énergie.

## 10. Résultat et résumé post-combat

Après une victoire, le joueur doit pouvoir identifier :

* l’XP attribuée à chaque créature participante ;
* les niveaux et points gagnés ;
* l’XP et l’éventuel niveau gagné par le compte ;
* les récompenses obtenues ;
* les évolutions déclenchées ;
* les déblocages de jalon ;
* les actions suivantes disponibles.

Après une défaite, le joueur peut recommencer avec la même équipe, sélectionner une autre équipe, retourner à la gestion ou quitter l’activité. L’interface ne doit pas imposer automatiquement un build ou une solution unique.

Lorsqu’un mode définit explicitement une XP de défaite, le résultat affiche le gain de chaque créature concernée sans présenter cette exception comme une victoire ni comme une récompense principale.

Un résumé statistique simple est accessible pour les deux équipes. Il est agrégé par créature, pas par Skill, et peut couvrir :

* dégâts infligés et reçus ;
* soins effectués ;
* Bouclier accordé ;
* Cleanse et Dispel effectués ;
* contrôles appliqués ;
* autres statistiques globales pertinentes à définir.

Il ne constitue pas un combat log technique détaillé.

## 11. Fiche d’une instance

La fiche permet d’accéder aux informations pertinentes de l’instance, notamment :

* numéro de famille ;
* nom officiel de la forme et surnom éventuel ;
* lore ;
* rareté ;
* niveau, XP et étoiles ;
* stade et branche ;
* éléments, rôles suggérés et profil offensif ;
* score de Puissance ;
* caractéristiques principales et secondaires ;
* points disponibles ;
* Basic Attack et quatre Skills, avec description et élément propre ;
* trois emplacements d’Artefacts et deux emplacements de Sources d’énergie ;
* tags et verrouillage ;
* apparences de formes débloquées ;
* informations d’évolution découvertes.

Une fiche de Skill indépendante n’est pas obligatoire. La consultation principale des capacités s’effectue depuis la fiche de l’instance.

Les descriptions affichent autant que possible les valeurs concrètes calculées pour l’instance : dégâts, soins, durée effective, Bouclier et autres valeurs calculables. Lorsqu’une valeur dépend d’une cible future, la formule relative reste visible sans faux montant final.

## 12. Parcours de progression d’une instance

La fiche doit permettre :

* d’attribuer des points ;
* de gérer l’équipement ;
* de modifier le surnom et les tags ;
* de verrouiller ou déverrouiller l’instance ;
* de choisir une apparence débloquée ;
* de consulter les conditions d’évolution découvertes ;
* d’effectuer une réinitialisation ou une redistribution ;
* d’utiliser des instances non verrouillées comme matériaux d’étoiles.

La réinitialisation complète, la redistribution et la consommation d’une instance sont des actions irréversibles ou destructives nécessitant une présentation et des confirmations adaptées.

Le verrouillage empêche ces actions tant que le joueur ne déverrouille pas volontairement l’instance.

## 13. Évolution et montée d’étoile

Lorsqu’exactement une évolution standard est valide après une montée de niveau, elle est automatique et ne demande ni choix ni confirmation.

Lorsque plusieurs branches concurrentes sont valides, aucune évolution ne se produit et l’interface ne présente pas un choix manuel qui contournerait cette règle.

Un objet consommable d’évolution peut demander une confirmation avant sa consommation volontaire.

Une suite de plusieurs évolutions obtenues après la même récompense d’XP doit être présentée dans l’ordre.

Une montée d’étoile doit identifier l’instance cible, les instances utilisées comme matériaux, leur verrouillage éventuel, la perte irréversible de leur progression et la restitution automatique de leurs équipements.

## 14. Liste des instances et capacité

La liste prend en charge :

* la recherche dynamique sensible aux formes ;
* les tris validés ;
* l’identification de la forme, du stade et de la branche ;
* le score de Puissance recalculé ;
* l’état verrouillé ;
* l’état inutilisable pour dépassement de capacité.

L’interface distingue :

* la capacité gratuite ;
* les extensions permanentes ;
* la capacité totale ;
* le nombre d’instances possédées ;
* les instances grisées ;
* leur ordre dans la file de déblocage.

Elle indique qu’une créature obtenue au-delà de la capacité n’est jamais perdue et que la plus ancienne instance bloquée redevient automatiquement utilisable lorsqu’une place se libère.

## 15. Encyclopédie et arbre d’évolution

L’encyclopédie :

* affiche uniquement les familles découvertes ;
* utilise leurs numéros permanents sans zéro superflu ;
* ne révèle jamais le nombre total de familles ;
* distingue lore familial et lore de forme ;
* présente progressivement les formes et branches découvertes ;
* masque le nombre et l’identité des branches inconnues.

Avant la découverte complète, un arbre peut afficher :

> Forme de base → ??? → ???

Une forme rencontrée peut apparaître sans que sa condition d’évolution soit révélée. Les conditions découvertes restent ensuite consultables pour toutes les instances de la famille.

## 16. Collection de skins et apparences

La collection de skins permet de :

* parcourir séparément les séries de skins de carte ;
* consulter les skins débloqués et non débloqués ;
* visualiser la progression `X / X` d’une série et identifier clairement sa complétion ;
* connaître la disponibilité et le mode général d’obtention lorsque communicables ;
* consulter les skins disponibles pour une forme précise ;
* appliquer un skin débloqué à une forme compatible.

L’appartenance à une série et la méthode d’acquisition sont présentées comme deux informations distinctes. L’interface doit pouvoir organiser des séries distribuées par paquets ou par d’autres méthodes explicitement définies sans les confondre avec les offres commerciales correspondantes.

Chaque skin est lié à une forme précise. Le sélecteur d’apparence d’une instance distingue clairement sa forme mécanique actuelle, ses anciennes formes réellement parcourues et les skins débloqués propres à la forme affichée. Le changement est gratuit, hors-combat et sans effet mécanique.

Un skin Secret non obtenu apparaît comme une entrée connue mais masquée. L’interface indique son existence, sa rareté, la probabilité exacte lorsqu’il appartient à un pool et, lorsqu’elle est communiquée, la créature concernée. Son illustration et son nom précis restent masqués jusqu’à son obtention personnelle.

Le placeholder peut utiliser `???`, une silhouette générique non identifiable ou une autre représentation neutre. Le choix visuel final reste réservé à l’UI et à l’Art.

## 17. Invocation et acquisitions directes

Le parcours d’invocation reste distinct de l’ouverture d’un paquet de skins.

Avant une invocation, le joueur doit pouvoir connaître la ressource utilisée, le coût unitaire et les informations publiques du pool permanent.

Le joueur choisit la quantité avec le sélecteur fonctionnel `MIN | - | nombre | + | MAX`. `MIN` sélectionne une invocation, `-` et `+` ajustent la quantité dans les limites permises et `MAX` sélectionne le nombre maximal finançable avec la ressource disponible. Une quantité dont le coût total ne peut pas être payé ne peut pas être sélectionnée ou confirmée.

Le parcours affiche le coût total correspondant à la quantité sélectionnée. Une opération de plusieurs invocations reste strictement équivalente au même nombre d’invocations unitaires et ne présente aucune remise, invocation gratuite, amélioration des taux ou garantie particulière.

Toute opération portant sur plus d’une invocation demande une confirmation avant la dépense. Cette confirmation affiche au minimum le nombre total d’invocations et leur coût total. Une invocation unitaire ne demande pas de confirmation supplémentaire du seul fait de sa quantité.

Une invocation unitaire utilise une révélation individuelle et une mise en scène plus ample. Une invocation multiple utilise une séquence globale suivie d’un récapitulatif groupé, sans imposer une longue succession de révélations individuelles complètes.

Chaque résultat doit permettre d’identifier :

* la famille et la forme de base obtenues ;
* la rareté de la famille ;
* la création d’une nouvelle instance ;
* une nouvelle découverte éventuelle ;
* l’ajout éventuel à la file de dépassement de capacité.

Il ne révèle pas les branches encore secrètes.

Le choix de la créature de départ et les autres acquisitions directes explicitement prévues utilisent un parcours adapté sans être présentés comme une invocation.

## 18. Quêtes journalières

L’interface présente les trois quêtes journalières du jour avec :

* leur objectif ;
* leur progression ;
* leur condition d’achèvement ;
* leur récompense ;
* le temps restant avant le renouvellement.

Elle ne propose que des quêtes utilisant des fonctionnalités déjà débloquées.

Une journée manquée ne retire aucune progression générale et ne supprime pas l’énergie accumulée. Aucune série de connexion punitive n’est présentée.

Le renouvellement, la récupération automatique ou manuelle et le traitement d’une récompense non réclamée restent à définir.

## 19. Fabrication, inventaire et sacs

Le système d’établi, ou équivalent, permet de sélectionner des composants et de fabriquer des Artefacts. Une bibliothèque conserve les recettes découvertes et permet de reproduire le même type d’Artefact, dont les propriétés finales peuvent varier.

Une combinaison invalide ne crée aucun objet et ne consomme aucun composant ; un feedback l’indique au joueur.

L’interface distingue l’inventaire principal limité du stockage illimité des composants. La capacité de base actuellement affichée est de `40` emplacements, valeur ajustable pendant les tests.

La gestion des sacs présente les six emplacements dédiés, la capacité de chaque sac et la capacité totale. Un sac reçu est automatiquement équipé lorsqu’un emplacement est libre ; sinon, il rejoint l’inventaire principal.

Le remplacement et le déséquipement doivent signaler clairement leurs conséquences sur la capacité et les places disponibles.

## 20. Parcours cosmétique et achats

La boutique est exclusivement cosmétique. Elle reste distincte des services payants de redistribution, de vitesse de visualisation, d’extension de capacité et de sacs.

Avant l’achat d’un paquet de skins, l’interface présente notamment :

* la série ;
* le nombre de skins contenus ;
* la liste des skins possibles ;
* les probabilités ;
* les règles et valeurs de conversion des doublons ;
* le prix réel ;
* la durée de disponibilité et la politique de retour ;
* l’absence de protection contre les doublons ou la malchance.

Lorsqu’un pool contient des skins Secrets, la liste indique leur existence, leur nombre, leur rareté `Secret` et leur probabilité exacte. Elle peut masquer leur illustration, leur nom précis et leurs détails esthétiques ; la créature concernée peut être affichée.

L’ouverture révèle uniquement des skins de carte. Elle n’utilise ni le vocabulaire, ni les ressources, ni la présentation fonctionnelle de l’invocation de créatures.

Chaque service de confort doit présenter son effet exact, son prix, ses limites, les alternatives gratuites concernées et le fait qu’il n’accorde aucune puissance inaccessible gratuitement.

## 21. Modes de long terme

Les layouts détaillés du PvP, des guildes, des événements, des Boss personnels, des World Boss, de la Tour infinie et des contenus saisonniers restent à concevoir à partir de leurs règles de Game Design.

Leurs parcours réutilisent les contrats communs d’information, de préparation, de résultat, de lisibilité et de transparence sans imposer dès maintenant une architecture de navigation.

### 21.1. Boss personnels

Le parcours d’un Boss personnel doit permettre de connaître :

* le boss actuellement disponible et sa rotation ;
* la progression persistante propre à ce boss ;
* le palier actuel et le palier précédent farmable ;
* les informations stratégiques nécessaires ;
* la table de loot ou un aperçu pertinent de ses récompenses ;
* le coût de la tentative en énergie générale.

### 21.2. World Boss

Le parcours d’un World Boss doit présenter :

* le temps restant de l’apparition ;
* les PV globaux restants et l’état vivant, vaincu ou expiré ;
* le coût normal d’une tentative ou son coût tardif majoré ;
* la contribution du joueur ;
* son éligibilité à la récompense finale et l’état de cette récompense ;
* les informations nécessaires à la préparation du combat.

Le résumé d’une tentative distingue les dégâts personnels, leur contribution réelle aux PV globaux lorsque le boss est vivant, l’état restant du boss et les dégâts seulement simulés d’une participation tardive.

### 21.3. Tour infinie

Le parcours de la Tour infinie doit permettre de connaître :

* la saison actuelle, son thème et ses modificateurs ;
* l’étage actuel et la récompense unique associée ;
* la progression saisonnière ;
* le classement et les informations de prestige disponibles ;
* les récompenses pertinentes ;
* le temps restant avant la fin de la saison lorsqu’il s’applique ;
* le coût de la tentative en énergie générale.

L’interface ne doit pas suggérer qu’un étage terminé peut être rejoué ou qu’un ancien étage constitue une boucle de farming.

## 22. Dépendances

Le présent document traduit les besoins fonctionnels des documents spécialisés, notamment [`09-GACHA.md`](./09-GACHA.md), [`10-PROGRESSION.md`](./10-PROGRESSION.md), [`11-COLLECTION.md`](./11-COLLECTION.md), [`12-MODES.md`](./12-MODES.md), [`13-PVE.md`](./13-PVE.md), [`14-PVP.md`](./14-PVP.md), [`16-EVENTS.md`](./16-EVENTS.md) et [`17-QUESTS.md`](./17-QUESTS.md).

Il dépend également des règles de combat, créatures, Skills, éléments, Effets de combat, évolutions, objets et monétisation. Une décision d’interface ne peut pas modifier leurs règles fonctionnelles.

## 23. Éléments à préciser ultérieurement

* L’architecture de navigation et le nombre d’écrans ou d’onglets.
* La disposition, les grilles et la densité d’information.
* La grammaire et les contrôles exacts de recherche.
* La présentation des tris et filtres.
* Les confirmations des actions irréversibles.
* Les règles détaillées d’accessibilité.
* Les informations visibles dans chaque variante contextuelle de carte.
* Le wording et le rendu graphique des tooltips, icônes, timers et feedbacks.
* La liste définitive des statistiques du résumé post-combat.
* La présentation détaillée de l’inventaire, de l’iLvl et des comparaisons d’équipement.
* Les protections lorsqu’un sac ne peut pas être déséquipé.
* Les tutoriels, leurs jalons et leur ordre exact.
* La disposition et le rendu graphique du sélecteur de quantité d’invocation.
* Le wording et la présentation détaillée de la confirmation d’une invocation multiple.
* Les animations de révélation unitaire, la séquence globale et le récapitulatif groupé d’une invocation multiple.
* Les animations d’évolution et de montée d’étoile.
* La présentation d’une série complétée et d’une éventuelle reconnaissance strictement cosmétique ou honorifique.
* L’organisation des séries utilisant des méthodes d’acquisition différentes.
* Le wording, le placeholder, la présentation de la rareté et l’affichage éventuel de la créature concernée pour un skin Secret.
* L’animation de révélation personnelle d’un skin Secret.
* La présentation commerciale des services de confort.

## 24. Questions ouvertes

* Quelle architecture de navigation relie le mode Histoire, les activités, la gestion, la collection et l’inventaire ?
* Quelles informations doivent être visibles dans chaque variante de carte sans surcharger l’écran mobile ?
* Quelles règles d’accessibilité doivent être obligatoires dès la première version ?
* Comment présenter les choix et filtres avancés de recherche sur écran tactile ?
* Comment organiser le résultat d’un combat lorsque plusieurs niveaux, évolutions, déblocages et récompenses se produisent ensemble ?
* Les récompenses de quêtes sont-elles récupérées automatiquement ou manuellement ?
