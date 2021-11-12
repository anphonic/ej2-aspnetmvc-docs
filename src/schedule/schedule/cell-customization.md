---
title: "Customizing Scheduler Cells"
component: "Scheduler"
description: "This topic demonstrates how to customize the cells of Scheduler using template option, methods and events available in Scheduler."
---

# Cell Customization

The cells of the Scheduler can be easily customized either using the cell template or `RenderCell` event.

## Setting cell dimensions in all views

The height and width of the Scheduler cells can be customized either to increase or reduce its size through the `CssClass` property, which overrides the default CSS applied on cells.

{% aspTab template="schedule/customization/cell-dimensions", sourceFiles="data.cs"  %}

{% endaspTab %}

## Check for cell availability

You can check whether the given time range slots are available for event creation or already occupied by other events using the `isSlotAvailable` method. In the following code example, if a specific time slot already contains an appointment, then no more appointments can be added to that cell.

{% aspTab template="schedule/customization/cell-availability", sourceFiles="data.cs"  %}

{% endaspTab %}

## Customizing cells in all the views

It is possible to customize the appearance of the cells using both template options and `RenderCell` event on all the views.

### Using template

The `CellTemplate` option accepts the template string and is used to customize the cell background with specific images or appropriate text on the given date values.

{% aspTab template="schedule/customization/cell-customization", sourceFiles="data.cs"  %}

{% endaspTab %}

### Using renderCell event

An alternative to `CellTemplate` is the `RenderCell` event, which can also be used to customize the cells with appropriate images or formatted text values.

{% aspTab template="schedule/customization/element-customization", sourceFiles="data.cs"  %}

{% endaspTab %}

You can customize cells such as work cells, month cells, all-day cells, header cells, resource header cells using `RenderCell` event by checking the `elementType` option within the event. You can check `elementType` with any of the following.

| Element type | Description |
|-------|---------|
| `dateHeader` | triggers on header cell rendering.|
| `monthDay` | triggers on header cell in month view rendering.|
| `resourceHeader` | triggers on resource header cell rendering.|
| `alldayCells` | triggers on all day cell rendering.|
| `emptyCells` | triggers on empty cell rendering on header bar.|
| `resourceGroupCells` | triggers on rendering of work cells for parent resource.|
| `workCells`| triggers on work cell rendering.|
| `monthCells` | triggers on month cell rendering.|
| `majorSlot` | triggers on major time slot cell rendering.|
| `minorSlot` | triggers on minor time slot cell rendering.|
| `weekNumberCell` | triggers on cell displaying week number.|

## Customizing cell header in month view

The month header of each date cell in the month view can be customized using the `CellHeaderTemplate` option which accepts the string or HTMLElement. The corresponding date can be accessed with the template.

{% aspTab template="schedule/customization/cell-header-customization" %}

{% endaspTab %}

![Month view cell header template](../../schedule/images/cell-header-template.png)

## Customizing the minimum and maximum date values

Providing the `minDate` and `maxDate` property with some date values, allows the Scheduler to set the minimum and maximum date range. The Scheduler date that lies beyond this minimum and maximum date range will be in a disabled state so that the date navigation will be blocked beyond the specified date range.

{% aspTab template="schedule/customization/date-customization", sourceFiles="data.cs"  %}

{% endaspTab %}

>By default, the `minDate` property value is set to new Date(1900, 0, 1) and `maxDate` property value is set to new Date(2099, 11, 31). The user can also set the customized `minDate` and `maxDate` property values.

## How to disable multiple cell and row selection in Schedule

By default, the `AllowMultiCellSelection` and `AllowMultiRowSelection` properties of the Schedule are set to `true`. So, the Schedule allows user to select multiple cells and rows. If the user want to disable this multiple cell and row selection. The user can disable this feature by setting up `false` to these properties.

> You can refer to our [ASP.NET MVC Scheduler](https://www.syncfusion.com/aspnet-mvc-ui-controls/scheduler) feature tour page for its groundbreaking feature representations. You can also explore our [ASP.NET MVC Scheduler](https://ej2.syncfusion.com/aspnetmvc/Schedule/Overview#/material) example to knows how to present and manipulate data.
