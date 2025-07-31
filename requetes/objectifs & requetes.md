## ❓1) Lister les numéros de contrats (contrat_ID) avec leur surface pour la commune de Caen

```sql
SELECT Contrat_ID, Surface
FROM Contrat
WHERE Commune = "CAEN"
