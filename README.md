# Analyzing weather data to decide where to open shops in Hawaii

We will be assiting an entrepreneur to decide where in Hawaii to open a Surf n' Shake shop and also to provide information to his investor.<br/>
Weather data was analyzed to have a better undestanding about how it could impact the shops.<br/>
The tools used to perform the analysis were Python, Pandas, SQLAlchemy SQLite and Flask.

A previous analysis was performed with weather data from Oahu,Hawaii. The provided database has information from 2010 to 2017. Our analyisis was based from August 2016 to August 2017 using python sqlalchemy and flask the results were presented. For this new task we will be analyzing weather data from the months of June and December.

In order to use python while exploring the sqlite db we have to import the sqlalchemy module which allows python to work with several types of db.<br/>
We create an __engine__ that will allows us to "talk" to the db. Then we have to reflect the existing database into a new model creating the Base variable with the __automap_base()__ . Once the database structure was reflected we have to reflect the tables with __Base.prepare()__

![](resources/engine.png)

In order for Python to be able to query information from the tables, we have to create classes from those tables and a __session__ variable. Also, the columns were printed to know their names and use them in our queries.

![](resources/classes.png)

The first task was to determine the summary statistics for June.<br/>
A query was created to obtain the temperatures from this month, then the results were passed to a pandas DataFrame to obtain the statistics from the dataframe.

![](resources/june_df.png)

![](resources/june_stats.png)

Same task was required for December.

![](resources/dec_temps.png)

![](resources/dec_stats.png)

With the results obtained from June and December, we can present the results in a web browser with the help of Flask.
We create an instance and then a route for the welcome page, june and december temperatures in python.

![](resources/routes.png)

![](resources/web_routes.png)

The results are displayed in our browser with the API we created.

![](resources/tobs_june.png)

![](resources/tobs_dec.png)

