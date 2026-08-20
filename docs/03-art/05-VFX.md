# Project Awakening — VFX

**Statut :** Draft de conception — base initiale à compléter

## 1. Rôle et périmètre du document

Ce document rassemble les principes validés concernant les effets visuels de **Project Awakening**.

Il ne définit pas encore les VFX précis de chaque élément, Skill, Effet de combat ou créature.

## 2. Fonction des VFX

Les VFX participent fortement au dynamisme et à la lisibilité des combats. Ils complètent les illustrations statiques et la mise en scène des cartes sans exiger que le personnage représenté dans chaque illustration soit animé.

Ils peuvent notamment matérialiser :

* les impacts ;
* les Skills ;
* les éléments ;
* les Effets de combat ;
* les projectiles ;
* les dégâts et les soins ;
* les surbrillances et flashs ;
* les particules et shaders ;
* les Ultimates.

Ces éléments constituent des possibilités de production et non une liste obligatoire à appliquer uniformément.

## 3. Indépendance de la simulation

Les VFX restituent les événements produits par la simulation. Ils ne doivent modifier ni le timing logique, ni le ciblage, ni les calculs, ni le RNG, ni les dégâts, ni les Effets de combat, ni les conditions de victoire.

Une vitesse de visualisation différente peut accélérer leur restitution sans modifier la simulation ou son résultat.

## 4. Production

Autant que raisonnablement possible, les VFX, shaders, paramètres et configurations doivent pouvoir être versionnés, reproduits, modifiés et vérifiés depuis le repository.

Le vectoriel peut être pertinent pour certains VFX, mais n’est pas imposé comme format universel.

## 5. Éléments à préciser ultérieurement

* Le langage visuel exact de chaque élément et Effet de combat.
* Les VFX propres aux Basic Attacks, Skills et Ultimates.
* Les niveaux d’intensité et priorités de lisibilité.
* Les règles de performance sur les appareils mobiles ciblés.
* Les formats, outils et pipelines de production.
* Les éventuelles variations de VFX liées aux skins de carte.
