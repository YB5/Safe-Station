# Safe-Station
Cross Railways Detection System

##Motivation:

People fall on train tracks, get injured and even die.

Sometimes we do not notice a person when he falls.

There’s a braking distance that doesn’t always prevent death


##Solution:

Analyze videos from camera’s stations.

Report to station manager and drivers in real time.

##Tech overview:
![alt text](https://github.com/YB5/Safe-Station/blob/main/tech%20overview.png)

###Image Processing:

Detect the yellow lines (forbidden area)

Detect moving objects

Check if any object enter the forbidden area

![alt text](https://github.com/YB5/Safe-Station/blob/main/cross.png)


###Alert and Upload to cloud:

HTTP request to flask server for Realtime Alert

Upload image and video to S3 bucket

HTTP request to flask server for notifying S3 update



###Insert data and Report to UI:

Insert alert (station, camera and video id) to database

Send realtime alert to Angular via PubNub service





###Fetching, Listening and Display:

Display notification history alerts from TinyDB.

Listening to PubNub channel and notify in UI.

Display the video and image from S3 bucket.



##What’s next?

Make static charts for each station and cameras

Report to train drivers designated for those stations

Display in UI what is happening in the cameras which are in the stations in real time

