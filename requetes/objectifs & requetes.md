## Requêtes du Projet

## 1) Lister les numéros de contrats (contrat_ID) avec leur surface pour la commune de Caen

```sql
SELECT Contrat_ID, Surface
FROM Contrat
WHERE Commune = "CAEN"```

## 2) Lister les numéros de contrat avec le type de contrat et leur formule pour les maisons du département de la Saône-et-Loire (Département 71)

```sql
SELECT Contrat_ID, Formule
FROM Contrat
WHERE Type_local = "Maison"
AND Code_departement = "71"```
