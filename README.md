# python-api-challenge
Python requests, APIs, and JSON are used here to answer a fundamental question: "What is the weather like as we approach the equator?"

The obvious answer is "It gets hotter.” But, if pressed for more information, how would you prove that?

### Part 1: WeatherPy
Create a Python script to visualise the weather of over 500 cities of varying distances from the equator.
1. Generate random geographic coordinates and find the nearest city to each latitude and longitude combination using the [citipy Python library](https://pypi.org/project/citipy/).
2. Next, the [OpenWeatherMap API](https://openweathermap.org/api) is used to retrieve waether data for each city.
3. Create a series of scatter plots to display the following relationships:
   -  Latitude vs. Temperature
   -  Latitude vs. Humidity
   -  Latitude vs. Cloudiness
   -  Latitude vs. Wind Speed
4. Separate the plots above into Northern and Southern hemispheres, then calculate the linear regression for each.

Linear regression is used to prove how the weather changes (or doesn't) depending on proximity to the equator.

![image](https://github.com/Borruu/python-api-challenge/assets/112932520/b999c2f3-eaa2-4f5f-b9b2-885277955646)


### Part 2: VacationPy
Show how weather data can be used to plan future vacations using the [Geoapify API](https://www.geoapify.com/) and the [geoViews Python library](https://geoviews.org/).
1. Create a map that displays a point for every city in the `city_data_df` DataFrame as shown in the following image. The size of the point indicates the humidity in each city.
2. Narrow down the city_data_df DataFrame to find your ideal weather condition. For example:
   - A max temperature lower than 27 degrees but higher than 21
   - Wind speed less than 4.5 m/s
   - Zero cloudiness
   - the main objective is to limit the dataframe to 10-20 rows.
3. Create a new DataFrame called hotel_df to store the city, country, coordinates, and humidity.
4. For each city, use the Geoapify API to find the first hotel located within 10,000 metres of your coordinates.
5. Add the hotel name and the country as additional information in the hover message for each city in the map as in the following image:

## User guide
1. Run `WeatherPy.ipynb` to collect and store weather data from approximately 550-650 cities around the world using randomly generated coordinates. **API keys will be required for Geoapify and OpenWeather App**.
2. Graphs created by `WeatherPy.ipynb` will be stored in `output_data`.
3. `VacationPy.ipynb` can be run after `WeatherPy.ipynb` as it is dependent on the data collected by latter.

## References
- **citipy Python library** https://pypi.org/project/citipy/
- **OpenWeatherMap API** https://openweathermap.org/api
- **Geoapify API** https://www.geoapify.com/
- **geoViews Python library** https://geoviews.org/
