# World_Weather_Analysis
## Overview
For this project the databases Google Maps and OpenWeatherMap are utilized to retrieve weather and lodging information for over 600 randomly generated cities around the globe. With that information, an app is simulated to offer the user travel recommendations based on desired weather and matching that to the current climate conditions for the randomly generated cities. Once the preferred destinations are selected a travel route can be generated to help potential travelers plan their trip.

### Purpose
Using available databases and user input this project aims to facilitate and inspire travelers looking to experience a pleasant vacation but that are flexible in terms of country/city destination.

## Results
This project is divided in 3 phases, these will be explained below:

### Weather Database
A set of randomly generated coordinates are created and the weather for the nearest city is pulled from the OpenWeatherMap. All revelant information is compiled into a Dataframe for further review. The information in this Dataframe will be used to filter the destination results in the next phase.
![Weather_Database.png](https://github.com/Li11iana/World_Weather_Analysis/blob/main/Weather_Database/Weather_Database.png)
As can be seen in the image above for each coordinate we obtain:
* The nearest city and country it belongs.
* The date and time of the weather report (all weather conditions correspond to that specific date).
* Coordenates: Latitude and Longitude
* Weather conditions: Max Temperature (Farenheit), Humidity (%), Cloudiness, Wind Speed, and Current description of the weather.
Generated dataframe can be reviewed as a CSV file : WeatherPy_Database.csv

### Vacation Search
Starting with an input dependent section, for this phase the results obtained in the Weather Databased are filter according user input, for this example the cities were filtered by temperature (65°F to 95°F). With that a filtered cities dataframe is used to generate a request for nearest lodging information, this is added to the dataframe in the "Hotel Name" column as shown in the following table:

![Preferred_cities_hotels.png](https://github.com/Li11iana/World_Weather_Analysis/blob/main/Vacation_Search/Preferred_cities_hotels.png)

Entries missing lodging information were eliminated. With the collected data a map is generated using Google maps tools to review visually all the cities + hotels with the desired weather.



### Vacation Itinerary
Finally using Google Directions a travel itinerary using 4 cities from the Preferred Cities Dataframe. For this example 4 cities in the island of Mauritus were selected. From those a route connecting the choseen destinations was generated, this map also contains the hotel and weather information collected in the previous section.
![WeatherPy_travel_map.png](https://github.com/Li11iana/World_Weather_Analysis/blob/main/Vacation%20Itinerary/WeatherPy_travel_map.png)
