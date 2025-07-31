## Requêtes du Projet

## 1) Lister les numéros de contrats (contrat_ID) avec leur surface pour la commune de Caen
```sql
SELECT Contrat_ID, Surface
FROM Contrat
WHERE Commune = "CAEN";
```

## 2) Lister les numéros de contrat avec le type de contrat et leur formule pour les maisons du département de la Saône-et-Loire (Département 71)
```sql
SELECT Contrat_ID, Formule
FROM Contrat
WHERE Type_local = "Maison"
AND Code_departement = "71";
```

## 3) Lister le nom des régions de France
```sql
SELECT DISTINCT reg_nom
FROM Region;
```

## 4) Combien existe-t-il de contrats sur les résidences principales ?
```sql
SELECT COUNT(DISTINCT(Contrat_ID)) AS nb_contrats_rp
FROM Contrat
WHERE Type_contrat = "Residence principale";
```

## 5) Quelle est la surface moyenne des logements avec un contrat à Paris 
```sql
SELECT AVG(Surface) AS moyenne_surface_paris
FROM Contrat
WHERE Commune LIKE "PARIS%";  ## On aurait aussi pu filtrer avec WHERE Code_département = '75'
```

