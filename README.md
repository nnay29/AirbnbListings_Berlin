1. 'Column profiling based on entire data set' en bas a gauche.
2. remove errors 'id'
3. Replace Empty values in column 'name' with 'No Name'.
4. Remove empty 'host_id'
5. 'latitude' et 'lingitude' en decimal number.
6. Remove empty 'last_review'. Vous remarquez que les Empty de 'reviews_per_month' disparaissent aussi.
7. S'assurer d'avoir 'reviews_per_month','latitude','longitude' en Decimal.
8. Add custom column sur 'review_score_ratings'. 
if [MaColonne] = null then Number.Round(List.Average(NomDeLetapePrecedente[MaColonne]), 0) else [MaColonne]

- Cliquer sur la **nouvelle** colonne 'review_score_ratings'.
Transform > Rounding > Rounding... > entrer le chiffre 0 Decimal places dans la boite de Dialogue. L'idee ici est d'arrondir la moyenne calculee a un chiffre apres la virgule.

9. Add custom column sur 'beds'. 
if [MaColonne] = null then Number.Round(List.Average(NomDeLetapePrecedente[MaColonne]), 0) else [MaColonne].

10. remove Errors et Empty sur 'zipcode'.

11. 'instant_bookable': Replace 't' with 'True' and 'f' with 'False'. Change column type to True/False.
Same for 'host_identity_verified' & 'host_is_superhost'.

12. remove empty  'host_identity_verified' & 'host_is_superhost'.

13. Replace Empty in 'space' with 'No description'

[Tuto Complet](https://youtu.be/r3nvrlh7PTU?si=Ag8fT_OCp-5WtW94&t=2708)

Ouupsss...
