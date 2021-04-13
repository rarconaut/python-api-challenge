# WeatherPy Part 1 - Python-API-Challenge
NOTE: This is Part 1 of WeatherPy, a global weather analysis and visualization project. Part 2 can be found in my "Web-Design-Challenge" GitHub repository. This repository contains the Jupyter Notebook scripts WeatherPy.ipynb and VacationPy.ipynb.

WeatherPy uses the citypy Python library and the OpenWeatherMap API to analyze the weather of more than 500 cities globally at varying latitudes from the equator; and, to create a representative model of world cities' weather. 

![image](https://user-images.githubusercontent.com/68246130/114631472-7ac68480-9c71-11eb-9e4e-00a2dc93539f.png)

It creates a series of scatter plots to explore the following relationships:
Temperature (*C) vs. Latitude <br>
Humidity (%) vs. Latitude <br>
Cloudiness (%) vs. Latitude <br>
Wind Speed (m/sec) vs. Latitude

![image](https://user-images.githubusercontent.com/68246130/114631618-caa54b80-9c71-11eb-8cea-251ac0996fe6.png)


The WeathePy script then runs a linear regression on each of these relationships, separated into Northern Hemisphere (latitude >= 0 degrees ) and Southern Hemisphere (latitude < 0 degrees):
Northern Hemisphere - Temperature (*C) vs. Latitude
Southern Hemisphere - Temperature (*C) vs. Latitude
Northern Hemisphere - Humidity (%) vs. Latitude
Southern Hemisphere - Humidity (%) vs. Latitude
Northern Hemisphere - Cloudiness (%) vs. Latitude
Southern Hemisphere - Cloudiness (%) vs. Latitude
Northern Hemisphere - Wind Speed (m/sec) vs. Latitude
Southern Hemisphere - Wind Speed (m/sec) vs. Latitude

![image](https://user-images.githubusercontent.com/68246130/114631861-43a4a300-9c72-11eb-8531-988b8b60109a.png)

Some unique attributes of the WeatherPy notebook are:

- It randomly selects at least 500 cities based on latitude and longitude.
- It performs successive API calls to check the day's weather for each of the cities.
- It includes a print log of each city as it's being processed with the city number and city name.
- And, it saves a CSV of all retrieved data and a PNG image for each scatter plot.

---------------------------------------------------------------------

VacationPy works with the weather data from WeatherPy to plan future vacations. 
![image](https://user-images.githubusercontent.com/68246130/114631243-1277a300-9c71-11eb-8949-5f4685dd27d3.png)

Using jupyter-gmaps and the Google Places API, VacationPy creates a heat map that displays the humidity for every city from WeatherPy, and narrows down the DataFrame to find only those cities with your ideal weather condition. In this example:
<ul><li>A maximum temperature lower than 30 degrees Celsius but higher than 20.</li>
  <li>A wind speed of less than 10 meters per second.</li>
  <li>And, 0% cloudiness.</li></ul>

VacationPy uses the Google Places API to find the first hotel located within 5000 meters of each of your city's coordinates. It then plots these hotels onto the humidity heatmap, with each pin containing the Hotel Name, City, and Country information.

2020-21 Data Science & Visualization Bootcamp - Rawaf Homework 6 Python APIs
