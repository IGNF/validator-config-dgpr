# validator-config-dgpr

[![License: AGPL-3.0](https://img.shields.io/badge/License-AGPL--3.0-blue.svg)](LICENSE)
[![Site](https://github.com/IGNF/validator-config-dgpr/actions/workflows/pages.yml/badge.svg)](https://ignf.github.io/validator-config-dgpr/)

Configuration de [IGNF/validator](https://github.com/IGNF/validator) pour la validation des standards DGPR au niveau du [Validateur](https://demo-validator.ign.fr).

---

## Consulter les modèles

Un démonstrateur interactif est disponible pour parcourir l'ensemble des modèles :
**[validator-config-dgpr](https://ignf.github.io/validator-config-dgpr/)**

---

## Utiliser les modèles

URL du modèle (Utilisé par l'[API de validation](https://demo-validator.ign.fr) : 

> https://ignf.github.io/validator-config-dgpr/config/<modèle>/files.json 


Exemple d'utilisation en ligne de commande (CLI) :

```bash
  java -jar validator-cli.jar document_validator \
    --model https://ignf.github.io/validator-config-dgpr/config/DREAL_canalTMD_2025/files.json \
    --input <dossier_du_document> ...
```

---

## Organisation du dépôt

```
config/
├── variables.json           # Variables d'affichage des regex (<MAILLAGE>, <YYYYMMDD>...)
└── <modèle>/
    ├── files.json           # Document (fichiers attendus, contraintes de nommage, métadonnées)
    ├── types/<TABLE>.json   # Colonnes et contraintes de chaque table
    └── codes/               # Tables de codes
```

---

## Modifier les modèles

Les fichiers du dossier config/ ne doivent pas être modifiés à la main. Utilisez l'éditeur dédié : **[IGNF/validator-config-editor](https://github.com/IGNF/validator-config-editor/)**.
