# get_coordinates

## get_coordinates(query_string: str, limit: int=1000000)

### Returns 
The results of a Neo4j query with geocoordinates in a JSON tuple of the form (`nodeData`, `edgeData`).

### Args
#### query_string: str
The Neo4j query to return from the database.

#### limit: int (OPTIONAL)
The amount of nodes to return from the query (defaults to 1,000,000).

## Usage

```
      const QUERY = "MATCH (n) RETURN n.latitude AS lat, n.longitude AS lon"
      fetch(`${FLASK_URI}/getcoordinates/${QUERY}`)
      .then(response => {
        if (!response.ok) throw new Error('Network error');
        return response.json();
      })
      .then((data) => {
        console.log(data[0]);
        setNodes(data[0]);
        setEdges(data[1]);
      })
      .catch(error =>
        console.error('There has been a problem with your fetch operation:', error)
      );
```