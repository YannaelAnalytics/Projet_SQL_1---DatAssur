## Requêtes du Projet

## 1) Lister les numéros de contrats (contrat_ID) avec leur surface pour la commune de Caen
```sql
SELECT
  c.contrat_ID,
  c.surface
FROM contrat c
WHERE c.commune = "CAEN";
```

## 2) Lister les numéros de contrat avec le type de contrat et leur formule pour les maisons du département de la Saône-et-Loire (Département 71)
```sql
SELECT
  c.contrat_ID,
  c.formule
FROM contrat
WHERE type_local = "Maison"
AND c.code_departement = "71";
```

## 3) Lister le nom des régions de France
```sql
SELECT
  DISTINCT r.reg_nom
FROM region r;
```

## 4) Combien existe-t-il de contrats sur les résidences principales ?
```sql
SELECT
  COUNT(DISTINCT c.contrat_ID) AS nb_contrats_rp
FROM contrat c
WHERE c.type_contrat = "Residence principale";
```

Il existe 25 620 contrats sur les résidences principales.

## 5) Quelle est la surface moyenne des logements avec un contrat à Paris 
```sql
SELECT
  ROUND(AVG(c.surface),2) AS moyenne_surface_paris
FROM contrat c
WHERE c.commune LIKE "PARIS%";
```
Une autre façon méthode est de filtrer avec "WHERE code_departement = '75'".

La surface moyenne des logements contractuels est de 51,77 m² à Paris.

## 6) Quels sont les 5 contrats avec les surfaces les plus élevées ?
```sql
SELECT
  c.contrat_ID,
  c.surface
FROM contrat c
ORDER BY c.surface DESC
LIMIT 5;
```

## 7) Quel est le prix moyen de la cotisation mensuelle ?
```sql
SELECT
  ROUND(AVG(c.prix_cotisation_mensuel),2) AS cotisation_moyenne
FROM contrat c;
```
Le prix moyen est de 19,33€ par mois.

## 8) Quel est le nombre de contrats pour chaque catégories de prix de la valeur déclarée des biens ?
```sql
SELECT
  c.valeur_declaree_biens,
  COUNT(DISTINCT c.contrat_ID) AS nb_contrats_valeur
FROM contrat c
GROUP BY valeur_declaree_biens
ORDER BY nb_contrats_valeur;
```
De 0 à 25 000 € de biens à assurer : 22 720 contrats
De 25 000 à 50 000€ de biens à assurer : 6815 contrats 
De 50 000 à 100 000€ de biens à assurer : 696 contrats 
+100 000€ de biens à assurer : 104 contrats

## 9) Quels sont les 10 départements où le prix moyen de la cotisation est le plus élevé ?
```sql
SELECT r.dep_nom, r.dep_code, AVG(c.prix_cotisation_mensuel) AS moyenne_prix_dpt
FROM contrat c 
JOIN region r ON c.code_postal = r.code_postal
GROUP BY r.dep_nom, r.dep_code
ORDER BY moyenne_prix_dpt DESC
LIMIT 10;
```

## 10) Quel est le nombre de contrats avec des formules "Integral" pour la région Pays de la Loire ?
```sql
SELECT COUNT(DISTINCT c.contrat_ID) AS nb_contrats_integral_pdl
FROM contrat c
JOIN region r ON c.code_postal = r.code_postal
WHERE c.formule = "Integral"
AND r.reg_nom = "Pays de la Loire";
```
Il y a 590 contrats "Intégral" dans la région Pays de la Loire.

## 11) Liste des communes ayant eu au moins 150 contrats ?
```sql
SELECT c.commune, COUNT(DISTINCT c.contrat_ID) AS nb_contrats_uniques
FROM contrat c
GROUP BY c.commune
HAVING nb_contrats_uniques >= 150;
```

## 12) Quel est le nombre de contrats pour chaque région ?
```sql
SELECT r.reg_nom, COUNT(DISTINCT c.contrat_ID) AS nb_contrats_regions
FROM contrat c
JOIN region r ON c.code_postal = r.code_postal
GROUP BY r.reg_nom;
```
