# Visualizing Your First Dataset With Project3

In this tutorial, we will walk you through how to visualize your first dataset, a simple but relatively large network based after the novel Frankenstein, using Project3.

## Set-Up

Project3 is currently in its alpha development phase. Reference our [developer documentation "How To Start The Project3 Development Environment" article here](../../developerDocs/task/basics/developmentEnv.md) to set up the Project3 environment on your local machine.

## What You Will Need

In order to visualize your first dataset, you will need the following:
- The Project3 Developer Environment set-up
- An empty Neo4j database instance

## Setting Up Neo4j Instance

Now that we have the environment set-up, we can begin visualizing our dataset! We will be using a network dataset based after the novel Frankenstein. It's a relatively simple network (undirected and unweighted); however as you will find it is significantly large, containing over 413,000 nodes!

Before we can visualize our dataset, we need to add the data to our empty Neo4j database instance. We recommend the following workflow.
1. In the root folder for Project3, run the command `python flask/demo_files/frankenstein_demo/setup_demo.py`
2. Wait for the run to exit
    - This process can take up to 10-20 minutes, as the Frankenstein dataset contains a signficant amount of data

## Visualization

Now that we have our demo set up, we can finally visualize the dataset and get an idea of what Project3 can do.

First, you will need to start the Project3 developer environment via the following workflow:
1. Ensure your Neo4j instance is running
2. From the root folder, run the command `python flask/app.py`. This command starts the Flask development environment
3. Open a seperate terminal, and from the root folder run `cd frontend` to navigate into the `frontend` directory
4. In the new terminal, run `npm run start` to start the frontend

Alternatively, on Mac & Linux, in the root folder for Project3 run the command `./start.sh`. This shell script will start the developer environment for you. Please note that your Neo4j database instance must be active before running this script in order for it to work properly.

Now, you can view the program by navigating to `https://localhost:3000/` in your web browser. NOTE: Check that the terminal after running `npm run start` to ensure that it lists `https://localhost:3000/`. On some devices, the development environment may run on `https://localhost:3001/` due to default port configurations.

## Entering Project3

When you start Project3, you should be met with the following in your UI:

![Intial Open](images/random_out.png)

You can zoom in using the `+` and `-` keys on your keyboard. Alternatively, if you are using a device with a trackpad, you can pinch and spread your fingers to zoom both in and out. Zoom out, and you'll be able to see that you're actually looking at a network composed of thousands of nodes:

![Zoom](images/random_zoom.png)

## Changing Layouts

Now that we know that our dataset's rendering properly, let's try changing the layout to see what happens. Navigate to the Layout Selector labeled "Random" in the upper left hand corner of the screen:

![Layout Selector](images/querybar.png)

From here, we can change the layout:

![Layouts](images/layouts.png)

1. Click the Layout Selector to reveal the current list of available layout options
2. From the dropdown, click your desired layout option (we'll choose "Grid" for this example)
3. A message labeled "Rendering with new layout..." will appear while data populates
4. The data will now be rendered on screen

![Grid Layout](images/grid_layout.png)

Congratulations, you've just rendered a network composed of hundreds of thousands of nodes in your web browser!

## Further Reading

Now that you've explored how to visualize a dataset with Project3, it's time to learn more about the different analysis options you have! We recommend referring to our [Cypher Querying article here](../howto/querying/CypherQuerying.md) to learn more about how to query your data with Cypher in Project3.
