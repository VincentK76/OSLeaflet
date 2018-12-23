# OSLeaflet

[Leaflet](https://leafletjs.com/) is the leading open-source JavaScript library for mobile-friendly interactive maps. Weighing just about 38 KB of JS, it has all the mapping features most developers ever need. The current version implemented is 1.3.4.

This component will try to have most features available in time. If you want to join with developing this component then please join the team.

The primary development efforts will be Web first. After this is complete (or my priorities need to change) I will then focus on Mobile and make the Map more interactive.

Forge UR: <TODO - Add url when published>  
Demo page: <TODO - Add url when available on private environment>

## How to use

The leaflet map component needs to dropped into an container. This containers needs an name and a height. The height is important because Leaflet needs to know how much vertical space it can use.

The following properties are required;

- ContainerID: ID of the container in which the Leaflet map is dropped
- StartLatitude: Latitude the map will center on
- StartLongitude: Longitude the map will center on
- StartZoom: The zoom level the map will begin with
- MaxZoom: The maximum zoom level the map will allow (depends mostly on your used map provider)

The following properties are optional;

- TileLayer: Specify a different map provider. Find usable [here](https://leafletjs.com/plugins.html#basemap-providers)
- Attribution: Small text to display at the bottom right of the map
- LeafletMapName: Name of the leaflet map. Usable when you need to use multiple maps in the same screen.

## (soon to be) Supported options

### UI Layers

- [Marker](Feature-Marker.md)
- Popup
- Tooltip

### Raster Layers

- TileLayer
- ImageOverlays
- VideoOverlays

### Vector Layers

- Polyline
- Polygon
- Rectangle
- Circle
- CircleMarker

### Other Layers

- LayerGroup
- FeatureGroup
- GeoJson

### Basic Types

- Icon
- DivIcon

### Functions

- FitBounds

## FAQ

Q. Why are not all features of leaflet supported?
A. The features that (will be) supported are the ones that I need most in my applications, this will also prioritize the development. If you need features that are not available (yet) then please join the team!

Q. After loading not all tiles of the Leaflet component are visible. Leaflet only renders all tiles after a resize of the window.
A. This is known issue with Leaflet maps. This is due to the fact that the map is first hidden (with an If block for instance) and later made visible. This also happens requently in [SilkUI](https://silkui.outsystems.com/) websites. To show all tiles after such action use the Draw\InvalidateSize Server Action.
