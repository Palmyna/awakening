# Project Awakening — Guildes

**Statut :** Draft de conception — cadrage en cours

## 1. Rôle et périmètre du document

Ce document constitue le référentiel spécialisé du système de Guildes de Project Awakening.

Cette première partie définit les décisions validées concernant :

* la philosophie, la structure et l’identité des Guildes ;
* leur création, leur recrutement et leurs rangs ;
* les départs, exclusions, transferts et dissolutions ;
* l’architecture générale de leurs activités ;
* le fonctionnement actuellement cadré du Boss de Guilde ;
* les premières dépendances avec les Saisons, les Hauts Faits, l’interface et le futur système Social / Communication.

Le cadrage des Guildes n’est pas terminé. L’Expédition de Guilde, le système Social / Communication, certaines protections anti-abus et les paramètres de balancing restent notamment à définir. Le présent document ne doit donc pas être considéré comme un référentiel finalisé.

## 2. Philosophie générale

Une Guilde sert principalement à créer :

* un sentiment d’appartenance ;
* une communauté durable ;
* de l’entraide entre joueurs ;
* des objectifs et accomplissements collectifs ;
* du prestige collectif ;
* une identité et un historique communs.

La participation à une Guilde ne doit pas devenir obligatoire pour progresser normalement. Les récompenses propres aux Guildes doivent principalement soutenir le prestige, les Hauts Faits, les cosmétiques, la personnalisation et l’identité de la Guilde, sans fournir de puissance exclusive indispensable.

Un joueur ne peut appartenir qu’à une seule Guilde à la fois.

### 2.1. Frontière avec les factions narratives

Une Guilde n’est pas automatiquement une faction narrative canonique et le joueur n’appartient à aucune faction narrative obligatoire du seul fait de rejoindre une Guilde.

Une affiliation future à une faction du lore reste une possibilité non validée, notamment pour l’identité visuelle, les décorations, les objectifs thématiques, les cosmétiques ou certains contenus narratifs. Elle ne devra ni accorder de puissance ni bloquer un accès essentiel. Toute décision de ce type devra respecter les référentiels Lore.

## 3. Taille, déblocage et création

La capacité maximale de référence d’une Guilde est de **40 membres**. Cette valeur reste ajustable pendant les tests et le balancing.

Le système de Guildes est débloqué après une progression suffisante du compte et/ou du mode Histoire. Le jalon exact reste à définir.

Créer une Guilde coûte une quantité de monnaie du jeu. Aucun coût en monnaie premium n’est prévu ; la valeur exacte relève du balancing.

## 4. Recrutement sur invitation

Les Guildes fonctionnent uniquement sur invitation. Il n’existe actuellement aucune entrée libre dans une Guilde ouverte.

Le parcours courant doit rester simple, par exemple depuis une interaction avec le pseudo ou le profil d’un joueur. Une recherche manuelle peut compléter ce parcours sans devenir le seul moyen ordinaire d’inviter.

Le Chef et les Sous-chefs peuvent envoyer des invitations. Une invitation :

* peut être acceptée ou refusée ;
* expire après une durée restant à définir ;
* devient invalide si la Guilde est pleine ;
* devient invalide si le joueur rejoint une autre Guilde entre-temps.

Un joueur peut recevoir plusieurs invitations, mais ne peut accepter une appartenance qu’à une seule Guilde.

## 5. Identité de la Guilde

Une Guilde possède notamment :

* un nom et un TAG ;
* une description et un message d’accueil ;
* une bannière et une identité visuelle personnalisable ;
* des couleurs, motifs, bordures, décorations et effets visuels ;
* une liste de membres ;
* ses Hauts Faits, son historique et ses accomplissements ;
* éventuellement sa date de création.

Les Hauts Faits, performances saisonnières, activités et autres accomplissements collectifs compatibles peuvent débloquer des personnalisations de Guilde. Aucune personnalisation n’accorde de puissance.

### 5.1. Nom

Le nom d’une Guilde :

* possède au minimum quatre caractères ;
* peut contenir des lettres majuscules ou minuscules, des chiffres, des caractères accentués et des espaces ;
* ne peut pas contenir de caractères spéciaux.

Sa longueur maximale reste à définir selon les contraintes techniques et d’interface.

Le nom est définitif après la création. Aucun renommage n’est actuellement prévu.

### 5.2. TAG

Chaque Guilde possède un TAG de exactement quatre lettres. Ce TAG :

* utilise uniquement les caractères `A-Z` ;
* est toujours affiché en majuscules ;
* ne contient ni chiffre, ni accent, ni espace, ni caractère spécial ;
* peut être proposé à partir du nom ou saisi manuellement à la création ;
* est définitif après la création ;
* est unique dans tout le jeu.

Deux Guildes ne peuvent donc pas posséder simultanément le même TAG, même si leurs noms diffèrent.

### 5.3. Identité publique et clé normalisée

Une clé publique conceptuelle peut être dérivée sous la forme :

> `nomnormalisé#TAG`

La normalisation actuellement définie convertit le nom en minuscules et supprime ses espaces. Cette clé peut servir aux contrôles d’identité et d’unicité, tandis qu’un identifiant technique interne distinct, par exemple un UUID, peut être conservé en parallèle.

La clé normalisée ne remplace jamais le nom affiché. L’interface conserve une présentation lisible telle que :

> `Les Éveilleurs [EVEI]`

## 6. Rangs et permissions

Une Guilde possède seulement trois rangs structurels :

1. **Chef** ;
2. **Sous-chef** ;
3. **Membre**.

Une Guilde peut avoir de zéro à trois Sous-chefs. Le Chef choisit librement de les nommer ou non.

### 6.1. Chef

Le Chef possède toutes les permissions administratives. Il peut notamment :

* inviter et exclure des joueurs ;
* nommer ou rétrograder les Sous-chefs ;
* modifier la présentation et le message d’accueil ;
* gérer la personnalisation, la bannière et les éléments visuels ;
* effectuer les actions administratives des activités de Guilde ;
* transférer son rôle ;
* déclencher le recalibrage volontaire du Boss de Guilde ;
* dissoudre la Guilde.

Ces permissions ne permettent pas de modifier le nom ou le TAG, qui restent définitifs.

### 6.2. Sous-chef

Un Sous-chef peut notamment :

* inviter des joueurs ;
* exclure des Membres ;
* gérer le message d’accueil ;
* effectuer les actions administratives nécessaires aux activités de Guilde lorsque celles-ci le permettent.

Il ne peut pas :

* modifier l’identité ou la personnalisation visuelle de la Guilde ;
* gérer sa bannière ou ses éléments cosmétiques ;
* exclure ou rétrograder un autre Sous-chef ;
* agir administrativement sur le Chef ;
* nommer de nouveaux Sous-chefs ;
* dissoudre la Guilde.

La nomination et la gestion des Sous-chefs restent sous l’autorité du Chef.

## 7. Chef inactif

Une Guilde active ne doit pas rester définitivement bloquée par l’absence prolongée de son Chef.

La référence actuelle pour déclencher un transfert automatique est d’environ **90 jours** d’inactivité du Chef. Cette durée reste ajustable.

Lorsque le transfert devient nécessaire :

1. le rôle revient au Sous-chef actif ayant la plus grande ancienneté dans la Guilde ;
2. à défaut de Sous-chef actif, il revient au Membre actif ayant la plus grande ancienneté ;
3. l’ancienneté dans la Guilde départage les candidats concernés.

La définition transversale exacte de compte actif ou membre actif reste ouverte.

## 8. Départs, exclusions et dissolution

Un Membre ou un Sous-chef peut quitter librement sa Guilde. Un joueur exclu en est simplement retiré. Aucun départ, changement de Guilde ou exclusion n’applique de pénalité générale disproportionnée au compte.

Les protections anti-abus éventuelles doivent cibler l’éligibilité, les récompenses, les classements, les contributions compétitives et les activités saisonnières.

Le Chef ne peut pas quitter une Guilde qui contient encore d’autres membres. Il doit d’abord transférer volontairement son rôle. S’il est le dernier membre, il peut dissoudre la Guilde.

### 8.1. Dissolution

La dissolution est définitive et exige une double confirmation explicite. La seconde confirmation doit notamment signaler la perte irréversible :

* de la Guilde ;
* de ses Hauts Faits ;
* de son historique ;
* de ses personnalisations ;
* de sa progression.

Aucune restauration fonctionnelle n’est prévue. Le nom et le TAG redeviennent immédiatement disponibles pour une autre création.

Des traces techniques minimales peuvent être conservées pour la sécurité, la modération, l’audit ou des obligations légales. Elles restent invisibles du point de vue Game Design et ne permettent pas de restaurer la Guilde.

## 9. Dépendance au système Social / Communication

Les Guildes dépendront d’un futur référentiel Social / Communication, prévu mais non cadré et non créé.

Ce futur cadrage devra notamment traiter les amis, messages privés, chat général, chat de Guilde, interactions depuis les pseudos ou profils, invitations, blocage, signalement, modération, anti-spam, anti-flood et protections contre les bots ou comportements abusifs.

Il ne s’agit pas de prévoir un serveur de communication complexe intégré avec de nombreux salons. La Guilde doit seulement pouvoir utiliser le futur canal de Guilde fourni par ce système. Ses règles détaillées devront être définies avant l’implémentation concrète des Guildes.

## 10. Architecture des activités de Guilde

### 10.1. Hauts Faits de Guilde

Les Hauts Faits de Guilde représentent l’histoire permanente et le prestige de la Guilde. Ils progressent principalement de manière passive à partir des actions normales des membres et ne doivent pas devenir une checklist artificielle.

Leur structure détaillée et leurs récompenses éventuelles appartiendront au futur `19-ACHIEVEMENTS.md`. Le présent document ne valide aucune liste exhaustive ni aucune récompense précise.

### 10.2. Objectifs saisonniers de Guilde

Une Saison peut proposer des objectifs propres aux Guildes. Le cadre transversal, la structure et les règles communes de ces objectifs appartiennent à [`16-SEASONS.md`](./16-SEASONS.md). Le présent document devra seulement définir leur application au contexte des Guildes lorsque celle-ci sera cadrée.

### 10.3. Boss de Guilde

Le Boss de Guilde constitue le mode compétitif saisonnier principal des Guildes. Son fonctionnement propre est défini dans les sections suivantes.

### 10.4. Expédition de Guilde

L’Expédition est envisagée comme une activité ou un mini-jeu coopératif de Guilde, distinct du Boss de Guilde compétitif.

Son gameplay, ses règles, sa progression, ses récompenses, son calendrier, ses ressources et son scoring ne sont pas encore cadrés et ne sont pas définis dans cette première partie.

### 10.5. Absence de quêtes hebdomadaires dédiées

Un système distinct de quêtes hebdomadaires de Guilde n’est pas retenu actuellement. Les Hauts Faits, objectifs saisonniers et véritables activités de Guilde doivent structurer l’activité collective sans ajouter artificiellement une nouvelle checklist régulière.

## 11. Boss de Guilde — identité et combat

Le Boss de Guilde mesure la progression des comptes, la qualité des collections, la construction d’équipes, les builds, les synergies, l’adaptation stratégique et la capacité collective à faire progresser suffisamment de membres.

Il reprend davantage la logique des Boss personnels que celle du World Boss :

* chaque joueur affronte individuellement une instance complète du Boss à 100 % de ses PV ;
* une tentative doit réduire ces PV de 100 % à 0 % pour constituer une réussite ;
* les dégâts d’une tentative ne persistent jamais ;
* aucun dégât et aucune réserve de PV ne sont partagés entre les membres.

Une tentative utilise le moteur et les règles standards de combat de [`02-COMBAT.md`](./02-COMBAT.md) et [`12-MODES.md`](./12-MODES.md), sauf mécanique du Boss, modificateur saisonnier ou autre exception locale explicitement documentée. Le joueur peut modifier son équipe et son build entre ses tentatives.

Aucune normalisation spécifique n’est actuellement appliquée. Le joueur utilise ses créatures, niveaux, évolutions, caractéristiques, builds et équipements réels.

## 12. Saison, progression et équité entre Guildes

Chaque Saison possède un Boss de Guilde saisonnier. Pendant cette Saison, son identité générale, ses éléments, ses Skills, ses mécaniques et ses éventuels modificateurs saisonniers restent stables. Une Saison ultérieure peut proposer un autre Boss ou une autre version selon le content design.

Toutes les Guildes commencent la Saison au Boss niveau 1. Lorsqu’un niveau est validé, le niveau suivant devient le niveau actuel de la Guilde. Cette progression ne possède aucune limite théorique prédéfinie et est réinitialisée à la nouvelle Saison selon le cadre de [`16-SEASONS.md`](./16-SEASONS.md).

Pour un niveau donné, le Boss est strictement identique pour toutes les Guildes : mêmes caractéristiques, mécaniques, Skills, règles et modificateurs saisonniers éventuels. Il n’existe aucun scaling selon la taille de la Guilde, aucun scaling selon la puissance du joueur et aucune adaptation cachée individuelle.

Les courbes, coefficients, paliers mécaniques et paramètres de difficulté restent réservés au balancing et au content design.

## 13. Tentatives individuelles et énergie

Un membre éligible affronte directement le niveau actuel de sa Guilde. Il n’a pas à rejouer personnellement les anciens niveaux.

Lorsqu’un joueur réussit le niveau actuel :

* sa réussite compte une seule fois pour la validation collective ;
* il ne peut plus rejouer ce niveau ;
* il attend le déblocage du niveau suivant pour tenter de nouveau le Boss de Guilde.

Après un échec, le joueur peut retenter tant qu’il dispose de suffisamment d’énergie. Il n’existe actuellement aucune limite quotidienne de tentatives.

Le Boss de Guilde utilise la réserve générale d’énergie. Il ne crée aucun ticket, aucune clé, aucune énergie de Guilde ni aucune monnaie spéciale d’entrée. Le coût doit suivre une philosophie relativement faible ou modérée, comparable aux Boss personnels et non au coût élevé du World Boss. Sa valeur exacte relève du balancing.

La limite d’une réussite par joueur et par niveau encourage une répartition naturelle des contributions entre les membres, sans ticket ni quota artificiel.

## 14. Validation collective et éligibilité

Un niveau est validé lorsque **40 % des membres éligibles et actifs**, arrondis à l’entier le plus proche, l’ont chacun réussi individuellement.

Chaque joueur compte au maximum une fois par niveau. La différence mathématique produite par l’arrondi entre certaines tailles de Guilde est acceptée au profit de la simplicité du système.

Une Guilde doit compter au moins **cinq membres éligibles et actifs** pour participer au Boss de Guilde et figurer dans son classement saisonnier.

Un membre éligible doit notamment :

* appartenir à la Guilde ;
* avoir atteint l’ancienneté minimale requise ;
* être considéré comme actif.

La référence actuelle d’ancienneté est d’environ **sept jours** après l’entrée dans la Guilde. Cette valeur reste ajustable. La définition exacte de compte actif ou membre actif reste volontairement ouverte, mais les membres inactifs ne doivent pas augmenter artificiellement le seuil de validation.

### 14.1. Snapshot du seuil

Lorsqu’un nouveau niveau devient actif, le système calcule immédiatement le nombre de membres éligibles et actifs puis le nombre de réussites nécessaires. Ce seuil est figé pour toute l’instance du niveau.

Les arrivées et départs ne modifient pas automatiquement ce seuil. Un nouveau snapshot est effectué au déblocage du niveau suivant.

Le snapshot fige uniquement le nombre de réussites nécessaires, pas une liste fermée de contributeurs. Un nouveau membre peut contribuer au niveau en cours dès qu’il remplit les conditions d’éligibilité.

Une réussite obtenue par un joueur alors qu’il était éligible reste valide pour l’instance du niveau même s’il quitte ensuite la Guilde. Les contributions ne sont pas retirées rétroactivement.

## 15. Recalibrage volontaire

Le Chef peut volontairement sacrifier un ou plusieurs niveaux de progression afin de recalibrer le Boss de Guilde sur le roster actuel.

Le recalibrage :

* annule la progression du niveau en cours ;
* fait réellement reculer la Guilde ;
* retire les niveaux sacrifiés de sa progression saisonnière ;
* crée une nouvelle instance du niveau choisi ;
* effectue un nouveau snapshot et recalcule le seuil avec les membres alors éligibles et actifs ;
* permet de nouvelles tentatives sans conserver les blocages individuels de l’ancienne instance.

Ce recul est immédiatement reflété dans le classement. La Guilde ne peut pas obtenir un seuil plus favorable tout en conservant artificiellement son ancien niveau classé.

## 16. Classement saisonnier

Le critère principal du classement est le niveau de Boss le plus élevé actuellement validé par la Guilde.

À niveau égal, l’instant serveur exact auquel ce niveau a été validé départage les Guildes. La Guilde l’ayant validé en premier est mieux classée. Le serveur peut enregistrer ce timestamp avec une précision allant jusqu’à la milliseconde si nécessaire, sans obligation d’afficher cette précision complète dans l’interface.

Si une Guilde descend sous cinq membres éligibles et actifs :

* elle est temporairement retirée du classement ;
* elle ne perd ni sa progression ni son historique saisonnier ;
* elle peut réintégrer la compétition lorsqu’elle atteint de nouveau le minimum.

À la fin de la Saison, une Guilde sous ce minimum n’apparaît pas dans le classement final et ne reçoit pas ses récompenses de classement. Les récompenses obtenues auparavant ne sont pas annulées rétroactivement.

## 17. Récompenses du Boss de Guilde

### 17.1. Récompenses de paliers

Certains paliers peuvent générer des récompenses personnelles pour tous les membres éligibles au moment où le palier est franchi. Il n’est pas nécessaire que chaque bénéficiaire ait lui-même réussi le niveau concerné.

Ces récompenses ne sont pas rétroactives. Un membre qui devient éligible après le franchissement d’un palier ne génère aucune ancienne récompense de ce palier.

Le contenu, la fréquence et les quantités exactes restent à définir. Les exemples de récompenses ou de fréquences envisagés pendant le cadrage restent illustratifs et ne constituent aucune règle obligatoire.

### 17.2. Récompenses de classement final

Les récompenses principales du classement final appartiennent de préférence à la Guilde et soutiennent son prestige collectif. Elles peuvent notamment prendre la forme de personnalisations de bannière, couleurs, effets, décorations, éléments visuels prestigieux, Hauts Faits de Guilde ou titres de Guilde.

Une performance saisonnière importante peut rester visible dans l’historique de la Guilde. Aucune récompense de classement ne doit fournir de puissance exclusive ou obligatoire.

### 17.3. Récupération manuelle

Lorsqu’une récompense de palier, de classement ou de fin de Saison est configurée pour une récupération manuelle, elle suit la règle transversale de [`10-PROGRESSION.md`](./10-PROGRESSION.md) : elle apparaît dans le centre de récompenses, doit être réclamée avant son expiration et est définitivement perdue après ce délai.

## 18. Frontières documentaires

Le Boss de Guilde reste un mode compétitif saisonnier dont les règles internes appartiennent au présent document. [`16-SEASONS.md`](./16-SEASONS.md) porte uniquement le cadre transversal des Saisons et les règles communes des futurs objectifs saisonniers.

Le futur `19-ACHIEVEMENTS.md` définira le système commun des Hauts Faits, tandis que le présent document conserve leur application à l’histoire et au prestige de la Guilde.

[`20-UI_FLOW.md`](./20-UI_FLOW.md) traduit les besoins fonctionnels des Guildes et du centre de récompenses sans fixer leur layout final.

Le futur `21-SOCIAL_AND_COMMUNICATION.md`, prévu mais non créé, portera les règles sociales et de communication communes.

## 19. Dépendances documentaires

| Document | Responsabilité liée |
| --- | --- |
| [`01-GAME_DESIGN_DOCUMENT.md`](./01-GAME_DESIGN_DOCUMENT.md) | Place des Guildes dans l’expérience de long terme |
| [`02-COMBAT.md`](./02-COMBAT.md) | Moteur standard utilisé par le Boss de Guilde |
| [`10-PROGRESSION.md`](./10-PROGRESSION.md) | Énergie générale et récupération manuelle de certaines récompenses |
| [`12-MODES.md`](./12-MODES.md) | Contrats transversaux des modes et résultats |
| [`13-PVE.md`](./13-PVE.md) | Philosophie des Boss personnels, distinction avec le World Boss et classement de la Tour infinie |
| [`16-SEASONS.md`](./16-SEASONS.md) | Cadre transversal des Saisons et objectifs saisonniers |
| [`20-UI_FLOW.md`](./20-UI_FLOW.md) | Parcours de Guilde, invitations, Boss et centre de récompenses |
| [`04-MONETIZATION.md`](../00-foundation/04-MONETIZATION.md) | Garde-fous économiques et récompenses cosmétiques |
| [`01-LORE.md`](../02-world/01-LORE.md) | Frontière entre Guildes fonctionnelles et factions narratives |
| [`03-FORCES_PEOPLES_AND_FACTIONS.md`](../02-world/03-FORCES_PEOPLES_AND_FACTIONS.md) | Absence de faction obligatoire pour le joueur |

Le futur `19-ACHIEVEMENTS.md` devra prendre en charge les Hauts Faits de Guilde. Le futur `21-SOCIAL_AND_COMMUNICATION.md` devra prendre en charge les fonctions sociales et de communication communes.

## 20. Éléments à préciser ultérieurement

* Le jalon exact de déblocage du système de Guildes.
* Le coût exact de création.
* La longueur maximale du nom.
* La durée d’expiration des invitations.
* La définition transversale exacte de compte actif ou membre actif.
* La durée définitive avant transfert automatique du Chef.
* La durée définitive avant éligibilité d’un nouveau membre au Boss de Guilde.
* Le coût exact en énergie des tentatives.
* Les courbes, coefficients et paliers mécaniques de difficulté du Boss.
* Les paliers de récompense, leur fréquence, leur contenu et leur équilibrage.
* Les récompenses exactes du classement final.
* La durée exacte de récupération manuelle des récompenses concernées.
* Les protections anti-abus détaillées.
* Le cadrage détaillé des Hauts Faits de Guilde.
* Le fonctionnement du système Social / Communication.
* Le gameplay, la progression, les récompenses, le calendrier, les ressources et le scoring de l’Expédition de Guilde.
* Les autres activités de Guilde éventuelles.

Ces paramètres et cadrages incomplets ne doivent pas être interprétés comme des décisions validées. Une deuxième partie de cadrage doit notamment compléter l’Expédition de Guilde et les autres éléments encore ouverts.
