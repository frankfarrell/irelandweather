#Spray client, Akka and streaming tweets

Twitter streaming & simple sentiment analysis application. To build & run the plain-vanilla version of the application, run ``sbt run``. Then you can type in the ``track`` command, which expects the Twitter search term to track. See https://dev.twitter.com/docs/api/1.1/post/statuses/filter for ``track`` filter.

##Twitter application
Before you run the application, create the ``~/.twitter/activator`` file, containing four lines; these lines represent your twitter consumer key and secret, followed by token value and token secret. To generate these values, head over to https://dev.twitter.com/apps/, create an application and add the appropriate lines to this file. An example ``~/.twitter/activator`` is

```
*************TqOdlxA
****************************Fv9b1ELexCRhI
********-*************************GUjmnWQvZ5GwnBR2
***********************************ybgUNqrZwD
```

Naturally, the you will need to replace the ``*``s with the values in your consumer token and secret; and token value and secret.

##Running
Having added the file above, you can see the application "in action", by run ``sbt run`` in an ANSI terminal. Once running, type in ``track christmas``, ``track daley``, or anything else that tickles your fancy.



Project to Learn Akka patterns. Consume live weather data for Ireland and compare it to twitter stream.

Phase 1:
Using Akka-Quartz or similar. Consume APIs for weather data and route according to coordinates, using ConsistentHashing router.
Parse data. -> Datex 2 XML Format.
Expose a simple weather contour map that updates over socket.
Weather data from here http://data.tii.ie/Info/Its

Phase 2:
Twitter stream on weather terms for bounding box of Ireland.
Do sentiment analysis on this and compare to actual data.
Use Spark Streaming on a trained model.
Learn: word2vec

Phase 3:
More data sources.
Weather: http://www.met.ie/latest/reports.asp
Comments: boards.ie current weather
Better model.

Phase 4:
MongoGeo and analysis.
Link to real time traffic feeds.


a) Basic actor setup
b) Akka-quartz-scheduler to hit data
c) Xml Processor Actor, XML Processing in Scala
d) Preload location data
e) Router based on coordinates
