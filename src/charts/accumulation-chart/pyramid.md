---
title: "Pyramid | ASP.NET MVC "

component: "Accumulation Chart"

description: "The pyramid chart displays series value as progressively decreasing amount to hundred percent in total"
---

# Pyramid Chart

To render a pyramid series, use the series [`Type`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.AccumulationSeries.html#Syncfusion_EJ2_Charts_AccumulationSeries_Type)
as `Pyramid`.

{% aspTab template="chart/accumulation-charts/pyramid/default", sourceFiles="default.cs" %}

{% endaspTab %}

## Mode

The Pyramid chart supports linear and surface modes of rendering. The default type of the
`PyramidMode` is `Linear`.

{% aspTab template="chart/accumulation-charts/pyramid/mode", sourceFiles="mode.cs" %}

{% endaspTab %}

## Size

The size of the pyramid chart can be customized by using the  `Width` and `Height` properties.

{% aspTab template="chart/accumulation-charts/pyramid/size", sourceFiles="size.cs" %}

{% endaspTab %}

## Gap Between the Segments

Pyramid chart provides options to customize the space between the segments by using the `GapRatio` property of the
series. It ranges from 0 to 1.

{% aspTab template="chart/accumulation-charts/pyramid/gap", sourceFiles="gap.cs" %}

{% endaspTab %}

## Explode

Points can be exploded on mouse click by setting the `Explode` property to true. You can also explode the point
on load using `ExplodeIndex`. Explode distance can be set by using `ExplodeOffset` property.

{% aspTab template="chart/accumulation-charts/pyramid/explode", sourceFiles="explode.cs" %}

{% endaspTab %}

## Customization

Individual points can be customized using the `PointRender` event.
{% aspTab template="chart/accumulation-charts/pyramid/custom", sourceFiles="custom.cs" %}

{% endaspTab %}

## See Also

* [Data label](./data-label/)
* [Grouping](./grouping/)