# Project Awakening — Quêtes

**Statut :** Rédigé — référence actuelle, à maintenir à jour

## 1. Rôle et périmètre du document

Ce document définit le fonctionnement commun actuellement validé :

* des quêtes journalières ;
* des quêtes hebdomadaires ;
* des quêtes mensuelles ;
* des quêtes saisonnières individuelles ;
* des quêtes saisonnières de Guilde.

Les journalières, hebdomadaires et mensuelles forment les **quêtes périodiques**. Elles partagent un même socle fonctionnel tout en utilisant des durées, des pools, des objectifs et des récompenses adaptés à leur horizon.

Les quêtes saisonnières utilisent le calendrier de la Saison globale et restent distinctes des quêtes périodiques. Les missions temporaires des Events constituent un autre système, défini dans [`17-EVENTS.md`](./17-EVENTS.md).

Les listes concrètes, valeurs d’objectifs, pondérations, quantités de récompenses et détails graphiques relèvent du content design, du balancing, de l’implémentation et de l’UI.

## 2. Fonction des quêtes

Les quêtes périodiques servent à :

* encourager le retour régulier au jeu ;
* proposer de petits objectifs complémentaires ;
* favoriser la variété sans imposer une façon unique de jouer ;
* distribuer régulièrement de petites récompenses ;
* accompagner les activités que le joueur réalise déjà.

Elles ne doivent pas transformer une session en checklist obligatoire. Le joueur doit pouvoir progresser normalement sans optimiser constamment ses actions autour des quêtes.

Les quêtes saisonnières ajoutent des objectifs liés à la Saison globale sans constituer une progression générale de Saison ni devenir nécessaires à la progression normale.

## 3. Quantités de référence

Les références initiales de balancing sont :

* **3 quêtes journalières** ;
* **4 quêtes hebdomadaires** ;
* **5 quêtes mensuelles**.

Ces trois valeurs sont indépendantes, ajustables séparément et non structurelles. Une modification du nombre d’une catégorie n’entraîne pas automatiquement celle des deux autres et ne nécessite aucun changement d’architecture.

## 4. Calendrier des quêtes périodiques

Les quêtes périodiques utilisent les périodes calendaires suivantes.

| Catégorie | Début de la période | Fin de la période |
| --- | --- | --- |
| Journalière | `23:00` | `22:59` le lendemain |
| Hebdomadaire | dimanche à `23:00` | dimanche suivant à `22:59` |
| Mensuelle | dernier jour du mois précédent à `23:00` | dernier jour du mois concerné à `22:59` |

Au début de chaque nouvelle période, la sélection correspondante est renouvelée.

Au lancement, l’heure de référence est celle de **Bruxelles**. Si plusieurs régions ou serveurs existent ultérieurement, le principe reste un reset à `23:00` dans l’heure de référence de l’environnement concerné. Le choix initial de Bruxelles ne constitue donc pas une dépendance technique universelle ou définitive.

## 5. Génération et pools

Au début de chaque période, le joueur reçoit une nouvelle sélection tirée dans un pool adapté. Les pools journaliers, hebdomadaires et mensuels peuvent être différents.

La sélection doit vérifier :

* les fonctionnalités réellement débloquées ;
* les actions et activités réellement disponibles ;
* l’état actuel du compte ;
* l’absence de condition impossible ;
* l’absence de doublon exact ;
* l’absence de combinaison manifestement redondante.

Les pondérations, protections techniques et algorithmes de sélection restent à définir. Deux formulations techniquement différentes ne doivent pas être réunies lorsqu’elles demandent en pratique presque la même action.

## 6. Accessibilité et conditions

Une quête périodique utilise uniquement une fonctionnalité déjà débloquée et une action que le joueur peut raisonnablement réaliser dans l’état réel de son compte.

Elle ne doit jamais imposer :

* une créature ou une famille précise ;
* un Skill précis ;
* un skin précis ;
* un Artefact ou un équipement précis ;
* un autre contenu que le joueur pourrait ne pas posséder.

Les objectifs restent génériques, mesurables et compréhensibles. Ils peuvent, à titre illustratif, porter sur des combats, dégâts, soins, activités, invocations lorsque le système est débloqué, fabrication accessible ou évolutions réalisables sur une période adaptée. Ces exemples ne constituent aucune taxonomie fermée.

Chaque quête indique clairement ce qui la fait progresser, sa condition d’achèvement et la progression suivie par le jeu.

Les quêtes périodiques ne constituent pas des conditions d’évolution et n’introduisent aucun compteur historique dans le système d’évolution.

## 7. Adaptation à la périodicité

Les trois catégories périodiques ne sont pas les mêmes objectifs avec de simples multiplicateurs différents.

Les journalières restent légères, rapides et réalisables dans une ou quelques sessions raisonnables. Les hebdomadaires peuvent demander plusieurs sessions, davantage d’actions ou une variété d’activités sur plusieurs jours. Les mensuelles peuvent utiliser des objectifs plus conséquents ou des actions naturellement plus rares, réalisables sur l’ensemble du mois.

La conception de chaque objectif tient compte :

* de sa quantité ;
* du type et de la fréquence naturelle de l’action ;
* du temps disponible ;
* de l’effort attendu ;
* de l’état réel du compte.

Un objectif comme faire évoluer plusieurs créatures illustre une direction potentiellement adaptée à une mensuelle sans devenir une catégorie obligatoire ni une quête journalière validée.

## 8. Absence de streak punitive

Les quêtes hebdomadaires et mensuelles ne doivent pas recréer indirectement une obligation quotidienne parfaite.

Elles ne demandent pas de se connecter chaque jour, de maintenir une série de connexion ou d’accomplir une quête journalière pendant un nombre imposé de jours distincts. Le joueur répartit librement son effort pendant la période.

Une période manquée ne retire aucune progression durable générale, aucune énergie accumulée et aucune récompense déjà générée avant son expiration propre.

## 9. Non-rétroactivité et progression simultanée

Une mission, quête ou objectif comparable ne comptabilise pas rétroactivement les actions réalisées avant son activation ou avant qu’il devienne accessible au joueur, sauf exception explicitement documentée.

Cette règle s’applique aux quêtes journalières, hebdomadaires, mensuelles, saisonnières et aux missions d’Event selon leur référentiel propriétaire.

Une même action peut en revanche faire progresser simultanément tous les objectifs actifs dont elle remplit les conditions. Un même combat peut ainsi progresser une journalière, une hebdomadaire, une mensuelle, une quête saisonnière et une mission d’Event sans exiger des actions séparées artificiellement.

## 10. Reroll des quêtes périodiques

Chaque catégorie périodique possède un reroll gratuit par période :

* un reroll journalier ;
* un reroll hebdomadaire ;
* un reroll mensuel.

Le reroll s’applique uniquement à une quête non terminée. Il :

* remplace définitivement la quête choisie ;
* supprime toute sa progression ;
* génère une nouvelle quête valide et accessible ;
* recommence sa progression à zéro ;
* évite les doublons et redondances manifestes avec les autres quêtes présentes.

Une quête terminée ne peut pas être rerollée. Le reroll gratuit n’a aucun coût, ne se cumule pas, n’est pas stocké et n’est jamais reporté à la période suivante.

Les quêtes saisonnières individuelles et de Guilde ne possèdent aucun reroll.

## 11. Suivi, achèvement et récupération

L’interface affiche directement la progression utile de chaque quête, par exemple une valeur courante rapportée à son objectif, plutôt qu’un simple statut générique `En cours` lorsque le compteur est plus informatif.

Lorsqu’une condition est remplie :

* la quête est terminée ;
* sa récompense devient récupérable ;
* elle est mise en évidence ;
* le joueur doit la récupérer manuellement.

La récompense n’est pas créditée automatiquement. Après récupération, la quête passe en état `Récupéré` ou équivalent et peut être visuellement atténuée.

## 12. Fin de période et récompenses non réclamées

À la fin d’une période périodique :

* une quête non terminée disparaît ;
* sa progression est perdue ;
* elle ne peut plus progresser ;
* aucune progression n’est transférée à une future quête similaire ;
* la nouvelle sélection de la catégorie devient active.

Une quête terminée avant le reset a déjà généré sa récompense. Si celle-ci n’a pas été réclamée :

* elle quitte la liste active des quêtes ;
* elle reste récupérable dans le centre de récompenses ;
* elle suit la fenêtre temporelle générale d’environ **sept jours** définie dans [`10-PROGRESSION.md`](./10-PROGRESSION.md) ;
* elle expire définitivement si elle n’est pas réclamée à temps.

La même logique s’applique aux journalières, hebdomadaires, mensuelles et quêtes saisonnières terminées. Le centre de récompenses affiche leur provenance et leur délai restant sans conserver artificiellement les anciennes quêtes dans les listes actives.

## 13. Récompenses des quêtes

Les quêtes utilisent les systèmes ordinaires de récompenses et ne constituent jamais la seule source indispensable d’une puissance durable nécessaire à la progression normale ou à la compétition.

### 13.1. Journalières

Les journalières peuvent notamment accorder :

* de la monnaie générale ;
* des composants ;
* de petites ressources de progression ;
* une petite quantité de ressource générale d’invocation ;
* de l’énergie générale ;
* d’autres petites récompenses adaptées.

Les paquets cosmétiques ne font pas partie des récompenses ordinaires des journalières.

### 13.2. Hebdomadaires et mensuelles

Les hebdomadaires et mensuelles peuvent utiliser les mêmes familles de récompenses avec une importance adaptée à leur durée. Elles peuvent également proposer des paquets cosmétiques.

Les récompenses mensuelles peuvent être plus importantes que les hebdomadaires lorsque l’investissement demandé le justifie, sans devenir une source exclusive de puissance indispensable.

### 13.3. Règles communes

L’énergie générale accordée par une quête est immédiatement ajoutée à la réserve commune, sans consommable, ticket ou ressource parallèle, selon [`10-PROGRESSION.md`](./10-PROGRESSION.md). Sa présence n’est obligatoire dans aucune catégorie.

La ressource d’invocation reste la ressource générale définie dans [`09-GACHA.md`](./09-GACHA.md). Les quêtes ne créent aucun ticket spécifique, aucune monnaie parallèle ni aucun nouveau type d’invocation.

Un paquet obtenu gratuitement utilise exactement le même pool, les mêmes probabilités, le même nombre de skins, les mêmes règles de doublons et les mêmes règles d’ouverture que le paquet commercial correspondant.

Aucune quête ne peut exiger un achat réel, une dépense obligatoire dans la boutique, l’achat d’un skin, l’ouverture d’un contenu acheté ou l’utilisation d’un service payant.

Les catégories concrètes, quantités, fréquences et répartitions restent du balancing et du content design.

## 14. Quêtes saisonnières

Une Saison peut proposer des quêtes saisonnières individuelles et des quêtes saisonnières de Guilde. Elles :

* utilisent le calendrier de la Saison globale défini dans [`16-SEASONS.md`](./16-SEASONS.md) ;
* restent distinctes des journalières, hebdomadaires, mensuelles et missions d’Event ;
* sont légères, accessibles et non obligatoires pour la progression normale ;
* ne possèdent aucun reroll ;
* ne créent ni niveau, ni XP, ni barre globale, ni Battle Pass, ni parcours général de récompenses.

Les quêtes saisonnières de Guilde constituent des objectifs collectifs supplémentaires cohérents avec [`15-GUILDS.md`](./15-GUILDS.md). Elles ne créent aucun système permanent de quêtes quotidiennes ou hebdomadaires de Guilde.

### 14.1. Disponibilité progressive

De nouvelles quêtes saisonnières peuvent être ajoutées progressivement pendant une Saison. Une fois disponible, une quête reste normalement accessible jusqu’à la clôture.

Le content design doit éviter les ajouts trop tardifs laissant un temps irréaliste au regard de la difficulté, de la quantité demandée et de la fréquence naturelle de l’action. Les anciennes quêtes ne sont pas supprimées après quelques jours par une rotation punitive.

### 14.2. Récompenses saisonnières

Une quête saisonnière peut accorder de petites récompenses issues des systèmes normaux du jeu, notamment monnaie générale, composants, ressources de progression, ressource générale d’invocation ou énergie générale.

Une simple quête saisonnière ne doit pas automatiquement accorder un cosmétique exclusif important. La complétion d’un ensemble de quêtes peut éventuellement débloquer une récompense globale plus intéressante, notamment un paquet cosmétique, sans que cette structure soit obligatoire pour chaque Saison.

### 14.3. Clôture

À la clôture de la Saison :

* une quête non terminée devient indisponible et ne peut plus progresser ;
* une quête terminée reste accomplie ;
* une récompense déjà gagnée, y compris une éventuelle récompense globale, reste récupérable selon la fenêtre temporelle commune de la section 12.

## 15. Relation avec les Events

Les missions d’Event restent totalement distinctes des quêtes. Elles ne remplacent aucune quête périodique, ne modifient ni leurs sélections ni leur calendrier et ne deviennent pas des quêtes saisonnières.

Le joueur peut avoir simultanément des journalières, hebdomadaires, mensuelles, quêtes saisonnières et missions d’Event. Une même action peut les faire progresser en parallèle lorsque leurs conditions respectives sont remplies, sans créer de relation structurelle entre les systèmes.

## 16. Onboarding et besoins fonctionnels d’interface

Le système de Quêtes est introduit à un moment cohérent de la progression. Les jalons exacts et le tutoriel restent à définir, mais aucune quête ne peut apparaître avant les systèmes nécessaires à sa compréhension et à sa réalisation.

L’interface distingue clairement :

* les journalières ;
* les hebdomadaires ;
* les mensuelles ;
* les saisonnières.

Pour chaque quête, elle présente au minimum :

* l’objectif et sa progression utile ;
* la récompense ;
* la période et le temps restant ;
* les états terminé et récupéré ;
* la disponibilité du reroll lorsqu’il existe.

Cette séparation peut utiliser des onglets, sections, filtres ou une autre architecture. Le présent document n’impose aucun layout final ; les besoins détaillés appartiennent à [`20-UI_FLOW.md`](./20-UI_FLOW.md).

## 17. Dépendances documentaires

| Document | Responsabilité liée |
| --- | --- |
| [`01-GAME_DESIGN_DOCUMENT.md`](./01-GAME_DESIGN_DOCUMENT.md) | Place des quêtes dans la session et les objectifs du joueur |
| [`09-GACHA.md`](./09-GACHA.md) | Ressource générale d’invocation distribuée par certaines quêtes |
| [`10-PROGRESSION.md`](./10-PROGRESSION.md) | Énergie générale et fenêtre temporelle des récompenses non réclamées |
| [`12-MODES.md`](./12-MODES.md) | Activités pouvant faire progresser des objectifs |
| [`15-GUILDS.md`](./15-GUILDS.md) | Quêtes saisonnières collectives et absence de quêtes périodiques de Guilde dédiées |
| [`16-SEASONS.md`](./16-SEASONS.md) | Calendrier des quêtes saisonnières et clôture de la Saison |
| [`17-EVENTS.md`](./17-EVENTS.md) | Missions temporaires distinctes et progression simultanée possible |
| [`20-UI_FLOW.md`](./20-UI_FLOW.md) | Présentation, suivi, reroll et récupération manuelle |
| [`04-MONETIZATION.md`](../00-foundation/04-MONETIZATION.md) | Paquets gratuits et absence de dépense obligatoire |

## 18. Éléments à préciser ultérieurement

Le cadrage fonctionnel est établi. Restent réservés au content design, au balancing, à l’UI, à l’onboarding ou à l’implémentation :

* les pools et objectifs concrets de chaque catégorie ;
* les valeurs nécessaires à chaque objectif ;
* les pondérations et protections techniques contre les répétitions ;
* l’ajustement éventuel des références `3 / 4 / 5` ;
* les quantités, répartitions et fréquences exactes des récompenses ;
* la fréquence réelle des paquets cosmétiques ;
* les premières quêtes saisonnières ;
* les jalons exacts de déblocage et le tutoriel ;
* le wording, les icônes et le layout final.

Aucune question fonctionnelle bloquante ne subsiste actuellement pour le système de Quêtes.
