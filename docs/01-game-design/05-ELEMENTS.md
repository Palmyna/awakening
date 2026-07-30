# Project Awakening — Éléments

**Statut :** Draft de conception — base initiale à compléter

## 1. Rôle et périmètre du document

Ce document rassemble les décisions validées concernant les éléments des créatures et des attaques.

Il complète les [règles de combat](./02-COMBAT.md). Il ne fixe pas encore les coefficients de réduction, l’équilibrage des profils élémentaires ni la répartition des éléments entre les créatures et les Skills.

## 2. Les neuf éléments officiels

1. Feu ;
2. Eau ;
3. Terre ;
4. Vent ;
5. Plante ;
6. Métal ;
7. Électricité ;
8. Lumineux ;
9. Ténèbres.

Le nom officiel du huitième élément est **Lumineux**.

## 3. Élément d’une créature

Chaque forme d’une créature possède un ou deux éléments au maximum :

* une créature mono-élément en possède un ;
* une créature bi-élément en possède deux.

Les deux éléments d’une créature bi-élément sont mécaniquement égaux et ne sont pas hiérarchisés comme principal et secondaire.

Toutes les combinaisons de deux éléments sont autorisées par défaut. Une évolution peut ajouter, perdre ou remplacer un élément lorsque l’évolution des pouvoirs, des capacités, des résistances ou du style de combat de la créature le justifie. Deux branches d’une même famille peuvent donc porter des éléments différents.

## 4. Élément d’une attaque

Chaque Basic Attack et chaque Skill possède son propre élément ou est explicitement sans élément. Une attaque ne possède pas deux éléments simultanément dans le système initial.

L’élément d’une attaque peut être différent de celui ou de ceux de la créature qui l’utilise.

Une attaque sans élément, également qualifiée de Neutre lorsque sa fiche l’indique ainsi, ne déclenche aucune interaction élémentaire.

## 5. Principe défensif

Le système élémentaire standard est défensif :

* il n’accorde aucun bonus offensif automatique ;
* un élément de la cible peut résister à l’élément de l’attaque ;
* une relation non déclarée est neutre ;
* le même élément contre lui-même est neutre ;
* les relations ne sont pas obligatoirement réciproques ;
* la table ne produit aucune immunité naturelle.

Un Skill peut créer explicitement une immunité élémentaire particulière.

## 6. Table des résistances

La table se lit ainsi : **élément de la cible → éléments d’attaque auxquels il résiste**.

| Élément de la cible | Résiste aux attaques |
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

Chaque élément défensif possède exactement trois résistances. Chaque élément d’attaque est résisté par exactement trois éléments.

## 7. Créature bi-élément

Pour une cible bi-élément :

* si un seul de ses éléments résiste à l’attaque, la réduction est appliquée une fois ;
* si ses deux éléments résistent à l’attaque, les deux réductions sont appliquées successivement et de manière multiplicative ;
* les réductions ne sont jamais additionnées directement.

Une créature bi-élément ne reçoit aucun avantage ou désavantage global automatique, et une créature mono-élément aucune compensation systématique.

## 8. Place dans la chaîne de dégâts

La résistance élémentaire est appliquée après la défense dans la chaîne standard des dégâts et avant les autres réductions, l’Absorption, les Boucliers et les PV.

Le True Damage ignore les défenses et plusieurs réductions générales, mais il reste soumis aux résistances élémentaires.

Les règles complètes de résolution appartiennent à [`02-COMBAT.md`](./02-COMBAT.md).

## 9. Éléments à préciser ultérieurement

* Le coefficient d’une résistance simple.
* Le résultat numérique exact de deux résistances successives.
* Les conventions d’affichage des interactions élémentaires dans l’interface.
* La répartition des éléments entre les créatures, les Basic Attacks et les Skills.
