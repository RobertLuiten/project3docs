# Style Guide

Project3 can be a complex project at times, so as such it's essential to ensure that your code is clear, well commented, and understandable such that the other people on our development team will be able to understand it.

We don't have many guidelines in place currently due to the size of the project, however for the few we do have it's essential that we follow them in order to ensure a smooth development experience for everybody.

## Variable Names
The convention for variable names in Project3 differs depending on if you're working in the backend (Flask) or frontend (React) of the project.

## Global Variables
In all contexts, global variables must be written in all caps and in `snake_case`, and have a name that clearly indicates what they are representing. For example, a Neo4j password might be styled as `NEO4J_PASSWORD`.

### Variables in Flask
Variables and arguments in the Flask server must utilize `snake_case`, and have a name that clearly indicates what they are representing. Avoid using variable names such as `x` or `var_1` outside of contexts such as for-loops; rather, make the name itself a short description (i.e. `query_string`, `layout_type`, `running_sum`).

### Variables in React
Variables and arguments in React must utilize `camelCase`, and similarly to the Flask server have a name clearly indicates what they are representing. Avoid using variable names such as `x` or `var1` outside of contexts such as for-loops; rather, make the name itself a short description (i.e. `queryString`, `layoutType`, `runningSum`).

For React states, ensure the "set" variable has the same name as the main variable, just with the word `set` at the front. For example, the variable `exampleVar` should have the state setting variable `setExampleVar` paired with it. Please note that this alters the casing of the original variable.

## Function Names
Function names in Project3 must use `snake_case` in order to maintain consistency, and have a name which indicates what they are intended to be used for (i.e. `get_coordinates`).

## Commenting
Since Project3 is an open-source project, commenting is crucial in order to ensure the continuation and interpretability of our codebase. Comments are mandatory for all functions, global variables, and React states, and must adhere to the following requirements:

### Functions
All functions, regardless of usage or scope, should have comments that contain the following information in the following order:
- A brief description of what the function is intended for
- What arguments the function takes, along with the type and a brief description for each.
- What the function returns, including a brief description and it's return type.

#### Good Example of Function Comments:
```
    def visualize_igraph(layout_type: str = "random", query_string: str = """MATCH (n)-[r]->(m) RETURN n.id AS source, m.id AS target""", limit: int = 1000000):
    """
    Generates an igraph layout for a graph based on the data in 'frank_data.csv'.

    args:
        layout_type (str): The type of layout to use. Supports most layouts listed in igraph documentation.
            Please note that the input is simply the last word in the function name (i.e. to use "igraph.layout_random", use "random" as the input).
            Defaults to "random", and has following options:
            - default (if coordinates exist, will return "grid" layout if otherwise)
            - random
            - circle
            - fruchterman_reingold
            - star
            - grid
            - kamada_kaway
            - graphopt
            - drl
            - davidson_harel
            - sugiyama

    returns:
        JSON response with a tuple containing node data & edge data.
    """    
```

#### Bad Example of Function Comments
```
    """
    def visualize_igraph(layout_type: str = "random", query_string: str = """MATCH (n)-[r]->(m) RETURN n.id AS source, m.id AS target""", limit: int = 1000000):
    """

    args:
        layout_type: the layout type

    returns:
        JSON
    """    
```

Notice how the bad example doesn't contain a description function, variable types, or a good description for the return? This quickly leads to unclear code!

For Python, this is the template we recommend:
```
    (Brief description of the function)

    args:
        (Insert list of args w/ typeshere)

    returns:
        (Insert return type with description here)
    """    
```

### Global Variables
All global variables must have a brief description of their purpose and usage to ensure clarity for developers later on.

#### Good Global Variable Comment Example
```
# The Password used for the Neo4j database instance
NEO4J_PASSWORD = "PASSWORD_HERE123"
```

#### Bad Global Variable Comment Example
```
\\ The query
QUERY = "id"
```

See how the bad example doesn't provide a clear indication for what it's being used for in its description?

### React States
Like local variables, all React States, global or not, must have a brief description of their purpose and usage. Use the `/** */` comment brackets when making comments for React hooks to ensure consistency with comments which may take up multiple lines.

#### Good React State Comment Example
```
/** The graph layout to be utilized by Neo4j */
const [layout, setLayout] = useState("random");
```

#### Bad React State Comment Example
```
// Layout
const [layout, setLayout] = useState("random");
```

See how the bad example uses the single line `//` brackets and doesn't provide a clear description of the variable's usage? We want to avoid this!