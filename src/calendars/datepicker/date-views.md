# Start and Depth View

The DatePicker has the following predefined views
that provides a flexible way to navigate back and forth to select the date.

| **View** | **Description** |
| --- | --- |
| month (default) | Displays the days in a month |
| year | Displays the months in a year |
| decade | Displays the years in a decade |

## Start view

You can use the [`start`](https://help.syncfusion.com/cr/cref_files/aspnetcore-js2/aspnetcore/Syncfusion.EJ2~Syncfusion.EJ2.Calendars.DatePicker~Start.html) property to define the initial rendering view.

The following example demonstrates how to create a DatePicker with `decade` as initial rendering view.

{% aspTab template="datepicker/view/start" %}

{% endaspTab %}

## Depth view

Define the [`depth`](https://help.syncfusion.com/cr/cref_files/aspnetcore-js2/aspnetcore/Syncfusion.EJ2~Syncfusion.EJ2.Calendars.DatePicker~Depth.html) property to control the view navigation.

> Always the depth view has to be smaller than the start view, otherwise the view restriction
will be not restricted.

The following example demonstrates how to create a DatePicker that allows users to select a month.

{% aspTab template="datepicker/view/depth" %}

{% endaspTab %}

> To know more about Calendar views refer the Calendar's
[Calendar Views](../calendar/calendar-views.html)
section.