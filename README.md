# espace-pilotage

> **Espace Grist clé en main.** Un document Grist prêt à l'emploi pour **piloter une équipe** : un écran de management visuel, les réunions, les projets et un tableau de bord d'indicateurs, reliés entre eux et au Système de design de l'État (DSFR).

Un **espace** est un document Grist complet — tables, formules, pages, widgets et réglages — à importer en une fois. Il assemble des widgets de la famille `grist-…` autour d'une manière de travailler. Chaque widget reste utilisable seul.

## À quoi ça sert

- **Voir d'un coup d'œil** où en est l'équipe : météo du jour, problèmes signalés et escaladés, actions en retard, prochaine réunion, projets à relancer.
- **Se réunir** avec un ordre du jour préparé par l'équipe, des notes, des décisions et un relevé d'actions.
- **Piloter les projets** de l'équipe avec leur plan d'action et leur journal.
- **Mesurer** avec des indicateurs à seuils d'alerte, calculés sur les données du document.
- **Afficher** l'écran de management en grand, en mode affichage, pour le point quotidien.
- **Prioriser ensemble** : l'équipe répartit des points entre les chantiers proposés, le classement éclaire le choix des projets.
- **Voir les parties prenantes** de chaque projet : structures, porteurs et équipes reliés dans un graphe, et la position de chaque structure selon son influence et son intérêt.

## Ce que contient l'espace

| Page | Outil | Contenu |
| --- | --- | --- |
| **Management visuel** | [grist-management](https://github.com/lab17bis/grist-management) | Écran d'équipe : chiffres clés, météo, signalements, actions, prochaine réunion. Tables `Meteo` et `Signalements`. |
| **Réunions** | [grist-reunion](https://github.com/lab17bis/grist-reunion) | Ordre du jour, séance, compte rendu, suivi des actions. Tables `Reunions`, `Points`, `Decisions`, `Actions_reunion`. |
| **Priorités** | [grist-decision](https://github.com/lab17bis/grist-decision) | Consultation de l'équipe en vote par points pour classer les chantiers. Tables `Consultations`, `Propositions`, `Criteres`, `Votes`, `Votants`. |
| **Indicateurs** | [grist-graphique](https://github.com/lab17bis/grist-graphique) | Tableau de bord d'indicateurs. Page *Régler les indicateurs* pour le modifier. |
| **Projets** | [grist-projet](https://github.com/lab17bis/grist-projet) | Banque de projets, fiches projet, plans d'action, journal et règles d'accès. Tables `Projets`, `Actions`, `Journal`, `Documents`, `Personnes`, `Structures`, `Comptes`, `Parametres`. |
| **Parties prenantes** | [grist-graphe](https://github.com/lab17bis/grist-graphe) | Graphe des projets, des structures et des personnes, reliés par les références des fiches projet (structure porteuse, porteurs, équipe, structures associées). Vue *Positions* selon les colonnes `Influence` et `Interet` des structures. |

## L'installer en 2 minutes

1. **Télécharger** le fichier de l'espace :
   - [`espace-pilotage.grist`](https://github.com/lab17bis/espace-pilotage/raw/main/espace-pilotage.grist) : l'espace vide, prêt à l'usage ;
   - [`espace-pilotage-exemple.grist`](https://github.com/lab17bis/espace-pilotage/raw/main/espace-pilotage-exemple.grist) : le même, rempli de données fictives, pour essayer.
2. **L'importer dans Grist** : depuis l'accueil de votre espace Grist, *Ajouter › Importer un document*, puis choisissez le fichier.
3. **L'ouvrir** : les pages et les widgets sont déjà en place. Si Grist le demande, confirmez l'accès complet des widgets au document.
4. **Inviter l'équipe** (*Partager*), en éditeur pour celles et ceux qui saisissent.

Vous êtes propriétaire du document importé. Rien n'est installé ailleurs : les widgets sont des pages web publiques, qui lisent et écrivent dans votre document avec les droits de la personne connectée.

Les widgets sont chargés depuis leur **adresse stable** (`…/v1/`) : une évolution d'un widget ne modifie pas votre espace sans que vous l'ayez décidé.

## Le régler

- **Management visuel** : bouton *Réglages* de l'écran (écrans et zones, rubriques de la météo, niveaux d'escalade, rotation de l'affichage).
- **Réunions** : lien *Réglages* en bas du widget (instances, types de points, états des actions).
- **Projets** : lien *Réglages du suivi* (listes, couleurs, en-tête et pied de page).
- **Priorités** : bouton *Nouvelle consultation*, puis onglet *Gérer* (mode de vote, points par personne, échéance, visibilité des résultats).
- **Parties prenantes** : bouton *Réglages* du graphe (tables d'acteurs, sources de liens) ; ajoutez une table `Liens` depuis le widget pour saisir des liens à la main.
- **Indicateurs** : page *Régler les indicateurs*.

Les réglages sont enregistrés dans le document. Ils partagent les mêmes réglages d'en-tête et de pied de page.

## Données et droits d'accès

Les votes de la page *Priorités* portent l'adresse de leur auteur, visible des propriétaires dans la table `Votes`. L'espace contient aussi les **règles d'accès** de grist-projet, qui protègent les projets restreints. Elles ne concernent que les tables de projets : les autres tables restent accessibles à tous les membres du document. Vérifiez-les dans *Permissions avancées* avant d'inviter l'équipe.

Les tables `Personnes` et `Structures`, quand l'espace en contient, suivent la règle commune des widgets : un widget de la famille ajouté plus tard les reprend et les complète, au lieu d'en créer d'autres.

Les fichiers de ce dépôt ne contiennent aucune donnée réelle. L'exemple est entièrement fictif.

## Widgets utilisés

- [grist-graphique](https://github.com/lab17bis/grist-graphique) : tableaux de bord et indicateurs à seuils au DSFR.
- [grist-projet](https://github.com/lab17bis/grist-projet) : banque de projets partagée et plans d'action.
- [grist-reunion](https://github.com/lab17bis/grist-reunion) : ordres du jour, notes, décisions, actions et comptes rendus.
- [grist-management](https://github.com/lab17bis/grist-management) : écran de management visuel : météo d'équipe, signalements, chiffres clés.
- [grist-decision](https://github.com/lab17bis/grist-decision) : consultations : boîte à idées, valorisation des réalisations, votes et suites données.
- [grist-graphe](https://github.com/lab17bis/grist-graphe) : cartographie des acteurs et de leurs liens, matrice influence / intérêt.

## Autres espaces

- [espace-collaboratif](https://github.com/lab17bis/espace-collaboratif) : faire ensemble : réunions, projets partagés, décisions collectives et ressources communes d'une équipe.
- [espace-accompagnement](https://github.com/lab17bis/espace-accompagnement) : suivre les personnes qui sollicitent un service : offre de service, sollicitations, fiches contact et satisfaction.
- [espace-sondage](https://github.com/lab17bis/espace-sondage) : concevoir un questionnaire, savoir qui a répondu et lire les résultats en indicateurs.
- [espace-reseau](https://github.com/lab17bis/espace-reseau) : animer un réseau ou une communauté de pratique : membres, groupes, rencontres, présences, ressources partagées, retours, carte et liens entre acteurs.
- [espace-contributions](https://github.com/lab17bis/espace-contributions) : faire participer : boîte à idées, valorisation des réalisations des équipes, votes et suites données.

## Écosystème

- **[Grist](https://grist.numerique.gouv.fr)** : tableur-base de données libre ([gristlabs/grist-core](https://github.com/gristlabs/grist-core)), proposé aux agents publics par la [DINUM](https://www.numerique.gouv.fr/) dans [La Suite numérique](https://lasuite.numerique.gouv.fr/). L'espace s'importe dans toute instance de Grist.
- **[Système de design de l'État (DSFR)](https://www.systeme-de-design.gouv.fr/)** ([GouvernementFR/dsfr](https://github.com/GouvernementFR/dsfr)). Son usage est réservé aux sites des services de l'État.

## Mots-clés

Grist, espace Grist, modèle Grist, document clé en main, management visuel, pilotage d'équipe, tableau de bord, indicateurs, météo d'équipe, réunion d'équipe, plan d'action, gestion de projet, priorisation, vote par points, parties prenantes, DSFR, Système de design de l'État, La Suite numérique, service public, logiciel libre.

## Licence

Fichiers de l'espace et documentation sous licence Creative Commons [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.fr) : réutilisation et adaptation autorisées, en citant la source et en partageant sous la même licence. Le code des widgets est sous licence MIT, dans leurs dépôts.

Conçu par le Lab 17 bis, laboratoire d'innovation publique de l'académie de Reims. Contact : <lab17bis@ac-reims.fr>
