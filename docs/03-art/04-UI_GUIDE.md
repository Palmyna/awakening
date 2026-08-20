# Project Awakening — UI Guide

**Statut :** Draft de conception — base initiale à compléter

## 1. Rôle et périmètre du document

Ce document rassemble les principes visuels et de production actuellement validés pour l’interface.

Les besoins fonctionnels et parcours déjà établis restent définis dans le [draft UI Flow](../01-game-design/18-UI_FLOW.md). Le présent document ne fixe pas encore la navigation finale, la palette, les typographies ou un layout précis.

## 2. Mobile-first et tactile

L’interface est conçue d’abord pour Android et iOS et doit rester naturelle sur un écran tactile.

Les interactions, la densité d’information et la hiérarchie visuelle doivent préserver la lisibilité sur mobile. L’interface doit permettre de comprendre les informations utiles et les conséquences des actions sans ajouter de complexité inutile.

## 3. Composants réutilisables

L’interface doit favoriser une architecture composée d’éléments réutilisables.

Une représentation de créature ou de carte doit pouvoir servir dans différents contextes, notamment le combat, la composition d’équipe, la collection, la fiche d’une instance, l’encyclopédie, la sélection et l’acquisition.

Les informations affichées peuvent s’adapter au contexte. Cette adaptation ne modifie ni l’identité fonctionnelle de la créature ni la distinction entre la créature, sa carte et son illustration.

## 4. Lisibilité et cohérence

L’interface doit notamment :

* rendre lisibles les informations nécessaires à l’action en cours ;
* distinguer clairement les différents espaces fonctionnels ;
* signaler les états importants, les Effets de combat et les actions irréversibles ;
* préserver une cohérence d’usage entre les variantes d’un même composant ;
* éviter de surcharger chaque carte avec des informations sans utilité dans son contexte.

## 5. Production reproductible

Autant que raisonnablement possible, les composants UI, leurs configurations et leurs comportements doivent pouvoir être lus, créés, modifiés, versionnés, testés et vérifiés depuis le repository par les membres de l’équipe et les agents IA.

Ce principe vise l’autonomie et la reproductibilité. Il n’interdit pas une intervention humaine ni l’emploi d’outils ou d’assets externes lorsque ceux-ci sont pertinents.

## 6. Éléments à préciser ultérieurement

* L’architecture finale de navigation.
* La palette et les typographies.
* La grille, les espacements et les layouts précis.
* Le design exact et les dimensions des cartes.
* Le style définitif des icônes.
* Les états et transitions détaillés des composants.
* Les règles détaillées d’accessibilité.
* Les informations affichées par chaque variante contextuelle de carte.
