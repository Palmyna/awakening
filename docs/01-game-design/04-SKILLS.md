# Project Awakening — Skills

**Statut :** Draft de conception — base initiale à compléter

## 1. Rôle et périmètre du document

Ce document rassemble les décisions validées concernant la Basic Attack et les trois catégories de Skills des créatures.

Il complète les [règles de combat](./02-COMBAT.md) sans les remplacer. Il ne constitue ni une liste de Skills, ni une spécification technique, ni un document d’équilibrage.

## 2. Structure d’action d’une créature

Chaque créature possède :

* une Basic Attack, distincte de ses Skills ;
* exactement quatre Skills prédéfinis.

Les quatre Skills comprennent exactement :

* une Ultimate ;
* trois autres Skills formant une combinaison fixe d’Active et de Passive.

Les répartitions possibles comprennent notamment :

* une Active, deux Passive et une Ultimate ;
* deux Active, une Passive et une Ultimate.

Le joueur ne choisit pas et ne remplace pas ces Skills.

La Basic Attack et les quatre Skills appartiennent à l’identité de la famille. Ils conservent cette identité à travers les évolutions.

Une nouvelle forme peut améliorer ou enrichir la version d’une même capacité, notamment par ses coefficients, valeurs, durées, probabilités, nombres de hits, ciblages cohérents, effets supplémentaires ou statuts. Des branches différentes peuvent faire évoluer cette capacité de manières différentes sans la remplacer par une capacité sans rapport.

## 3. Basic Attack

Chaque Basic Attack définit notamment :

* une catégorie Physique ou Spéciale, sauf formule particulière explicitement déclarée ;
* un élément ou l’absence explicite d’élément ;
* un intervalle contrôlé par l’Agilité ;
* une quantité d’énergie générée lorsqu’elle réussit ;
* un nombre de hits ;
* un ciblage ;
* les éventuels effets associés.

La première Basic Attack survient après l’écoulement de son intervalle complet.

Une Basic Attack esquivée ne produit ni dégâts, ni énergie, ni progression des compteurs d’Active, ni effets liés à un hit réussi.

### 3.1. Basic multi-hit ou multi-cible

Une Basic Attack multi-hit ou multi-cible est réussie si au moins un hit touche au moins une cible.

Elle accorde alors :

* son énergie une seule fois ;
* une progression des compteurs d’Active une seule fois.

Le nombre de hits ou de cibles touchés ne multiplie pas ces gains. Si tous les hits sont esquivés par toutes les cibles, elle n’accorde ni énergie ni progression d’Active.

## 4. Active

Une Active devient prête après un nombre défini de Basic Attacks réussies par la créature.

Une Active :

* n’est pas une Basic Attack ;
* remplace la Basic Attack de l’opportunité d’action où elle est utilisée ;
* ne fait pas progresser par défaut les compteurs d’Active ;
* peut déclarer explicitement une exception.

Si plusieurs Active sont prêtes :

1. leur ordre sur la fiche de la créature détermine leur priorité ;
2. une seule est utilisée pour une même opportunité d’action ;
3. les autres restent prêtes pour les opportunités suivantes.

## 5. Passive

Une Passive produit un effet permanent, conditionnel ou déclenché sans occuper une opportunité d’action comme une Active ou une Ultimate, sauf exception explicitement définie.

Une mécanique particulière, comme une auto-résurrection, doit être portée par une Passive ou un autre effet explicitement documenté. Il n’existe pas de résurrection générale d’un allié.

## 6. Ultimate

Chaque créature possède exactement une Ultimate.

Sa jauge d’énergie :

* commence à 0 ;
* est limitée à 100 ;
* revient à 0 après utilisation ;
* perd tout excédent au-delà de 100.

En Auto, une Ultimate prête est sélectionnée à la prochaine opportunité d’action valide. En Manuel, le joueur peut la conserver à 100 ou demander son déclenchement ; elle est alors utilisée à la prochaine opportunité valide.

Une Ultimate remplace la Basic Attack qui aurait normalement eu lieu.

## 7. Priorité à une opportunité d’action

Lorsqu’une créature atteint une opportunité d’action valide :

1. Ultimate prête et autorisée ;
2. sinon Active prête ;
3. sinon Basic Attack.

Une exception à cet ordre doit être déclarée explicitement par le Skill ou l’effet concerné.

## 8. Ciblage et géométrie

La priorité générale est :

1. règle explicite du Skill ;
2. effet de statut modifiant le ciblage ;
3. ciblage standard de la Basic Attack.

Les Skills peuvent définir :

* une cible unique ;
* une AoE globale ;
* une AoE de ligne ;
* une AoE de colonne ;
* un splash de proximité ;
* un nombre limité de cibles ;
* plusieurs hits.

Une Basic Attack AoE reste confinée à une seule ligne. Les diagonales ne font pas partie du voisinage standard et un emplacement vide rompt l’adjacence.

Chaque cible et chaque hit sont résolus indépendamment pour l’Esquive, le Crit, les défenses, les résistances élémentaires, les réductions, l’Absorption, les Boucliers et les effets liés au hit.

## 9. Dégâts, soins et éléments

Un Skill offensif déclare sa catégorie ou ses composantes :

* dégâts Physiques ;
* dégâts Spéciaux ;
* composantes Physique et Spéciale pour un hit hybride ;
* True Damage, lorsque cette exception est explicitement prévue.

Il déclare également sa caractéristique offensive ou sa formule particulière.

Chaque Basic Attack et chaque Skill possède son propre élément ou est explicitement sans élément. Cet élément peut être différent de celui ou de ceux de la créature.

Les règles de calcul appartiennent à [`02-COMBAT.md`](./02-COMBAT.md) et les interactions élémentaires à [`05-ELEMENTS.md`](./05-ELEMENTS.md).

### 9.1. Hit hybride

Un hit hybride reste un seul hit même lorsqu’il comporte plusieurs composantes de dégâts :

* un seul jet d’Esquive ;
* un seul jet de Critique ;
* un seul déclenchement des effets liés au hit.

Ses composantes sont calculées séparément selon leurs caractéristiques offensives, défenses, résistances et modificateurs applicables. La fiche du Skill doit déclarer explicitement chaque composante.

## 10. Esquive, Crit et application des statuts

Pour un hit standard, l’Esquive est résolue avant le Crit. Aucun jet de Crit n’est effectué si le hit est esquivé.

Un Skill peut être explicitement inesquivable. Un statut directement lié à un hit réussi s’applique sans second jet caché. Lorsqu’une probabilité d’application est explicitement définie, l’Esquive est résolue avant ce jet.

Les règles détaillées appartiennent à [`06-STATUS_EFFECTS.md`](./06-STATUS_EFFECTS.md).

## 11. Principe d’exception explicite

Une fiche de Skill peut déroger à une règle standard uniquement si l’exception est explicite, localisée et compréhensible. Une exception ne modifie pas le comportement général des autres Basic Attacks ou Skills.

## 12. Éléments à préciser ultérieurement

* Les coefficients, intervalles, gains d’énergie, compteurs et durées propres à chaque Basic Attack ou Skill.
* Les listes et fiches de Skills.
* Les règles d’interface de sélection manuelle des Ultimate.
* Les conventions détaillées de rédaction et de données des fiches de Skill.
