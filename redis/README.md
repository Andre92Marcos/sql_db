# REDIS

## Overview

Databases are a collection of organized information that can be easily accessed, managed and updated. In
most environments, database systems are very important because they communicate information related
to your sales transactions, product inventory, customer profiles and marketing activities.
There are different types of databases and one among them is Redis, which is an 'in-memory' database. In-
memory databases are the ones that rely essentially on the primary memory for data storage (meaning that
the database is managed in the RAM of the system); in contrast to databases that store data on the disk or
SSDs. As the primary memory is significantly faster than the secondary memory, the data retrieval time in
the case of 'in-memory' databases is very small, thus offering very efficient & minimal response times.
In-memory databases like Redis are typically used to cache data that is frequently requested for quick
retrieval. For example, if there is a website that returns some prices on the front page of the site. The
website may be written to first check if the needed prices are in Redis, and if not, then check the traditional
database (like MySQL or MongoDB). When the value is loaded from the database, it is then stored in Redis
for some shorter period of time (seconds or minutes or hours), to handle any similar requests that arrive
during that timeframe. For a site with lots of traffic, this configuration allows for much faster retrieval for the
majority of requests, while still having stable long term storage in the main database.

## What is Redis?

Redis (REmote DIctionary Server) is an open-source advanced NoSQL key-value data store used as a
database, cache, and message broker. The data is stored in a dictionary format having key-value pairs. It is
typically used for short term storage of data that needs fast retrieval. Redis does backup data to hard drives
to provide consistency.

The server
	Redis runs as server-side software so its core functionality is in its server component. The server listens for connections from clients, programmatically or through the command-line interface.

The CLI
	The command-line interface (CLI) is a powerful tool that gives you complete access to Redis’s data and its functionalities if you are developing a software or tool that needs to interact with it.

Database
The database is stored in the server's RAM to enable fast data access. Redis also writes the contents of the database to disk at varying intervals to persist it as a backup, in case of failure.

## Installing redis-cli

Now, to be able to interact remotely with the Redis server, we need to download the redis-cli utility. It
can be downloaded using the following command :
	sudo apt install redis-tools
Alternatively, we can also connect to the Redis server using the netcat utility
