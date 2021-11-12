---
title: "Calendar Mode in ASP.Net MVC Scheduler"
component: "Scheduler"
description: "This section explains how to change the default calendar mode on Scheduler to display it either on Gregorian or Islamic mode."
---

# Calendar mode

The Scheduler supports the following two types of calendar mode.

* Gregorian Calendar
* Islamic Calendar

## Gregorian Calendar

The Scheduler by default displays the gregorian calendar dates which is the most widely used calendar in the world. The Gregorian calendar is a solar calendar which has 12 months with 28 to 31 days each. A year which is divisible by four is said to be a leap year in this calendar mode. A leap year usually has 366 days whereas the regular year has 365 days.

## Islamic Calendar

The Islamic Calendar, also known as the Hijri or Muslim calendar, is a lunar calendar which has 12 months in a year with 354 or 355 days. Each month of this calendar denotes the birth of the new lunar cycle and therefore, each month can have 29 or 30 days depending on the visibility of the moon. Here, the odd-numbered months have 30 days and the even months have 29 days.

> The current Islamic year is 1440 AH. Usually the Gregorian calendar runs from approximately 11 September 2018 to 30 August 2019 for this 1440 AH year.

The Scheduler has a property `CalendarMode` which is used to switch between the gregorian and islamic calendar modes. By default, it is set to `Gregorian` and to use it with Islamic calendar dates, define the `CalendarMode` of Scheduler to `Islamic`. The following example depicts, how to display the Islamic calendar dates on Scheduler.

It requires the following CLDR data to be loaded using loadCldr function.

* numberingSystems.json
* ca-gregorian.json
* numbers.json
* timeZoneNames.json
* ca-islamic.json

> To know more information on, how to install the CLDR data, refer the [`Internationalization`](https://ej2.syncfusion.com/aspnetmvc/documentation/common/internationalization/#installing-cldr-data) topic.

{% aspTab template="schedule/islamic-calendar/calendar", sourceFiles="data.cs"  %}

{% endaspTab %}

**Note:** However, this feature does not yet support recurrence options, which we are planning to add them in the next release.

> You can refer to our [ASP.NET MVC Scheduler](https://www.syncfusion.com/aspnet-mvc-ui-controls/scheduler) feature tour page for its groundbreaking feature representations. You can also explore our [ASP.NET MVC Scheduler](https://ej2.syncfusion.com/aspnetmvc/Schedule/Overview#/material) example to knows how to present and manipulate data.
