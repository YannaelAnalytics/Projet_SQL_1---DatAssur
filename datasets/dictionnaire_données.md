## 📘 Dictionnaire de données

### Table : `Contrat`

| Champ                     | Type | Taille | Contrainte   |Description                                                                       |
|---------------------------|------|--------|--------------|----------------------------------------------------------------------------------|
| `Contrat_ID`              | CHAR | 10     | Clé Primaire | Identifiant unique du contrat                                                    |
| `No_voie`                 | INT  | 10     |              | Numéro dans la voie pour l'adresse du logement assuré                            |
| `B_T_Q`                   | CHAR | 10     |              | Indicateur éventuel de répétition pour l'adresse du logement assuré              |
| `Type_de_voie`            | CHAR | 10     |              | Type de voie pour l'adresse du logement assuré: rue, av (Avenue), rte (Route), … |
| `Voie`                    | CHAR | 50     |              | Libellé de la voie pour l'adresse du logement assuré                             |
| `Code_postal`             | CHAR | 10     |              | Code postal pour l'adresse du logement assuré                                    |
| `Commune`                 | CHAR | 25     |              | Libellé de la commune de l'adresse du logement                                   |
| `Code_departement`        | CHAR | 10     |              | Code du departement pour l'adresse du logement                                   |
| `Surface`                 | INT  | 10     |              | Surface du logement                                                              |
| `Type_local`              | CHAR | 25     |              | Type de logement (Maison, Appartement)                                           |
| `Occupation`              | CHAR | 15     |              | Type d'occupation (Locataire ou Propriétaire)                                    |
| `Type_contrat`            | CHAR | 25     |              | Type de contrat (Residence principale, secondaire ou mise en location)           |
| `Formule`                 | CHAR | 10     |              | Type de formule choisi par l'assuré (Integral ou Classique)                      |
| `Valeur_declare_mobilier` | CHAR | 25     |              | Montant biens déclarés par l'assuré                                              |
| `Prix_cotisation_mensuel` | INT  | 10     |              | Montant cotisation mensuelle client                                              |

---

### Table : `Region`

| Champ         | Type | Taille | Contrainte   | Description                                                               |
|---------------|------|--------|--------------|---------------------------------------------------------------------------|
| `code_postal` | CHAR | 10     | Clé Primaire | Code commune (referentiel-geographique-francais, source www.data.gouv.fr) |
| `reg_code`    | CHAR | 10     |              | Code Région                                                               |
| `reg_nom`     | CHAR | 25     |              | Libellé région                                                            |
| `aca_nom`     | CHAR | 25     |              | Libellé de l'académie                                                     |
| `dep_nom`     | CHAR | 25     |              | Libellé du département                                                    |
| `com_nom_maj` | CHAR | 25     |              | Libellé de la commune en majuscule                                        |
| `dep_code`    | CHAR | 10     |              | Code département                                                          |
| `dep_nom_num` | CHAR | 25     |              | Libellé du département et code                                            |
