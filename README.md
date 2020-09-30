# python-api-challenge
Data Science & Visualization Bootcamp - Homework 6 Python APIs


This repository contains the Jupyter Notebook scripts WeatherPy.ipynb and VacationPy.ipynb. 

WeatherPy uses the library cityp and the OpenWeatherMap API to analyze the weather of more than 500 cities globally at varying latitudes from the equator; and, to create a representative model of world cities' weather. It creates a series of scatter plots to explore the following relationships:

Temperature (*C) vs. Latitude
Humidity (%) vs. Latitude
Cloudiness (%) vs. Latitude
Wind Speed (m/sec) vs. Latitude

The WeathePy script then runs a linear regression on each of these relationships, separated into Northern Hemisphere (latitude >= 0 degrees ) and Southern Hemisphere (latitude < 0 degrees):

Northern Hemisphere - Temperature (*C) vs. Latitude
Southern Hemisphere - Temperature (*C) vs. Latitude
Northern Hemisphere - Humidity (%) vs. Latitude
Southern Hemisphere - Humidity (%) vs. Latitude
Northern Hemisphere - Cloudiness (%) vs. Latitude
Southern Hemisphere - Cloudiness (%) vs. Latitude
Northern Hemisphere - Wind Speed (m/sec) vs. Latitude
Southern Hemisphere - Wind Speed (m/sec) vs. Latitude


Some unique attributes of the WeatherPy notebook are:

- It randomly select at least 500 cities based on latitude and longitude.
- It performs successive API calls to check the day's weather for each of the cities.
- It includes a print log of each city as it's being processed with the city number and city name.
- And, it saves a CSV of all retrieved data and a PNG image for each scatter plot.

---------------------------------------------------------------------

VacationPy works with the weather data from WeatherPy to plan future vacations. 

Using jupyter-gmaps and the Google Places API, VacationPy creates a heat map that displays the humidity for every city from WeatherPy, and narrows down the DataFrame to find only those cities with your ideal weather condition. In this example:

-A maximum temperature lower than 30 degrees Celsius but higher than 20.
-A wind speed of less than 10 meters per second.
-And, 0% cloudiness.


VacationPy uses the Google Places API to find the first hotel located within 5000 meters of each of your city's coordinates. It then plots these hotels onto the humidity heatmap, with each pin containing the Hotel Name, City, and Country information.