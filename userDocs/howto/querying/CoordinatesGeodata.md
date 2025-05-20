# Geocoordinate Data In Project3

In this article, we will discuss how to add data with geocoordinates to Project3.

## Geocoordinate Info

In order to properly add geocoordinate info, you will need to ensure the following:
1. That coordinate fields in the Neo4j database instance are titled "Lat1" and "Long1".
2. That coordinate fields in the Neo4j database instance are titled "Lat2" and "Long2" for connecting nodes for proper edge rendering.

## Render Geocoordinates

In order the data with geocoordinates, you will need to select the "Default" option from the Layout Selector:

![The Layout Selector](images/querybar.png)
1. Click the Layout Selector to reveal the current list of avalible layout options.
2. From the dropdown, select "Default".
3. A message labeled "Rendering with new layout..." will appear while data populates.
4. After a moment, the data with geocoordinate based layout will be rendered on screen.

You can switch the layout to another, non-coordinate based layout as well:
1. Click the Layout Selector to reveal the current list of avalible layout options.
2. From the dropdown, click your desired layout option.
3. A message labeled "Rendering with new layout..." will appear while data populates.
4. After a moment, the data with new layout will be rendered on screen.