## 📘 Dictionnaire de données

### Table : `Contrat`

| Champ                 | Type          | Taille | Description                                      |
|-----------------------|-------------|--------|------------------------------------------|
| `Contrat_ID`          | CHAR        |        | Identifiant unique du client                    |
| `No_voie`             | INT     |        |Nom complet du client                           |
| `B_T_Q`               | CHAR            |        | Date de naissance du client                     |
| `Type_de_voie`        | CHAR           |        | Revenu annuel estimé (€)                        |
| `Voie`                    | CHAR            |        |Date du dernier achat réalisé                   |
| `Code_postal` | CHAR            |        | Date du dernier achat réalisé                   |
| `Commune` |     CHAR        |        |Date du dernier achat réalisé                   |
| `Code_departement` |    CHAR         |        |Date du dernier achat réalisé                   |
| `Surface` |   INT         |        |Date du dernier achat réalisé                   |
| `Type_local` |    CHAR    |               | Date du dernier achat réalisé                   |
| `Occupation` |     CHAR   | |Date du dernier achat réalisé                   |
| `Type_contrat` |   CHAR   | |Date du dernier achat réalisé                   |
| `Formule` |    CHAR       | |Date du dernier achat réalisé                   |
| `Valeur_declare_mobilier` | CHAR     | |Date du dernier achat réalisé                   |
| `Prix_cotisation_mensuel` |  INT    | |Date du dernier achat réalisé                   |

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
