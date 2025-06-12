## Working With Neo4j

In this article, we will cover how to begin working with Neo4j in Project3.

## Neo4j

Neo4j a powerful graph database framework which Project3 uses as it's primary source for data. Neo4j allows us not only to store data, but to query data as well, which proves to be useful for a network analysis program.

Before we begin, ensure that you have a Neo4j instance running for testing. Refer to [this Neo4j documentation](https://neo4j.com/docs/aura/classic/auradb/getting-started/create-database/) for more information on creating a Neo4j instance.

## Setting Up Routes

To use Neo4j, you will need to configure the correct `URI` and `Password` in our Flask server. This correct configuration allows Flask to connect to the Neo4j database, and in turn, allows the frontend to connect as well. You can do so via the following workflow:
1. Get the correct `URI` and `Password` for your Neo4j instance.
    - If you do not know either, refer to [this Neo4j documentation](https://neo4j.com/docs/browser-manual/current/operations/dbms-connection/).
2. From the root folder of Project3, navigate to `flask/app.py`.
3. Near the top of the file, change the global `URI` variable to the correct Neo4j `URI` value.
4. Near the top of the file, change the global `AUTH` variable to the correct Neo4j `Password` value.
5. To verify connection, from the root folder of Project3 run the command `python flask/app.py`.
    - If the authentication information is incorrect or the Neo4j instance is not running, the Flask server will not start.
    - Likewise, if the authentication information is correct, the Flask server should begin without issue.

## Further Reading

For more information on Neo4j, refer to their [Getting Started With Neo4j article here](https://neo4j.com/docs/getting-started/).