# OSLeaflet

[Leaflet](https://leafletjs.com/) is the leading open-source JavaScript library for mobile-friendly interactive maps. Weighing just about 38 KB of JS, it has all the mapping features most developers ever need. The current version implemented is 1.3.4.

This component will try to have most features available in time. If you want to join with developing this component then please join the team.

The primary development efforts will be Web first. After this is complete (or my priorities need to change) I will then focus on Mobile and make the Map more interactive.

Forge UR: <TODO - Add url when published>  
Demo page: <TODO - Add url when available on private environment>

## How to use

The leaflet map component can be dropped anywhere. The webblock accepts several options but requires only one namelijk the height. The height can be supplied in regular HTML formats like "500px".

The following properties are required;

- MapHeight: Height of the map. You must also specify the height unit. For example "450px" or "30%"
- StartLatitude: Latitude the map will center on. Default is 0.
- StartLongitude: Longitude the map will center on. Default is 0.
- StartZoom: The zoom level the map will begin with. Default is 0.
- TileLayer: The struture that defines a tilelayer including its source and maximum zoom. Default leaflet will use the OpenStreetMap.Mapnik map.
- LeafletMapName: The name of the map used internally. If you supply a different name then be sure to supply the same name for all objects and functions as well. The default name is "OSLeafletMap".

## (soon to be) Supported options

### UI Layers

- Marker
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

- BindPopUp
- FitBound \*
- FitBounds
- FitBoundsOfObject \*
- FitWorld
- FlyTo
- FlyToBounds
- GetBoundsOfPoints
- Hide
- InvalidateSize
- InvalidateSizeWithZoomPanOptions \*
- PanBy
- PanTo
- Redraw
- SetMaxBounds
- SetMaxZoom
- SetMinZoom
- SetTileLayer
- SetView
- SetZoom
- Show
- Stop
- ZoomIn
- ZoomOut

\*: Extra functions that are not wrapped of LeafletJS but are used to support a different usecase.

### Events

- OnClick
- OnDblClick
- OnMouseMove
- OnMouseOut
- OnMouseOver

## Structures

More information about the structures in Leaflet please check [this page](Structures.md).

## FAQ

**Q:** Why are not all features of leaflet supported?  
**A:** The features that (will be) supported are the ones that I need most in my applications, this will also prioritize the development. If you need features that are not available (yet) then please join the team!

**Q:** After loading not all tiles of the Leaflet component are visible. Leaflet only renders all tiles after a resize of the window.  
**A:** This is known issue with Leaflet maps. This is due to the fact that the map is first hidden (with an If block for instance) and later made visible. This also happens requently in [SilkUI](https://silkui.outsystems.com/) websites. To show all tiles after such action use the Draw\InvalidateSize Server Action.

**Q:** I want to toggle certain leaflet objects from view. How can I do that?  
**A:** First create the object (an marker for instance) and then use the Hide and Show functions to toggle its visibility.
