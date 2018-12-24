# Structures

The leaflet component uses different structures to perform its actions. This page describes structures types. When possible the names of these structures are the same name as the Leaflet counterpart.

## Point

Contains 2 decimals (latitude and longitude) that point to a certain coordinate.  
![Point](/images/Structure-Point.jpg)

## LatLongBounds

Contains 2 points that specify the boundary of an box. This is used mostly by FitBounds methods.  
![LatLongBounds](/images/Structure-LatLongBounds.jpg)

## Marker

Defines a marker on the map. Most properties can be defined straight from this marker like a Popup.  
![Marker](/images/Structure-Marker.jpg)

## FeatureGroupMarkers

A collection of Markers. This can be used to combine all markers to a single entity. This can be used to perform certain actions with all markers at once.  
![FeatureGroupMarker](/images/Structure-FeatureGroupMarkers.jpg)
