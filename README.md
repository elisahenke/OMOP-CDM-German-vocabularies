# OMOP-CDM-German-vocabularies

This folder contains semantic mappings of German vocabularies as CSV-files for use within OMOP CDM. 

The semantic mappings are separated in a) new 2-billion-concepts and b) mappings to standard-concepts.

## 2-billion-concepts

New 2-billion-concepts were created for the following missing German vocabularies in OMOP CDM:

- Ambulante Entgeltarten

- *Anatomisch-Therapeutisch-Chemische Klassifikation - German Modification (ATC-GM)

- Behandlungsart

- Einheitlicher Bewertungsmaßstab (EBM)

- Heilmittelkatalog (HMK)

- Bundeseinheitliches Heilmittelpositionsnummernverzeichnis (HPNR)

- Patient Clinical Complexity Level (PCCL)/Schweregrad

- Bundeseinheitlicher Katalog für die Dokumentation der Leistungen der psychiatrischen Institutsambulanzen (PIA)

- Stationäre Entgeltarten

*Datenquelle des amtlichen ATC-Index mit DDD-Angaben: GKV-Arzneimittelindex im Wissenschaftlichen Institut der AOK (WIdO), AOK Bundesverband GbR Stand 08.11.2023

For every vocabulary, imports are included for the OMOP CDM tables `vocabulary`, `concept_class`, `concept` and `concept_relationship`. 

:warning: Before importing the vocabularies into your OMOP CDM database, please check whether the concept_ids used in the imports are not yet assigned in the OMOP CDM database to be populated. If the concept_ids have already been used, the concept_ids in the csv files provided must be adjusted manually.

After checking, please use the imports provided in the following order:

1) *_concept_Metadata.csv
2) *_vocabulary.csv
3) *_concept_class.csv
4) *_concept.csv
5) *_concept_relationship.csv


## Mappings to standard-concepts

Mappings to standard-concepts were created with Usagi for the following missing German vocabularies in OMOP CDM:

- Fachabteilungsschlüssel

- Art der ambulanten Behandlung

- Art des Aufenthalts/der Behandlung

- Arztfachgruppen

- Ambulante spezialfachärztliche Versorgung (ASV; Erkrankungs- und Leistungsbereichsschlüssel nach § 166b SGB V)

- Aufnahmeanlass

- Aufnahmegrund

- Diagnoseart

- Diagnosesicherheit

- Entlass-/Verlegungsgrund

- Geschlecht

- Interpretation

- Kontakt Klasse

- Pflegegrad

- Pflegestufe

- Seitenlokalisation

For every vocabulary, imports are included for the OMOP CDM table `source_to_concept_map`.

The vocabulary _Fachabteilungsschlüssel_ (specialist department codes) is an exception. Imports for the `care_site` table are provided for this vocabulary.

:warning: Before importing the vocabularies into your OMOP CDM database, please check whether the `source_to_concept_map.source_vocabulary_id` or the `care_site.care_site_id` used in the imports are not yet assigned in the OMOP CDM database to be populated. If they have already been used, the `source_to_concept_map.source_vocabulary_id` or `care_site.care_site_id` in the csv files provided must be adjusted manually.