---
title: " Stock Chart Crosshair  | ASP.NET MVC "

component: "Stock Chart"

description: "Crosshair has a vertical and horizontal line to view the value of the axis at mouse position.The trackball used to display data collections"
---

# Add Crosshair

Crosshair has a vertical and horizontal line to view the value of the axis at mouse or touch position.

Crosshair lines can be enabled by using [`Enable`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.ChartCrosshairSettings.html#Syncfusion_EJ2_Charts_ChartCrosshairSettings_Enable)
property in the `Crosshair`.

{% aspTab template="stock-chart/user-interaction/crosshair-trackball/crosshair", sourceFiles="crosshair.cs" %}

{% endaspTab %}

## Tooltip for axis

Tooltip label for an axis can be enabled by using [`Enable`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.ChartCrosshairTooltip.html#Syncfusion_EJ2_Charts_ChartCrosshairTooltip_Enable)
property of `CrosshairTooltip` in the corresponding axis.

{% aspTab template="stock-chart/user-interaction/crosshair-trackball/axis-tooltip", sourceFiles="axis-tooltip.cs" %}

{% endaspTab %}

## Customization

The [`Fill`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.ChartSeries.html#Syncfusion_EJ2_Charts_ChartSeries_Fill)
and [`TextStyle`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.ChartCrosshairSettings.html)
property of the `CrosshairTooltip` is used to customize the background color and font style of the crosshair label
respectively. Color and width of the crosshair line can be customized by using the
[`Line`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.ChartCrosshairSettings.html#Syncfusion_EJ2_Charts_ChartCrosshairSettings_Line) property in the crosshair.

{% aspTab template="stock-chart/user-interaction/crosshair-trackball/custom", sourceFiles="custom.cs" %}

{% endaspTab %}

## Add Trackball

Trackball is used to track a data point closest to the mouse or touch position. Trackball marker indicates the
closest point and trackball tooltip displays the information about the point.

Trackball can be enabled by setting the [`Enable`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.ChartCrosshairSettings.html) property of the crosshair to true and
[`Shared`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.ChartCrosshairSettings.html) property in `Tooltip` to true in chart.

{% aspTab template="stock-chart/getting-started/trackball", sourceFiles="trackball.cs" %}

{% endaspTab %}
