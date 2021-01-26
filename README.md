# SqlAlchemy-Challenge
 This repo contain the assignment for module 10 - SQL Alchemy

 I've decided to treat yourself to a long holiday vacation in Honolulu, Hawaii! To help me with the trip planning, I need to do some climate analysis on the area. The following outlines what I need to do.

At Climate_Analysis notebook:
1. Find the most recent date (newest) in the database
2. Retrieve the last 12 months of precipitation data by querying the 12 preceding months of data

### Station Analysis
3. Design a query to calculate the total number of stations in the dataset.
4. Design a query to find the most active stations(i.e. which stations have the most rows?)
5. Design a query to retrieve the last 12 months of temperature observation data (TOBS).

## Step 2 - Climate App - app.py

Now that you have completed your initial analysis, design a Flask API based on the queries that you have just developed.


### Routes

* `/`

  * Home page.

  * List all routes that are available.

* `/api/v1.0/precipitation`

  * Convert the query results to a dictionary using `date` as the key and `prcp` as the value.

  * Return the JSON representation of your dictionary.

* `/api/v1.0/stations`

  * Return a JSON list of stations from the dataset.

* `/api/v1.0/tobs`
  * Query the dates and temperature observations of the most active station for the last year of data.

  * Return a JSON list of temperature observations (TOBS) for the previous year.

* `/api/v1.0/<start>` and `/api/v1.0/<start>/<end>`

  * Return a JSON list of the minimum temperature, the average temperature, and the max temperature for a given start or start-end range.

  * When given the start only, calculate `TMIN`, `TAVG`, and `TMAX` for all dates greater than and equal to the start date.

  * When given the start and the end date, calculate the `TMIN`, `TAVG`, and `TMAX` for dates between the start and end date inclusive.