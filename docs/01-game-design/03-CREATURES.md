# Project Awakening — Créatures

**Statut :** Rédigé — référence actuelle, à maintenir à jour

## 1. Rôle et périmètre du document

Ce document définit la structure fonctionnelle des créatures jouables de **Project Awakening**.

Il constitue la référence actuelle concernant notamment :

* la distinction entre famille, forme et instance possédée ;
* les données appartenant à chacun de ces niveaux ;
* les caractéristiques des créatures ;
* leur progression en niveau ;
* leurs évolutions et branches d’évolution ;
* leur niveau d’étoiles ;
* leur équipement ;
* leur score de Puissance ;
* leur organisation par le joueur ;
* leur utilisation dans une équipe ;
* leur découverte dans l’encyclopédie ;
* la capacité de créatures possédées.

Il complète la [Vision](../00-foundation/01-VISION.md), le [GDD central](./01-GAME_DESIGN_DOCUMENT.md) et les [règles de combat](./02-COMBAT.md).

Il ne définit pas :

* les formules détaillées du moteur de combat ;
* les valeurs définitives de balancing ;
* les listes individuelles de Skills ;
* les tables élémentaires ;
* les règles détaillées des effets de statut ;
* les coûts exacts d’évolution ;
* les coûts exacts des montées d’étoiles ;
* les règles détaillées des objets et équipements ;
* la formule définitive du score de Puissance ;
* l’interface finale de gestion des créatures ;
* la grammaire exacte du système de recherche.

Ces sujets sont approfondis dans leurs documents spécialisés.

---

## 2. Définitions structurelles

### 2.1. Famille

Une **famille de créatures** représente l’identité persistante d’une lignée de créatures.

Lorsqu’un joueur obtient la forme de base d’une créature, il obtient une **instance possédée de cette famille**.

La famille définit notamment :

* son identité générale ;
* sa rareté ;
* son numéro d’encyclopédie ;
* son texte de lore général ;
* l’ensemble de ses formes et branches d’évolution ;
* l’identité de sa Basic Attack ;
* l’identité de ses quatre Skills prédéfinis.

Une famille peut contenir plus de trois formes différentes lorsqu’elle possède plusieurs branches d’évolution.

---

### 2.2. Forme

Une **forme** correspond à une étape ou variante précise de l’évolution d’une famille.

Une forme définit notamment :

* son nom ;
* son apparence de référence ;
* son texte de lore propre ;
* son ou ses éléments ;
* son profil de caractéristiques de base ;
* son ou ses rôles suggérés ;
* son profil offensif suggéré ;
* la version de la Basic Attack utilisée à cette forme ;
* les versions des Skills utilisées à cette forme.

Une forme peut donc modifier significativement l’orientation fonctionnelle d’une créature.

Une branche d’évolution peut par exemple faire évoluer une créature naturellement offensive vers une forme orientée Tank.

---

### 2.3. Instance possédée

Une **instance possédée** est l’exemplaire individuel d’une famille appartenant au joueur.

Elle persiste à travers les évolutions.

Une évolution ne crée jamais une nouvelle instance et ne remplace pas la créature possédée.

L’instance conserve notamment :

* son niveau ;
* son expérience ;
* ses points de caractéristiques ;
* son niveau d’étoiles ;
* son équipement ;
* son surnom ;
* ses tags personnalisés ;
* son état verrouillé ou déverrouillé ;
* son chemin d’évolution ;
* les apparences de formes qu’elle a personnellement débloquées.

Plusieurs instances d’une même famille peuvent être possédées simultanément et développées différemment.

---

### 2.4. Stade d’évolution

Chaque instance traverse toujours exactement **trois stades d’évolution** :

1. stade 1 — forme de base ;
2. stade 2 — forme intermédiaire ;
3. stade 3 — forme finale.

Cette règle est commune à toutes les créatures afin de conserver une structure de progression et d’équilibrage cohérente.

Une famille peut néanmoins contenir beaucoup plus de trois formes différentes grâce aux branches.

Une instance individuelle n’en parcourt toujours que trois.

---

### 2.5. Branche d’évolution

Une **branche d’évolution** représente un chemin distinct au sein de l’arbre d’une famille.

La divergence peut intervenir :

* lors du passage au stade 2 ;
* lors du passage au stade 3 ;
* ou à plusieurs endroits successifs de l’arbre.

Le nombre de branches possibles pour une famille n’est pas limité structurellement.

Une fois qu’une instance emprunte une branche, ce choix est définitif.

---

## 3. Identité fonctionnelle

Chaque créature possède notamment :

* une famille ;
* une forme mécanique actuelle ;
* une rareté de famille ;
* un ou deux éléments au maximum ;
* une Basic Attack ;
* exactement quatre Skills prédéfinis ;
* six caractéristiques principales ;
* trois caractéristiques secondaires système ;
* un niveau ;
* de l’expérience ;
* des points de caractéristiques ;
* un niveau d’étoiles ;
* un ensemble d’équipement ;
* un score de Puissance ;
* un ou deux rôles suggérés ;
* un profil offensif suggéré ;
* éventuellement un surnom personnalisé ;
* éventuellement des tags personnalisés.

Le joueur personnalise principalement ses créatures par :

* la répartition de leurs points de caractéristiques ;
* leur équipement ;
* leur progression en niveau ;
* leur niveau d’étoiles ;
* leur évolution ;
* le choix de leur branche ;
* leur utilisation dans différentes compositions.

Il n’existe pas de système d’IV ou de variation aléatoire cachée des caractéristiques intrinsèques.

Deux instances d’une même forme possèdent les mêmes valeurs de base avant les choix de progression du joueur.

---

## 4. Rareté, numéro et lore

### 4.1. Rareté

La rareté appartient à la **famille**.

Les quatre raretés retenues sont :

1. Rare ;
2. Épique ;
3. Légendaire ;
4. Mythique.

Toutes les formes et toutes les branches d’une même famille conservent la même rareté.

La rareté représente principalement :

* la difficulté d’obtention ;
* la valeur de collection ;
* le prestige de la famille.

Elle ne constitue pas une hiérarchie automatique de puissance.

Une créature Mythique n’est pas automatiquement plus forte qu’une créature Rare.

Une rareté supérieure peut néanmoins rendre indirectement la progression en étoiles plus difficile lorsque les doublons nécessaires sont plus rares à obtenir.

Les probabilités d’obtention appartiennent au document consacré au Gacha.

---

### 4.2. Numéro d’encyclopédie

Chaque famille possède un **numéro unique et permanent**.

L’affichage utilise directement le nombre sans zéros superflus :

> #1
> #42
> #133

Le numéro appartient à la famille et non à chacune de ses formes.

Toutes les formes d’une même famille partagent donc le même numéro.

Un numéro déjà attribué n’est jamais modifié ou réorganisé à la suite de l’ajout ultérieur de nouvelles familles.

---

### 4.3. Lore

Chaque famille possède :

* un court texte de lore général ;
* un court texte de lore propre à chacune de ses formes.

Les informations narratives plus développées appartiennent aux documents consacrés au lore des créatures.

---

## 5. Caractéristiques

### 5.1. Caractéristiques principales

Les six caractéristiques principales sont :

1. PV ;
2. Attaque ;
3. Attaque spéciale ;
4. Défense ;
5. Défense spéciale ;
6. Agilité.

Seules ces six caractéristiques peuvent recevoir directement les points gagnés lors des montées de niveau.

L’Agilité contrôle l’intervalle des Basic Attacks selon les règles du document Combat.

Elle n’augmente pas le Crit.

---

### 5.2. Caractéristiques secondaires

Les trois caractéristiques secondaires système sont :

1. Crit ;
2. Dégâts critiques ;
3. Esquive.

Elles ne peuvent pas recevoir directement les points de caractéristiques gagnés lors des montées de niveau.

Elles peuvent notamment provenir :

* des valeurs de base de la forme ;
* de l’évolution ;
* de l’équipement ;
* des Skills ;
* des Passive ;
* des buffs ;
* des debuffs ;
* d’autres systèmes explicitement documentés.

Les formules, rendements décroissants et caps éventuels sont définis dans le document Combat.

---

### 5.3. Valeurs de base propres aux formes

Chaque forme possède son propre **profil de caractéristiques de base**.

Une évolution peut modifier la répartition de ces caractéristiques.

Une branche orientée Dégâts et une branche orientée Tank appartenant à la même famille peuvent donc utiliser des répartitions de base différentes.

Lors d’une évolution, les anciennes valeurs de base sont remplacées par celles de la nouvelle forme.

Les points ajoutés par le joueur, l’équipement et les autres bonus ne servent jamais de nouvelles valeurs de base.

---

### 5.4. Multiplicateur de stade d’évolution

Le stade d’évolution applique un multiplicateur aux valeurs de base de la forme :

* stade 1 : ×1 ;
* stade 2 : ×2 ;
* stade 3 : ×3.

Ce multiplicateur concerne :

* les six caractéristiques principales ;
* les trois caractéristiques secondaires.

Le multiplicateur est toujours déterminé par le stade.

Une branche ne peut pas bénéficier d’un multiplicateur de stade différent d’une autre branche de même stade.

---

### 5.5. Ordre conceptuel de construction des caractéristiques

Pour les caractéristiques principales, l’ordre conceptuel est :

> valeurs de base propres à la forme
> → multiplicateur du stade d’évolution
> → multiplicateur d’étoiles
> → points distribués par le joueur
> → équipement
> → autres bonus permanents
> → modifications de combat

Pour les caractéristiques secondaires :

> valeurs de base propres à la forme
> → multiplicateur du stade d’évolution
> → équipement et autres sources
> → modifications de combat

Le multiplicateur d’étoiles ne s’applique pas aux caractéristiques secondaires.

Les points attribués par le joueur ne sont jamais multipliés rétroactivement par l’évolution ou les étoiles.

---

## 6. Niveau, expérience et points de caractéristiques

### 6.1. Niveau sans limite maximale

Il n’existe pas de niveau maximum pour les créatures.

Une instance peut théoriquement continuer à gagner des niveaux indéfiniment.

La quantité d’expérience nécessaire augmente fortement avec les niveaux afin que chaque nouvelle montée devienne progressivement plus difficile.

La formule exacte de cette courbe appartient au document Progression.

Il n’existe pas de système de prestige remplaçant ou réinitialisant automatiquement les niveaux élevés.

Le niveau réel reste affiché directement.

---

### 6.2. Montée de niveau

Une montée de niveau n’augmente jamais automatiquement les caractéristiques de la créature.

Chaque niveau gagné accorde actuellement :

> **5 points de caractéristiques**

à répartir parmi les six caractéristiques principales.

Cette valeur constitue la référence de conception actuelle et reste ajustable pendant le balancing.

Le joueur peut :

* attribuer immédiatement ses points ;
* en conserver autant qu’il souhaite sans les dépenser ;
* les distribuer plus tard.

Les points non attribués ne produisent aucun effet et n’augmentent pas le score de Puissance.

---

### 6.3. XP obtenue dans une activité

L’expérience est attribuée **après le combat**, jamais pendant celui-ci.

Toutes les créatures ayant participé au combat sont éligibles à l’XP, qu’elles aient :

* survécu ;
* été tuées ;
* été contrôlées ;
* été temporairement exclues ;
* ou peu agi pendant le combat.

L’activité définit une quantité de base :

> `XPActivité`

Cette quantité est calculée individuellement pour chaque créature participante.

Elle n’est jamais divisée par le nombre de membres de l’équipe.

Jouer avec une seule créature ne permet donc pas d’obtenir plusieurs fois l’XP prévue pour celle-ci.

---

### 6.4. Ajustement de l’XP selon les niveaux de l’équipe

La ou les créatures possédant le niveau le plus élevé parmi les participantes reçoivent **100 % de l’XP de l’activité**.

Les créatures de niveau inférieur reçoivent un pourcentage déterminé par interpolation linéaire entre :

* un ratio minimum pour une créature niveau 1 ;
* 100 % pour le niveau le plus élevé de l’équipe.

Le ratio minimum actuellement envisagé est :

> **10 %**

Cette valeur reste un paramètre de balancing.

Pour `NiveauMaxÉquipe > 1` :

> **RatioXP = RatioMinimum + (1 − RatioMinimum) × ((NiveauCréature − 1) / (NiveauMaxÉquipe − 1))**

Puis :

> **XPGagnée = XPActivité × RatioXP**

Avec :

* `RatioMinimum` : actuellement 0,10 ;
* `NiveauCréature` : niveau de la créature avant attribution de l’XP ;
* `NiveauMaxÉquipe` : niveau le plus élevé parmi les créatures participantes avant attribution de l’XP.

Lorsque toutes les créatures participantes sont niveau 1, elles reçoivent toutes 100 % de l’XP de l’activité.

Le niveau de référence et le ratio sont calculés **avant l’attribution de l’XP**.

Le ratio reste ensuite fixe pour toute la récompense, même si la créature gagne plusieurs niveaux grâce à cette XP.

Ce système permet notamment :

* d’aider une créature récemment reset à regagner ses premiers niveaux ;
* de permettre du power-leveling contrôlé ;
* d’éviter qu’une créature très faible accompagnée d’une équipe extrêmement développée récupère immédiatement la totalité de l’XP d’une activité très avancée.

---

### 6.5. Plusieurs niveaux obtenus simultanément

Une même récompense d’XP peut faire gagner plusieurs niveaux.

Tous les niveaux gagnés sont appliqués.

La créature reçoit les points de caractéristiques correspondant à chaque niveau obtenu.

Avec la valeur actuelle de 5 points par niveau, gagner trois niveaux donne donc 15 points de caractéristiques.

Il n’existe pas de limite artificielle d’un niveau gagné par combat.

---

## 7. Basic Attack, Skills et profil fonctionnel

### 7.1. Ensemble fixe

Chaque famille possède :

* une Basic Attack ;
* exactement quatre Skills prédéfinis.

Les quatre Skills comprennent :

* exactement une Ultimate ;
* trois autres Skills formant une combinaison fixe d’Active et de Passive.

Le joueur :

* ne choisit pas ces Skills dans une liste ;
* ne les remplace pas ;
* ne construit pas le kit de la créature.

Ils définissent l’identité fonctionnelle de la famille.

---

### 7.2. Évolution des Skills avec les formes

Une évolution ne remplace pas la Basic Attack ou les Skills par des capacités sans rapport.

Les mêmes identités de capacités sont conservées à travers la famille.

Une nouvelle forme peut néanmoins **améliorer ou enrichir** leur fonctionnement.

Une évolution peut notamment modifier :

* les coefficients ;
* les valeurs ;
* les durées ;
* les probabilités ;
* le nombre de hits ;
* certains paramètres de ciblage ;
* des effets existants ;
* ajouter un nouvel effet cohérent ;
* ajouter ou modifier un effet de statut.

Les branches d’évolution peuvent faire évoluer une même capacité différemment.

Une branche peut par exemple ajouter un effet de Brûlure tandis qu’une autre ajoute un effet de Glacé.

Les modifications doivent conserver l’identité fonctionnelle de la capacité d’origine.

---

### 7.3. Rôles suggérés

Chaque forme possède un ou deux **rôles suggérés** au maximum.

La taxonomie officielle est :

* Dégâts ;
* Tank ;
* Support ;
* Contrôle.

Ces rôles sont uniquement informatifs.

Ils :

* n’accordent aucun bonus ;
* ne produisent aucun calcul ;
* ne limitent pas l’équipement ;
* n’empêchent pas le joueur de construire la créature autrement.

Ils décrivent l’orientation naturelle de la forme actuelle.

Une évolution ou une branche peut modifier les rôles suggérés.

---

### 7.4. Profil offensif suggéré

Chaque forme possède également un profil offensif suggéré :

* Physique ;
* Spécial ;
* Hybride.

Ce profil est informatif et n’impose aucune restriction.

Une forme Hybride peut notamment :

* posséder des capacités Physiques et Spéciales différentes ;
* posséder une même attaque comprenant plusieurs composantes de dégâts.

---

### 7.5. Hit hybride

Une même attaque ou un même Skill peut comporter, par exemple, une composante Physique et une composante Spéciale.

Un hit hybride reste **un seul hit**.

Pour ce hit :

* l’Esquive est résolue une seule fois ;
* le Critique est résolu une seule fois ;
* si le hit est esquivé, toutes ses composantes échouent ;
* si le hit Critique, le résultat de Critique s’applique au hit selon les règles prévues ;
* les effets liés au hit sont déclenchés une seule fois.

En revanche, les composantes de dégâts sont calculées séparément.

La composante Physique utilise notamment :

* la caractéristique offensive correspondante ;
* la Défense ;
* les réductions et protections applicables.

La composante Spéciale utilise notamment :

* la caractéristique offensive correspondante ;
* la Défense spéciale ;
* les réductions et protections applicables.

Les résultats des différentes composantes constituent ensuite les dégâts du hit.

Les règles détaillées doivent être synchronisées dans les documents Combat et Skills.

---

## 8. Évolution

### 8.1. Principe général

L’évolution représente une transformation permanente de la même instance possédée.

Elle peut modifier :

* l’apparence ;
* le ou les éléments ;
* le profil de caractéristiques de base ;
* les rôles suggérés ;
* le profil offensif ;
* les versions de la Basic Attack et des Skills.

Elle ne supprime jamais les choix ou investissements déjà attachés à l’instance.

---

### 8.2. Conditions propres aux créatures

Les conditions d’évolution ne sont pas uniformes.

Chaque transition peut posséder ses propres conditions.

Elles peuvent notamment dépendre :

* d’un niveau minimum ;
* d’un niveau d’étoiles minimum ;
* du port d’un objet particulier ;
* d’autres conditions explicitement prévues pour cette évolution.

Certaines évolutions peuvent utiliser uniquement une condition de niveau.

D’autres peuvent demander une combinaison de plusieurs conditions.

---

### 8.3. Objets comme conditions d’évolution

Lorsqu’un objet doit simplement être :

* possédé ;
* porté ;
* ou équipé ;

pour satisfaire une condition d’évolution, il n’est pas consommé.

Une évolution peut exceptionnellement demander explicitement la consommation d’un objet.

Dans ce cas seulement, l’objet disparaît.

Les objets consommables d’évolution ne constituent pas une obligation générale du système.

Lorsque de tels objets existent, leur obtention doit être cohérente avec la progression et leur rôle doit pouvoir être compris grâce aux informations disponibles en jeu.

---

### 8.4. Découverte des conditions

Les conditions d’évolution peuvent être inconnues lors de la première rencontre avec une famille.

Le joueur doit pouvoir les découvrir grâce à des indices raisonnables intégrés au jeu.

Ces indices peuvent notamment provenir :

* du lore ;
* des descriptions d’objets ;
* d’activités ;
* d’ennemis ;
* d’autres éléments cohérents du monde.

Une description peut suggérer un lien entre un objet et une famille sans indiquer explicitement la recette d’évolution.

Les conditions ne doivent pas reposer sur des associations totalement arbitraires nécessitant obligatoirement une ressource externe pour être comprises.

---

### 8.5. Déclenchement d’une évolution

Une évolution est déclenchée lors d’une montée de niveau lorsque les conditions nécessaires sont remplies.

L’XP est d’abord attribuée après le combat.

Le nouveau niveau de la créature est ensuite établi.

Une condition de niveau est une condition de **niveau minimum**.

Une créature n’a donc pas besoin d’évoluer exactement au niveau indiqué.

Si une évolution demande le niveau 45 et qu’une créature atteint le niveau 46 tout en remplissant les autres conditions, elle peut évoluer.

Si une créature dépasse le niveau requis sans remplir une autre condition, elle n’évolue pas.

Lorsqu’elle remplira plus tard les conditions restantes, l’évolution pourra être déclenchée lors d’une nouvelle montée de niveau.

---

### 8.6. Plusieurs évolutions après une même récompense d’XP

Une même récompense d’XP peut permettre plusieurs évolutions successives.

Si une créature gagne suffisamment de niveaux et remplit successivement les conditions de plusieurs stades :

* la première évolution est appliquée ;
* la seconde peut ensuite être appliquée si ses propres conditions sont également remplies.

Les évolutions sont alors présentées visuellement l’une après l’autre.

Aucune limite artificielle d’une évolution par combat n’est imposée.

---

### 8.7. Branches concurrentes

Lorsqu’un stade possède plusieurs branches possibles, leurs conditions doivent idéalement permettre au joueur de provoquer volontairement la branche recherchée.

Une branche ne doit pas devenir automatiquement l’évolution par défaut uniquement parce que ses conditions sont plus faciles à remplir que celles des autres branches.

Les conditions de branches concurrentes peuvent être conçues comme mutuellement exclusives.

Si plusieurs évolutions différentes sont néanmoins valides simultanément, le joueur choisit exceptionnellement la branche à appliquer.

---

### 8.8. Irréversibilité

Une évolution obtenue est définitive pour l’instance.

Une branche déjà empruntée ne peut jamais être remplacée par une branche incompatible.

Pour obtenir une autre branche, le joueur doit développer une autre instance de la même famille.

---

### 8.9. Conservation de la progression

Une évolution ne fait jamais perdre la progression de l’instance.

Elle conserve notamment :

* le niveau ;
* l’XP ;
* le niveau d’étoiles ;
* les points de caractéristiques déjà attribués ;
* les points non attribués ;
* l’équipement ;
* le surnom ;
* les tags ;
* le verrouillage.

Les points de caractéristiques déjà attribués restent exactement dans les caractéristiques choisies par le joueur.

Ils ne sont jamais redistribués automatiquement lorsqu’une évolution modifie le profil naturel de la créature.

Le joueur est responsable de ses choix de build.

---

### 8.10. Apparence cosmétique des anciennes formes

Lorsqu’une instance atteint une nouvelle forme, l’apparence de cette forme est définitivement débloquée pour cette instance.

Elle conserve également l’accès cosmétique aux formes précédemment atteintes sur son propre chemin d’évolution.

Une instance au stade 3 peut donc afficher visuellement :

* sa forme de stade 1 ;
* sa forme de stade 2 ;
* sa forme de stade 3 ;

si elle a réellement traversé ces formes.

Elle ne peut pas utiliser l’apparence d’une branche qu’elle n’a jamais empruntée.

Le choix visuel est purement cosmétique.

La créature conserve toujours mécaniquement :

* sa forme réelle ;
* ses caractéristiques réelles ;
* ses éléments réels ;
* ses Skills réels ;
* son niveau réel ;
* son score de Puissance réel.

---

## 9. Niveau d’étoiles

### 9.1. Structure générale

Une nouvelle instance commence à :

> **0 étoile**

Elle peut ensuite obtenir au maximum **15 montées d’étoiles**.

Elles sont regroupées visuellement en trois rangs :

### Bronze

* Bronze ★1 = étoile globale 1 ;
* Bronze ★2 = étoile globale 2 ;
* Bronze ★3 = étoile globale 3 ;
* Bronze ★4 = étoile globale 4 ;
* Bronze ★5 = étoile globale 5.

### Argent

* Argent ★1 = étoile globale 6 ;
* Argent ★2 = étoile globale 7 ;
* Argent ★3 = étoile globale 8 ;
* Argent ★4 = étoile globale 9 ;
* Argent ★5 = étoile globale 10.

### Or

* Or ★1 = étoile globale 11 ;
* Or ★2 = étoile globale 12 ;
* Or ★3 = étoile globale 13 ;
* Or ★4 = étoile globale 14 ;
* Or ★5 = étoile globale 15.

Les rangs Bronze, Argent et Or constituent une présentation du niveau global d’étoiles et non trois progressions indépendantes.

---

### 9.2. Effet des étoiles

Les étoiles augmentent uniquement les **six caractéristiques principales de base**.

Elles n’augmentent pas directement :

* le Crit ;
* les Dégâts critiques ;
* l’Esquive.

Le multiplicateur d’étoiles s’applique aux caractéristiques principales issues de la forme actuelle et de son stade.

Il ne multiplie pas :

* les points distribués par le joueur ;
* les caractéristiques fournies par l’équipement ;
* les buffs ;
* les autres bonus externes.

---

### 9.3. Progression non linéaire

Le multiplicateur total fourni par les étoiles n’évolue pas de manière linéaire.

Plus les étoiles deviennent difficiles à obtenir, plus la valeur marginale des nouveaux paliers doit pouvoir augmenter.

Le principe recherché est qu’une étoile avancée produise un gain plus significatif qu’une étoile de début de progression.

Les multiplicateurs exacts des 15 niveaux d’étoiles restent à déterminer pendant le balancing.

Ils doivent être appliqués comme **multiplicateurs totaux correspondant au palier actuel** et non comme une multiplication successive incontrôlée des résultats précédents.

---

### 9.4. Matériaux de montée d’étoile

Les montées d’étoiles utilisent comme matériaux d’autres instances de la **même famille**.

La forme et la branche de l’instance consommée n’ont pas d’importance en elles-mêmes.

Une instance d’une branche peut donc servir à améliorer une instance appartenant à une autre branche de la même famille.

Certains paliers peuvent cependant imposer que les instances utilisées comme matériaux possèdent elles-mêmes un niveau d’étoiles minimum.

Les conditions d’une montée d’étoile portent uniquement sur les étoiles des instances utilisées comme matériaux.

Une montée d’étoile ne demande pas :

* un niveau minimum de la créature cible ;
* une forme particulière ;
* une branche particulière ;
* un équipement particulier ;
* une autre condition de progression.

Les quantités et exigences précises de chaque palier appartiennent au document Progression.

---

### 9.5. Consommation d’une instance

Une instance utilisée comme matériau de montée d’étoile disparaît définitivement.

Sa progression individuelle est perdue.

Avant sa disparition, tous les objets qu’elle porte sont automatiquement :

1. déséquipés ;
2. replacés dans l’inventaire du joueur.

L’équipement n’est jamais détruit avec la créature consommée.

---

### 9.6. Irréversibilité

Une montée d’étoile est permanente.

Une instance ne peut jamais perdre volontairement des étoiles ou revenir à un palier inférieur.

Les instances consommées ne peuvent pas être récupérées.

---

## 10. Réinitialisation de progression

### 10.1. Reset complet gratuit

Le joueur peut effectuer une réinitialisation complète gratuite.

Cette réinitialisation :

* remet la créature niveau 1 ;
* remet son XP au niveau correspondant ;
* retire tous les points de caractéristiques acquis par les niveaux ;
* oblige le joueur à regagner ces points en remontant ses niveaux.

Elle ne modifie jamais :

* la forme actuelle ;
* la branche déjà choisie ;
* le niveau d’étoiles ;
* l’équipement ;
* le surnom ;
* les tags ;
* les apparences déjà débloquées ;
* les autres progressions permanentes de l’instance.

La créature niveau 1 utilise donc les caractéristiques de base de sa **forme évoluée actuelle**.

---

### 10.2. Conséquence sur une évolution non encore obtenue

Un reset ne fait jamais régresser une évolution déjà réalisée.

En revanche, une évolution qui n’avait pas encore été obtenue doit toujours respecter ses conditions après le reset.

Exemple conceptuel :

* une créature forme 2 niveau 44 n’a pas encore obtenu sa forme 3 nécessitant le niveau 45 ;
* elle est reset niveau 1 ;
* elle reste en forme 2 ;
* elle devra remonter jusqu’au niveau minimum requis avant de pouvoir obtenir sa forme 3.

---

### 10.3. Redistribution sans reset de niveau

Une méthode rare obtenue par le gameplay permet de redistribuer les points de caractéristiques sans revenir au niveau 1.

Un service payant limité peut fournir le même résultat immédiat.

Dans ces cas :

* le niveau ne change pas ;
* l’XP ne change pas ;
* tous les points déjà gagnés sont rendus immédiatement disponibles ;
* le joueur peut les redistribuer directement.

Ces méthodes n’accordent aucun point supplémentaire.

---

## 11. Score de Puissance

Chaque instance possède un **score de Puissance**.

Ce score représente une estimation synthétique de son développement et de sa puissance numérique actuelle.

Il doit notamment pouvoir refléter les éléments réellement actifs de la créature, comme :

* sa forme ;
* son évolution ;
* ses étoiles ;
* ses caractéristiques effectivement attribuées ;
* son équipement ;
* les autres sources permanentes de puissance.

La formule exacte reste à définir.

Le score doit être recalculé **en temps réel**.

Exemples :

* retirer un objet modifie immédiatement le score ;
* équiper un objet modifie immédiatement le score ;
* attribuer un point de caractéristique modifie immédiatement le score ;
* une évolution modifie immédiatement le score ;
* une montée d’étoile modifie immédiatement le score.

Un point de caractéristique non attribué n’augmente pas la Puissance.

Le score doit permettre une comparaison générale entre différentes familles et instances.

Il ne représente cependant pas une mesure absolue de l’efficacité d’une créature dans toutes les situations.

Les Skills, les éléments, les effets de statut, les rôles, les synergies et les compositions peuvent rendre une créature moins puissante numériquement beaucoup plus adaptée à un combat particulier.

---

## 12. Équipement

Chaque instance dispose de son propre **ensemble d’équipement actif**.

Cet ensemble est composé de plusieurs objets d’équipement répartis dans plusieurs emplacements.

Un **objet d’équipement** est un objet individuel.

Lorsqu’il n’est pas équipé, il appartient à l’inventaire.

L’équipement appartient à l’instance et non :

* à la famille ;
* à la forme.

Deux instances d’une même famille peuvent donc utiliser des équipements entièrement différents.

Une évolution conserve l’ensemble d’équipement de l’instance.

Le choix d’une apparence cosmétique différente ne modifie jamais l’équipement.

Les objets d’équipement possèdent notamment un **iLvl visible** représentant leur niveau de puissance propre.

L’iLvl des objets possède un cap.

Les règles détaillées concernant :

* le nombre de slots ;
* les types de slots ;
* les restrictions ;
* les statistiques ;
* les affixes ;
* les raretés ;
* les améliorations ;
* les sets ;
* les caps d’iLvl ;
* les règles de loot ;

appartiennent au document `08-ITEMS.md`.

---

## 13. Gestion individuelle d’une instance

### 13.1. Surnom

Chaque instance peut recevoir un **surnom personnalisé facultatif**.

Le surnom :

* appartient uniquement à l’instance ;
* ne remplace jamais le nom officiel de la forme ;
* peut être modifié ;
* peut être retiré ;
* peut être utilisé par le système de recherche.

---

### 13.2. Tags personnalisés

Chaque instance peut recevoir des **tags créés librement par le joueur**.

Exemples :

* PVP ;
* Boss ;
* Team Feu ;
* Tank ;
* À améliorer.

Ces tags :

* appartiennent à l’instance ;
* n’ont aucun effet de gameplay ;
* servent uniquement à l’organisation, la recherche et le filtrage.

Ils sont distincts des rôles suggérés par le jeu.

---

### 13.3. Verrouillage

Chaque instance peut être verrouillée ou déverrouillée.

Une instance verrouillée est protégée contre les actions destructrices ou les resets importants.

Elle ne peut notamment pas :

* être consommée comme matériau d’étoile ;
* être supprimée ;
* subir un reset complet niveau 1 ;
* utiliser une redistribution de caractéristiques ;
* utiliser le service payant équivalent de redistribution.

Le verrouillage ne bloque pas la progression normale.

Une instance verrouillée peut toujours :

* gagner de l’XP ;
* gagner des niveaux ;
* évoluer ;
* monter en étoiles ;
* changer d’équipement ;
* changer de surnom ;
* modifier ses tags ;
* changer d’apparence cosmétique ;
* être utilisée dans une équipe.

---

### 13.4. Favoris

Aucun système spécifique de **Favoris** n’est retenu actuellement.

Les besoins d’organisation doivent être couverts principalement par :

* les tags personnalisés ;
* les surnoms ;
* le verrouillage ;
* la recherche ;
* le tri.

---

## 14. Recherche et tri des créatures possédées

La gestion des créatures doit privilégier une **recherche dynamique unifiée** plutôt qu’une multiplication obligatoire de menus de filtres.

La recherche doit pouvoir exploiter notamment :

* les noms de famille ;
* les noms de formes ;
* les surnoms ;
* les rôles suggérés ;
* les éléments ;
* la rareté ;
* les tags personnalisés ;
* d’autres propriétés pertinentes.

La grammaire exacte, les opérateurs, les commandes et l’autocomplétion appartiennent aux futurs documents Collection et UI Flow.

---

### 14.1. Recherche par nom de forme

Rechercher le nom de la forme de base d’une famille retourne toutes les instances possédées de cette famille.

Rechercher une forme évoluée retourne :

* les instances possédant actuellement cette forme ;
* les instances situées sur une forme antérieure dont le chemin d’évolution peut encore mener à cette forme.

Les instances ayant déjà emprunté une branche incompatible sont exclues.

Ainsi, une forme future peut servir de recherche pour identifier les instances encore capables de l’atteindre.

---

### 14.2. Tri

Les créatures doivent pouvoir être ordonnées selon différentes propriétés.

Cela comprend notamment :

* Puissance ;
* rareté ;
* niveau ;
* étoiles ;
* ordre alphabétique ;
* rôle suggéré ;
* profil offensif ;
* élément ;
* stade ou progression d’évolution.

Les critères exacts, leur ordre et leur présentation appartiennent aux documents Collection et UI Flow.

---

## 15. Composition d’équipe et branches

Une équipe peut contenir jusqu’à six créatures selon les règles du document Combat.

Pour plusieurs instances appartenant à une même famille, la règle globale suivante s’applique :

> **Deux instances d’une même famille ne peuvent cohabiter dans une équipe que si leurs chemins d’évolution ont déjà réellement divergé.**

Une instance située sur le tronc commun avant une divergence est incompatible avec toutes les autres instances de sa famille dans cette équipe.

Exemple conceptuel :

Si l’arbre est :

> Forme de base
> → Forme intermédiaire commune
> → Forme finale Feu
> ou Forme finale Givre

alors :

* Forme finale Feu + Forme finale Givre : autorisé ;
* Forme intermédiaire commune + Forme finale Feu : interdit ;
* Forme intermédiaire commune + Forme finale Givre : interdit ;
* deux Formes intermédiaires communes : interdit.

Si les chemins divergent dès le stade 2, les deux branches peuvent cohabiter dès que les deux instances ont effectivement emprunté leurs branches distinctes.

Cette règle est globale et ne dépend pas du mode de jeu.

---

## 16. Acquisition d’une nouvelle instance

Une nouvelle instance obtenue normalement commence :

* dans sa forme de stade 1 ;
* niveau 1 ;
* à 0 étoile ;
* sans point de caractéristique déjà attribué.

La découverte antérieure de formes évoluées sur le compte ne modifie pas cette progression.

Obtenir à nouveau une famille déjà connue donne toujours une nouvelle instance individuelle à développer.

L’invocation donne normalement accès à la forme de base.

Les éventuelles exceptions d’acquisition directe par le gameplay doivent être explicitement documentées.

---

## 17. Encyclopédie des créatures

### 17.1. Séparation entre gestion et encyclopédie

L’**encyclopédie** constitue un menu distinct de la liste des créatures actuellement possédées.

La gestion des instances sert à :

* développer les créatures ;
* gérer leurs builds ;
* les équiper ;
* les organiser ;
* constituer les équipes.

L’encyclopédie sert à conserver la connaissance acquise par le compte sur les familles et formes découvertes.

---

### 17.2. Principe de découverte

Voir une créature ne constitue jamais une découverte.

Affronter une créature :

* dans une activité ;
* chez un autre joueur ;
* dans un combat PvP ;
* ou dans toute autre situation ;

n’ajoute rien automatiquement à l’encyclopédie.

Cette observation peut néanmoins fournir au joueur des indices sur l’existence de formes qu’il ne connaît pas encore.

Une famille ou une forme devient officiellement découverte uniquement lorsque le compte **l’obtient réellement** pour la première fois.

---

### 17.3. Découverte permanente au niveau du compte

Une découverte appartient au **compte** et non à l’instance.

Elle n’est jamais perdue.

Une forme reste donc connue même si :

* l’instance ayant permis sa découverte évolue ensuite ;
* l’instance est consommée ;
* le joueur ne possède plus actuellement aucune instance sous cette forme.

---

### 17.4. Données encyclopédiques

L’encyclopédie présente les données intrinsèques d’une forme.

Elle ne présente pas les valeurs personnalisées de l’instance ayant permis sa découverte.

Une fiche encyclopédique peut notamment présenter :

* le numéro de la famille ;
* le nom de la famille ou de la forme ;
* le lore général de la famille ;
* le lore propre à la forme ;
* la rareté ;
* les éléments ;
* les rôles suggérés ;
* le profil offensif ;
* les caractéristiques de base ;
* la Basic Attack ;
* les Skills et leur version propre à cette forme ;
* les informations d’évolution déjà découvertes.

Cela permet par exemple de consulter ultérieurement les informations d’une forme intermédiaire même lorsque toutes les instances possédées ont déjà évolué au-delà.

---

### 17.5. Familles non découvertes

L’encyclopédie n’affiche pas une liste complète de toutes les familles existantes.

Elle affiche uniquement ce que le joueur a réellement découvert.

Si un joueur possède les entrées :

> #1
> #42
> #53

les numéros manquants lui indiquent naturellement qu’il existe d’autres familles.

Le jeu ne lui indique cependant pas combien de familles existent au total ou combien il lui en reste à découvrir.

---

### 17.6. Arbre d’évolution partiellement caché

Lorsqu’une famille est découverte pour la première fois, le jeu ne révèle pas automatiquement toutes ses branches.

La représentation initiale peut se limiter à la structure générale des trois stades :

> Forme de base → ??? → ???

Cette représentation ne révèle pas :

* combien de formes intermédiaires existent réellement ;
* combien de formes finales existent ;
* combien de branches sont possibles.

Les branches sont ajoutées à l’arbre connu uniquement lorsqu’elles sont effectivement découvertes.

Le joueur ne sait donc jamais automatiquement combien de branches secrètes restent à trouver.

---

### 17.7. Conditions d’évolution découvertes

Avant qu’une évolution soit réalisée pour la première fois, ses conditions peuvent rester secrètes et être uniquement suggérées par les indices du jeu.

Une fois l’évolution obtenue, le compte mémorise définitivement :

* l’existence de la forme ;
* sa place connue dans l’arbre ;
* ses informations ;
* les conditions d’évolution découvertes.

Les conditions déjà réussies deviennent ensuite consultables explicitement.

Un joueur n’est pas obligé de redécouvrir une recette d’évolution pour chaque nouvelle instance de la même famille.

---

## 18. Capacité de créatures possédées

### 18.1. Capacité gratuite dynamique

Le compte possède une capacité maximale de créatures actives et utilisables.

La capacité gratuite est calculée selon :

> **CapacitéGratuite = arrondi(1,30 × NombreBranchesDisponibles)**

L’arrondi est effectué à l’entier le plus proche.

Exemples :

* 132,2 → 132 ;
* 132,8 → 133.

---

### 18.2. Calcul du nombre de branches

Pour le calcul de la capacité, chaque **chemin d’évolution distinct** compte comme une branche.

L’endroit exact où la divergence commence n’a pas d’importance.

Une famille entièrement linéaire compte donc pour :

> 1 branche

Une famille possédant trois chemins Feu, Givre et Foudre compte pour :

> 3 branches

même si ces chemins divergent uniquement au dernier stade ou dès le deuxième stade.

---

### 18.3. Augmentation automatique avec le contenu

Lorsque de nouvelles branches sont ajoutées au jeu, la capacité gratuite est recalculée automatiquement pour tous les comptes.

Ainsi, l’augmentation de la quantité de contenu disponible augmente également gratuitement l’espace de base accordé aux joueurs.

L’objectif est que la capacité gratuite reste suffisamment généreuse pour permettre une utilisation normale du système de collection.

---

### 18.4. Extensions payantes

Le joueur peut acheter des extensions permanentes de capacité.

Ces extensions sont **flat**.

Une extension achetée de :

> +50 places

reste toujours :

> +50 places

Elle ne diminue jamais lorsque la capacité gratuite augmente et n’est jamais absorbée par cette augmentation.

La capacité totale est donc :

> **CapacitéTotale = CapacitéGratuite + ExtensionsPayantes**

Les prix et tailles exactes des extensions restent à définir.

Les extensions de capacité constituent un **service de confort** et n’accordent aucune puissance de combat.

---

### 18.5. Dépassement de capacité

Une créature obtenue alors que la capacité utilisable est pleine n’est jamais perdue.

Elle est ajoutée à la collection dans un état :

* grisé ;
* bloqué ;
* inutilisable.

Une instance dans cet état ne peut notamment pas :

* être utilisée dans une équipe ;
* être développée ;
* recevoir de l’équipement ;
* servir de matériau d’étoile ;
* être manipulée normalement.

Elle reste néanmoins la propriété du joueur.

L’obtention de sa forme de base compte également comme une découverte valide dans l’encyclopédie.

---

### 18.6. File de déblocage

Les créatures bloquées par manque de capacité sont conservées selon leur ordre d’obtention.

Lorsqu’une place devient disponible :

> la plus ancienne instance bloquée est automatiquement rendue utilisable.

Le joueur ne choisit pas librement quelle créature sortir de cette file.

Cela empêche d’utiliser la zone bloquée comme un système de stockage gratuit entièrement flexible.

---

### 18.7. Obtention malgré une capacité pleine

Le joueur peut continuer à obtenir de nouvelles créatures même lorsque sa capacité est dépassée.

Les nouvelles instances rejoignent simplement la file des créatures grisées et inutilisables.

Le manque de capacité ne détruit donc jamais une récompense obtenue et ne bloque pas directement les systèmes d’acquisition.

---

## 19. Créatures jouables et monstres ennemis

Une **créature** est une entité :

* jouable ;
* collectionnée ;
* possédée ;
* développée par le joueur.

Un **monstre** est une entité ennemie rencontrée dans une activité.

Un monstre :

* n’est pas une créature possédée ;
* n’est pas ajouté à la collection de créatures du joueur ;
* n’est pas développé comme une instance ;
* ne fait pas partie d’une équipe possédée par le joueur.

Les deux termes ne sont pas interchangeables.

---

## 20. Dépendances documentaires

Les documents spécialisés doivent approfondir les règles de ce document sans les contredire.

### `02-COMBAT.md`

Doit rester la référence pour :

* les formules de caractéristiques ;
* les caps ;
* les rendements décroissants ;
* les dégâts ;
* l’Esquive ;
* le Crit ;
* le timing ;
* les règles de hit.

Il doit notamment être synchronisé avec la possibilité d’un **hit hybride Physique / Spécial**.

### `04-SKILLS.md`

Doit détailler :

* la Basic Attack ;
* les Active ;
* les Passive ;
* les Ultimate ;
* les variations des mêmes Skills à travers les formes ;
* les variantes de Skills liées aux branches ;
* les hits hybrides.

### `05-ELEMENTS.md`

Doit détailler les interactions élémentaires.

Une forme peut changer d’élément lors d’une évolution ou selon une branche.

### `06-STATUS_EFFECTS.md`

Doit détailler les effets de statut pouvant notamment être ajoutés ou modifiés par certaines évolutions de Skills.

### `07-EVOLUTIONS.md`

Doit approfondir notamment :

* la structure des arbres ;
* les branches ;
* les conditions ;
* les indices ;
* la découverte ;
* le déclenchement ;
* les objets liés aux évolutions ;
* la présentation des évolutions successives.

Il ne doit pas imposer un modèle uniforme de conditions à toutes les familles.

### `08-ITEMS.md`

Doit approfondir notamment :

* les objets d’équipement ;
* les slots ;
* l’iLvl ;
* les caps d’iLvl ;
* les statistiques ;
* les règles de loot ;
* les objets éventuellement liés à certaines évolutions.

### `10-PROGRESSION.md`

Doit approfondir notamment :

* la courbe d’XP infinie ;
* la valeur définitive des points gagnés par niveau ;
* le ratio minimum définitif d’XP ;
* les règles numériques d’arrondi de l’XP ;
* les 15 multiplicateurs d’étoiles ;
* les exigences de matériaux par palier ;
* la formule du score de Puissance ;
* les détails des resets.

### `11-COLLECTION.md`

Doit approfondir notamment :

* la gestion des instances ;
* l’encyclopédie ;
* les formes découvertes ;
* les arbres partiellement connus ;
* la recherche dynamique ;
* la grammaire de recherche ;
* les tris ;
* la capacité ;
* les créatures grisées ;
* la file de déblocage.

### `18-UI_FLOW.md`

Doit définir la présentation finale :

* de la fiche d’instance ;
* de l’encyclopédie ;
* de l’arbre d’évolution ;
* de la recherche ;
* des tris ;
* des créatures bloquées par manque de capacité.

---

## 21. Informations fonctionnelles à rendre accessibles sur une instance

Sans imposer la structure finale de l’interface, le joueur doit pouvoir accéder aux informations pertinentes de son instance, notamment :

* numéro de famille ;
* nom officiel de la forme actuelle ;
* surnom éventuel ;
* lore ;
* rareté ;
* niveau ;
* progression d’XP ;
* niveau d’étoiles ;
* stade et branche d’évolution ;
* éléments ;
* rôles suggérés ;
* profil offensif ;
* score de Puissance ;
* six caractéristiques principales ;
* trois caractéristiques secondaires ;
* points de caractéristiques disponibles ;
* Basic Attack ;
* quatre Skills ;
* équipement ;
* tags personnalisés ;
* état verrouillé ;
* formes cosmétiques débloquées ;
* accès aux informations d’évolution déjà découvertes.

La disposition, les onglets et les interactions appartiennent au document UI Flow.

---

## 22. Éléments à préciser ultérieurement

Les éléments suivants ne sont pas encore fixés et doivent rester ouverts jusqu’à leurs documents ou phases de balancing correspondants :

* la courbe exacte d’XP par niveau ;
* la validation définitive des 5 points de caractéristiques par niveau après balancing ;
* la validation définitive du ratio minimum d’XP actuellement envisagé à 10 % ;
* les règles exactes d’arrondi des gains d’XP ;
* les multiplicateurs exacts des 15 niveaux d’étoiles ;
* les quantités et niveaux d’étoiles requis pour les instances utilisées comme matériaux ;
* la formule exacte du score de Puissance ;
* les nombres et types de slots d’équipement ;
* les caps et valeurs exactes d’iLvl ;
* les prix et tailles des extensions de capacité ;
* la grammaire exacte de la recherche dynamique ;
* la présentation finale de l’encyclopédie et des arbres d’évolution ;
* les valeurs de base et profils numériques des différentes familles et formes.

---

## 23. Principe de maintenance

Ce document constitue la référence fonctionnelle actuelle pour les créatures jouables.

Les futurs documents spécialisés peuvent préciser ses systèmes, leurs valeurs et leurs interfaces.

Ils ne doivent pas modifier silencieusement les règles structurelles établies ici.

Si une décision ultérieure nécessite de faire évoluer l’un de ces principes, les documents concernés doivent être mis à jour ensemble afin de maintenir la cohérence de la documentation.

La documentation de monétisation doit notamment être synchronisée avec le service payant d’extension de capacité.

Les services de confort actuellement validés ne doivent pas être présentés comme une liste définitivement exhaustive : d’autres services de confort pourront être envisagés ultérieurement s’ils sont explicitement validés et restent compatibles avec les principes Free-to-Play, d’équité et d’absence de puissance payante du projet.
