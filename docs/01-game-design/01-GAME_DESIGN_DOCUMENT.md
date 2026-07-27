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
* les modèles de créatures et de monstres ;
* les compétences, éléments et effets de statut ;
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
* les coefficients et tables d’affinités ;
* les coûts en énergie ;
* les temps de régénération ;
* les valeurs d’expérience ;
* les probabilités d’invocation ou d’ouverture ;
* les quantités de récompenses ;
* les limites numériques précises ;
* les listes exhaustives de créatures, compétences, effets de statut, équipements ou quêtes ;
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

Le joueur possède un rôle fictionnel légèrement défini. Il est capable de créer un lien avec les créatures, de révéler leur potentiel, de les accompagner et de diriger plusieurs équipes.

Le nom provisoire de ce rôle est **Éveilleur**. Ce nom ne constitue pas encore un terme définitif de l’univers.

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
* des effets de statut ;
* des synergies.

Le contrôle laissé au joueur pendant le combat offre une implication limitée. Il ne doit pas transformer le timing ou la précision gestuelle en facteur principal de réussite.

### 3.3. Personnalisation autour d’identités fixes

Chaque créature possède une identité fonctionnelle déterminée notamment par :

* son ensemble fixe de quatre compétences ;
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

La collection valorise ce que le joueur possède et lui permet de visualiser ce qu’il lui manque. Elle ne remplace ni la gestion des créatures ni l’inventaire.

La personnalisation cosmétique renforce l’attachement et la collection sans produire de puissance.

### 4.3. Deux rythmes complémentaires

Le jeu alterne :

* des moments d’activité rapides, centrés sur la sélection d’une équipe et le combat ;
* des moments de gestion, centrés sur la progression, l’équipement et l’optimisation des équipes.

Le joueur ne doit pas être obligé d’ouvrir tous les systèmes de gestion entre deux niveaux.

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
* compléter le catalogue des créatures ;
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
* créer une équipe de six créatures ;
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
* servir de principale source de déblocage des fonctionnalités ;
* pouvoir recevoir de nouveaux mondes et niveaux au fil du développement ;
* soutenir une progression très longue sans exiger une narration détaillée pour chaque ajout.

La puissance d’équipe peut servir d’indication de difficulté. Elle ne constitue pas un verrou systématique.

### 8.4. Informations avant un niveau

Pour un contenu ordinaire, le joueur doit connaître suffisamment d’informations pour sélectionner une équipe pertinente :

* les éléments des monstres ;
* les principales menaces ;
* les effets de statut importants ;
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

Elle possède notamment :

* une rareté de créature ;
* un ou deux éléments au maximum ;
* six caractéristiques principales ;
* un ensemble fixe de quatre compétences ;
* une progression individuelle ;
* un niveau d’étoiles ;
* une forme dans sa famille de créatures ;
* un emplacement d’équipement.

### 10.2. Compétences fixes

L’ensemble de compétences comprend :

* une compétence active ;
* deux compétences passives ;
* une compétence ultime.

Lorsqu’une créature est obtenue, cet ensemble est déjà déterminé.

Le joueur :

* ne choisit pas les compétences ;
* ne les remplace pas ;
* ne sélectionne pas un ensemble alternatif ;
* ne construit pas le build à partir d’une liste de compétences.

Les compétences définissent l’identité fonctionnelle, le rôle et les synergies potentielles de la créature.

**Question ouverte :**

* Une nouvelle forme obtenue lors d’une évolution conserve-t-elle les mêmes compétences ou possède-t-elle un nouvel ensemble prédéfini ?

Dans tous les cas, le joueur ne sélectionne pas librement les compétences de la forme obtenue.

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

* La conservation de l’évolution, du niveau d’étoiles, de l’équipement et des autres éléments lors d’une réinitialisation complète.
* La méthode d’obtention et le rythme de distribution de l’objet.
* La limite exacte du service payant, notamment par compte ou par créature.
* Le prix et la présentation du service.

### 10.4. Équipes enregistrées

Une équipe complète comporte six créatures.

Le joueur peut :

* créer plusieurs équipes ;
* sélectionner les six créatures de chacune ;
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
* les affinités élémentaires ;
* les effets de statut ;
* les synergies de la composition.

### 11.2. Mode de contrôle

Les attaques et compétences ordinaires sont utilisées automatiquement.

Le joueur peut :

* déclencher manuellement les compétences ultimes ;
* activer une option automatique qui gère également les compétences ultimes.

Le combat peut ainsi être semi-automatique ou entièrement automatique selon le choix du joueur.

Les contenus déjà maîtrisés doivent pouvoir être joués entièrement automatiquement.

### 11.3. Rythme et lisibilité

La durée moyenne visée d’un combat est de **30 à 60 secondes**.

Le combat doit rendre visibles :

* les actions importantes ;
* les effets de statut ;
* les affinités déterminantes ;
* les compétences ultimes ;
* les éliminations ;
* les changements majeurs dans l’équilibre du combat.

Les règles exactes d’ordre des actions, de ciblage, de dégâts, de coups critiques et d’intelligence de combat seront définies dans `02-COMBAT.md`.

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

Une défaite n’accorde :

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

Le résultat doit fournir des informations utiles sur :

* les principales sources de dégâts ;
* les éléments importants ;
* les effets de statut subis ;
* les créatures mises hors combat ;
* les moments déterminants ;
* la progression générale du combat.

Le jeu ne doit pas imposer automatiquement une solution ou un build unique.

## 13. Progression des créatures et du compte

### 13.1. Progression des créatures

Les créatures gagnent de l’expérience en participant aux combats remportés.

Lorsqu’une créature monte de niveau :

* sa progression individuelle augmente ;
* elle reçoit des points de caractéristiques ;
* le joueur répartit ces points sur cette même créature.

La progression doit pouvoir se poursuivre très longtemps. Le temps nécessaire à chaque nouveau niveau augmente progressivement selon un principe de rendements décroissants.

### 13.2. Progression du compte

Le compte possède un niveau numérique.

Il gagne de l’expérience lorsque le joueur accomplit une activité.

La progression du compte :

* est beaucoup plus lente que celle des créatures ;
* représente la progression générale et l’ancienneté du joueur ;
* accorde une récompense à chaque niveau ;
* peut participer à certains déblocages secondaires ;
* ne remplace pas le mode Histoire comme principale source de déblocage.

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

* la présence ou l’absence d’un niveau maximal strict ;
* les courbes d’expérience ;
* les valeurs nécessaires à chaque niveau ;
* les récompenses du niveau de compte ;
* les éventuels déblocages secondaires ;
* les interactions entre niveau, évolution et niveau d’étoiles.

## 14. Énergie et régulation

### 14.1. Fonction

Le mode Histoire utilise une énergie nécessaire pour entrer dans ses niveaux.

Cette énergie régule :

* le nombre de niveaux joués sur une période ;
* le gain d’expérience des créatures ;
* le gain d’expérience du compte ;
* la vitesse générale de progression.

### 14.2. Régénération et accumulation

L’énergie :

* se régénère avec le temps ;
* continue à s’accumuler lorsque le joueur ne joue pas ;
* ne doit pas être perdue simplement parce que le joueur ne s’est pas connecté pendant une journée ;
* doit permettre d’utiliser ultérieurement une partie du temps de régénération accumulé.

La récupération d’énergie constitue la seule progression hors ligne validée.

### 14.3. Garde-fous

L’énergie ne doit pas être vendue contre de l’argent réel.

Le système doit préserver :

* la possibilité de rattrapage ;
* la lisibilité ;
* l’équilibrage économique ;
* les contraintes techniques ;
* un rythme mobile qui ne bloque pas immédiatement un joueur absent.

### 14.4. Éléments à préciser ultérieurement

`10-PROGRESSION.md` devra définir :

* le coût des niveaux ;
* le rythme de régénération ;
* la limite d’accumulation ou l’absence de limite stricte ;
* les éventuels objets de récupération obtenus en jouant ;
* les autres activités utilisant éventuellement cette énergie ;
* les exceptions de consommation pendant l’onboarding.

## 15. Acquisition et invocation de créature

### 15.1. Voie principale

L’invocation de créature constitue la principale voie d’obtention des créatures.

Une invocation accorde la forme de base d’une famille de créatures, jamais directement sa forme finale.

Certaines créatures peuvent être accordées directement par le gameplay lorsqu’elles constituent une exception explicitement documentée.

### 15.2. Créature de départ

Le joueur choisit directement sa première créature parmi trois.

Cette obtention constitue une exception validée à l’invocation comme voie principale.

### 15.3. Ressource générale d’invocation

Une ressource générale principale permet d’effectuer les invocations de créatures.

Elle est obtenue principalement grâce :

* au mode Histoire ;
* aux quêtes journalières ;
* aux activités ;
* aux récompenses de progression ;
* aux événements.

Elle reste entièrement séparée de l’économie cosmétique.

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

### 16.2. Fonction dans la boucle globale

La collection :

* valorise les acquisitions ;
* rend visible la progression du joueur ;
* permet d’identifier ce qui manque ;
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

Le service payant de réinitialisation des points de caractéristiques constitue une exception de confort limitée, distincte de la boutique cosmétique. Il permet uniquement de redistribuer des points déjà gagnés sans retour au niveau 1 et ne fournit aucun avantage de potentiel par rapport aux méthodes gratuites.

Les règles complètes de la boutique, des paquets de skins de carte, des doublons et de cette exception sont définies par le cadre de monétisation.

## 17. Motivation et retour au jeu

### 17.1. Moteurs principaux

Les principaux moteurs de long terme sont :

1. développer les créatures favorites ;
2. créer et maîtriser plusieurs équipes spécialisées ;
3. progresser dans les mondes et niveaux du mode Histoire ;
4. débloquer de nouvelles fonctionnalités et activités ;
5. obtenir de nouvelles créatures et synergies ;
6. compléter le catalogue des créatures ;
7. compléter les séries de skins de carte ;
8. progresser ultérieurement en PvP ;
9. participer ultérieurement à une guilde ou à des objectifs communautaires.

### 17.2. Régulation de la progression longue

La progression très longue est maîtrisée par :

* des rendements décroissants ;
* l’énergie ;
* l’augmentation progressive de la difficulté ;
* le besoin de diversifier les équipes et stratégies.

Ces principes ne valident pas encore une progression strictement infinie ni une formule précise.

### 17.3. Événements et rotations

Les événements pourront :

* proposer de nouveaux défis ;
* mettre en valeur certaines équipes ou certains éléments ;
* offrir des récompenses particulières ;
* renouveler les objectifs ;
* introduire temporairement de nouveaux contenus.

Leur calendrier, leur cadence et leurs règles détaillées ne sont pas définis dans le GDD.

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

Les fondations envisagent :

* des boss personnels ;
* des boss de serveur ;
* une tour infinie ;
* du PvP ;
* des événements temporaires ;
* des guildes ;
* des contenus saisonniers.

Leur présence dans cette liste ne valide ni leurs règles, ni leur ordre de production, ni leur date de disponibilité.

### 18.5. Possibilités non validées

Tout autre mode ou variante non explicitement validé doit rester présenté comme une possibilité.

Les règles détaillées et le statut futur de chaque mode seront définis dans `12-MODES.md` et les documents spécialisés associés.

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
* quatre compétences fixes par créature ;
* quelques éléments ;
* quelques effets de statut ;
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
* les boss de serveur ;
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

Le GDD dépendra des futurs documents suivants pour les détails :

* `02-COMBAT.md` — déroulement, ordre des actions, ciblage, dégâts et contrôle ;
* `03-CREATURES.md` — modèle des créatures, caractéristiques, rôles et règles de progression propres ;
* `04-SKILLS.md` — structure et règles des compétences fixes ;
* `05-ELEMENTS.md` — table des affinités et coefficients ;
* `06-STATUS_EFFECTS.md` — liste, application, cumul, retrait, résistances et immunités ;
* `07-EVOLUTIONS.md` — conditions et effets des évolutions ;
* `08-ITEMS.md` — équipements et objets, dont l’objet de réinitialisation ;
* `09-GACHA.md` — règles de l’invocation de créature ;
* `10-PROGRESSION.md` — expérience, niveaux, énergie, réinitialisations et progression du compte ;
* `11-COLLECTION.md` — catalogue et collections ;
* `12-MODES.md` à `17-ACHIEVEMENTS.md` — activités et objectifs spécialisés ;
* `18-UI_FLOW.md` — écrans, navigation, tutoriels et parcours.

### 20.2. Questions ouvertes conservées

Les questions suivantes ne bloquent pas le fonctionnement global décrit par le GDD :

* le nom définitif du rôle provisoirement appelé « Éveilleur » ;
* le maintien ou le remplacement prédéfini des compétences lors d’une évolution ;
* l’existence d’un bonus entre une créature et une compétence partageant son élément ;
* la table exacte des affinités et ses coefficients ;
* le rôle exact de l’Agilité dans l’ordre et la fréquence des actions ;
* les règles détaillées des effets de statut ;
* les règles de conservation lors d’une réinitialisation complète ;
* la méthode d’obtention et le rythme de distribution de l’objet de réinitialisation ;
* la limite et le prix du service payant de réinitialisation ;
* les courbes d’expérience et l’existence éventuelle de niveaux maximaux ;
* les récompenses et usages secondaires du niveau de compte ;
* les coûts, la régénération et l’accumulation exacte de l’énergie ;
* le nom, la représentation et le rythme d’obtention de la ressource générale d’invocation ;
* les premières créatures, invocations garanties et jalons exacts de l’onboarding ;
* le nombre d’équipes enregistrables et leurs règles de partage des créatures ;
* les listes et récompenses des quêtes journalières ;
* les règles détaillées des modes envisagés ;
* la cadence des événements et mises à jour ;
* les quantités et données exactes de la vertical slice.

### 20.3. Principe de maintien

Une question ouverte ne doit pas être transformée en règle définitive sans validation.

Lorsqu’un futur document spécialisé répond à une question qui modifie le fonctionnement global, la réponse doit être reportée dans le GDD. Lorsqu’elle modifie un principe de fondation, les documents de fondation concernés doivent également être mis à jour.
