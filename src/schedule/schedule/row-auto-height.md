---
title: "Auto row height in ASP.Net MVC Scheduler"
component: "Scheduler"
description: "This section shows the way to auto-adjust the height of the work-cells of Scheduler based on the number of appointments present in those time ranges."
---

# Row Auto Height

By default, the height of the Scheduler rows in Timeline views are static and therefore, when the same time range holds multiple overlapping appointments, a `+n more` text indicator will be displayed. With this feature enabled, you can now view all the overlapping appointments present in those specific time range by auto-adjusting the row height based on the presence of the appointments count, instead of displaying the `+n more` text indicators.

To enable auto row height adjustments on Scheduler Timeline views and Month view, set `true` to the `rowAutoHeight` property whose default value is `false`.

> This auto row height adjustment is applicable only on all the Timeline views as well as on the calendar Month view.

Now, let's see how it works on those applicable views with examples.

## Calendar month view

By default, the rows of the calendar Month view can hold only the limited appointments count based on its row height, and the rest of the overlapping appointments are indicated with a `+n more` text indicator. The following example shows how the month view row auto-adjusts based on the number of appointments count, when this `RowAutoHeight` feature is enabled.

{% aspTab template="schedule/row-auto-height/month-view", sourceFiles="data.cs"  %}

{% endaspTab %}

## Timeline views

When the feature `RowAutoHeight` is enabled in Timeline views, the row height gets auto-adjusted based on the number of overlapping events occupied on the same time range, which is demonstrated in the following example.

{% aspTab template="schedule/row-auto-height/timeline-view", sourceFiles="data.cs"  %}

{% endaspTab %}

## Timeline views with multiple resources

The following example shows how the auto row adjustment feature works on timeline views with multiple resources.

{% aspTab template="schedule/row-auto-height/timeline-resource", sourceFiles="data.cs"  %}

{% endaspTab %}

## Appointments occupying entire cell

By default, with the feature `RowAutoHeight`, there will be a space in the bottom of the cell when appointment is rendered. To avoid this space, we can set true to the property `IgnoreWhitespace` with in `EventSettings` whereas its default property value is false. In the following code example, the whitespace below the appointments has been ignored.

{% aspTab template="schedule/row-auto-height/ignore-whitespace", sourceFiles="data.cs"  %}

{% endaspTab %}

**Note**: The property `IgnoreWhitespace` will be applicable only when `RowAutoHeight` feature is enabled in the Scheduler

> You can refer to our [ASP.NET MVC Scheduler](https://www.syncfusion.com/aspnet-mvc-ui-controls/scheduler) feature tour page for its groundbreaking feature representations. You can also explore our [ASP.NET MVC Scheduler](https://ej2.syncfusion.com/aspnetmvc/Schedule/Overview#/material) example to knows how to present and manipulate data.
