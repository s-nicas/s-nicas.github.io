---
layout: post
title:      "How to download MongoDB on Mac "
date:       2019-02-27 23:09:11 +0000
permalink:  how_to_download_mongodb_on_mac
---


I’ve walked into the world of MongoDB this week and I’ve really enjoyed learning it! 

MongoDB is classified as a NoSQL database. MongoDB uses JSON-like documents with schemas. As a result MongoDB reduces the complexity of deployments. 


For this walkthrough you will need to install Hombrew. For more information on Homebrew and to download it navigate to [Homebrew](http://brew.sh/)


Once homebrew is installed. 

To install MongoDB

In your terminal run

```
$brew install mongodb
```

Once installed we need to create a directory where MongoDB will store its data. By default MongoDB stores data at this directory 

/data/db


To create this directory in your terminal run 

```
$sudo mkdir -p/data/db
```

*Heads-up:* You will be prompted to add your password. 


Next - update the permission on this file to ensure it will work with MongoDB

In your terminal run

```
sudo chown -R `id -un`data/db
```

Next we need to run Mongo daemon. Mongo daemon is a service the runs in the background and listens for connections at a given port. 

Important - open a new terminal to start Mongo dameon. Mongo dameon should remain running in the background. 

In your terminal run
```
$mongod
```
You should see “waiting for connections on port 27017”

WooHOO! 

Now let's download a client to connect to mongoDB. 

Navigate to [MongoDB]( https://www.mongodb.com/download-center/compass)

Click download and follow the prompts. 

Once the download is complete - Open MongoDB in you applications.

You will see a homepage that says “Connect to Host”. 

Leave all the default values and click **connect**. 

Once connected you should see 2 databases: admin & local - these are for MongoDB. Don’t touch them - let them be - and al is well :) 

That’s it! You’re all set. 

In my next blog I will review how to connect your Node.js project to MongoDB. 

