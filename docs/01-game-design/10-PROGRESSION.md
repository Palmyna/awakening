# Project Awakening — Progression

**Statut :** Draft de conception — base initiale à compléter

## 1. Rôle et périmètre du document

Ce document rassemble les décisions validées concernant les niveaux, l’XP, les étoiles, les réinitialisations, le score de Puissance, l’énergie et la progression du compte.

Il ne fixe pas les courbes, coûts, multiplicateurs ou valeurs encore réservés au balancing.

## 2. Niveau et points de caractéristiques

Le niveau d’une instance ne possède pas de maximum.

Il reste affiché directement. Aucun système de prestige ne le remplace ou ne réinitialise automatiquement les niveaux élevés.

La quantité d’XP nécessaire augmente fortement avec les niveaux afin que chaque nouvelle montée devienne progressivement plus difficile. La courbe exacte reste à définir.

Une montée de niveau :

* n’augmente aucune caractéristique automatiquement ;
* accorde actuellement cinq points de caractéristiques ;
* permet de répartir ces points uniquement entre les six caractéristiques principales.

La valeur de cinq points constitue la référence actuelle mais reste ajustable pendant le balancing.

Les points non attribués peuvent être conservés indéfiniment. Ils n’augmentent pas le score de Puissance tant qu’ils ne sont pas attribués.

## 3. Attribution de l’XP d’une activité

L’XP est attribuée après le combat. Chaque créature participante reçoit son propre gain ; l’XP n’est jamais divisée entre les membres de l’équipe.

Toutes les participantes reçoivent leur gain, y compris si elles sont mortes, contrôlées ou temporairement exclues à la fin du combat.

Utiliser une équipe réduite n’augmente jamais le gain individuel d’une participante.

La ou les créatures du niveau le plus élevé parmi les participantes reçoivent 100 % de `XPActivité`.

Pour les autres :

> **RatioXP = RatioMinimum + (1 − RatioMinimum) × ((NiveauCréature − 1) / (NiveauMaxÉquipe − 1))**

Puis :

> **XPGagnée = XPActivité × RatioXP**

Avec :

* `RatioMinimum` : part minimale, actuellement fixée à 10 % mais ajustable pendant le balancing ;
* `NiveauCréature` : niveau de la participante concernée avant la récompense ;
* `NiveauMaxÉquipe` : niveau le plus élevé parmi les participantes avant la récompense ;
* `XPActivité` : valeur d’XP de l’activité ;
* `XPGagnée` : gain individuel calculé.

Lorsque toutes les participantes sont niveau 1, elles reçoivent 100 % de l’XP.

Les niveaux et ratios sont calculés avant l’attribution et restent fixes pour toute la récompense. Une récompense peut accorder plusieurs niveaux.

Tous les niveaux ainsi obtenus sont appliqués et accordent chacun les points de caractéristiques correspondants. Il n’existe aucune limite artificielle d’un niveau gagné par combat.

Ce ratio doit faciliter la remontée d’une créature récemment réinitialisée et permettre un power-leveling contrôlé, sans accorder immédiatement toute l’XP d’une activité avancée à une créature très peu développée.

## 4. Interaction avec les évolutions

Après l’attribution de l’XP, le nouveau niveau est établi puis les évolutions dont toutes les conditions sont remplies peuvent se déclencher.

Une même récompense peut provoquer plusieurs évolutions successives. Les règles détaillées appartiennent au [draft Évolutions](./07-EVOLUTIONS.md).

## 5. Niveau d’étoiles

Une nouvelle instance commence à 0 étoile et peut obtenir quinze montées :

* Bronze ★1 à ★5 : étoiles globales 1 à 5 ;
* Argent ★1 à ★5 : étoiles globales 6 à 10 ;
* Or ★1 à ★5 : étoiles globales 11 à 15.

Les étoiles augmentent uniquement les six caractéristiques principales de base de la forme et du stade actuels. Elles ne multiplient ni les caractéristiques secondaires, ni les points distribués, ni l’équipement, ni les buffs, ni les autres bonus externes.

Les multiplicateurs totaux doivent progresser de manière non linéaire. Les étoiles avancées doivent pouvoir produire un gain marginal supérieur, sans multiplication successive incontrôlée des paliers précédents.

## 6. Matériaux d’étoiles

Une montée d’étoile consomme des instances de la même famille, quelle que soit leur forme ou leur branche.

Certains paliers peuvent exiger que les instances utilisées comme matériaux possèdent elles-mêmes un niveau d’étoiles minimum. Les seules conditions d’une montée d’étoile portent sur les étoiles de ces instances.

Une montée d’étoile ne demande pas de niveau, de forme, de branche, d’équipement ou d’autre condition de progression à l’instance cible.

L’opération est irréversible. Une instance consommée disparaît définitivement et sa progression individuelle est perdue. Ses équipements retournent automatiquement dans l’inventaire.

Une instance ne peut pas perdre volontairement des étoiles ou revenir à un palier inférieur. Les instances consommées ne peuvent pas être récupérées.

## 7. Réinitialisations

### 7.1. Réinitialisation complète gratuite

La réinitialisation complète :

* remet l’instance au niveau 1 et à l’XP correspondante ;
* retire les points gagnés grâce aux niveaux ;
* impose de regagner ces points par la progression.

Elle conserve la forme actuelle, la branche, les étoiles, l’équipement, le surnom, les tags et les apparences déjà débloquées.

L’instance niveau 1 utilise donc les caractéristiques de base de sa forme évoluée actuelle.

Une évolution déjà obtenue n’est jamais perdue. Une évolution non encore obtenue devra toujours satisfaire ses conditions après la réinitialisation.

### 7.2. Redistribution sans retour au niveau 1

Un objet rare obtenu en jouant et un service payant limité fournissent le même résultat :

* le niveau et l’XP ne changent pas ;
* les points déjà gagnés redeviennent disponibles ;
* aucun point supplémentaire n’est accordé.

## 8. Score de Puissance

Chaque instance possède un score de Puissance recalculé en temps réel lorsque sa puissance active change.

Il reflète notamment la forme, le stade, les étoiles, les points attribués, l’équipement et les autres sources permanentes actives. Il sert au tri et à la comparaison générale sans mesurer absolument l’efficacité stratégique.

Les points de caractéristiques non attribués ne l’augmentent pas.

La formule exacte reste ouverte.

## 9. Progression du compte et énergie

Le compte possède un niveau numérique et gagne de l’expérience lorsqu’une activité est accomplie. Cette progression est plus lente que celle des créatures, représente l’avancement général du joueur, accorde une récompense par niveau et peut participer à certains déblocages secondaires.

Le mode Histoire utilise une énergie consommée à l’entrée d’un niveau. Hors ligne, seule cette énergie se régénère passivement ; les créatures et le compte ne gagnent aucune progression automatique.

## 10. Éléments à préciser ultérieurement

* La courbe exacte d’XP sans niveau maximal.
* La validation finale des cinq points par niveau.
* La validation finale du ratio minimum actuellement fixé à 10 %.
* Les règles d’arrondi de l’XP.
* Les quinze multiplicateurs d’étoiles.
* Les quantités et niveaux d’étoiles exigés pour les matériaux.
* La formule exacte du score de Puissance.
* La méthode d’obtention et le rythme de l’objet de réinitialisation.
* La limite et le prix du service payant de redistribution.
* Les récompenses et usages secondaires du niveau de compte.
* Les coûts, la régénération et l’accumulation exacte de l’énergie.
