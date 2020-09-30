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


Some unique attributes of this notebook are:

- It randomly select at least 500 cities based on latitude and longitude.
- It performs successive API calls to check the day's weather for each of the cities.
- It includes a print log of each city as it's being processed with the city number and city name.
- And, it saves a CSV of all retrieved data and a PNG image for each scatter plot.