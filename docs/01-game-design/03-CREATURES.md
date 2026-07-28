# Project Awakening — Créatures

**Statut :** Draft de conception — base initiale à compléter

## 1. Rôle et périmètre du document

Ce document rassemble les décisions validées qui définissent la structure fonctionnelle des créatures jouables de **Project Awakening**.

Il complète la [vision](../00-foundation/01-VISION.md), le [GDD central](./01-GAME_DESIGN_DOCUMENT.md) et les [règles de combat](./02-COMBAT.md). Il ne définit pas les formules du moteur de combat, les listes de Skills, la table élémentaire détaillée, les règles individuelles des effets de statut, les coûts de progression ou le modèle technique des données.

## 2. Identité fonctionnelle d’une créature

Une créature est une entité jouable collectionnée, possédée, développée et utilisée par le joueur. Elle est représentée dans l’interface par une carte de créature.

Chaque créature possède notamment :

* une rareté de créature ;
* un ou deux éléments au maximum ;
* une Basic Attack ;
* exactement quatre Skills prédéfinis ;
* six caractéristiques principales ;
* trois caractéristiques secondaires système ;
* une progression individuelle ;
* un niveau d’étoiles ;
* une forme dans une famille de créatures ;
* un emplacement d’équipement.

Ces propriétés définissent son identité fonctionnelle, son rôle et ses synergies potentielles. Le modèle de données complet reste à concevoir ultérieurement.

## 3. Caractéristiques

### 3.1. Caractéristiques principales

Les six caractéristiques principales sont :

1. PV ;
2. Attaque ;
3. Attaque spéciale ;
4. Défense ;
5. Défense spéciale ;
6. Agilité.

Seules les caractéristiques principales reçoivent les points de caractéristiques gagnés lors des montées de niveau.

L’Agilité contrôle l’intervalle des Basic Attacks selon les règles du document Combat. Elle n’augmente pas le Crit.

### 3.2. Caractéristiques secondaires

Les trois caractéristiques secondaires système sont :

1. Crit ;
2. Dégâts critiques ;
3. Esquive.

Elles ne reçoivent pas directement les points gagnés lors des montées de niveau. Elles peuvent notamment provenir des valeurs de base de la créature, de son équipement, de ses Skills, de ses Passive, des buffs, des debuffs ou d’autres systèmes de progression explicitement documentés.

### 3.3. Valeurs utilisées en combat

Le moteur de combat reçoit les caractéristiques finales préparées hors combat. Les règles de conversion, de précision numérique et de modification temporaire sont définies dans [`02-COMBAT.md`](./02-COMBAT.md).

**Éléments à préciser ultérieurement :**

* Les valeurs de base et les courbes propres aux créatures.
* Les éventuelles limites de répartition des points de caractéristiques.
* Les règles détaillées reliant progression, évolution, niveau d’étoiles et valeurs finales.

## 4. Basic Attack et ensemble fixe de Skills

La Basic Attack est distincte des quatre Skills de la créature. Elle possède notamment son propre élément, son intervalle, son gain d’énergie, son nombre de hits et ses règles de ciblage.

L’ensemble fixe comprend exactement :

* une Ultimate ;
* trois autres Skills formant une combinaison fixe d’Active et de Passive.

Les répartitions possibles comprennent notamment :

* une Active, deux Passive et une Ultimate ;
* deux Active, une Passive et une Ultimate.

Le joueur ne choisit pas ces Skills, ne les remplace pas et ne construit pas le build de la créature en les sélectionnant dans une liste.

**Question ouverte :**

* Une nouvelle forme obtenue lors d’une évolution conserve-t-elle les mêmes Skills ou possède-t-elle un nouvel ensemble prédéfini ?

## 5. Éléments

Une créature est mono-élément ou bi-élément. Les deux éléments d’une créature bi-élément sont mécaniquement égaux et ne sont pas hiérarchisés comme principal et secondaire.

Les éléments d’une créature restent distincts de l’élément de sa Basic Attack et de chacun de ses Skills. Les règles complètes sont définies dans [`05-ELEMENTS.md`](./05-ELEMENTS.md).

## 6. Équipe et formation

Une équipe peut réunir jusqu’à six créatures.

La formation de combat utilise une grille de trois lignes et six colonnes. Le joueur choisit :

* la ligne de chaque créature ;
* son ordre de gauche à droite dans cette ligne.

Les colonnes sont attribuées automatiquement et la formation est centrée. Le joueur ne crée pas volontairement d’emplacement vide pendant la préparation.

Les positions restent fixes pendant le combat. Elles ne sont pas recentrées après la mort ou l’Exclusion d’une créature.

Les règles complètes de présence, de ciblage et de voisinage appartiennent au document Combat.

**Éléments à préciser ultérieurement :**

* La taxonomie officielle des rôles de créature.
* Les informations affichées sur la fiche de créature et l’écran de formation.
* Les éventuelles restrictions de composition propres à certains modes.

## 7. Progression, évolution et niveau d’étoiles

Les créatures gagnent de l’expérience en participant aux combats. Lors d’une montée de niveau, les points reçus sont attribués à la créature concernée et répartis par le joueur entre ses caractéristiques principales.

L’invocation donne normalement accès à la forme de base d’une famille de créatures. Le joueur accompagne ensuite cette créature au fil de sa progression et de ses évolutions ; la forme finale n’est pas obtenue directement par invocation.

Les doublons de créature servent à améliorer le niveau d’étoiles de la créature concernée et à augmenter progressivement son potentiel sans recommencer son évolution.

La répartition des caractéristiques n’est pas librement réversible. Les trois voies validées sont :

1. une réinitialisation complète gratuite avec retour au niveau 1 ;
2. un objet rare obtenu en jouant, sans retour au niveau 1 ;
3. un service payant limité fournissant le même résultat immédiat que cet objet.

Les coûts, rythmes, limites, courbes et règles détaillées appartiendront aux documents consacrés aux évolutions, aux objets et à la progression.

## 8. Créatures jouables et monstres ennemis

Une **créature** est jouable, collectionnée, possédée et développée par le joueur.

Un **monstre** est une entité ennemie affrontée dans une activité. Il n’est ni collectionné, ni possédé, ni développé comme une créature jouable et ne fait pas partie de l’équipe du joueur.

Une même inspiration visuelle ou narrative ne suffit pas à confondre ces deux catégories fonctionnelles.

## 9. Dépendances documentaires

* [`02-COMBAT.md`](./02-COMBAT.md) définit les règles communes du moteur de combat.
* [`04-SKILLS.md`](./04-SKILLS.md) organise la Basic Attack, les Active, les Passive et les Ultimate.
* [`05-ELEMENTS.md`](./05-ELEMENTS.md) définit les interactions élémentaires.
* [`06-STATUS_EFFECTS.md`](./06-STATUS_EFFECTS.md) organise les effets de statut.
* Les futurs documents `07-EVOLUTIONS.md`, `08-ITEMS.md` et `10-PROGRESSION.md` détailleront les systèmes de développement correspondants.

