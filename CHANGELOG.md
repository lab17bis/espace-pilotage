# Journal des modifications

Les fichiers publiés ne sont jamais retirés : chaque version ajoute ou corrige, sans casser l'existant.

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
