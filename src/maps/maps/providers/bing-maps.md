# Bing Maps

Bing Maps is a online Maps provider, owned by Microsoft. As like OSM, it provide Maps tile images based on our requests and combines those images into a single one to display Maps area.

## Adding Bing Maps

The Bing Maps can be rendered by setting the `LayerType` property as **Bing** and the key for the Bing Maps must be set in the [`Key`](../api/maps/layerSettingsModel/#key) property. The Bing Maps key can be obtained from [here](https://www.microsoft.com/en-us/maps/create-a-bing-maps-key).

{% aspTab template="maps/map-providers/bing", sourceFiles="bing.cs" %}

{% endaspTab %}

>Specify Bing Maps key in the `key` property.

## Types of Bing Maps

Bing Maps provides different types of Maps and it is supported in the Maps component.

* **Aerial** - Displays satellite images to highlight roads and major landmarks for easy identification.
* **AerialWithLabel** - Displays aerial Maps with labels for the continent, country, ocean, etc.
* **Road** - Displays the default Maps view of roads, buildings, and geography.
* **CanvasDark** - Displays dark version of the road Maps.
* **CanvasLight** - Displays light version of the road Maps.
* **CanvasGray** - Displays grayscale version of the road Maps.

To render the light version of the road Maps, set the `BingMapType` to `CanvasLight` as demonstrated in the following code sample.

{% aspTab template="maps/map-providers/bing", sourceFiles="bing.cs" %}

{% endaspTab %}

>Specify Bing Maps key in the `key` property.

## Zooming and Panning

Bing Maps layer can be zoomed and panned. Zooming helps to get a closer look at a particular area on a Maps for in-depth analysis. Panning helps to move a Maps around to focus the targeted area.

{% aspTab template="maps/map-providers/bingzoom", sourceFiles="bingzoom.cs" %}

{% endaspTab %}

>Specify Bing Maps key in the `key` property.

## Adding markers and navigation line

Markers can be added to the layers of Bing Maps by setting the corresponding location's coordinates of latitude and longitude using `MarkerSettings`. Navigation lines can be added on top of an Bing Maps layer for highlighting a path among various places by setting the corresponding location's coordinates of latitude and longitude in the `NavigationLineSettings`.

{% aspTab template="maps/map-providers/bingmarker", sourceFiles="bingmarker.cs" %}

{% endaspTab %}

>Specify Bing Maps key in the `Key` property.

## Sublayer

Any GeoJSON shape can be rendered as a sublayer on top of the Bing Maps layer for highlighting a particular continent or country in Bing Maps by adding another layer and specifying the [`type`](../api/maps/layerSettingsModel/#type) property of Maps layer to **SubLayer**.