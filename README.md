# sqlalchemy-challenge
-----
![Hawaii Weather Station](https://user-images.githubusercontent.com/123334523/232326553-0baa4541-943e-4791-be5d-2299e0110ba7.png)

## Project Description
The goal of this project was analyze data taken from several weather stations in Hawaii and then publish the results in a json format to an app, which can later be used by others.
In the initial data analysis and exploration, SQLAlchemy was used in a jupyter notebook to query and visualize the relevant information.
In the designing of the climate app, a python file (app.py) was written to create a Flash application, which generates a landing page and then allows the retreival of information from several static and some dynamic routes.

### Table of Contents
- [1. Analysis and Exploration of Climate Data](https://github.com/jonnybrammah/sqlalchemy-challenge/blob/main/README.md#analysis-and-exploration-of-climate-data)
- [2. Designing Climate App](https://github.com/jonnybrammah/sqlalchemy-challenge/blob/main/README.md#designing-climate-app)

### Analysis and Exploration of Climate Data
#### Precipiation Data
The jupyter notebook file (climate_starter.ipynb) was written to perform some queries of the data using SQLAlchemy. This allowed us to find the most recent date in the database and then determine the precipitation amounts in inches for every date in the previous year, which was then plotted as a graph, which can be seen here:


The mean amount of preciipitation over the previous twelve months was 0.17 inches, with a maximum rainfall of 6.7 inches and an expected minimum of zero inches on a rainless day.

#### Temperature Data
There are several weather stations in the database, and code was written to determine the station that had recorded the most data. This station was then used to analyze temperatures, to determine the coldest and warmest temperatures recorded, as well as the average temperature. Again, the previous year of data were queried and a histogram was plotted of this data, which can be seen here:

The lowest temperature recorded at the most active station was 54°F, and the highest was 85°F, consistent with Hawaii's climate, and the average temperature at this station over the previous twelve months was 72°F.

### Designing Climate App
Once the main pieces of data had been analyzed in the jupyter notebook, a python file (app.py) was created to generate a Flask application to display the raw data in json form.
The landing page returns all the possible routes a user could use to collect data from, and looks like this:


The top three routes are all static and return:
- Precipitation data (in inches) by date in the database for the last year of data
- A list of all the stations in the database
- Temperature data by date from the most active station, for the last year of data
