# AirbnbPricePrediction

## Description
This project focuses on developing a predictive model for forecasting the pricing of Airbnb listings within the European Union before they are made available on the market. By leveraging advanced data analytics and machine learning techniques, the goal is to create a robust algorithm that can analyze various factors influencing the pricing dynamics of Airbnb accommodations. These factors may include location, amenities, seasonality, and local market trends. 

There are two usage scenarios for the program:
- When a user wants to list their property on Airbnb, they can use this tool to determine the most appropriate price.
- It allows a user looking to stay in a specific accommodation to check if the property is more expensive than it should be or, on the contrary, a great deal."

## Context of the project

This project was undertaken as part of the Introduction to Data Science course at the University of Skövde in Sweden, during my exchange semester from the University of Technology of Troyes. It is important to note that the project was an individual project, not a group project.

## Dataset

The data is sourced from [Determinants of Airbnb prices in European cities: A spatial econometrics approach (Zenodo)](https://zenodo.org/records/4446043#.Y9Y9ENJBwUE).
The authors of the dataset are Gyódi, Kristóf, Nawaro, Łukasz.

This dataset provides several informations about Airbnb accommodations (price, number of rooms, type of lodging, etc.) for several cities in Europe (Amsterdam, Athens, Barcelona, Berlin, Budapest, Lisbon, London, Paris, Rome, Vienna). Moreover, the dataset presents the information based on whether it is the weekend or the weekday. When downloading the dataset, we receive a set of CSV files, with two CSV for each city (one for the weekend and another for the weekday).

The dataset must be downloaded using the provided link and then placed in a folder named 'data.' All that remains is to extract the downloaded data in such a way as to have the project structure as follows :
```
notebook.ipynb
data
|- amsterdam_weekdays.csv
|- amsterdam_weekends.csv
|- ...
```

For each CSV, columns are as following:
- ``realSum``: the full price of accommodation for two people and two nights in EUR
- ``room_type``: the type of the accommodation 
- ``room_shared``: dummy variable for shared rooms
- ``room_private``: dummy variable for private rooms
- ``person_capacity``: the maximum number of guests 
- ``host_is_superhost``: dummy variable for superhost status
- ``multi``: dummy variable if the listing belongs to hosts with 2-4 offers
- ``biz``: dummy variable if the listing belongs to hosts with more than 4 offers
- ``cleanliness_rating``: cleanliness rating
- ``guest_satisfaction_overall``: overall rating of the listing
- ``bedrooms``: number of bedrooms (0 for studios)
- ``dist``: distance from city centre in km
- ``metro_dist``: distance from nearest metro station in km
- ``attr_index``: attraction index of the listing location
- ``attr_index_norm``: normalised attraction index (0-100)
- ``rest_index``: restaurant index of the listing location
- ``attr_index_norm``: normalised restaurant index (0-100)
- ``lng``: longitude of the listing location
- ``lat``: latitude of the listing location

## Setup the Project
0. Ensure you have Python installed on your system. 

1. Clone the repository:
    ```bash
    git clone git@github.com:Antoine-ValentinCharpentier/AirbnbPricePrediction.git
    cd AirbnbPricePrediction
    ```

2. Download the dataset and place it as indicated in the Dataset section.
    
3. Initialise the venv:
    ```bash
    python -m venv .venv
    .venv\Scripts\activate OU source .venv/bin/activate
    pip install -r requirements.txt
    ```

4. Execute the script ``notebook.ipynb``
