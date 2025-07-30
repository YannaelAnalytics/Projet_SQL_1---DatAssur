## 📘 Dictionnaire de données

### Table : `Contrat`

| Champ                     | Type | Taille | Description                                                                      |
|---------------------------|------|--------|----------------------------------------------------------------------------------|
| `Contrat_ID`              | CHAR | 10     | Identifiant unique du contrat                                                    |
| `No_voie`                 | INT  | 10     | Numéro dans la voie pour l'adresse du logement assuré                            |
| `B_T_Q`                   | CHAR | 10     | Indicateur éventuel de répétition pour l'adresse du logement assuré              |
| `Type_de_voie`            | CHAR | 10     | Type de voie pour l'adresse du logement assuré: rue, av (Avenue), rte (Route), … |
| `Voie`                    | CHAR | 50     | Libellé de la voie pour l'adresse du logement assuré                             |
| `Code_postal`             | CHAR | 10     | Code postal pour l'adresse du logement assuré                                    |
| `Commune`                 | CHAR | 25     | Libellé de la commune de l'adresse du logement                                   |
| `Code_departement`        | CHAR | 10     | Code du departement pour l'adresse du logement                                   |
| `Surface`                 | INT  | 10     | Surface du logement                                                              |
| `Type_local`              | CHAR | 25     | Type de logement (Maison, Appartement)                                           |
| `Occupation`              | CHAR | 15     | Type d'occupation (Locataire ou Propriétaire)                                    |
| `Type_contrat`            | CHAR | 25     | Type de contrat (Residence principale, secondaire ou mise en location)           |
| `Formule`                 | CHAR | 10     | Type de formule choisi par l'assuré (Integral ou Classique)                      |
| `Valeur_declare_mobilier` | CHAR | 25     | Montant biens déclarés par l'assuré                                              |
| `Prix_cotisation_mensuel` | INT  | 10     | Montant cotisation mensuelle client                                              |

---

### Table : `Region`

| Champ               | Type        | Description                                      |
|---------------------|-------------|--------------------------------------------------|
| `vente_id`          | INTEGER     | Identifiant unique de la vente                   |
| `client_id`         | INTEGER     | Identifiant du client (clé étrangère)            |
| `produit_id`        | INTEGER     | Identifiant du produit vendu                     |
| `date_vente`        | DATE        | Date de la vente                                 |
| `quantite`          | INTEGER     | Quantité vendue                                  |
| `prix_unitaire`     | DECIMAL     | Prix unitaire du produit (€)                     |
