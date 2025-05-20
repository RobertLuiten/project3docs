# How To Start The Project3 Development Environment

In this article, we will cover how to start the Project3 development environment.

## Dependencies

Before running the Project3 development environment, the following dependencies will need to be installed in your Python environment:
- [igraph, a networks library for Python documentation](https://igraph.org/python/tutorial/0.9.8/install.html) for installation details.
- [NetworkX, a networks library for Python documentation](https://networkx.org/documentation/stable/install.html) for installation details.
- [Neo4j Python Driver documentation](https://neo4j.com/docs/api/python-driver/current/) for installation details.
- [Flask Driver documentation](https://flask.palletsprojects.com/en/stable/installation/) for installation details.

After you have the required Python dependencies installed, you will need to ensure you have the React dependencies installed:
1. Ensure that [npm is installed on your device](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm).
2. From the root folder of Project3, navigate in to the `frontend` directory.
3. Running the command `npm i`. This will install all dependencies you'll need for the project.

Finally, ensure that you have a Neo4j instance running for testing. We recommend referring to [this Neo4j documentation](https://neo4j.com/docs/aura/classic/auradb/getting-started/create-database/) for more information on creating a Neo4j instance.

## Setting Up Routes

Before you can run the project, you will need to set the correct `URI` & `password` for both the Flask & Neo4j environments. 
- [Working With Neo4j In Project3](workWithNeo4j.md)
- [Working With igraph and Flask In Project3](workWithFlaskigraph.md)

## Starting The Environment

We recommend starting the development environment via the following workflow:
1. Ensure your Neo4j instance is running.
2. From the root folder, run the command `python flask/app.py`. This will start the Flask development environment.
3. Open a seperate terminal, and from the root folder run `cd frontend` to navigate into the `frontend` directory.
4. Run `npm run start` to start the frontend.
5. You can view the program by navigating to `https://localhost:3000/` in your web browser.
    - NOTE: Check the terminal after running `npm run start` to ensure that it lists `https://localhost:3000/`. On some devices, the development environment may run on `https://localhost:3001/` due to port configurations.

Alternatively on Mac & Linux, in the root folder for Project3 run the command `./start.sh`. This shell script will start the developer environment for you. Please note that your Neo4j database instance will have to be active before running this script in order for it to work properly.