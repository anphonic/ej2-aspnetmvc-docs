# Bubbles

Bubbles in the Maps control represent the underlying data values of the Maps. It can be scattered throughout the Maps shapes that contain values in the data source. Bubbles are enabled by setting the `Visible` property of `MapsBubble` to **true**. To add bubbles to the Maps, bind the data source to the `DataSource` property of `MapsBubble` and set the field name, that contains the numerical data, in the data source to the `ValuePath` property.

{% aspTab template="maps/bubble/bubble", sourceFiles="bubble.cs" %}

{% endaspTab %}

![Bubbles](./images/Bubble/bubble.PNG)

## Bubble shapes

The following types of shapes are available to render the bubbles in Maps.

* Circle
* Square

By default, bubbles are rendered in the **Circle** type. To change the type of the bubble, set the `BubbleType` property of `MapsBubble` as **Square** to render the square shape bubbles.

{% aspTab template="maps/bubble/bubble-shape", sourceFiles="bubble-shape.cs" %}

{% endaspTab %}

![Bubble shape](./images/Bubble/bubble-shape.PNG)

## Customization

The following properties are available in `MapsBubble` to customize the bubbles of the Maps component.

* `Border` – To customize the color, width and opacity of the border of the bubbles in Maps.
* `Fill` – To apply the color for bubbles in Maps.
* `Opacity` – To apply opacity to the bubbles in Maps.
* `AnimationDelay` - To change the time delay in the transition for bubbles.
* `AnimationDuration` - To change the time duration of animation for bubbles.

{% aspTab template="maps/bubble/bubble-customization", sourceFiles="bubble-customization.cs" %}

{% endaspTab %}

![Bubble customization](./images/Bubble/bubble-customization.PNG)

## Setting colors to the bubbles from the data source

The color for each bubble in the Maps can be set using the `ColorValuePath` property of `MapsBubble`. The value for the `ColorValuePath` property is the field name from the data source of the `MapsBubble` which contains the color values.

{% aspTab template="maps/bubble/bubble-valuepath", sourceFiles="bubble-valuepath.cs" %}

{% endaspTab %}

![Bubble valuepath](./images/Bubble/bubble-valuepath.PNG)

## Setting the range of the bubble size

The size of the bubbles is calculated from the values got from the `ValuePath` property. The range for the radius of the bubbles can be modified using `MinRadius` and `MaxRadius` properties.

{% aspTab template="maps/bubble/bubblesize", sourceFiles="bubblesize.cs" %}

{% endaspTab %}

![Bubble shape](./images/Bubble/bubble-sizing.PNG)

## Multiple bubble groups

Multiple groups of bubbles can be added in the Maps by adding multiple `MapsBubble` in the `MapsBubbles` and customization for the bubbles can be done with the `MapsBubble` class. In the following example, the gender-wise population ratio is demonstrated with two different bubble groups.

{% aspTab template="maps/bubble/multiple-bubble", sourceFiles="multiple-bubble.cs" %}

{% endaspTab %}

![Bubble shape](./images/Bubble/multiple-bubble.PNG)

## Enable tooltip for bubble

The tooltip for the bubbles can be enabled by setting the `Visible` property of the `MapsTooltipSettings` as **true**. The content for the tooltip can be set using the `ValuePath` property in the `MapsTooltipSettings` of the `MapsBubble` where the value for the `ValuePath` property is the field name from the data source of the `MapsBubble`. Any HTML element can be added as the template in tooltip using the `Template` property.

{% aspTab template="maps/bubble/bubble-tooltip", sourceFiles="bubble-tooltip.cs" %}

{% endaspTab %}

![Enable tooltip for bubble](./images/Bubble/bubble-tooltip.PNG)