# Cypher Querying

In this article, we will cover how to query your Neo4j data using Cypher in Project3, both manually and with Assisted Mode.

## Manual Cypher Querying

To manually query your Neo4j data directly in Project3 using Cypher, you can do so via the following workflow:
![Project3's Cypher Query Bar](images/querybar.png)
1. Navigate to the upper right corner of the screen
2. Type your query in the bar labeled "Query"
4. To clear your query search, click the "Clear Query Search" button

To run and visualize your query, click the "Run Query" button and wait a moment for results to populate.

## Cypher Querying With Assisted Mode

You can use Project3's assisted Cypher querying to quickly and easily compose Cypher queries by enabling Assisted Mode. To enable assisted mode:
1. Navigate to the upper right corner of the screen
2. Click the "Assisted" button

From here, you are presented with several options for composing a query:
![Project3's Assisted Query Bar](images/assistedbar.png)
- The first four buttons will append that particular string to the end of your Cypher query (i.e. "WHERE clause" + "MATCH (n)" -> "WHERE clause MATCH (n)")
- The "GET EVERYTHING" button returns and visualizes all data in the database instance
- The "Subset Size" button returns a subset of the dataset. Note that this setting is applied to all queries as well