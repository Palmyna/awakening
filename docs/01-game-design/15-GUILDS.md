# Project Awakening — Guildes

**Statut :** Rédigé — référence fonctionnelle actuelle, à maintenir à jour

## 1. Rôle et périmètre du document

Ce document constitue le référentiel spécialisé du système de Guildes de Project Awakening et réunit les décisions validées des deux parties du cadrage fonctionnel concernant :

* la philosophie, la structure et l’identité des Guildes ;
* leur création, leur recrutement et leurs rangs ;
* les départs, exclusions, transferts et dissolutions ;
* l’architecture générale de leurs activités ;
* le fonctionnement du Boss de Guilde ;
* les Expéditions de Guilde ;
* les demandes et dons de composants ;
* les dépendances avec les Saisons, les Hauts Faits, l’interface et le futur système Social / Communication.

Le système de Guildes est fonctionnellement cadré à son niveau actuel. Les valeurs de balancing, le contenu concret des Expéditions et des Hauts Faits, le système Social / Communication et certaines protections transversales restent à définir dans leurs cadres respectifs. Cette clôture fonctionnelle ne signifie donc pas que ces contenus ou paramètres sont finalisés.

## 2. Philosophie générale

Une Guilde sert principalement à créer :

* un sentiment d’appartenance ;
* une communauté durable ;
* de l’entraide entre joueurs ;
* des objectifs et accomplissements collectifs ;
* du prestige collectif ;
* une identité et un historique communs.

La participation à une Guilde ne doit pas devenir obligatoire pour progresser normalement. Les activités de Guilde peuvent fournir de la monnaie générale, des ressources, des composants ou d’autres récompenses utiles, mais jamais une puissance exclusive indispensable. Toute ressource importante pour la progression ou les builds doit rester accessible par d’autres moyens lorsque l’équilibre général le nécessite.

Le prestige, les Hauts Faits, les cosmétiques, la personnalisation, l’identité et l’historique de la Guilde restent des orientations majeures, particulièrement pour les accomplissements compétitifs ou de complétion.

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
* récupérer au nom de la Guilde les récompenses de ses Hauts Faits ;
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
* de ses Tours de force et points de Hauts Faits ;
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

Les Hauts Faits de Guilde représentent l’histoire permanente et le prestige de la Guilde. Ils progressent automatiquement à partir des actions normales des membres et ne doivent pas devenir une checklist artificielle. La Guilde possède son propre score de points et ses propres Tours de force, sans complétion globale ni leaderboard général.

Seules les actions réalisées pendant l’appartenance d’un joueur contribuent aux Hauts Faits de sa Guilde actuelle. Un départ ne transfère aucun accomplissement, point, Tour de force ou historique collectif. Un nouveau membre peut consulter l’histoire déjà acquise sans en devenir personnellement propriétaire.

Une récompense de Haut Fait de Guilde appartient à la Guilde et non à ses membres. Lorsqu’elle nécessite une récupération, elle apparaît dans le centre de récompenses du Chef, identifiée comme propriété de la Guilde ; le Chef la récupère au nom de celle-ci. La fiche publique de la Guilde permet de consulter ses points, Hauts Faits, Tours de force, compteur de Tours de force et dates.

La structure commune, les catégories, les récompenses éventuelles et la consultation de ces accomplissements sont définies dans [`19-ACHIEVEMENTS.md`](./19-ACHIEVEMENTS.md). Le présent document ne valide aucune liste exhaustive ni aucune récompense précise.

### 10.2. Quêtes saisonnières de Guilde

Une Saison peut proposer des quêtes saisonnières collectives propres aux Guildes. Elles :

* restent disponibles pendant la Saison concernée ;
* sont légères, accessibles et non contraignantes ;
* ne constituent ni une rotation hebdomadaire, ni une checklist permanente ;
* ne recréent pas un système général de quêtes quotidiennes ou hebdomadaires de Guilde.

Leur cadre saisonnier commun appartient à [`16-SEASONS.md`](./16-SEASONS.md) et leur fonctionnement comme quêtes à [`18-QUESTS.md`](./18-QUESTS.md). Les objectifs et récompenses concrets relèvent du content design.

### 10.3. Boss de Guilde

Le Boss de Guilde constitue le mode compétitif saisonnier principal des Guildes. Son fonctionnement propre est défini dans les sections suivantes.

### 10.4. Expédition de Guilde

L’Expédition est une activité coopérative, asynchrone, permanente et non compétitive, distincte du Boss de Guilde. Son fonctionnement est défini à partir de la section 18.

### 10.5. Demandes et dons de composants

Les Guildes proposent un mécanisme simple d’entraide permettant aux membres éligibles de demander et donner certains composants de fabrication. Il ne constitue ni un marché, ni un commerce, ni un troc. Son fonctionnement est défini à la section 24.

### 10.6. Absence de quêtes hebdomadaires dédiées

Un système distinct de quêtes hebdomadaires de Guilde n’est pas retenu actuellement. Les Hauts Faits, quêtes saisonnières et véritables activités de Guilde doivent structurer l’activité collective sans ajouter artificiellement une nouvelle checklist régulière.

Les quêtes hebdomadaires générales du compte restent disponibles selon [`18-QUESTS.md`](./18-QUESTS.md), mais ne deviennent pas pour autant des objectifs collectifs de Guilde.

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

Le Boss de Guilde utilise la Saison globale commune définie dans [`16-SEASONS.md`](./16-SEASONS.md). Pendant cette Saison, son identité générale, ses éléments, ses Skills, ses mécaniques et ses éventuels modificateurs restent stables.

Une Saison ultérieure peut renouveler fortement ce contenu avec un autre Boss ou une nouvelle version : Skills, phases, mécaniques, comportements et identité visuelle ou narrative peuvent différer. Un ancien Boss peut revenir en conservant une partie de son identité ou de ses mécaniques tout en recevant des modifications, voire une légère évolution de son lore local. Cette règle ne s’étend pas automatiquement aux autres catégories de Boss.

Toutes les Guildes commencent la Saison au Boss niveau 1. Lorsqu’un niveau est validé, le niveau suivant devient le niveau actuel de la Guilde. Cette progression ne possède aucune limite théorique prédéfinie et est réinitialisée à la nouvelle Saison selon le cadre de [`16-SEASONS.md`](./16-SEASONS.md).

Le Boss de Guilde est fermé pendant l’inter-saison. Son classement final est figé à la clôture et aucune nouvelle tentative n’est lancée avant la Saison suivante.

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

Lorsque cela est pertinent, certaines de ces récompenses personnelles de progression peuvent inclure une petite quantité de ressource générale d’invocation. Cette possibilité n’impose pas cette ressource à chaque palier.

Le contenu, la fréquence et les quantités exactes restent à définir. Les exemples de récompenses ou de fréquences envisagés pendant le cadrage restent illustratifs et ne constituent aucune règle obligatoire.

### 17.2. Récompenses de classement final

Les récompenses principales du classement final appartiennent de préférence à la Guilde et soutiennent son prestige collectif. Les paquets cosmétiques et autres récompenses directes du mode peuvent rester portés par le Boss de Guilde, tandis qu’une récompense spécifiquement liée au prestige d’un accomplissement peut être portée par le Haut Fait ou le Tour de force correspondant.

Une performance saisonnière importante peut valider un Haut Fait de Guilde temporaire à `0` point. À la clôture, il devient un Tour de force de Guilde s’il a été obtenu et conserve son résultat final et sa date ; s’il a été manqué, il disparaît. Les Tours de force portent la mémoire durable des résultats pertinents sans exiger un historique séparé de toutes les anciennes Saisons.

Aucune récompense de classement ne doit fournir de puissance exclusive ou obligatoire.

Le classement final saisonnier du Boss de Guilde ne distribue jamais de ressource générale d’invocation, d’invocations de créatures ni d’énergie générale. Ses récompenses privilégient le prestige collectif de la Guilde, les Hauts Faits, les titres, les personnalisations et les éléments cosmétiques.

### 17.3. Récupération manuelle

Lorsqu’une récompense du Boss de Guilde est configurée pour une récupération manuelle, elle est actuellement temporelle et suit les règles transversales de [`10-PROGRESSION.md`](./10-PROGRESSION.md). Sa fenêtre normale correspond à l’inter-saison, soit environ sept jours, tandis que sa durée exacte reste ajustable. Cette règle locale ne rend pas toutes les autres récompenses du jeu temporelles.

## 18. Expéditions — identité et régulation

Une Expédition représente l’exploration collective progressive d’un lieu. Elle repose principalement sur :

* l’exploration et la découverte ;
* des missions, tâches, puzzles et choix ;
* l’observation, la logique et l’utilisation d’indices ;
* le lore du lieu et ses secrets ;
* l’utilisation éventuelle de la collection de créatures.

L’Expédition est :

* coopérative et asynchrone ;
* permanente et sans durée globale ;
* non compétitive et sans classement entre Guildes ;
* indépendante des Saisons, sans reset saisonnier ;
* non répétable et non conçue pour le farming ;
* jouable sans combat obligatoire.

Elle reste distincte du Boss de Guilde, du World Boss, de la Tour infinie et des modes PvE classiques. Un contenu peut exceptionnellement employer un combat si son design le justifie, mais le combat n’est pas la mécanique centrale de l’Expédition.

L’Expédition n’utilise ni énergie générale, ni énergie propre, ni ticket, ni clé, ni monnaie spéciale d’entrée. Sa régulation repose sur la contribution quotidienne des membres.

## 19. Contribution quotidienne et tâche active

Chaque membre éligible peut commencer au maximum **une nouvelle tâche d’Expédition par jour**. Cette possibilité n’est ni une monnaie ni une ressource stockable : une contribution inutilisée ne s’accumule jamais.

Un joueur ne peut posséder qu’une seule tâche d’Expédition active à la fois. Une tâche peut durer plusieurs jours et ne possède aucune limite de durée individuelle par défaut. Tant qu’elle reste active :

* le joueur ne peut pas en sélectionner une autre ;
* aucune nouvelle contribution quotidienne ne lui est accordée ;
* les jours écoulés ne créent aucune contribution en réserve.

Après une réussite, un abandon ou un échec définitif, le joueur ne peut commencer une nouvelle tâche qu’à partir du lendemain.

### 19.1. Résolution et libération

En cas de réussite :

* la contribution est validée ;
* la progression, les découvertes et les déblocages correspondants sont appliqués ;
* la réservation est levée et la tâche est marquée comme terminée.

En cas d’abandon :

* aucune contribution n’est validée ;
* la tâche est libérée pour les autres membres ;
* le joueur attend le lendemain avant une nouvelle sélection.

Si le détenteur d’une tâche devient inactif selon la future définition transversale de compte ou membre actif, sa tâche est automatiquement libérée sans valider de contribution. Le délai exact d’inactivité n’est pas défini ici.

La contribution quotidienne est unique à l’échelle de toutes les Expéditions accessibles : elle peut être utilisée dans l’Expédition principale ou dans le contenu facultatif restant d’une ancienne Expédition terminée, mais pas dans les deux le même jour.

## 20. Zones, missions et découvertes

Une Expédition comporte plusieurs zones, chacune pouvant réunir des missions principales, facultatives ou secrètes et leurs tâches.

Les zones ne forment pas une suite linéaire obligatoire. Dès le lancement, un grand nombre de missions doit être disponible simultanément dans plusieurs zones afin que les membres puissent contribuer en parallèle et choisir librement où agir.

Une zone organise notamment une partie du lieu, son identité visuelle, ses missions, ses découvertes, son lore, ses énigmes et ses secrets. Elle n’est pas automatiquement plus difficile ou plus avancée qu’une autre.

### 20.1. Dépendances entre missions

Une mission peut :

* en débloquer une autre ;
* révéler une nouvelle zone ;
* fournir un indice utile ailleurs ;
* dépendre de plusieurs missions ;
* rester accessible avant que tous les indices utiles aient été trouvés.

Toutes les dépendances ne sont donc pas des verrous techniques. Une mission peut être disponible tout en étant plus difficile à résoudre sans les informations découvertes ailleurs.

### 20.2. Lore et informations découvertes

Il n’existe aucun Journal d’Expédition séparé. Le lore, les découvertes, les indices validés et les informations débloquées restent consultables directement dans les zones, missions et contenus de l’Expédition.

Les informations importantes nécessaires à la résolution doivent pouvoir être découvertes dans l’Expédition elle-même. Le système ne doit pas réduire son identité à des questionnaires exigeant des connaissances extérieures au contenu exploré.

Les informations apprises uniquement par essais et erreurs ne sont pas nécessairement enregistrées automatiquement comme découvertes officielles. Les membres pourront les partager naturellement grâce au futur chat de Guilde, sans que le présent document définisse ce système de communication.

## 21. Missions, tâches et tentatives

Une mission peut comporter une seule tâche, plusieurs tâches parallèles ou successives, ainsi que des tâches dépendantes les unes des autres.

Lorsqu’un joueur sélectionne une tâche :

* cette instance lui est réservée ;
* aucun autre membre ne peut l’accomplir en parallèle ;
* les autres tâches disponibles restent accessibles.

La réservation prend fin après une réussite, un abandon, un échec définitif ou l’inactivité du détenteur. Une réussite termine la tâche ; dans les trois autres cas, elle redevient disponible pour les autres membres.

### 21.1. Mécaniques réutilisables

Le système doit proposer un catalogue de mécaniques génériques réutilisables, ensuite habillées selon le lieu et le contexte de chaque Expédition. Il peut notamment prendre en charge l’observation, la recherche dans une illustration, la logique, les puzzles, les séquences, les symboles, les questionnaires, les choix, l’enquête, la déduction, l’utilisation d’indices ou la sélection de créatures.

Ces familles sont des exemples de capacités du système, pas une liste obligatoire de tâches à produire pour chaque Expédition. Les mécaniques et contenus concrets relèvent du content design.

Certaines tâches peuvent exploiter la collection sans combat, par exemple en demandant une créature satisfaisant une condition d’élément, de caractéristique ou de Skill. Les conditions doivent généralement accepter plusieurs solutions et éviter d’exiger une créature ultra-spécifique ou rare précise qui bloquerait artificiellement les joueurs.

### 21.2. Tentatives

Chaque tâche définit individuellement son nombre de tentatives, qui peut être limité ou illimité. Cette information doit être clairement affichée avant que le joueur sélectionne la tâche.

Lorsqu’une tentative échoue :

* elle est consommée ;
* la tâche reste active s’il reste des tentatives ;
* le joueur peut réessayer ultérieurement.

Lorsque toutes les tentatives sont consommées :

* la tâche échoue pour ce joueur ;
* elle est automatiquement libérée pour les autres membres ;
* aucune contribution n’est validée ;
* le joueur attend le lendemain avant de sélectionner une nouvelle tâche.

Une tâche à tentatives illimitées reste active jusqu’à sa réussite, son abandon ou sa libération pour inactivité.

## 22. Progression, complétion et catalogue

Une Expédition est officiellement terminée lorsque toutes les missions principales de toutes ses zones sont terminées. Elle ne nécessite ni zone finale, ni mission finale unique, ni Boss final.

Les missions facultatives, secrets, zones secrètes, énigmes secondaires et autres contenus supplémentaires ne sont pas requis pour cette fin principale. Ils peuvent alimenter le lore, les Hauts Faits, le prestige, des récompenses adaptées et la complétion totale.

Une Expédition atteint 100 % lorsque tout le contenu comptabilisé est accompli. Elle peut donc être terminée sans être complétée à 100 %.

Une fois les missions principales terminées :

* la Guilde conserve cette Expédition comme terminée ;
* le Chef peut lancer une nouvelle Expédition principale ;
* les contenus facultatifs restants demeurent accessibles ;
* les membres peuvent continuer à y consacrer leur contribution quotidienne unique.

### 22.1. Catalogue et choix du Chef

Toutes les Expéditions publiées et disponibles apparaissent dans un catalogue sans ordre imposé, arbre de progression, prérequis entre Expéditions, coût, clé, monnaie d’entrée ou niveau de Guilde requis.

Le Chef choisit librement quelle Expédition non terminée devient l’unique Expédition principale active. Une fois lancée, elle le reste jusqu’à la fin de toutes ses missions principales et ne peut pas être remplacée librement en cours de route.

Une Expédition terminée à 100 % reste consultable avec son lore, ses découvertes et son historique, mais ne peut être recommencée ni farmée. Si la Guilde termine toutes les Expéditions disponibles à 100 %, elle attend simplement l’ajout futur de nouveaux contenus, sans reset, mode infini ou répétition artificielle.

## 23. Récompenses et états des Expéditions

Une petite tâche n’accorde pas nécessairement de récompense matérielle personnelle. Sa contribution peut uniquement produire une progression, un indice, une découverte, du lore, une nouvelle mission ou une nouvelle zone.

La fin principale peut générer une récompense personnelle unique contenant notamment de la monnaie générale, des composants généraux, une petite quantité de ressource générale d’invocation ou d’énergie générale, d’autres ressources de progression déjà disponibles ailleurs, des éléments thématiques, des cosmétiques ou des éléments de collection. Ces ressources constituent des récompenses possibles et non un contenu obligatoire de chaque Expédition. Les contenus, quantités et valeurs exacts restent à définir.

La complétion à 100 % soutient principalement les Hauts Faits, le prestige, l’historique, les titres, la personnalisation de Guilde et les récompenses cosmétiques ou symboliques. Une récompense personnelle supplémentaire reste possible mais n’est pas obligatoire.

### 23.1. État de Guilde et état personnel

La Guilde conserve durablement :

* les Expéditions terminées ;
* leur pourcentage de complétion ;
* leurs découvertes, secrets et accomplissements.

Chaque compte conserve séparément l’information indiquant si la récompense personnelle de chaque Expédition a déjà été récupérée. Changer de Guilde ne remet jamais cet historique personnel à zéro.

La récompense principale d’une Expédition ne peut être obtenue qu’une seule fois par compte. Une autre Guilde ne peut pas la générer une deuxième fois pour un joueur qui l’a déjà récupérée.

### 23.2. Récompense permanente mais conditionnelle

La récompense personnelle principale d’une Expédition est permanente mais conditionnelle. Pour la récupérer, le joueur doit :

* ne jamais l’avoir récupérée auparavant ;
* appartenir actuellement à une Guilde ;
* être devenu membre éligible dans cette Guilde ;
* appartenir à une Guilde ayant terminé l’Expédition concernée.

La référence actuelle d’ancienneté reste d’environ sept jours, valeur ajustable. Lorsqu’un joueur devient éligible dans une Guilde avancée, les récompenses des Expéditions qu’elle a déjà terminées peuvent donc devenir récupérables s’il ne les a jamais obtenues.

Si le joueur quitte sa Guilde avant de récupérer une récompense d’Expédition, il perd immédiatement son éligibilité actuelle. La récompense disparaît du centre de récompenses sans apparaître grisée, verrouillée ou inactive, mais elle n’est pas considérée comme obtenue.

Elle peut réapparaître si le joueur rejoint plus tard une autre Guilde ayant terminé cette Expédition et y redevient éligible. Les catégories de disponibilité et les conditions générales d’éligibilité appartiennent à [`10-PROGRESSION.md`](./10-PROGRESSION.md).

## 24. Demandes et dons de composants

Le système d’entraide permet aux membres éligibles de demander et donner volontairement certains composants de fabrication. Il ne constitue ni un marché, ni un commerce, ni un échange avec contrepartie, ni un troc.

Les demandes utilisent une interface dédiée plutôt que le chat de Guilde. Celui-ci peut servir à en discuter, mais ne porte pas leur fonctionnement.

Un membre éligible peut publier **une demande par jour**, portant sur un seul type de composant. Chaque composant autorisé possède son propre paramètre interne de quantité maximale demandable quotidiennement ; aucune limite globale identique n’est imposée à tous les composants.

Seuls les composants de fabrication explicitement autorisés sont demandables. Sont notamment exclus :

* les Sources d’énergie ;
* les équipements complets ;
* les monnaies générales ou premium ;
* toute autre catégorie non explicitement autorisée.

Plusieurs membres peuvent compléter une même demande. Le donateur ne reçoit aucune contrepartie, monnaie, XP, point de Guilde, progression dédiée ou récompense spécifique.

Une demande reste active jusqu’à sa complétion ou jusqu’au reset quotidien suivant. Lorsqu’elle disparaît au reset, les composants déjà reçus restent définitivement acquis au demandeur et ne sont pas remboursés aux donateurs.

Aucune limite supplémentaire propre au donateur n’est actuellement validée. Les protections reposent sur l’éligibilité, la demande quotidienne, la quantité maximale définie par composant et les quantités réellement possédées. Un garde-fou supplémentaire ne devra être ajouté que si les tests révèlent un besoin réel.

## 25. Frontières documentaires

Le Boss de Guilde reste le mode compétitif saisonnier principal des Guildes. Ses règles internes appartiennent au présent document, tandis que [`16-SEASONS.md`](./16-SEASONS.md) porte la Saison globale, l’inter-saison et les règles communes. Les quêtes saisonnières de Guilde sont cadrées transversalement avec [`18-QUESTS.md`](./18-QUESTS.md).

Les Expéditions sont permanentes : elles ne reset pas, n’expirent pas, ne dépendent d’aucun classement saisonnier et ne possèdent aucun chrono global.

[`19-ACHIEVEMENTS.md`](./19-ACHIEVEMENTS.md) définit le système commun des Hauts Faits, notamment ceux pouvant exploiter les Expéditions terminées, leur complétion à 100 % et leurs secrets. Le présent document conserve uniquement les accomplissements de Guilde susceptibles de les alimenter.

Le futur `21-SOCIAL_AND_COMMUNICATION.md`, prévu mais non créé, portera le chat de Guilde et les autres règles sociales ou de communication. Les Expéditions peuvent utiliser ce futur chat pour partager indices, pistes, erreurs et découvertes sans définir ici son fonctionnement.

[`08-ITEMS.md`](./08-ITEMS.md) porte les catégories d’objets et composants pouvant entrer dans le système d’entraide. [`10-PROGRESSION.md`](./10-PROGRESSION.md) porte les règles transversales de disponibilité et d’éligibilité des récompenses. [`20-UI_FLOW.md`](./20-UI_FLOW.md) traduit les besoins fonctionnels des Guildes, Expéditions, demandes et récompenses sans fixer leur layout final.

## 26. Dépendances documentaires

| Document | Responsabilité liée |
| --- | --- |
| [`01-GAME_DESIGN_DOCUMENT.md`](./01-GAME_DESIGN_DOCUMENT.md) | Place des Guildes dans l’expérience de long terme |
| [`02-COMBAT.md`](./02-COMBAT.md) | Moteur standard utilisé par le Boss de Guilde |
| [`08-ITEMS.md`](./08-ITEMS.md) | Composants de fabrication demandables et catégories explicitement exclues |
| [`09-GACHA.md`](./09-GACHA.md) | Ressource générale d’invocation utilisée dans certaines récompenses personnelles |
| [`10-PROGRESSION.md`](./10-PROGRESSION.md) | Énergie générale, disponibilité et éligibilité des récompenses |
| [`11-COLLECTION.md`](./11-COLLECTION.md) | Collection de créatures éventuellement sollicitée par certaines tâches |
| [`12-MODES.md`](./12-MODES.md) | Contrats transversaux des modes et résultats |
| [`13-PVE.md`](./13-PVE.md) | Distinction avec les Boss personnels, le World Boss et la Tour infinie |
| [`16-SEASONS.md`](./16-SEASONS.md) | Cadre transversal des Saisons et objectifs saisonniers |
| [`18-QUESTS.md`](./18-QUESTS.md) | Quêtes saisonnières collectives distinctes des activités permanentes |
| [`19-ACHIEVEMENTS.md`](./19-ACHIEVEMENTS.md) | Points, Tours de force, récompenses et historique des Hauts Faits de Guilde |
| [`20-UI_FLOW.md`](./20-UI_FLOW.md) | Parcours de Guilde, Boss, Expéditions, demandes et centre de récompenses |
| [`04-MONETIZATION.md`](../00-foundation/04-MONETIZATION.md) | Garde-fous économiques et récompenses cosmétiques |
| [`01-LORE.md`](../02-world/01-LORE.md) | Frontière entre Guildes fonctionnelles, contenu d’Expédition et canon narratif |
| [`03-FORCES_PEOPLES_AND_FACTIONS.md`](../02-world/03-FORCES_PEOPLES_AND_FACTIONS.md) | Absence de faction obligatoire pour le joueur |

Le futur `21-SOCIAL_AND_COMMUNICATION.md` devra prendre en charge les fonctions sociales et de communication communes.

## 27. Éléments à préciser ultérieurement

* Le jalon exact de déblocage du système de Guildes.
* Le coût exact de création.
* La longueur maximale du nom.
* La durée d’expiration des invitations.
* La définition transversale exacte de compte actif ou membre actif.
* La durée définitive avant transfert automatique du Chef.
* La durée définitive avant éligibilité d’un nouveau membre aux systèmes de Guilde.
* Le coût exact en énergie des tentatives du Boss de Guilde.
* Les courbes, coefficients et paliers mécaniques de difficulté du Boss.
* Les paliers de récompense du Boss, leur fréquence, leur contenu, les quantités éventuelles de ressource générale d’invocation et leur équilibrage.
* Les récompenses honorifiques ou cosmétiques exactes du classement final.
* La durée exacte des récompenses temporelles concernées.
* Les protections anti-abus détaillées.
* Les Hauts Faits concrets de Guilde et d’Expédition, leurs valeurs, seuils et récompenses précises.
* Le fonctionnement du système Social / Communication.
* Le nombre moyen de zones, missions et tâches des Expéditions.
* Le catalogue concret des mini-mécaniques et le contenu de chaque Expédition.
* Le nombre de tentatives défini par chaque tâche concrète.
* Les récompenses exactes des Expéditions, dont les quantités éventuelles de ressource générale d’invocation, et de leur complétion à 100 %.
* La liste définitive des composants demandables et la limite propre à chacun.
* Les éventuels garde-fous économiques supplémentaires révélés par les tests.
* Les détails finaux d’interface et de présentation.
* Les autres activités de Guilde éventuelles.

Ces éléments relèvent du balancing, du content design, des futurs référentiels spécialisés ou de la passe globale finale des Game Design Documents. Ils ne remettent pas en cause la clôture fonctionnelle actuelle du système de Guildes.
