# BI Dashboard - AfterHours

---

## Description
Comprehensive Power BI daahboard designed to provide insights in to the _"3- Airbnb Listings - Berlin.csv"_ dataset. It shows the most the most relevant analyzes the dataset can demonstrate.
The dashboard is intended to business managers to visualize and analyze data effectively.

## Overview
<img width="1115" height="625" alt="Analyse Geographique" src="https://github.com/user-attachments/assets/8a47dd29-ddfd-4286-af3f-28cb58e25c39" />

---

## Table of Contents

- [Dashboard Sneak Peek](#-overview)
- [Data Cleaning Steps](#-data-cleaning-steps)
- [Dashboard Features](#-dashboard-features)
- [How to Use](#-how-to-use)
- [Screenshots Gallery](#-screenshots)
- [Requirements](#-requirements)
- [Setup & Refresh](#-setup--refresh)

---

## Data Cleaning Steps

1. _'Column profiling based on top 1000 rows'_ >> _'Column profiling based on entire data set'_ en bas a gauche.
   
   <img width="386" height="152" alt="image" src="https://github.com/user-attachments/assets/b1efd790-fce7-4e88-ba25-bc66e986d6ad" />

3. Remove errors 'id'.
4. Replace Empty values in column 'name' with 'No Name'.
5. Remove empty 'host_id'
6. Convert types 'latitude' and 'longitude' to decimal number.
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

### Applying after dataset Cleaning.

[Tuto Complet](https://youtu.be/r3nvrlh7PTU?si=Ag8fT_OCp-5WtW94&t=2708)

Ouupsss...




https://github.com/user-attachments/assets/9cce180e-57a0-497d-a1ba-14e12bc3d08a


---
## Screenshots
### i. Geographic Analysis.

<img width="1115" height="625" alt="Analyse Geographique" src="https://github.com/user-attachments/assets/8a47dd29-ddfd-4286-af3f-28cb58e25c39" />

### ii. Market Overview.
<img width="1115" height="625" alt="Apercu du marche" src="https://github.com/user-attachments/assets/6462b7a0-f2a5-4f27-ac13-4707c305a4b0" />



### iii. Customer and Host experience.

<img width="1115" height="625" alt="Client et Hotes" src="https://github.com/user-attachments/assets/7e8f68f9-65a4-40da-8b11-1d04d97a37eb" />


---

## 🖥️ How to Use

1. Open the `AirbnbListings_Berlin.pbix` file in Power BI Desktop.
<!--2. Refresh data if needed (requires [data source access])
3. Use slicers on [page name] to filter by [date/region/product]
4. Click on [any chart element] to drill through to [detail page] -->


<!--## 🔧 Setup & Refresh

```text
1. Clone this repo
2. Open /dashboard/dashboard-name.pbix
3. Go to Home → Transform Data → Data Source Settings → Edit credentials
4. Click Refresh -->

Listening to [this](https://youtu.be/Ylf8gJQe8So?si=jHPSKnEl1dGrYctD&t=35)
# ***Bisouuuu*** 😘


