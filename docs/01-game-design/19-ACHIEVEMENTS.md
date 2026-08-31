# Project Awakening — Hauts Faits

**Statut :** Rédigé — référence actuelle, à maintenir à jour

## 1. Rôle et périmètre du document

Ce document constitue le référentiel fonctionnel du système de **Hauts Faits** de Project Awakening. Il définit les règles communes aux accomplissements personnels et de Guilde, leur progression, leurs points, les Tours de force, leurs récompenses éventuelles et leur consultation.

Les Hauts Faits forment avant tout une bibliothèque des choses accomplies. Ils servent à conserver l'historique du joueur ou de la Guilde, valoriser l'ancienneté et l'investissement, reconnaître les performances remarquables et soutenir le prestige. Ils permettent une comparaison informelle sans constituer une progression de puissance, une monnaie ou une seconde boucle économique.

Le système doit partir d'un socle simple et utile, puis s'enrichir progressivement lorsqu'un volume réel de contenu ou un besoin fonctionnel justifie de nouveaux Hauts Faits ou de nouvelles catégories. Il ne doit pas être rempli artificiellement.

La liste concrète des Hauts Faits, leurs valeurs, leurs seuils, leurs récompenses précises et les contenus propres aux Saisons ou Events relèvent du content design et du balancing.

## 2. Deux espaces et deux propriétaires

Le système possède deux espaces fonctionnels :

1. les **Hauts Faits personnels**, appartenant au compte ;
2. les **Hauts Faits de Guilde**, appartenant à la Guilde.

Ils utilisent autant que possible les mêmes principes généraux. Une règle personnelle est transposée aux Guildes lorsqu'elle a du sens, sauf exception explicitement documentée.

Un Haut Fait personnel lié à une activité de Guilde reste la propriété du compte. Il est conservé après un départ, un changement de Guilde ou la dissolution de la Guilde. À l'inverse, un accomplissement collectif de Guilde, ses points et son historique restent exclusivement attachés à cette Guilde.

## 3. Catégories initiales

Les catégories personnelles initiales sont :

* Général ;
* Créatures ;
* Combat ;
* PvE ;
* PvP ;
* Guilde ;
* Events ;
* Saisons ;
* Tours de force.

Les catégories initiales des Hauts Faits de Guilde sont :

* Général ;
* Boss de Guilde ;
* Expéditions ;
* Saisons ;
* Tours de force.

Ces listes constituent le socle initial sans être fermées. Une catégorie supplémentaire n'est créée que lorsqu'un besoin concret ou un volume réel de contenu le justifie. Une activité appartenant déjà à un domaine, comme l'Histoire au PvE, ne reçoit pas automatiquement une catégorie distincte.

## 4. Structure et progression

### 4.1. Haut Fait binaire, progressif ou à paliers

Un Haut Fait peut être :

* binaire ;
* progressif ;
* composé de plusieurs paliers.

Il n'est jamais répétable. Une fois obtenu, il ne peut pas être recommencé afin de regagner sa validation, ses points ou ses récompenses. Des accomplissements de structure comparable peuvent néanmoins rester distincts lorsqu'ils correspondent à des périodes ou faits historiques différents.

Chaque palier peut représenter une étape du même accomplissement, rapporter ses propres points et, exceptionnellement, porter une récompense. Aucune grille universelle de paliers ou de points n'est validée.

### 4.2. Progression automatique et simultanée

Tous les Hauts Faits applicables progressent automatiquement. Le joueur n'active, ne sélectionne et ne met en suivi aucun Haut Fait au détriment des autres. Une même action fait progresser simultanément tous ceux dont elle satisfait les conditions.

Un système propriétaire peut exiger une action volontaire pour accomplir son activité. Cette exigence ne crée aucune activation séparée du Haut Fait qui observe le résultat.

### 4.3. Compteurs historiques et meilleurs résultats

Les Hauts Faits progressifs mesurent autant que possible des actions ou cumuls historiques qui ne régressent pas. Leur formulation doit privilégier ce qui a été accompli plutôt qu'un stock actuel susceptible de diminuer.

Lorsqu'une condition repose exceptionnellement sur une valeur qui peut ensuite redescendre, le Haut Fait porte sur le fait d'avoir atteint cette valeur et conserve le meilleur résultat obtenu. Une condition fondée sur un résultat final reste évaluée au moment de sa clôture.

Lorsque la condition est connue, la progression chiffrée réelle peut être affichée. Un Haut Fait binaire peut se limiter à son état obtenu ou non obtenu.

### 4.4. Représentation fonctionnelle des paliers

La progression d'un Haut Fait à paliers ne doit pas reposer uniquement sur un compteur compact. Elle doit permettre d'identifier visuellement les paliers obtenus et ceux qui restent à atteindre, par exemple au moyen de plusieurs éléments graphiques activés ou atténués.

Ce besoin fonctionnel n'impose ni pictogramme, ni couleur, ni animation, ni disposition, ni comportement tactile. Ces choix appartiennent à la future validation de [`20-UI_FLOW.md`](./20-UI_FLOW.md) et à la direction UI.

## 5. Permanence, dates et rétroactivité

### 5.1. Accomplissements permanents

Un Haut Fait obtenu reste définitivement acquis, même si sa condition n'est plus remplie ensuite. La même règle s'applique à une Guilde tant qu'elle existe. La dissolution constitue l'exception structurelle : elle détruit les accomplissements et l'historique appartenant à la Guilde.

### 5.2. Date d'obtention

Chaque Haut Fait personnel ou de Guilde obtenu conserve sa date d'obtention. L'heure exacte n'a pas besoin d'être affichée par défaut.

Pour un accomplissement conservant un meilleur résultat, la date correspond au moment où le résultat retenu a été atteint. Pour un accomplissement fondé sur un résultat final, elle correspond à la validation finale de ce résultat.

### 5.3. Rétroactivité fiable

Un Haut Fait peut être validé ou progressé rétroactivement lorsqu'une donnée historique fiable existe. La même règle s'applique aux Hauts Faits de Guilde.

Aucune donnée n'est inventée et aucune progression n'est reconstruite approximativement. Lorsque l'information fiable n'existe pas, le suivi commence seulement au moment où la donnée devient réellement disponible.

Cette règle est propre aux Hauts Faits et ne contredit pas la non-rétroactivité des quêtes et missions temporaires définie dans [`18-QUESTS.md`](./18-QUESTS.md).

## 6. Points, importance et absence de complétion globale

### 6.1. Points personnels et de Guilde

Les Hauts Faits personnels peuvent rapporter des **points de Hauts Faits**, accumulés dans un score global du compte. Les Guildes possèdent leur propre score, composé uniquement de leurs points de Hauts Faits.

Ces scores représentent l'accomplissement, l'ancienneté, l'investissement et le prestige. Ils ne constituent ni une monnaie, ni une ressource dépensable, ni un niveau, ni une progression de puissance et ne donnent aucun avantage mécanique.

Les points de Guilde appartiennent exclusivement à la Guilde et disparaissent avec elle lors de sa dissolution.

### 6.2. Absence de rareté officielle

Les Hauts Faits ne possèdent aucune rareté structurelle. Leur importance ressort de leur objectif, de leurs paliers, de leurs points éventuels et de leurs éventuelles récompenses. Les valeurs de points relèvent du content design selon l'importance et la difficulté de l'accomplissement.

### 6.3. Aucun total ni classement global

Le système n'affiche aucun nombre total de Hauts Faits existants ni pourcentage de complétion globale. Cette règle protège les secrets, les joueurs arrivés plus tard et l'extensibilité de la bibliothèque.

Il n'existe aucun leaderboard général des points de Hauts Faits personnels ou de Guilde. Les scores servent uniquement à la comparaison informelle lors de la consultation d'un profil ou d'une fiche de Guilde. Un classement ne pourra être étudié ultérieurement que si un besoin concret apparaît.

## 7. Hauts Faits secrets

Un Haut Fait secret non obtenu est totalement invisible. Il ne possède aucun emplacement vide, intitulé masqué, silhouette ou compteur permettant d'en déduire l'existence.

Après son obtention, il apparaît normalement avec son nom, son état validé, ses points éventuels et sa date. Sa condition d'obtention reste absente et n'est pas remplacée par une indication artificielle.

La consultation publique applique exactement la même règle : un secret non découvert n'apparaît pas, tandis qu'un secret obtenu est visible avec les mêmes informations que pour son propriétaire, sans révéler sa condition.

## 8. Tours de force

### 8.1. Identité, points et compteur

Les **Tours de force** représentent des accomplissements historiques, exceptionnels ou devenus définitivement limités dans le temps. Ils forment une catégorie spéciale dans les espaces personnel et de Guilde.

Un Tour de force :

* ne rapporte jamais de points de Hauts Faits ;
* compte toujours pour `1` dans le compteur de Tours de force de son propriétaire ;
* ne contribue à aucun total ou pourcentage de complétion globale.

Le compteur indique uniquement le nombre obtenu. Il n'affiche ni total existant, ni pondération selon la difficulté, le prestige, le résultat ou les anciens paliers.

### 8.2. Visibilité et sous-catégories

La rubrique `Tours de force` n'apparaît que lorsque le compte ou la Guilde en possède au moins un.

Les Tours de force personnels réutilisent comme sous-catégories les domaines personnels pertinents : Général, Créatures, Combat, PvE, PvP, Guilde, Events ou Saisons. Ceux de Guilde réutilisent Général, Boss de Guilde, Expéditions ou Saisons.

Une sous-catégorie n'apparaît que si elle contient réellement un Tour de force obtenu. Aucun Tour de force manqué, aucune rubrique vide et aucun filtre de contenus historiques impossibles ne sont affichés.

### 8.3. Accomplissement temporaire et conversion

Un accomplissement rattaché à une fenêtre temporaire non reproductible et destiné à devenir historique peut être présenté comme un Haut Fait actif pendant cette fenêtre. Il peut :

* apparaître dans sa catégorie fonctionnelle normale ;
* afficher sa progression et ses paliers ;
* proposer certaines récompenses ;
* rapporter `0` point lorsqu'il est destiné dès l'origine à devenir un Tour de force.

L'absence de points évite toute hausse temporaire du score suivie d'une diminution à la conversion.

À la fin de la période :

* s'il a été obtenu, il devient un Tour de force, quitte sa catégorie active et rejoint la sous-catégorie adaptée ;
* s'il n'a pas été obtenu, il disparaît complètement de la bibliothèque.

Le Tour de force obtenu conserve son identité, la période concernée, son meilleur résultat pertinent, sa date et les récompenses déjà gagnées. Il montre uniquement le résultat réellement accompli : les anciens paliers inférieurs, supérieurs ou manqués et le prochain objectif ne sont plus affichés.

Cette règle remplace l'ancienne conservation des Hauts Faits saisonniers expirés et non obtenus comme contenus historiques indisponibles.

### 8.4. Reclassification d'un ancien Haut Fait

Un Haut Fait classique devenu définitivement impossible à obtenir à la suite d'une évolution du jeu peut être reclassé en Tour de force.

Pour ses propriétaires, il conserve sa date, son état accompli et ses récompenses acquises, rejoint la sous-catégorie adaptée et ses anciens points sont retirés du score global. Pour les comptes ou Guildes qui ne l'avaient pas obtenu, il disparaît. Une reclassification ne retire jamais rétroactivement une récompense gagnée.

## 9. Saisons, Events et performances temporaires

Les accomplissements propres à une Saison peuvent suivre le cycle défini pour les contenus temporaires. Des performances différentes, comme un meilleur seuil atteint et un classement final, peuvent former des Tours de force distincts lorsqu'elles représentent des faits conceptuellement différents.

Dans le PvP, un accomplissement temporaire de cote peut conserver le meilleur résultat atteint même si la cote redescend avant la clôture. Un accomplissement de classement reste fondé sur le résultat final figé.

Dans la Tour infinie, un Tour de force peut conserver un résultat remarquable, le meilleur étage atteint ou un classement final lorsque le contenu le prévoit. Le reset de la progression jouable ne supprime donc pas la mémoire des accomplissements importants.

Les Events distinguent :

* les Hauts Faits généraux et durables liés aux Events, qui peuvent progresser au fil de plusieurs occurrences et rapporter des points ;
* les accomplissements temporaires propres à une occurrence, qui peuvent devenir des Tours de force s'ils ont été obtenus et disparaissent sinon.

Cette logique n'est pas réservée techniquement aux Saisons et aux Events. Tout futur système comportant une fenêtre temporaire non reproductible peut l'utiliser lorsque l'accomplissement est destiné à devenir historique. Un accomplissement qui reste réellement obtenable peut demeurer un Haut Fait classique.

## 10. Récompenses

### 10.1. Séparation entre gameplay et prestige

Les Hauts Faits ne constituent pas un second système de progression économique. Les récompenses de puissance, d'invocation, d'énergie, d'équipement, de composants, de ressources économiques ou de progression mécanique restent principalement distribuées directement par les systèmes propriétaires.

Aucun Haut Fait ou Tour de force n'accorde directement de puissance de combat, d'augmentation de statistique, de créature, de ressource générale d'invocation, d'énergie générale, d'équipement, de composant ou monnaie de progression, ni d'avantage compétitif obligatoire.

Les paquets cosmétiques peuvent continuer à être distribués directement par le PvP, la Tour, les Quêtes, les Events ou d'autres systèmes compatibles. Ils n'ont pas à devenir des récompenses de Hauts Faits.

### 10.2. Récompenses propres aux Hauts Faits

Un Haut Fait ordinaire n'accorde normalement que sa validation et ses points éventuels. Une récompense supplémentaire reste exceptionnelle et réservée aux accomplissements ou paliers qui la justifient.

Un Haut Fait majeur, un palier important ou un Tour de force peut porter une récompense de prestige ou cosmétique, notamment un titre, un badge, une bordure ou un contour, un skin prestigieux, une personnalisation ou une autre récompense honorifique. Aucune récompense précise n'est rendue obligatoire par cette liste.

Un Haut Fait à paliers n'a aucune obligation d'accorder une récompense à chaque palier. La répartition précise relève du content design.

Le principe de propriété est le suivant : les récompenses économiques ou de gameplay restent portées par l'activité qui les génère ; une récompense spécifiquement liée au prestige d'un accomplissement peut être portée par le Haut Fait ou le Tour de force correspondant.

### 10.3. Validation et récupération

Lorsqu'un Haut Fait personnel est obtenu, sa validation et ses points éventuels sont crédités automatiquement. Une récompense supplémentaire peut être générée dans le centre de récompenses et récupérée manuellement.

Une récompense propre à un Haut Fait est permanente : elle ne possède aucun délai d'expiration intrinsèque et reste récupérable tant que ses autres conditions applicables restent valides, selon le cadre commun de [`10-PROGRESSION.md`](./10-PROGRESSION.md).

### 10.4. Récompenses de Guilde

Une récompense provenant d'un Haut Fait de Guilde appartient exclusivement à la Guilde. Elle ne constitue pas une récompense personnelle distribuée aux membres. Elle peut notamment débloquer une bannière, un emblème, une décoration, un titre de Guilde, une personnalisation ou un autre élément collectif de prestige.

Lorsqu'elle doit être réclamée, elle apparaît dans le centre de récompenses du Chef et doit être clairement identifiée comme appartenant à la Guilde. Le Chef agit comme personne autorisée à la récupérer pour la Guilde ; elle ne devient jamais la propriété de son compte personnel. Le détail visuel de cette distinction relève de l'UI.

## 11. Règles propres à la propriété de Guilde

Seules les actions réalisées pendant l'appartenance d'un joueur à une Guilde contribuent aux Hauts Faits de cette Guilde. Les contributions antérieures ne sont pas transférées à une nouvelle Guilde. Le suivi d'un Haut Fait personnel lié aux activités de Guilde reste, lui, attaché au compte.

Un joueur quittant une Guilde n'emporte aucun Haut Fait, point, Tour de force ou historique collectif et n'en reçoit aucune copie personnelle. Lorsqu'il rejoint une Guilde existante, il peut consulter son score, ses Hauts Faits, ses Tours de force et son histoire antérieure sans devenir personnellement propriétaire des accomplissements obtenus avant son arrivée.

La dissolution détruit définitivement les Hauts Faits, Tours de force, points, historiques, personnalisations liées et progressions appartenant à la Guilde. Les éventuelles traces techniques invisibles conservées pour la sécurité ou les obligations légales ne permettent aucune restauration fonctionnelle.

## 12. Consultation publique et indicateurs internes

Les Hauts Faits personnels font partie du profil public du joueur. Un visiteur peut consulter le score global, les Hauts Faits obtenus et leurs dates, les Tours de force, leur compteur et les récompenses honorifiques visibles participant à l'identité publique. Il voit le même état de bibliothèque que son propriétaire. Aucune option de masquage spécifique n'est actuellement validée.

La fiche publique d'une Guilde expose selon la même logique ses points, Hauts Faits, Tours de force, compteur, dates et accomplissements prestigieux. Les parcours d'accès précis relèvent du futur référentiel Social / Communication.

Le système utilise des pastilles internes pour signaler le nouveau contenu ou les accomplissements nouvellement obtenus. Leur état peut se propager sur l'entrée générale `Hauts Faits`, l'espace Personnel ou Guilde concerné, une catégorie et l'accomplissement concerné.

Une action permettant de **tout marquer comme vu** en une seule fois est obligatoire. Le joueur ne doit pas ouvrir individuellement chaque catégorie, Haut Fait ou Tour de force uniquement pour retirer les indicateurs.

Les Hauts Faits ne génèrent aucune notification téléphone ou push hors de l'application.

## 13. Frontières documentaires

[`10-PROGRESSION.md`](./10-PROGRESSION.md) porte l'architecture commune de disponibilité, d'éligibilité et de récupération des récompenses. Le présent document définit la permanence et la propriété des récompenses propres aux Hauts Faits.

[`13-PVE.md`](./13-PVE.md) conserve les règles de la Tour infinie et des autres modes PvE. Il expose les performances susceptibles d'alimenter un accomplissement, tandis que le présent document définit leur conservation comme Haut Fait ou Tour de force.

[`14-PVP.md`](./14-PVP.md) porte la cote, les jalons, l'activité et le classement. Le présent document porte les Hauts Faits saisonniers correspondants, le meilleur résultat conservé et la distinction entre accomplissements de cote et de classement.

[`15-GUILDS.md`](./15-GUILDS.md) reste propriétaire des actions, activités, permissions et de la dissolution des Guildes. Le présent document porte la structure, les points, les Tours de force, les récompenses et l'historique de leurs Hauts Faits.

[`16-SEASONS.md`](./16-SEASONS.md) porte le calendrier, l'inter-saison, la clôture et la validation des résultats finaux. Le présent document porte le cycle des Hauts Faits temporaires et leur conversion en Tours de force.

[`17-EVENTS.md`](./17-EVENTS.md) porte les occurrences, missions et récompenses directes des Events. Le présent document distingue les Hauts Faits généraux des accomplissements propres à une occurrence.

[`18-QUESTS.md`](./18-QUESTS.md) porte les objectifs de période, généralement non rétroactifs, et leurs récompenses régulières. Les Hauts Faits sont des accomplissements historiques automatiques pouvant exploiter une donnée rétroactive fiable. Une même action peut progresser simultanément une quête et plusieurs Hauts Faits.

Le futur `21-SOCIAL_AND_COMMUNICATION.md` devra permettre l'accès aux profils et fiches publiques nécessaires sans que le présent document fixe les parcours, permissions sociales ou interactions depuis un pseudo.

[`20-UI_FLOW.md`](./20-UI_FLOW.md) devra être relu et validé ultérieurement après le cadrage Social / Communication. Il devra reprendre les besoins fonctionnels définis ici sans que le présent référentiel impose un layout final.

## 14. Dépendances documentaires

| Document | Responsabilité liée |
| --- | --- |
| [`01-GAME_DESIGN_DOCUMENT.md`](./01-GAME_DESIGN_DOCUMENT.md) | Place des accomplissements dans l'expérience de long terme |
| [`10-PROGRESSION.md`](./10-PROGRESSION.md) | Centre de récompenses, disponibilité, éligibilité et récupération manuelle |
| [`11-COLLECTION.md`](./11-COLLECTION.md) | Skins, séries et récompenses cosmétiques |
| [`13-PVE.md`](./13-PVE.md) | Performances de la Tour infinie et autres accomplissements PvE |
| [`14-PVP.md`](./14-PVP.md) | Cote, jalons, classements et performances PvP |
| [`15-GUILDS.md`](./15-GUILDS.md) | Propriété collective, activités, permissions et dissolution |
| [`16-SEASONS.md`](./16-SEASONS.md) | Fenêtres saisonnières, clôture et résultats finaux |
| [`17-EVENTS.md`](./17-EVENTS.md) | Accomplissements généraux ou propres à une occurrence |
| [`18-QUESTS.md`](./18-QUESTS.md) | Frontière avec les objectifs temporaires non rétroactifs |
| [`20-UI_FLOW.md`](./20-UI_FLOW.md) | Besoins fonctionnels de présentation à reprendre lors de sa future validation |
| [`04-MONETIZATION.md`](../00-foundation/04-MONETIZATION.md) | Garde-fous économiques et récompenses cosmétiques |

## 15. Éléments à préciser ultérieurement

Restent volontairement réservés au content design, au balancing, à l'UI ou à l'implémentation :

* la liste et le nombre des Hauts Faits de lancement et futurs ;
* les valeurs de points, seuils, paliers et compteurs concrets ;
* les récompenses précises et leur répartition ;
* le contenu propre à chaque Saison et Event ;
* le rythme d'ajout de nouveaux Hauts Faits ;
* les Tours de force propres aux futurs contenus temporaires ;
* les choix graphiques et l'ergonomie détaillée ;
* le schéma de données, les algorithmes internes et les données historiques disponibles ;
* les outils éventuels de content design et de gestion des Hauts Faits.

Aucun de ces sujets n'empêche le présent document de servir de référentiel fonctionnel actuel.
