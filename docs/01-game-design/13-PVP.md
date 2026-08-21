# Project Awakening — PvP

**Statut :** Draft de conception — à relire et valider

## 1. Rôle et périmètre du document

Ce document rassemble les contraintes déjà validées qui devront encadrer un futur mode PvP.

Le PvP est envisagé à long terme. Il n’est pas confirmé pour la première version jouable et il est exclu de la vertical slice. Ce draft ne valide donc aucun format, matchmaking, classement, saison, récompense ou calendrier.

## 2. Place dans l’expérience

La compétition et la reconnaissance se situent après l’attachement aux créatures, la maîtrise des équipes, la progression, la découverte et la collection dans la hiérarchie actuelle des motivations.

Le PvP doit prolonger la stratégie de préparation : compréhension des créatures, builds, équipements, éléments, Effets de combat, formation et synergies.

Il ne doit pas transformer les réflexes ou la puissance achetée en facteur principal de réussite, ni définir la première expérience du jeu.

## 3. Contrat de combat applicable

Sauf exception explicitement définie par le futur format PvP, les règles générales du combat restent applicables :

* une équipe peut réunir jusqu’à six créatures ;
* deux instances d’une même famille ne cohabitent que si leurs chemins ont réellement divergé ;
* la formation utilise trois lignes et les positions restent fixes pendant le combat ;
* la simulation est continue, déterministe et reproductible à partir de la seed RNG ;
* les Basic Attacks et Active sont automatiques ;
* le mode Auto ou Manuel détermine globalement l’autorisation des Ultimate ;
* le timeout standard est de 120 secondes de simulation ;
* les conditions standard de départage s’appliquent lorsqu’aucune règle de mode différente n’est définie.

Le choix entre un affrontement synchrone, asynchrone ou une autre structure n’est pas validé. Cette décision déterminera notamment le rôle réel des équipes attaquante et défenseuse, du contrôle Manuel et des replays.

## 4. Intégrité et reproductibilité

Le résultat d’un combat doit pouvoir être reproduit à partir des mêmes conditions initiales, des mêmes décisions d’entrée et de la même seed RNG.

Cette propriété doit rester compatible avec :

* les replays ;
* le debugging ;
* la validation serveur ;
* la détection d’incohérences ;
* les simulations de balancing.

La représentation visuelle, les animations, les VFX et la vitesse de visualisation ne modifient jamais la simulation, les calculs, le résultat ou les récompenses.

Les responsabilités techniques de validation, d’autorité serveur et de sécurité ne sont pas encore définies.

## 5. Équité compétitive et monétisation

Le PvP doit respecter les fondations Free-to-Play du projet.

La boutique cosmétique ne vend aucune créature, invocation, ressource de progression, énergie, équipement ou puissance.

Les services de confort validés ne doivent pas créer de puissance inaccessible gratuitement :

* une redistribution payante ne fait que réattribuer des points déjà gagnés et possède un équivalent obtenu en jouant ;
* les vitesses ×2 et ×4 changent uniquement la restitution en temps réel ;
* une extension de capacité de créatures ne modifie aucune instance utilisable dans un combat déjà constitué ;
* un sac d’inventaire n’accorde aucune puissance de combat exclusive.

La progression, les équipements et les étoiles peuvent produire des écarts de puissance réels parce qu’ils appartiennent au développement normal des créatures. Leur traitement en PvP — conservation intégrale, normalisation, catégories ou autre solution — constitue une décision de conception encore ouverte.

## 6. Composition et préparation

Les règles globales de composition s’appliquent au PvP, notamment la limite de six créatures et la coexistence d’instances d’une même famille uniquement après divergence réelle de leurs chemins.

Le PvP doit permettre au joueur d’exprimer ses choix de build et de composition. Les rôles suggérés et profils offensifs restent informatifs et n’imposent aucune structure d’équipe par défaut.

Les éventuelles restrictions supplémentaires, informations visibles sur l’adversaire, règles de défense enregistrée ou possibilités de modification avant le combat ne sont pas validées.

## 7. Accès et énergie générale

Le PvP utilise par défaut la même réserve générale d’énergie que les autres modes individuels.

Le joueur peut choisir d’investir une grande partie ou la totalité de sa réserve disponible dans une session PvP. Le fait d’affronter un autre joueur ne crée pas automatiquement une énergie, un ticket, une clé ou une autre ressource d’entrée propre au PvP.

Le coût exact d’une participation relève du balancing futur. Une régulation différente nécessiterait une exception explicitement justifiée et documentée dans le présent référentiel.

Cette règle fixe uniquement la relation du PvP avec l’énergie. Elle ne détermine ni son format, ni son matchmaking, ni ses classements, ses saisons, ses récompenses ou son caractère synchrone ou asynchrone.

## 8. Résultats, classements et récompenses

Le système général prévoit qu’un mode peut définir sa propre condition de victoire, de défaite ou de score. Le futur PvP devra donc expliciter :

* son format d’affrontement ;
* son départage au timeout ;
* la gestion des abandons ou déconnexions ;
* le calcul d’un éventuel classement ;
* la progression compétitive ;
* les récompenses de participation, victoire, classement ou saison ;
* les règles de réinitialisation ou de conservation d’une saison à l’autre.

Aucun de ces systèmes n’est actuellement validé.

Une éventuelle récompense PvP doit respecter la séparation entre gameplay et économie cosmétique. Une récompense cosmétique ne confère aucune puissance ; une récompense de progression doit rester accessible selon des règles équitables qui ne transforment pas le paiement en avantage compétitif.

## 9. Présentation et analyse

Le combat PvP doit conserver la lisibilité générale du moteur de combat : actions importantes, Effets de combat, immunités, Ultimate, éliminations et changements majeurs.

Un résumé post-combat agrégé par créature doit permettre d’analyser les contributions des deux équipes sans exposer un combat log technique détaillé.

Les informations publiques, l’historique, les profils, les replays partageables et les règles de confidentialité ne sont pas validés.

## 10. Dépendances

| Document | Responsabilité liée |
| --- | --- |
| [`02-COMBAT.md`](./02-COMBAT.md) | Simulation, formation, ciblage et départage standard |
| [`03-CREATURES.md`](./03-CREATURES.md) | Identité, puissance et composition des équipes |
| [`10-PROGRESSION.md`](./10-PROGRESSION.md) | Sources de puissance, score de Puissance et réserve générale d’énergie |
| [`12-MODES.md`](./12-MODES.md) | Statut de périmètre et contrat commun des modes |
| [`18-UI_FLOW.md`](./18-UI_FLOW.md) | Préparation, combat, résultat et analyse |
| [`04-MONETIZATION.md`](../00-foundation/04-MONETIZATION.md) | Limites économiques et équité |

## 11. Éléments à préciser ultérieurement

* Les valeurs de classement et de matchmaking.
* Les quantités, fréquences et paliers de récompenses.
* La durée éventuelle des saisons et leurs paramètres.
* Les seuils ou catégories numériques d’appariement.
* Le coût exact en énergie générale d’une participation.

## 12. Questions ouvertes

* Le PvP doit-il être synchrone, asynchrone ou proposer plusieurs formats ?
* Le contrôle Manuel des Ultimate est-il disponible dans chaque format ?
* Comment les équipes attaquante et défenseuse sont-elles définies et configurées ?
* Les niveaux, étoiles, équipements et points attribués sont-ils conservés intégralement, normalisés ou répartis entre plusieurs catégories ?
* Quel système de matchmaking et de classement doit être retenu ?
* Quelle règle de départage doit remplacer ou conserver le départage standard au timeout ?
* Quelles récompenses peuvent soutenir la reconnaissance sans rendre le PvP obligatoire pour la progression normale ?
* Comment gérer les déconnexions, abandons, replays, historique et confidentialité ?
