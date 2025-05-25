# visualize_igraph

## visualize_igraph(layoutType: str, query_string: str, limit: int=1000000)

### Returns 
The results of a Neo4j query with the specified layout type (generated with igraph) in a JSON tuple of the form (`nodeData`, `edgeData`).

### Args
#### layoutType: str
The layout type of the returned data. Can be one of the following:
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

#### query_string: str
The Neo4j query to return from the database.

#### limit: int (OPTIONAL)
The amount of nodes to return from the query (defaults to 1,000,000).

## Errors
Throws `500: Layout Not Found` error if layout is not from the specified list above.

## Usage

```
    fetch(`${FLASK_URI}/getlayout/${layout_type}/${query_string}/${limit}`)
      .then(response => {
        if (!response.ok) throw new Error('Network error');
        return response.json();
      })
      .then((data) => {
        console.log(query);
        setNodes(data[0]);
        setEdges(data[1]);
      })
      .catch(error =>
        console.error('There has been a problem with your fetch operation:', error)
      );
```