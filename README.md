# Twitter Analytics Web Service

Description
-----------

The project is to build a web service for Twitter data analysis. A raw dump of tweets that runs into tens of gigabytes was provided. The dataset will have to be stored within our web service. The web service should be able to handle a specific number of requests per second for several hours. However, the budget is limited, thus the task is to build an effective and cost efficient solution utilizing Amazon Web Services resources.


Resource
--------
Class materials: The dataset collected from Twitter provided by the instructor. Each file contains roughly 20,000 tweets stored in JSON format.

Language & Framework
--------------------
+ Front-end: Java, Tomcat
+ Back-end: Python
+ Database: HBase or MySQL

Development Guildlines 
----------------------
The web service solution provides data statistics on the twitter dataset. Users can submit queries about tweets based on userids or time.

- Front end should be able to receive and respond to queries.
  * The web service’s front end will have to handle the following query types through HTTP GET requests on port 80:
     1. Heartbeat (q1): The query asks about the state of the web service. The front end server responds with the current timestamp.
     2. Text of tweets (q2): The query asks for the tweets created at a specific second.
     3. Number of tweets (q3): The query asks for the total number of tweets sent by a range of userids.
     4. Who retweeted a tweet (q4): The query asks for the set of userids who have retweeted any tweet posted by a given userid.

- Back end system is used to store the data to be queried.
  * Spot instances for the back end system development
  * On demand instances for the live test.

- ETL(Data extract, transform and load)
 * Load the Twitter dataset into the database using the extract, transform and load (ETL) process in data warehousing.

Owner
-----
Wenhua474
