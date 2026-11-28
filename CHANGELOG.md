# Journal des modifications

Les fichiers publiés ne sont jamais retirés : chaque version ajoute ou corrige, sans casser l'existant.

## 2026-11-28 (management à deux niveaux)
- Documentation : le widget grist-management propose maintenant deux niveaux, **Équipe** (priorités et points chauds, signalements de l'équipe, charge vécue facultative) et **Pilotage** (escalades, arbitrages, tension de charge de chaque équipe), avec des règles d'accès par équipe. Il est lu à l'adresse stable `/v1/` : rien à réimporter, les fichiers `.grist` sont inchangés. Les tables nécessaires s'ajoutent depuis *Réglages › Deux niveaux* du widget.

## 2026-11-28 (noms des éditeurs)
- Les pages de réglage s'appellent désormais « Éditeur des indicateurs », « Éditeur des ressources », « Éditeur de l'offre de service », « Éditeur du questionnaire » (au lieu de « Régler … » et « Concevoir le questionnaire »), et chaque vue de configuration a pour titre « Éditeur du widget ». Fichiers .grist (vide et exemple) et README mis à jour ; aucune table ni aucun réglage ne change.

## 2026-11-26 (correctifs des widgets)

### Corrigé
- Correctifs des widgets utilisés par cet espace, pris en compte sans rien réinstaller (rechargez la page) :
  - grist-management : dans la version `/v1/`, les tableaux de bord de grist-graphique ne se chargeaient plus (erreur 404 sur ses modules) ;
  - grist-projet : le filtre « État » de la banque et la liste « État » du formulaire de projet étaient masqués ;
  - style commun de configuration (grist-annuaire, grist-consultation, grist-graphe, grist-management, grist-projet, grist-reunion) : il ne masque plus que le badge « Enregistré » sur l'onglet de l'outil.

### Ajouté
- Brancher un outil sur un document qui a déjà ses propres tables (grist-management, grist-reunion, grist-projet, grist-consultation, grist-graphe, grist-annuaire) : si une table du même nom existe sans toutes les colonnes attendues, l'outil le signale et propose de les ajouter, avec le conseil de renommer d'abord une colonne qui porte la même information sous un autre nom. Rien à refaire dans cet espace : ses tables sont complètes.

## 2026-11-26 (suivi de projets et réunions)

### Modifié
- Fichiers `.grist` (vide et exemple) : la table `Reunions` a maintenant les colonnes `Projet` et `Notes`, donc l'onglet « Rendez-vous » de grist-projet fonctionne dès l'import, sans bouton à activer. Aucune autre table ni règle d'accès modifiée ; un document déjà importé n'est pas touché (le bouton « Activer l'onglet Rendez-vous » de grist-projet fait la même chose).
- Documentation : le widget grist-projet permet maintenant de choisir les champs affichés sur les cartes et les filtres de la banque, de reprendre une colonne déjà présente dans la table `Projets`, et d'ouvrir un onglet « Rendez-vous » sur la fiche d'un projet (Réglages > Rendez-vous, qui ajoute `Projet` et `Notes` à la table `Reunions`). Le widget grist-reunion propose alors « Projet lié » et « Notes ». Les widgets sont chargés par leur adresse : rien à réimporter, le fichier `.grist` est inchangé.

## 2026-11-26 (questionnaire enrichi)

### Modifié
- Documentation : le widget grist-questionnaire sait maintenant classer par ordre (glisser-déposer), proposer un tableau de choix, un choix « Autre », des bornes de choix, une réponse par défaut, un ordre aléatoire, des types lien, heure et date et heure, et intégrer image, son, vidéo et PDF. Ces options sont facultatives et déjà disponibles dans cet espace (le widget est lu à l'adresse stable `/v1/`). Aucun changement dans les fichiers `.grist`.

## 2026-11-25 (annuaire)

### Ajouté
- Page **Annuaire** ([grist-annuaire](https://github.com/lab17bis/grist-annuaire)) : recherche des personnes et des structures, fiches, doublons et fusion, import CSV, archivage et délai de conservation.
- Colonnes ajoutées aux tables existantes, sans rien renommer ni supprimer : `Personnes` (archivage, fusion, rôle gestionnaire de l'annuaire, réglages) et `Structures` (courriel, site, adresse si absente).
- Règles d'accès de l'annuaire : rôle « gestionnaire de l'annuaire », et aucune personne visible d'un visiteur anonyme.

## 2026-11-24

### Modifié
- Documentation : l'outil de consultation s'appelle désormais `grist-consultation` (ancien nom `grist-decision`).
- Les fichiers `.grist` à importer pointent vers `lab17bis.github.io/grist-consultation/v1/` (ancienne adresse `grist-decision`).
