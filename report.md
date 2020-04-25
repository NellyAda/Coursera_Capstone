# Introduction
Looking for a place to live has never been such an arduous task as it is nowadays. Not only we should find a nice apartment with all the facilities we could need, it is equally important to live in an area that satisfies all our needs. Well, maybe we know a neighbourhood that fits our needs but it could be quite expensive, so we have to invest a lot of time an effort looking for another similir area where to live.\
Here, we are going to help the stakeholders identifying neighborhoods that could be interesting for them.\
How are we going to identify a neighborhood as _interesting_? Well, we have to provide two things:
1. the ideal neighborhood
2. the city where we want lo look for an apartment
With this, we can try to find a similar neighborhood into the provided city.

# Data

For the purposes of our study, we will be foucusing on:
1. Soto del Henares in Torrejón de Ardoz (Madrid, Spain) as our ideal neighborhood
2. Madrid city as the city where we want to live.

The data we will need to carry out this study will be the information about the neighborhoods in Madrid and the information about Torrejón de Ardoz.\
We will obtain the information about the neighborhoods in Madrid city parsing the information from https://es.wikipedia.org/wiki/Anexo:Barrios_administrativos_de_Madrid. There is a table with the districts and the neighborhoods in Madrid city.\
From there we will create a dataframe with this content:

idx | District | Neighborhood
-| -------- | -------------
0 | Centro | Palacio
1 | Centro | Embajadores
... | ... | ...
130 | Barajas | Corralejos

We will be using a geolocator to obtain the coordinates (latitude and longitude) for each neighborhood and include it in the dataframe

idx | District | Neighborhood | Latitude | Longitude
--- | -------- | ------------ | -------- | ---------
0 | Centro | Palacio | 40.415 | -3.7133
1 | Centro | Embajadores | 40.408 | -3.69972
... | ... | ... | ... | ...
130 | Barajas | Corralejos | 40.4644 | -3.59

Anologuously, we have to obtain the same information for Torrejón de Ardoz.

Using Foursquare API, we will obtain a list of venues in each neighbourhood (including the target one) and with the obtained information we will be ready to process the data.

idx | District | Neighborhood | N. Latitude | N.Longitude | Venue | Venue Longitude | Venue Latitude | Venue Category
--- | -------- | ------------ | ----------- | ----------- | ----- | --------------- | -------------- | --------------
0 | Centro | Palacio | 40.415 | -3.7133 | Coffee Starr | 40.415 | -3.712 | Coffee Shop
1 | Centro | Embajadores | 40.408 | -3.69972 | Los amigos | 40.407 | -3.699 | Restaurant
... | ... | ... | ... | ... | ... | ... | ... | ...
130 | Barajas | Corralejos | 40.4644 | -3.59 | Lungo | 40.466 | -3.591 | Coffee Shop

# Methodology

# Results

# Discussion

# Conclussion
