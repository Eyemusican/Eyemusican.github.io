---
Title : DBS101 Flipped class 6
categories : [DBS201, Flipped_Class6]
tags : [DBS101]
---

### What I learned during flipped class!
---
Kuzu zangpola! Here's another journal entry on what I learned in Flipped Class, Day six. Today I will explain the concept of NoSQL database and it's types. Without any further, let's get started.

### NoSQL Database
---
Without going into deep, firstly, let us understand what database and NoSQL are, database is a collection of structured data or information which is stored in a computer system and can be accessed easily.

NoSQL is a non-relational database that is used to store the data in the nontabular form.
NoSQL databases are a type of database management system that stores and retrieves data in a way that is different from traditional relational databases ( MySQL, PostgreSQL, etc.).

#### Advantage and Disadvantages of NoSQL Databases ;
![alt text](../15.png)




### Types of NoSQL Database
---
1. Document-based databases
2. Key-value stores
3. Column-oriented databases
4. Graph-based databases
5. Vector Databases
6. Time-series Databases

Let us understand each one of them in detail.

### Document-based databases
---
It is a nonrelational database, which store data in flexible, semi-structured documents(JSON, BSON, or XML documents.)

Key features of document databases are their flexible schema, faster creation and maintenance, absence of foreign keys, and the use of open formats like XML and JSON to build documents. 
```
{
   "_id": ObjectId("11910002347"),
   "name": "Tenzin Namgay",
   "email": "Tenzey@gmail.com",
   "address": {
      "street": "123 Main St",
      "city": "Thimphu",
      "state": "CA",
      "zip": "12345"
   },
   "interests": ["reading", "hiking", "photography"]
}
```

The above is the example of document-based database which stores data in flexible, JSON-like documents with dynamic schemas. It is designed to be scalable, high-performance, and easy to use.


### Key-value stores
---
 key-value databases or key-value stores, are a type of non-relational database that stores data as a collection of key-value pairs. It is the simplest form of a NoSQL database.
 In this data model, each data element is associated with a unique key and the values can be simple data types like strings and numbers or complex objects.

 Key-value stores are designed to be highly scalable  and efficient for simple read and write operations. They are  fast access to data.

 ```
 {
  "TableName": "Users",
  "Item": {
    "UserId": {"S": "1234"},
    "Name": {"S": "Karma yangzom"},
    "Email": {"S": "Karma@gmail.com"}
  }
}
```
the above example is highly scalable NoSQL database that can be used as a key-value store, among other data models.

### Column Oriented Databases
---
Column-oriented databases are a type of NoSQL database that stores data in columns instead of rows.

Column-oriented databases are designed to be highly efficient and retrieve the data with greater speed. It involve in  reading large data across a subset of columns.

```
CREATE KEYSPACE example WITH replication = {'class':'SimpleStrategy', 'replication_factor':1};
USE example;
CREATE TABLE users (
    user_id uuid PRIMARY KEY,
    name text,
    email text,
    age int
);

INSERT INTO users (user_id, name, email, age) VALUES (uuid(), 'Rinchen Dorji', 'Rinchhen@yahoo.com', 20);
INSERT INTO users (user_id, name, email, age) VALUES (uuid(), 'Tenzin Namgay', 'tenzinn@gmail.com', 18);

SELECT name, email FROM users;
```
The above example is  highly scalable NoSQL database that uses a column-oriented database.

### Graph-based databases
---
Graph databases are a type of NoSQL database designed to store and navigate relationships between the elements by using the links. Graph databases represent data as nodes (entities) and edges (relationships) in a graph-like structure.

```
// Creating nodes
CREATE (john:Person {name: 'Dophu Dorji', age: 32})
CREATE (jane:Person {name: 'kelly lhendrup', age: 28})

// Creating a relationship
CREATE (Dophu)-[:KNOWS {since: 2015}]->(Kelly)

// Querying
MATCH (p:Person)-[:KNOWS]->(friend)
RETURN p.name, friend.name
```
The above example uses the property graph model, where nodes and relationships can have properties (key-value pairs) associated with them.

###  Vector Databases
---
Vector databases are a type of database system designed to store and search high-dimensional vector representations of data, such as text embeddings, image embeddings, or other numerical vectors. These databases are particularly useful for tasks that require finding similar or related items based on their vector representations.

```
import pinecone

# Initialize Pinecone
pinecone.init(api_key="your-api-key", environment="your-environment")

# Create or retrieve an index
index = pinecone.Index("my-index")

# Insert vectors
vectors = [[1.2, 0.3, ...], [0.8, -0.2, ...], ...]
metadata = [{"text": "Hello, world!"}, {"text": "This is a example."}]
index.upsert(vectors=vectors, metadata=metadata)

# Query for similar vectors
query_vector = [0.9, 0.1, ...]
results = index.query(query_vector, top_k=5, include_metadata=True)
print(results)
```
The above example uses vector database service designed for production-scale machine learning applications. It supports various embedding types 

### Time-series Databases
---
Time-series data is simply data with a timestamp collected with the intent of tracking changes over time. It is designed to handle the unique characteristics of time-series data, including high ingestion rates, efficient storage and retrieval of time-stamped data and aggregation functions.

```
-- Create a database and a measurement
CREATE DATABASE mydb
USE mydb
CREATE MEASUREMENT sensor_data

-- Insert data points
INSERT sensor_data,location=office,sensor_id=1 temperature=25.3,humidity=60.2 1598041200000000000 -- Unix nanosecond timestamp

-- Query data
SELECT mean(temperature) as avg_temp, max(humidity) as max_humidity
FROM sensor_data
WHERE time >= '2020-08-21T00:00:00Z' AND time <= '2020-08-22T00:00:00Z'
GROUP BY time(1h)
```

The above example distributes time-series database designed for handling high-volume write and query loads. It uses an SQL-like query language and supports features like data compression and many more.



### What I did in flipped class!
---
During the flipped classroom session, I engaged in an interactive learning experience focused on non-relational databases. The class was divided into six expert groups, and my group was assigned the Key-value stores. After getting the instructions, my expert group had a detailed discussion on Key-value stores. We looked at their advantages, disadvantages, and real-world uses. We shared what we already knew, analyzed examples, and together developed a thorough understanding of the topic.

After the expert group discussions, we formed new home groups. Each home group had members from the different expert groups. In my home group, we each took turns presenting the database type we had discussed in our respective expert groups. I presented the insights and knowledge I had gained about Key-value stores.

After the home group discussions, our lecturer asked questions by picking each member from different groups. This interactive session helped explain things better, resulting in a deeper understanding of how these non-relational databases work.

 


