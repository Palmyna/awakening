# Project Awakening — Animations

**Statut :** Draft de conception — base initiale à compléter

## 1. Rôle et périmètre du document

Ce document rassemble les principes validés concernant l’animation et la mise en scène visuelle.

Il ne définit pas encore un catalogue précis d’animations pour chaque action, Skill, créature ou écran.

## 2. Principe général

L’animation repose largement sur les cartes, l’UI et la mise en scène. Une illustration de créature peut rester statique et le personnage qu’elle représente n’a pas besoin d’être animé directement.

Le dynamisme peut notamment utiliser :

* des déplacements ponctuels de carte ;
* des zooms et changements d’échelle ;
* de légères rotations ;
* des impacts et secousses ;
* des flashs et surbrillances ;
* l’affichage de dégâts, de soins ou de statuts ;
* des transitions et animations d’interface ;
* des VFX et projectiles associés.

Ces possibilités ne constituent pas une liste obligatoire d’animations uniformes.

## 3. Mise en scène des actions

Une attaque peut être restituée par une combinaison de mouvement de carte, d’impact, de texte, de VFX et d’animations d’interface.

Les Ultimates peuvent employer une mise en scène plus spectaculaire que les actions ordinaires, sans que cette différence modifie leur résolution dans la simulation.

## 4. Indépendance de la simulation

La restitution animée reste indépendante de la simulation de combat. Elle présente ses événements sans modifier la timeline, les positions logiques, les ciblages, les calculs, les dégâts, les Skills, les statuts, le RNG, les priorités ou les conditions de victoire.

Cette séparation doit rester compatible avec les replays et les différentes vitesses de visualisation.

## 5. Production

Autant que raisonnablement possible, les animations de cartes, d’UI et de présentation doivent être décrites, paramétrées, versionnées, testées et reproduites depuis le repository.

## 6. Éléments à préciser ultérieurement

* Le catalogue précis des animations.
* Les durées, courbes et transitions définitives.
* Les animations propres à chaque type d’action ou événement.
* Les mises en scène détaillées des Ultimates.
* Les animations d’invocation, d’évolution et de montée d’étoile.
* Les règles d’adaptation aux vitesses de visualisation.
* Les contraintes de performance mobile et le pipeline de production.

