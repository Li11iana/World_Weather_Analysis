# World_Weather_Analysis
## Overview
For this project the databases Google Maps and OpenWeatherMap are utilized to retrieve weather and lodging information for over 600 randomly generated cities around the globe. With that information, an app is simulated to offer the user travel recommendations based on desired weather and matching that to the current climate conditions for the randomly generated cities. Once the preferred destinations are selected a travel route can be generated to help potential travelers plan their trip.

### Purpose
Using available databases and user input this project aims to facilitate and inspire travelers looking to experience a pleasant vacation but that are flexible in terms of country/city destination.

## Results
The project unfolds in three distinct phases, outlined below:

### Weather Database
Randomly generated coordinates produce weather data for the nearest city fetched from OpenWeatherMap. All pertinent information is consolidated into a DataFrame for further analysis. 
The information in this Dataframe will be used to filter the destination results in the next phase.

![Weather_Database.png](https://github.com/Li11iana/World_Weather_Analysis/blob/main/Weather_Database/Weather_Database.png)
As can be seen in the image above for each coordinate we obtain:
* The nearest city and country.
* The date and time of the weather report (all weather conditions correspond to that specific date).
* Coordenates: Latitude and Longitude
* Weather conditions: Max Temperature (Farenheit), Humidity (%), Cloudiness, Wind Speed, and Current description of the weather.
Generated dataframe can be reviewed as a CSV file : WeatherPy_Database.csv

### Vacation Search
In this phase, results from the Weather Database are filtered based on user input, with a specific focus on temperature criteria (65°F to 95°F). The filtered cities DataFrame is then employed to request information about the nearest lodgings, which is added to the DataFrame under the "Hotel Name" column. 

![Preferred_cities_hotels.png](https://github.com/Li11iana/World_Weather_Analysis/blob/main/Vacation_Search/Preferred_cities_hotels.png)

Entries without lodging information are removed. A map, utilizing Google Maps tools, is generated for a visual overview of all cities and associated hotels that meet the desired weather conditions.



### Vacation Itinerary
Utilizing Google Directions, a travel itinerary is crafted using four cities from the Preferred Cities DataFrame. As an example, four cities on the island of Mauritius were selected. The resulting map incorporates the chosen destinations, hotels, and weather information gathered in the previous section.
![WeatherPy_travel_map.png](https://github.com/Li11iana/World_Weather_Analysis/blob/main/Vacation%20Itinerary/WeatherPy_travel_map.png)


## Conclusion

By harnessing API requests, the Python script developed for this project demonstrates its adaptability to cater to diverse user preferences, consistently delivering up-to-date travel recommendations. The integration of dynamically generated maps serves as a valuable visual aid, offering users an immersive and informative experience throughout their vacation planning journey.

