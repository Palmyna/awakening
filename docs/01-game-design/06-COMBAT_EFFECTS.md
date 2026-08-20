# Project Awakening — Combat Effects

**Statut :** Rédigé — référence actuelle, à maintenir à jour

## 1. Rôle et périmètre du document

Ce document définit les règles spécialisées des **Combat Effects**, ou **Effets de combat**, de **Project Awakening**.

Il constitue la référence actuelle pour les effets qui continuent d’exister après leur création ou leur application : effets persistants, périodiques, retardés, défensifs, de contrôle, utilitaires ou modificatifs.

Il complète les [règles de combat](./02-COMBAT.md), les [Skills](./04-SKILLS.md), les [éléments](./05-ELEMENTS.md) et les besoins fonctionnels d’[interface](./18-UI_FLOW.md) sans les remplacer.

Les règles communes de timeline, de résolution numérique, de dégâts, de soins et de priorité appartiennent au document Combat. La composition des capacités et l’ordre de leurs résultats appartiennent au document Skills. Le présent document définit le lifecycle commun des Effets de combat.

Il reste un document de game design. Il n’impose ni schéma technique, ni liste rigide de champs, ni catalogue définitif des effets concrets du jeu.

## 2. Résultat direct et Effet de combat

### 2.1. Résultat direct

Un **résultat direct** est entièrement résolu au moment où il se produit. Il peut modifier durablement l’état du combat, mais ne crée aucune entité possédant ensuite sa propre existence.

Exemples :

* infliger ou soigner immédiatement une valeur ;
* retirer ou voler immédiatement de l’énergie ;
* modifier immédiatement un compteur d’Active ;
* détruire immédiatement le Bouclier ;
* effectuer immédiatement un Cleanse ou un Dispel.

Retirer 20 énergie laisse la jauge dans un nouvel état, mais aucun effet temporaire ne reste attaché à la créature : il s’agit donc d’un résultat direct.

### 2.2. Effet de combat

Un **Effet de combat** continue d’exister après sa création ou son application et possède son propre lifecycle. Il peut notamment porter :

* une durée ou une condition de fin ;
* des stacks ;
* une règle de réapplication ;
* des ticks ou un déclenchement retardé ;
* une règle de retrait ;
* un snapshot ;
* une ou plusieurs conséquences persistantes.

Brûlure, Poison, HoT, Buff, Debuff, CC, Silence, Exclusion, Bouclier, Absorption, effet retardé, changement temporaire d’élément et blocage temporaire d’une mécanique sont des exemples d’Effets de combat.

Principe :

> Si tout est résolu immédiatement et que rien ne continue d’exister, il s’agit d’un résultat direct.

> Si quelque chose reste actif avec ses propres règles de vie, il s’agit d’un Effet de combat.

### 2.3. Unité de lifecycle

Un même Effet de combat peut produire plusieurs conséquences lorsqu’elles commencent, expirent, se cumulent, se réappliquent et sont retirées ensemble.

Exemple : un effet peut infliger un DoT et réduire les soins reçus. Si ces deux conséquences partagent intégralement le même lifecycle, elles appartiennent au même Effet de combat.

Si leurs durées, retraits ou règles de vie doivent différer, elles appartiennent à des Effets de combat distincts. Un Cleanse ou un Dispel retire toujours l’intégralité de l’Effet de combat concerné, jamais une seule de ses conséquences internes.

## 3. Catégories, principes et tags

### 3.1. Catégories fonctionnelles

La taxonomie fonctionnelle peut notamment distinguer :

* Offensif ;
* Défensif ;
* Soin ;
* Contrôle / CC ;
* Buff ;
* Debuff ;
* Utilitaire.

Cette taxonomie structure la conception et les données. Elle reste évolutive et ne détermine pas l’éligibilité au Cleanse ou au Dispel.

### 3.2. Principe mécanique et nom contextuel

Le système sépare :

> catégorie fonctionnelle → principe mécanique générique → nom ou tag contextuel.

Ainsi, Glacé et Stun peuvent partager le principe interne de CC total, tandis que Brûlure et Gelure peuvent partager un principe de DoT standard.

Le joueur voit le nom contextuel de l’effet, pas les appellations techniques internes telles que « CC total », « DoT standard » ou « DoT cumulatif ».

### 3.3. Tags et interactions

Le nom contextuel peut également servir de tag mécanique identifiable. Un Skill peut donc interagir avec une cible `Glacée`, `Brûlée` ou porteuse de tout autre tag précis, même lorsque plusieurs tags reposent sur le même principe interne.

Cette distinction s’applique à tous les Effets de combat, pas uniquement aux contrôles.

## 4. Durée, réapplication et identité

### 4.1. Formes de durée

Une durée peut être exprimée notamment en :

* secondes ;
* nombre de Basic Attacks ;
* nombre d’utilisations ;
* jusqu’à la prochaine Active ou Ultimate ;
* jusqu’à un événement ou une condition ;
* jusqu’à la fin du combat.

« Jusqu’à la fin du combat » est un type normal de durée. Il n’existe pas de catégorie séparée d’effet « permanent de combat ».

Tous les Effets de combat prennent fin au plus tard avec le combat en cours. Leur durée ne détermine pas leur éligibilité au Cleanse ou au Dispel.

### 4.2. Règle propre à chaque effet

Il n’existe pas de règle universelle de réapplication. Un effet peut explicitement prévoir :

* un refresh de durée ;
* un ajout de durée ;
* un remplacement ;
* une nouvelle stack ;
* une nouvelle instance ;
* un recalcul ;
* une autre règle locale.

### 4.3. Même applicateur et applicateurs différents

La même créature réappliquant exactement son même effet ne crée pas par défaut une deuxième instance indépendante. La réapplication suit la règle propre à cet effet.

Deux créatures différentes peuvent en revanche appliquer simultanément le même effet contextuel à une même cible. Leurs instances restent indépendantes lorsque leurs lifecycles le sont.

Le moteur conserve l’identité minimale nécessaire pour distinguer la réapplication du même applicateur d’une application provenant d’un autre applicateur. Cette identité ne crée pas une mécanique générale de « source d’effet » librement exploitable par les Skills.

## 5. Snapshot, élément et application

### 5.1. Snapshot complet de l’applicateur

À l’application, toutes les informations nécessaires dépendant de l’applicateur sont calculées et snapshotées, selon les besoins : puissance, caractéristiques offensives, élément, Crit, cadence et paramètres propres à l’effet.

Une modification ultérieure de l’applicateur ne modifie pas rétroactivement un effet déjà appliqué. Toute réapplication recalcule entièrement le snapshot à partir de l’état actuel, même lorsqu’elle ne fait que refresh la durée ou ajouter une stack.

La mort de l’applicateur ne supprime pas les Effets de combat déjà créés et n’empêche pas leur fonctionnement.

### 5.2. État dynamique de la cible

Lorsqu’un Effet de combat produit ultérieurement un résultat, les protections et états défensifs pertinents de la cible sont évalués à cet instant : Défense, Défense spéciale, résistances, réductions, Absorption, Bouclier, réduction des soins ou autre état applicable.

Principe :

> applicateur snapshoté à l’application ; cible évaluée au moment de la résolution du résultat.

### 5.3. Élément

Un Effet de combat produit par une capacité hérite normalement de l’élément actuel de cette capacité au moment de son application. Cet élément est snapshoté.

Les résistances élémentaires réduisent uniquement les dégâts concernés. Elles ne réduisent ni la probabilité d’application, ni la durée, ni les soins ou autres résultats non dommageables.

Une immunité élémentaire peut empêcher l’application d’un effet positif ou négatif de l’élément concerné. Chaque Effet de combat produit par un même Skill vérifie indépendamment son application lorsque nécessaire.

Le Bouclier suit une règle élémentaire particulière décrite en section 11.

### 5.4. Esquive et probabilité

Un Effet de combat offensif visant une cible est esquivable par défaut, même s’il ne produit aucun dégât immédiat, sauf s’il est explicitement inesquivable.

Lorsqu’il dépend d’un hit, l’Esquive de ce hit suffit : si le hit échoue, l’effet lié n’est pas appliqué ; s’il réussit, aucun second jet d’Esquive caché n’est effectué. Une fois l’effet correctement appliqué, ses ticks et conséquences internes ne sont pas esquivés une seconde fois.

Une probabilité supplémentaire d’application n’existe que si le Skill ou l’effet la définit explicitement.

## 6. Effets périodiques

### 6.1. Moteur commun

Les DoT et HoT utilisent un moteur périodique commun. Chaque application définit notamment :

* une valeur totale de référence ;
* un nombre fixe de ticks ;
* un intervalle de référence ;
* les règles de Crit ;
* les règles de réapplication ;
* les éventuelles stacks.

Le nombre de ticks et la valeur totale non critique sont fixes pour l’application. Chaque tick reçoit une part de cette valeur totale et peut effectuer indépendamment son propre jet de Crit lorsque la mécanique est compatible. Les Critiques peuvent donc porter la valeur réellement obtenue au-delà de la valeur totale non critique de référence.

### 6.2. Agilité et cadence

La configuration de référence d’un effet périodique est exprimée pour une Agilité de référence égale à `1`.

L’Agilité de l’applicateur au moment de l’application accélère la cadence selon une courbe à rendement décroissant comparable conceptuellement à celle de la Basic Attack, avec ses propres paramètres d’équilibrage et son propre intervalle minimum.

L’Agilité ne change ni le nombre de ticks, ni la puissance totale non critique. Elle rapproche les ticks et réduit ainsi la durée effective :

> **DuréeEffective = NombreDeTicks × IntervalleEffectif**

La cadence calculée est snapshotée. Une modification ultérieure de l’Agilité n’affecte pas l’effet déjà présent.

### 6.3. Timing et refresh

Le premier tick survient après un intervalle complet. Aucun tick immédiat n’existe par défaut. Le dernier tick prévu est résolu, puis l’effet expire.

Lorsqu’un effet périodique est refresh :

* son snapshot est entièrement recalculé ;
* sa durée repart de zéro ;
* toute progression partielle vers le prochain tick est perdue ;
* le prochain tick arrive après un nouvel intervalle complet.

Cette règle s’applique également lorsqu’une nouvelle stack refresh un effet cumulatif.

### 6.4. DoT

Un DoT standard non stackable peut définir une puissance totale, un nombre fixe de ticks et une cadence déterminée à l’application. Sa réapplication par le même applicateur effectue un nouveau snapshot et un refresh ; un autre applicateur peut conserver sa propre instance indépendante.

Un DoT cumulatif ou progressif peut utiliser un maximum de stacks propre à l’effet, un timer commun et un nouveau snapshot à chaque réapplication. Les stacks n’ont pas de timers individuels. Leur progression de puissance peut être linéaire, progressive ou suivre toute autre formule explicitement définie.

Brûlure, Gelure, Poison ou Saignement peuvent employer ces principes sans que leur nom impose à lui seul une formule particulière. Aucune formule définitive de ces effets n’est arrêtée par le présent document.

### 6.5. HoT

Les HoT peuvent employer les mêmes principes standard, cumulatifs ou progressifs. Ils définissent leur valeur totale de soin, leur nombre fixe de ticks, leur cadence snapshotée, leur durée résultante et leurs règles de réapplication.

Par défaut, tout soin excédant les PV maximum est perdu. Un effet peut explicitement exploiter cet overheal comme exception locale.

## 7. Mort, auto-résurrection et Exclusion

### 7.1. Mort et état non vivant

La mort n’agit pas comme un Cleanse. Les Effets de combat restent attachés à une créature morte ou temporairement non vivante dans le cadre d’une auto-résurrection, et leurs timers continuent normalement.

Un effet nécessitant une cible vivante ne produit pas son résultat normal pendant cet état. Pour un effet périodique, une opportunité de tick survenant pendant l’état non vivant est consommée sans produire le résultat exigeant une cible vivante.

Si l’effet expire avant le retour de la créature, il disparaît. Si la créature revient avant l’expiration, l’effet reprend avec son état restant.

### 7.2. Exclusion

Pendant une Exclusion, la créature est retirée temporairement du combat : elle ne peut ni agir, ni être ciblée, ni être incluse dans une AoE, mais conserve sa position logique.

Ses timers personnels et tous ses Effets de combat sont gelés. À son retour, elle reprend la même position et ses effets continuent avec leurs durées et états restants.

## 8. Contrôles

### 8.1. CC total

Le principe interne de **CC total** empêche complètement une créature d’agir pendant sa durée. Stun, Glacé, Peur, Choc, Sommeil, Pétrification ou d’autres futurs tags contextuels peuvent employer ce principe tout en restant distincts pour les interactions de Skills.

Plusieurs instances de CC total provenant de créatures différentes peuvent coexister. Leurs durées ne sont pas additionnées : chaque instance expire indépendamment, et la cible reste sous CC total tant qu’au moins une instance est active.

### 8.2. Rupture éventuelle par les dégâts

Une instance de CC total peut définir une faible chance d’être rompue lorsqu’une instance de dégâts atteint réellement les PV de la cible. Chaque hit direct, hit d’un multi-hit, tick de DoT ou dégât retardé pertinent effectue alors son propre jet, quelle que soit sa source.

Un dégât entièrement absorbé par le Bouclier ne provoque aucun jet de rupture. Si une partie atteint les PV, le jet prévu a lieu. La chance exacte reste un paramètre de balancing.

### 8.3. Diminishing returns

Les contrôles utilisent des diminishing returns (DR) réduisant leur durée, jamais leur probabilité d’application.

Chaque créature possède trois historiques de DR distincts :

1. CC total ;
2. Silence ;
3. Exclusion.

Les tags partageant le principe de CC total alimentent le même historique. Silence et Exclusion n’affectent pas cet historique ni celui l’un de l’autre.

Les paliers, multiplicateurs, durées d’historique, règles de récupération et éventuels minimums de durée restent à équilibrer.

### 8.4. Silence

Silence est distinct du CC total. Pendant Silence :

* la Basic Attack reste disponible ;
* une Basic Attack réussie continue à générer son énergie et à progresser les compteurs d’Active ;
* les Active et l’Ultimate ne peuvent pas être utilisées ;
* une Active ou Ultimate déjà prête le reste.

À la fin du Silence, les priorités normales reprennent. Silence utilise son propre historique de DR.

### 8.5. Exclusion

Exclusion est un contrôle distinct employant les règles de présence et de gel de la section 7. Elle utilise son propre historique de DR.

### 8.6. Immunités et modifications de durée

Une immunité explicitement accordée peut viser un principe, une famille, un contrôle ou un tag contextuel précis. Elle bloque les nouvelles applications de son périmètre, mais ne retire pas rétroactivement un effet déjà appliqué.

Un Skill qui doit aussi retirer les effets existants doit l’indiquer explicitement.

Un Skill ou une Passive peut modifier explicitement la durée de certains contrôles infligés ou reçus. L’Agilité ne réduit jamais naturellement leur durée et aucune caractéristique secondaire universelle de résistance aux statuts ou aux CC n’est créée.

L’ordre conceptuel est :

> durée de base → modifications explicites de durée infligée ou reçue → diminishing returns → durée finale appliquée.

La durée finale est fixée à l’application. Un modificateur apparaissant ou disparaissant ensuite ne la change pas rétroactivement.

### 8.7. Root, Taunt et ciblage forcé

Il n’existe pas de mécanique générale de Root, les créatures ne se déplaçant normalement pas.

Il n’existe pas de mécanique générale de Taunt / Provocation ni, plus largement, de mécanique ennemie destinée à modifier ou forcer le ciblage des actions adverses. Un Skill peut uniquement définir sa propre règle de ciblage pour ses propres actions.

## 9. Buffs, Debuffs et modifications persistantes

Les Buffs et Debuffs sont des Effets de combat pouvant modifier des caractéristiques, multiplicateurs, règles de combat, gains d’énergie, soins, dégâts, durées de contrôle ou autres comportements explicitement définis.

Les modifications de caractéristiques sont appliquées chronologiquement selon les règles du document Combat. Lorsqu’un modificateur expire ou est retiré, la valeur est recalculée en conservant les autres modificateurs dans leur ordre d’application.

Une modification « jusqu’à la fin du combat » reste un Effet de combat utilisant ce type de durée. Elle n’est pas automatiquement non-dispellable et sa possibilité de retrait dépend uniquement de ses propriétés explicites.

## 10. Cleanse et Dispel

### 10.1. Éligibilité explicite

La polarité positive, négative ou neutre ne détermine pas le retrait. Chaque Effet de combat possède explicitement l’une des configurations suivantes :

* éligible à Cleanse ;
* éligible à Dispel ;
* éligible aux deux ;
* éligible à aucun.

L’absence d’éligibilité signifie que l’effet ne peut pas être retiré par Cleanse ou Dispel.

### 10.2. Résolution et sélection

Cleanse retire un Effet de combat éligible à Cleanse. Dispel retire un Effet de combat éligible à Dispel.

Un Skill peut préciser la quantité retirée, tous les effets éligibles, une catégorie ou une autre sélection particulière. S’il existe plusieurs effets éligibles et que le Skill ne précise pas lequel retirer, le choix est aléatoire et utilise la RNG déterministe du combat.

### 10.3. Retrait complet

Le retrait supprime l’intégralité du package : toutes ses conséquences, ses stacks, son timer et son état. Cleanse et Dispel ne retirent jamais une conséquence interne isolée.

## 11. Bouclier et Absorption

### 11.1. Réserve commune de Bouclier

Le Bouclier est un Effet de combat défensif particulier. Chaque créature possède conceptuellement une seule réserve commune de Bouclier, comparable à une seconde barre de vie temporaire. Elle absorbe les dégâts avant les PV, après les autres étapes prévues par la chaîne de dégâts.

Chaque nouvelle application :

1. calcule la valeur accordée selon le Skill ;
2. l’ajoute à la réserve restante ;
3. refresh la durée de la réserve avec la durée de la nouvelle application.

Il n’existe ni sous-Boucliers séparés, ni ordre de consommation entre anciennes applications. Lorsque la durée expire, toute la réserve restante disparaît. L’Agilité n’influence pas cette durée.

Il n’existe aucune limite universelle de quantité de Bouclier. Une limite éventuelle doit être définie localement par un Skill ou une mécanique.

### 11.2. Élément du Bouclier

L’application accordant du Bouclier possède l’élément du Skill. Une immunité élémentaire peut donc empêcher cette application.

Une fois la valeur ajoutée, la réserve commune n’a plus d’élément propre. Des applications Feu et Eau peuvent ainsi former une seule réserve sans conserver l’origine élémentaire de ses portions.

### 11.3. Suppression spécifique

Le Bouclier n’est pas retiré par Cleanse ou Dispel. Une mécanique spécifique de suppression permet à un Skill anti-Bouclier de produire comme résultat direct :

> Détruit le Bouclier de la cible.

Toute la réserve actuelle passe alors immédiatement à `0`, quelle que soit sa valeur ou l’origine de ses applications. Le nom final de cette mécanique n’est pas encore fixé.

### 11.4. Absorption

L’Absorption est distincte du Bouclier. Elle réduit un pourcentage des dégâts entrants avant la réserve de Bouclier, n’est pas une réserve de points et possède son propre lifecycle.

Elle peut définir ses propres règles de réapplication ou de coexistence avec d’autres Absorptions.

Chaîne concernée :

> réductions applicables → Absorption → Bouclier → PV.

Bouclier et Absorption ne Critiquent pas.

## 12. Effets retardés et manipulations utilitaires

### 12.1. Effet retardé

Un effet qui existe pendant un délai avant de produire son résultat est un Effet de combat. Il peut posséder une icône, un snapshot, une éligibilité au retrait, une condition et un résultat déclenché à expiration.

L’applicateur est snapshoté à l’application ; l’état défensif de la cible est évalué au déclenchement. Une fois l’effet appliqué, aucune nouvelle Esquive n’est effectuée à son déclenchement, sauf exception explicite.

### 12.2. Frontière utilitaire

La distinction résultat direct / Effet de combat s’applique à toutes les mécaniques :

* « Retire immédiatement 20 énergie » est un résultat direct ;
* « Pendant 8 secondes, les Basics génèrent 50 % d’énergie en moins » est un Effet de combat ;
* « Ajoute immédiatement 2 progressions au compteur » est un résultat direct ;
* « Pendant 10 secondes, chaque Basic compte double » est un Effet de combat ;
* « Détruit immédiatement le Bouclier » est un résultat direct ;
* « Ne peut pas recevoir de Bouclier pendant 8 secondes » est un Effet de combat.

### 12.3. Changement temporaire d’élément

Un changement d’élément qui continue d’exister après son application est un Effet de combat, qu’il dure quelques secondes ou jusqu’à la prochaine utilisation de la capacité concernée.

Dans le modèle actuel, ces effets de changement temporaire d’élément ne sont éligibles ni à Cleanse, ni à Dispel.

## 13. Simultanéité, données et extensibilité

### 13.1. Priorité déterministe

Lorsqu’un tick, une expiration, un Cleanse, un Dispel ou un autre événement partage exactement le timestamp d’un autre événement, la priorité déterministe générale du moteur s’applique. Le premier événement est résolu, puis l’état du combat est réévalué.

Les choix aléatoires et résultats RNG nécessaires sont conservés afin qu’un replay reproduise exactement le combat original.

### 13.2. Description data-driven

Les Effets de combat doivent rester data-driven et extensibles sans être transformés en formulaires rigides. Leur texte mécanique définit précisément leur comportement.

Selon ses besoins, un effet peut notamment porter un nom contextuel, un tag, un principe interne, une catégorie, un élément, une durée, des stacks, une réapplication, des éligibilités de retrait, un snapshot, des paramètres, des conditions et des conséquences. Toutes ces propriétés ne sont pas obligatoires pour chaque effet.

Un principe générique n’est pas dupliqué pour chaque Skill. Le Skill fournit les paramètres nécessaires à son application ; il ne crée pas artificiellement plusieurs variantes de Brûlure uniquement parce que les valeurs diffèrent.

### 13.3. Exceptions locales

Le système suit le principe :

> règle générale simple, exception locale explicitement définie.

Un comportement atypique reste local tant qu’il n’est pas partagé par plusieurs effets. Un nouveau principe générique n’est ajouté que lorsqu’un besoin réutilisable réel apparaît.

### 13.4. Principes actuellement identifiés

La base de conception comprend actuellement :

* CC total ;
* Silence ;
* Exclusion ;
* DoT standard ;
* DoT cumulatif ou progressif ;
* HoT standard ;
* HoT cumulatif ou progressif ;
* Buff ;
* Debuff ;
* Bouclier ;
* Absorption ;
* effet retardé ;
* modification temporaire d’une règle ;
* changement temporaire d’élément ;
* blocage temporaire d’une mécanique.

Cette liste répond aux besoins actuels sans fermer l’ajout ultérieur de nouveaux principes.

## 14. Présentation et information joueur

Les besoins fonctionnels détaillés appartiennent au [document UI Flow](./18-UI_FLOW.md).

En combat, les effets importants utilisent des icônes. Un effet à stacks emploie une seule icône avec compteur ; deux instances indépendantes du même effet utilisent deux icônes distinctes. Un timer radial peut représenter la durée sans afficher constamment un nombre.

Une application réussie normale ou un gain de stack n’ajoute aucun texte : l’icône suffit. Une Esquive, une Immunité ou un échec probabiliste explicitement tenté utilise un feedback court.

Hors combat, la fiche affiche autant que possible les valeurs concrètes calculées pour l’instance. Une formule relative reste visible lorsqu’une valeur dépend d’une cible future et ne peut pas être calculée honnêtement.

Après le combat, un résumé agrégé par créature doit permettre d’examiner les deux équipes. La liste finale des statistiques reste à définir et ne nécessite pas un rapport Skill par Skill.

## 15. Éléments à préciser ultérieurement

* Les coefficients exacts des DoT et HoT.
* La courbe exacte d’accélération des ticks par l’Agilité et leur intervalle minimum.
* Les caps éventuels propres à certains effets.
* Le maximum de stacks et leur progression pour chaque effet concret.
* La chance exacte de rupture d’un CC lorsque des dégâts atteignent les PV.
* Les paliers, multiplicateurs, durées d’historique, récupérations et éventuels minimums des diminishing returns.
* Les valeurs de modification des durées de contrôle.
* Les valeurs des Buffs et Debuffs.
* Les règles propres aux futurs effets atypiques.
* La liste définitive des noms contextuels et des principes génériques.
* La liste définitive des statistiques post-combat.
* Le wording et le design visuel exacts des icônes, timers et feedbacks.
* Le nom final de la mécanique spécifique de suppression du Bouclier.
* Les paramètres, valeurs, probabilités et exceptions propres aux futurs Skills et Effets de combat concrets.
