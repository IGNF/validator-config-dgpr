# validator-config-dgpr

[![License: AGPL-3.0](https://img.shields.io/badge/License-AGPL--3.0-blue.svg)](LICENSE)

## Description

Dépôt de gestion de la configuration de [IGNF/validator](https://github.com/IGNF/validator) pour la validation des standards CNIG au niveau du [Validateur CNIG TRI](https://validateur-tri.ign.fr).

## Mises en garde

* Les schémas sont actuellement gérés avec un outil dédié travaillant sur le contenu `config-backup`.
* L'organisation de ce dépôt est amenée à évoluer.
* Les issues sont les bienvenues en cas de détection d'un problème.
* Les contributions directes sur ce dépôt (pull request) ne sont pas souhaitées dans l'immédiat.

## Principes de gestion des modèles

* Les méta-modèles sont gérés en base de données à l'aide de 4 tables :

  * [validator_document_model](config-backup/validator_document_model.csv) : Liste des standards modélisant le contenu des archives pour les PLU, POS, CC, PSMV, SUP et SCoT
  * [validator_file_model](config-backup/validator_file_model.csv) : Liste des fichiers attendus pour chaque standard
  * [validator_feature_type](config-backup/validator_feature_type.csv) : Modélisation des fichiers de type "table"
  * [validator_attribute_type](config-backup/validator_attribute_type.csv) : Modélisation des colonnes des tables
  * [validator_static_table](config-backup/validator_static_table.csv) : Liste des tables de codes (ex : [PrescriptionPSMVType2019](codes/PrescriptionPSMVType2019.csv))
