# Project Awakening — Éléments

**Statut :** Rédigé — référence actuelle, à maintenir à jour

## 1. Rôle et périmètre du document

Ce document définit la conception du système élémentaire de **Project Awakening**.

Il constitue la référence actuelle pour :

* les éléments des formes de créatures ;
* les éléments des Basic Attacks et des Skills ;
* l’héritage élémentaire des effets produits par une capacité ;
* les changements d’élément d’une capacité pendant le combat ;
* les résistances et immunités élémentaires ;
* les conséquences élémentaires sur la résolution et la lisibilité du combat.

Il complète les [règles de combat](./02-COMBAT.md), les [règles des créatures](./03-CREATURES.md), les [Skills](./04-SKILLS.md), les [Effets de combat](./06-COMBAT_EFFECTS.md) et les [évolutions](./07-EVOLUTIONS.md) sans les remplacer.

Les valeurs et formules générales de dégâts appartiennent au document Combat. Les éléments concrets des futures créatures et capacités appartiendront à leurs données de production.

## 2. Les neuf éléments officiels

La liste officielle comprend exactement neuf éléments :

1. Feu ;
2. Eau ;
3. Terre ;
4. Vent ;
5. Plante ;
6. Métal ;
7. Électricité ;
8. Lumineux ;
9. Ténèbres.

Le nom officiel du huitième élément est **Lumineux**, et non « Lumière ».

Il n’existe aucun élément **Neutre** et aucune capacité **sans élément**.

## 3. Éléments d’une créature

### 3.1. Forme mono-élément ou bi-élément

Chaque forme d’une créature possède :

* exactement un élément ;
* ou deux éléments.

Les deux éléments d’une créature bi-élément sont mécaniquement égaux. Aucun n’est principal ou secondaire.

Toutes les combinaisons de deux éléments sont autorisées par défaut. Une créature bi-élément ne reçoit aucun avantage ou désavantage global automatique, et une créature mono-élément aucune compensation systématique. Leur équilibre dépend de leur profil complet.

### 3.2. Évolution d’une forme

Une évolution peut ajouter, retirer ou remplacer un élément lorsque cela reste cohérent avec le lore, les pouvoirs, les capacités, les résistances ou le style de combat de la nouvelle forme.

Deux branches d’une même famille peuvent donc posséder des éléments différents.

### 3.3. Stabilité pendant le combat

Le ou les éléments de la forme mécanique actuelle restent fixes pendant tout le combat.

Aucun Skill ne peut temporairement :

* ajouter, retirer ou remplacer un élément de la créature ;
* transformer une créature mono-élément en créature bi-élément ;
* transformer une créature bi-élément en créature mono-élément.

Les changements d’éléments d’une créature appartiennent aux formes et aux évolutions, jamais à un effet temporaire de combat.

## 4. Élément d’une capacité

### 4.1. Élément obligatoire

Chaque capacité possède exactement un des neuf éléments officiels. Cette règle s’applique à :

* la Basic Attack ;
* chaque Active ;
* chaque Passive ;
* l’Ultimate.

Une Passive conserve un élément même lorsqu’elle ne produit normalement aucun effet soumis à une interaction élémentaire.

### 4.2. Indépendance par rapport à la créature

L’élément d’une capacité est indépendant du ou des éléments de la créature qui l’utilise.

Une capacité peut employer n’importe lequel des neuf éléments lorsque ce choix correspond à ce qu’elle représente et reste cohérent avec le lore et le concept de la créature. Aucune règle mécanique ne lui impose d’utiliser un élément naturel de son utilisateur.

### 4.3. Un seul élément à un instant donné

Une capacité possède toujours un seul élément à un instant donné, y compris lorsqu’elle est :

* multi-hit ;
* multi-cible ;
* une AoE ;
* composée de plusieurs effets ;
* fondée sur un hit hybride Physique et Spécial.

Tous les hits et toutes les composantes de dégâts d’une même utilisation emploient l’élément actuel de la capacité. Le système standard ne permet pas que différents hits d’une même utilisation possèdent des éléments différents.

### 4.4. Héritage par les effets produits

Tous les effets directement produits par une capacité héritent de l’élément de cette capacité au moment où ils sont créés ou appliqués.

Cela comprend notamment :

* les dégâts directs, périodiques et retardés ;
* les soins et HoT ;
* les buffs et debuffs ;
* les CC et autres Effets de combat ;
* les applications de Bouclier ;
* les autres effets appliqués à une cible.

Il n’est donc pas nécessaire d’attribuer manuellement un autre élément à chaque effet interne d’une même capacité.

Lorsqu’un effet provient d’une autre source explicitement documentée, cette source doit également définir l’élément transmis à l’effet.

## 5. Changement d’élément d’une capacité

### 5.1. Modification pendant le combat

Contrairement aux éléments de la créature, l’élément d’une capacité peut changer pendant le combat lorsqu’un Skill le prévoit explicitement.

Une capacité peut notamment modifier temporairement l’élément d’une Basic Attack ou d’un autre Skill, définir l’élément d’une prochaine utilisation ou faire dépendre son propre élément d’une condition explicite.

Tous les effets produits pendant que la capacité possède son nouvel élément héritent de ce nouvel élément.

### 5.2. Snapshot des effets créés

Un effet déjà créé ou appliqué conserve l’élément qu’il possédait à cet instant. Un changement ultérieur de l’élément de sa capacité source ne le modifie pas rétroactivement.

Cette règle s’applique notamment :

* aux DoT et HoT déjà appliqués ;
* aux buffs, debuffs et CC déjà appliqués ;
* aux effets retardés déjà créés.

Chaque nouvelle création ou application utilise l’élément actuel de la capacité à ce nouveau moment.

Le Bouclier constitue une exception après son application : la tentative d’ajout possède bien l’élément actuel du Skill et peut être bloquée par une immunité élémentaire, mais la valeur ajoutée rejoint ensuite une réserve commune qui ne possède plus d’élément propre.

### 5.3. Capacité déclenchée par une autre

Lorsqu’une capacité provoque l’utilisation d’une autre capacité, la capacité déclenchée conserve son propre élément actuel.

L’élément de la capacité déclencheuse n’est pas transmis automatiquement. Une transmission ou une modification n’existe que si l’effet la définit explicitement.

## 6. Résistances élémentaires

### 6.1. Système exclusivement défensif

Le système élémentaire standard est défensif. Il n’accorde aucun bonus offensif automatique.

Il n’existe aucune faiblesse élémentaire générale, aucun équivalent de « super efficace » et aucune augmentation automatique des dégâts contre un élément.

Les relations standard sont :

* une **résistance** lorsque l’un des éléments de la cible résiste à l’élément de la capacité ;
* une **interaction neutre** lorsqu’aucune résistance ne s’applique.

Le même élément contre lui-même est neutre. Les relations ne sont pas obligatoirement réciproques.

### 6.2. Table des résistances

La table se lit ainsi : **élément de la cible → éléments des capacités auxquels il résiste**.

| Élément de la cible | Résiste aux dégâts des capacités |
|---|---|
| Feu | Plante, Métal, Ténèbres |
| Eau | Feu, Lumineux, Métal |
| Plante | Eau, Terre, Lumineux |
| Terre | Électricité, Feu, Eau |
| Vent | Terre, Feu, Plante |
| Électricité | Vent, Eau, Ténèbres |
| Métal | Plante, Terre, Vent |
| Ténèbres | Lumineux, Vent, Électricité |
| Lumineux | Ténèbres, Électricité, Métal |

Chaque élément défensif possède exactement trois résistances. Chaque élément de capacité est résisté par exactement trois éléments.

### 6.3. Taux actuel

Le taux standard actuel d’une résistance élémentaire est fixé à :

> **30 %**

Une résistance conserve donc actuellement `70 %` des dégâts entrants correspondants :

> `Dégâts après résistance = Dégâts avant résistance × 0,70`

Le taux de `30 %` reste un paramètre ajustable pendant le balancing. Il constitue la référence actuelle, non une constante immuable du Game Design.

### 6.4. Double résistance

Pour une cible bi-élément :

* si un seul de ses éléments résiste, la réduction est appliquée une fois ;
* si les deux résistent, les deux réductions sont appliquées successivement et multiplicativement.

Avec le taux actuel :

> `Dégâts après double résistance = Dégâts avant résistance × 0,70 × 0,70`

La cible conserve alors `49 %` des dégâts entrants, soit une réduction effective totale de `51 %`.

Les deux résistances ne sont jamais additionnées directement. La deuxième ne possède ni cap ni traitement particulier.

### 6.5. Effets concernés

Une résistance élémentaire réduit uniquement les dégâts de l’élément correspondant :

* dégâts directs ;
* dégâts périodiques, dont les ticks de DoT ;
* dégâts retardés.

Elle ne réduit ni les soins, ni les HoT, buffs, debuffs, CC, Boucliers, probabilités d’application, durées d’Effets de combat ou autres résultats non dommageables.

Un DoT conserve l’élément enregistré lors de son application. Chacun de ses ticks utilise cet élément et les résistances de la cible au moment du tick.

### 6.6. Stabilité des résistances

Les résistances découlent exclusivement du ou des éléments fixes de la forme actuelle.

Aucun Skill ne peut directement gagner, perdre, supprimer, inverser, augmenter, réduire ou ignorer une résistance élémentaire standard pendant le combat. Un Skill ne peut pas davantage modifier le taux propre à une relation.

Les immunités explicitement accordées par des Skills restent un mécanisme distinct.

## 7. Immunité élémentaire

### 7.1. Attribution explicite

La table élémentaire ne confère aucune immunité naturelle.

Une immunité élémentaire existe uniquement lorsqu’un Skill l’accorde explicitement. Sa description définit l’élément concerné, ses conditions, sa durée et son éventuelle persistance jusqu’à la fin du combat.

### 7.2. Portée complète

Une immunité élémentaire bloque tous les effets de l’élément concerné, qu’ils soient positifs ou négatifs.

Elle peut donc bloquer notamment :

* les dégâts directs, périodiques et retardés ;
* les soins et HoT ;
* les buffs, debuffs, CC et autres Effets de combat ;
* les applications de Bouclier ;
* tout autre effet correspondant à cet élément.

Cette règle s’applique quelle que soit la source : ennemi, allié ou créature immunisée elle-même. Une immunité peut donc empêcher la créature de profiter d’un effet positif du même élément.

### 7.3. Résolution par cible

Une immunité est vérifiée indépendamment pour chaque cible et pour chaque effet concerné. Dans une capacité multi-cible, elle n’annule pas les résolutions destinées aux autres cibles.

Une immunité peut être temporaire, conditionnelle ou active jusqu’à la fin du combat. Dans ce contexte, le terme « permanent » signifie au maximum « jusqu’à la fin du combat ».

### 7.4. Immunités ciblées

Une immunité ciblée à un principe, une famille ou un tag d’Effet de combat reste distincte d’une immunité élémentaire. Elle bloque uniquement le périmètre explicitement déclaré et ne modifie ni la table ni les résistances élémentaires.

## 8. Esquive, hit réussi et immunité

### 8.1. Ordre de résolution

Pour un hit soumis à l’Esquive, l’ordre conceptuel est :

1. résolution de l’Esquive ;
2. si le hit n’est pas esquivé, validation du hit et des événements liés à une cible touchée ;
3. vérification de l’immunité élémentaire ;
4. annulation sur cette cible des effets couverts par l’immunité ;
5. résolution normale des autres résultats éventuels.

L’immunité ne transforme pas rétroactivement un hit en Esquive ou en échec.

### 8.2. Basic Attack réussie

Une Basic Attack ayant au moins un hit non esquivé reste réussie même si une immunité élémentaire annule ensuite tous ses effets sur la cible.

Elle peut donc normalement :

* accorder son énergie ;
* faire progresser les compteurs d’Active ;
* déclencher les effets dépendant d’une Basic Attack réussie.

Si tous ses hits sont esquivés par toutes leurs cibles, les règles normales d’échec de la Basic Attack restent applicables.

### 8.3. Événements liés au résultat

Une cible immunisée reste considérée comme touchée lorsqu’elle n’a pas esquivé le hit.

En revanche, un événement exigeant un résultat réellement produit ne se déclenche pas lorsque l’immunité l’annule. Cela concerne notamment :

* « lorsqu’elle subit des dégâts » si aucun dégât n’est appliqué ;
* « lorsqu’elle reçoit un soin » si aucun soin n’est appliqué ;
* « lorsqu’un Effet de combat lui est appliqué » si l’effet est bloqué.

## 9. Présentation et lisibilité

### 9.1. Fiche de la créature

Le ou les éléments de la forme doivent être clairement visibles sur sa fiche.

La fiche permet également de consulter directement la Basic Attack et les quatre Skills, dont leur description et leur élément propre. Une fiche de Skill séparée de la fiche de la créature n’est pas une exigence du système.

Les pictogrammes, couleurs, libellés et autres conventions graphiques restent à définir dans les documents d’interface et de direction artistique.

### 9.2. Tooltips contextuels

Les termes de gameplay affichés doivent pouvoir donner accès directement à un tooltip contextuel concis lorsqu’une explication est utile.

Le tooltip d’un élément peut notamment présenter son rôle et les éléments de capacité auxquels il résiste. Une matrice globale des résistances n’est pas obligatoire dans l’interface actuelle.

Ce principe est transversal et s’applique également aux caractéristiques, Effets de combat, statuts contextuels et autres mots-clés selon les règles du [document UI Flow](./18-UI_FLOW.md).

### 9.3. Feedbacks de combat

Le combat affiche les résultats utiles de la simulation sans exposer constamment tous ses calculs internes.

Une résistance élémentaire ne produit aucun feedback spécifique : le joueur voit la valeur finale des dégâts ou du tick.

Une Esquive, une Immunité ou l’échec probabiliste d’un effet explicitement tenté produit un feedback court permettant d’identifier la cause de l’échec. Le wording et le rendu graphique exacts restent à définir.

Un changement temporaire d’élément d’une capacité n’a pas besoin d’être affiché en permanence pendant le combat.

## 10. Répartition documentaire

| Document | Responsabilité principale |
|---|---|
| [`02-COMBAT.md`](./02-COMBAT.md) | Ordre de résolution, formules de dégâts et événements produits par la simulation |
| [`03-CREATURES.md`](./03-CREATURES.md) | Propriétés des formes et identité familiale des capacités |
| [`04-SKILLS.md`](./04-SKILLS.md) | Structure des capacités, effets produits et exceptions portées par les Skills |
| [`06-COMBAT_EFFECTS.md`](./06-COMBAT_EFFECTS.md) | Application, durée, snapshot, retrait et immunités propres aux Effets de combat |
| [`07-EVOLUTIONS.md`](./07-EVOLUTIONS.md) | Changements entre les formes et versions de capacités |
| [`18-UI_FLOW.md`](./18-UI_FLOW.md) | Consultation, tooltips et feedbacks fonctionnels |

## 11. Éléments à préciser ultérieurement

* Les ajustements éventuels du taux actuel de résistance pendant le balancing.
* Les pictogrammes, couleurs et conventions graphiques des éléments.
* La répartition concrète des éléments entre les futures formes et capacités.
* Les immunités élémentaires propres aux futurs Skills.
