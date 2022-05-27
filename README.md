# Mapping_Earthquakes

## Basic Project Plan
### Purpose
The purpose of this project is to visually show the differences between the magnitudes of earthquakes all over the world for the last seven days. The map presented will include three different visual style options, and will include overlays to present all earthquakes over the past 7 days, the tectonic plate lines, and the earthquakes of magnitude greater than 4.5 over the past 7 days. Each overlay will be independently displayed with the option to remove the overlay.

### Tasks
First, the initial configuration was completed as part of the module work, which included displaying the base map, with the overlay of earthquakes over the past 7 days. The default base map was of the streets styling from [Mapbox Styles](https://docs.mapbox.com/api/maps/styles/), with the option to change to a sattelite view. The earthquake data was presented in such a way as to colour code each earthquake by magnitudes, and the area of the marker displayed increased as the magnitude increased. A legend was included to indicate the magnitude ranges which were representative of the colours displayed on the map.

Second, a new overlay was created to display the tectonic plate lines, as found [at this GitHub repository](https://github.com/fraxen/tectonicplates/blob/master/GeoJSON/PB2002_boundaries.json). The raw json data url was passed through a D3.json call, with additional styling implemented to allow for the tectonic plate lines to be visible on all maps. Additionally, the tectonic plate lines were bound to a popup which would display the plate boundaries. This popup was not a requirement of the assignment and was added as extra practice with the method.

Third, an additional overlay was created to represent the earthquakes with magnitudes greater than 4.5 within the past 7 days. The raw json information was drawn from the USGS government website at [this link](https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/4.5_week.geojson). The overlay was created to display information independently of the original earthquakes data. Additional styling was performed to the data similar to the overlay for all earthquakes, with some notable changes:
- only 3 magnitude ranges were used for styling
    - greater than 6
    - greater than 5
    - less than 5
- earthquakes with magnitudes greater than 6 were styled with a darker red colour
- the original colour styles for earthquakes less than 5 and greater than 5 were kept consistent with the existing legend

Finally, one additional map styling was added to the base map options. The map styling chosen was the Dark map style. The default base map was unchanged from the Streets map style. 
