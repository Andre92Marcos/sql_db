# mongoDB ## Overview

There are different types of databases and one among them is MongoDB, which is a document-oriented
NoSQL database. It is crucial to be aware of how the data is stored in different types of databases and how
we can connect to these remote database servers and retrieve the desired data. In a document-oriented
NoSQL database, the data is organized into a hierarchy of the following levels:
	databases
	collections
	documents

Databases make up the top level of data organization in a MongoDB instance. Databases are organized into
collections which contain documents. Documents contain literal data such as strings, numbers, dates, etc. in
a JSON-like format.

MongoDB is a document-oriented NoSQL database. Instead of using tables and rows like in traditional
relational databases, MongoDB makes use of collections and documents. Each database contains
collections which in turn further contain documents. Each document consists of key-value pairs which are
the basic unit of data in a MongoDB database. A single collection can contain multiple documents and they
are schema-less meaning that the size and content of each document can be different from each another.

## Installing MongoDB Shell

	1st) curl -O https://fastdl.mongodb.org/linux/mongodb-linux-x86_64-3.4.7.tgz
	2nd) tar xvf mongodb-linux-x86_64-3.4.7.tgz
	3rd) Add this to .bashrc
		 export PATH="/opt/mongodb-linux-x86_64-3.4.7/bin:$PATH"

## MongoDb Shell Commands

	show dbs; #  list the databases present on the MongoDB server
	use <db_name> # selects the db to use
	show collections; #  list down the collections stored in current db
	db.<collection_name>.find() # dumps the content of a specific document of a collection
	db.<collection_name>.find().pretty(); # same as find but with better output format
