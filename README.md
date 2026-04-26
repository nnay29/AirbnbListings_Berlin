1. _'Column profiling based on top 1000 rows'_ >> _'Column profiling based on entire data set'_ en bas a gauche.
   
   <img width="386" height="152" alt="image" src="https://github.com/user-attachments/assets/b1efd790-fce7-4e88-ba25-bc66e986d6ad" />

3. Remove errors 'id'.
4. Replace Empty values in column 'name' with 'No Name'.
5. Remove empty 'host_id'
6. 'latitude' et 'lingitude' en decimal number.
7. Remove empty 'last_review'. Vous remarquez que les Empty de 'reviews_per_month' disparaissent aussi.
8. S'assurer d'avoir 'reviews_per_month','latitude','longitude' en Decimal.
9. Add custom column sur 'review_score_ratings'.
    ```M
    if [MaColonne] = null then Number.Round(List.Average(NomDeLetapePrecedente[MaColonne]), 0) else [MaColonne]
   

  * Cliquer sur la **nouvelle** colonne 'review_score_ratings'.
Transform > Rounding > Rounding... > entrer le chiffre 0 Decimal places dans la boite de Dialogue. L'idee ici est d'arrondir la moyenne calculee a un chiffre apres la virgule.

9. Add custom column sur 'beds'. Remplacer par moyenne 
   ```M
   if [MaColonne] = null then Number.Round(List.Mode(NomDeLetapePrecedente[MaColonne]), 0) else [MaColonne].

10. Remove Errors et Empty sur 'zipcode'.

11. 'instant_bookable': Replace 't' with 'True' and 'f' with 'False'. Change column type to True/False.
Same for 'host_identity_verified' & 'host_is_superhost'.

12. Remove empty  'host_identity_verified' & 'host_is_superhost'.

13. Replace Empty in 'space' with 'No description'

[Tuto Complet](https://youtu.be/r3nvrlh7PTU?si=Ag8fT_OCp-5WtW94&t=2708)

Ouupsss...




https://github.com/user-attachments/assets/9cce180e-57a0-497d-a1ba-14e12bc3d08a


# ***Bisouuuu*** 😘


