---
title: "Multiple Resources and Grouping | ASP.Net MVC Scheduler"
component: "Scheduler"
description: "This article demonstrates how to assign a single or multiple resources to events and also shows how to group them in both hierarchical and vertical mode."
---

# Multiple resources and grouping

Resources and grouping support allows the Scheduler to be shared by multiple resources. Also, the appointments of each resources are displayed under relevant resources. Each resource in the Scheduler is arranged in a column/row wise order, with individual spacing to display all its respective appointments on a single page. It also supports the multiple levels of grouping of resources, thus enabling the categorization of resources in a hierarchical structure and shows it either in expandable groups (Timeline views) or else vertical hierarchy one after the other (Calendar views).

It is also possible to assign one or more resources to the same appointment, by allowing multiple selection of resource options available in the event editor window.

The Scheduler groups the resources based on different criteria. It includes grouping appointments based on resources, grouping resources based on dates, and timeline scheduling. Also, the data for resources bind with Scheduler either as a local JSON collection or URL, retrieving data from remote data services.

## Resource fields

The default options available within the `Resources` collection are as follows,

| Field name | Type | Description |
|-------|---------| --------------- |
| `Field` | String | A value that binds to the resource field of event object. |
| `Title` | String | It holds the title of the resource field to be displayed on the event editor window. |
| `Name` | String | A unique resource name used for differentiating various resource objects while grouping. |
| `AllowMultiple` | Boolean | When set to `true`, allows multiple selection of resource names, thus creating multiple instances of same appointment for the selected resources. |
| `DataSource` | Object | Assigns the resource `DataSource`, where data can be passed either as an array of JavaScript objects, or else can create an instance of [`DataManager`](http://ej2.syncfusion.com/documentation/data/api-dataManager.html) in case of processing remote data and can be assigned to the `DataSource` property. With the remote data assigned to `DataSource`, check the available [adaptors](http://ej2.syncfusion.com/documentation/data/adaptors.html) to customize the data processing. |
| `Query` | Query | Defines the external [`Query`](http://ej2.syncfusion.com/documentation/data/api-query.html) that will be executed along with the data processing. |
| `IdField` | String | Binds the resource ID field name from the resources `DataSource`. |
| `TextField` | String | Binds the text field name from the resources `DataSource`. It usually holds the resource names. |
| `GroupIDField` | String | Binds the group ID field name from the resource `DataSource`. It usually holds the value of resource IDs of parent level resources. |
| `ColorField` | String | Binds the color field name from the resource `DataSource`. The color value mapped in this field will be applied to the events of resources. |
| `StartHourField` | String | Binds the start hour field name from the resource `DataSource`. It allows to provide different work start hour for the resources. |
| `EndHourField` | String | Binds the end hour field name from the resource `DataSource`. It allows to provide different work end hour for the resources. |
| `WorkDaysField` | String | Binds the work days field name from the resources `DataSource`. It allows to provide different working days collection for the resources. |
| `CssClassField` | String | Binds the custom CSS class field name from the resources `DataSource`. It maps the CSS class written for the specific resources and applies it to the events of those resources. |

## Resource data binding

The data for resources can bind with Scheduler either as a local JSON collection or a service URL, retrieving resource data from remote data services.

### Using local JSON data

The following code example depicts how to bind the local JSON data to the `DataSource` of `Resources` collection.

* Give the resource datasource in Index method
* Add the Scheduler code in View page

{% aspTab template="schedule/resources/local-data", sourceFiles="data.cs"  %}

{% endaspTab %}

### Using remote service URL

The following code example depicts how to bind the remote data for resources `dataSource`.

* Give the resource datasource in Index method
* Add the Scheduler code in View page

{% aspTab template="schedule/resources/remote-data", sourceFiles="data.cs"  %}

{% endaspTab %}

## Scheduler with multiple resources

It is possible to display the Scheduler in default mode without visually showcasing all the resources in it, but allowing to assign the required resources to the appointments through the event editor resource options.

The appointments belonging to the different resources will be displayed altogether on the default Scheduler, which will be differentiated based on the resource color assigned in the `Resources` (depicting to which resource that particular appointment belongs) collection.

**Example:** To display default Scheduler with multiple resource options in the event editor, ignore the group option and simply define the `Resources` property with all its internal options.

{% aspTab template="schedule/resources/without-group", sourceFiles="data.cs"  %}

{% endaspTab %}

> Setting `AllowMultiple` to `true` in the above code example allows you to select multiple resources from the event editor and also creates multiple copies of the same appointment in the Scheduler for each resources while rendering.

## Resource grouping

Resource grouping support allows the Scheduler to group the resources in a hierarchical structure both as an expandable groups (Timeline views) and as vertical hierarchy displaying resources one after the other (Resources view).

Scheduler supports both single and multiple levels of resource grouping that can be customized both in timeline and vertical Scheduler views.

### Vertical resource view

The following code example displays how the multiple resources are grouped and its events are portrayed in the default calendar views.

{% aspTab template="schedule/resources/multiple-resources", sourceFiles="data.cs"  %}

{% endaspTab %}

### Timeline resource view

The following code example depicts how to group the multiple resources on Timeline Scheduler views and its relevant events are displayed accordingly under those resources.

{% aspTab template="schedule/resources/timeline-multiple-resources", sourceFiles="data.cs"  %}

{% endaspTab %}

### Grouping single-level resources

This kind of grouping allows the Scheduler to display all the resources at a single level simultaneously. The appointments mapped under resources will be displayed with the colors as per the `ColorField` defined on the resources collection.

**Example:** To display the Scheduler with single level resource grouping,

{% aspTab template="schedule/resources/single-level", sourceFiles="data.cs"  %}

{% endaspTab %}

> The `Name` field defined in the **resources** collection namely `Owners` will be mapped within the `Group` property, in order to enable the grouping option with those resource levels on the Scheduler.

### Grouping multi-level resources

It is possible to group the resources of Scheduler in multiple levels, by mapping the child resources to each parent resource. In the following example, there are 2 levels of resources, on which the second level resources are defined with `GroupIDField` mapping to the first level resource's ID so as to establish the parent-child relationship between them.

{% aspTab template="schedule/resources/timeline-multiple-resources", sourceFiles="data.cs"  %}

{% endaspTab %}

### One-to-One grouping

In multi-level grouping, Scheduler usually groups the resources on the child level based on the `GroupIDField` that maps with the `IdField` field of parent level resources (as `ByGroupID` set to true by default). There are also option which allows you to group all the child resource(s) against each of its parent resource(s). To enable this kind of grouping, set `false` to the `ByGroupID` option within the `Group` property. In the following code example, there are two levels of resources, on which all the 3 resources at the child level is mapped one to one with each resource on the first level.

{% aspTab template="schedule/resources/group-child", sourceFiles="data.cs"  %}

{% endaspTab %}

### Grouping resources by date

It groups the number of resources under each date and is applicable only on the calendar views such as Day, Week, Work Week, Month, Agenda and Month-Agenda. To enable such grouping, set `ByDate` option to `true` within the `Group` property.

**Example:** To display the Scheduler with resources grouped by date,

{% aspTab template="schedule/resources/group-date", sourceFiles="data.cs"  %}

{% endaspTab %}

> This kind of grouping by date is not applicable on any of the **timeline views**.

## Customizing parent resource cells

In timeline view work cells of parent resource can be customized by checking the `elementType` as `resourceGroupCells` in the event `RenderCell`. In the following code example, background color of the work hours has been changed.

{% aspTab template="schedule/resources/parent-resources", sourceFiles="data.cs"  %}

{% endaspTab %}

## Working with shared events

Multiple resources can share the same events, thus allowing the CRUD action made on it to reflect on all other shared instances simultaneously. To enable such option, set `AllowGroupEdit` option to `true` within the `Group` property. With this property enabled, a single appointment object will be maintained within the appointment collection, even if it is shared by more than one resource – whereas the resource fields of such appointment object will be in array which hold the IDs of the multiple resources.

> Any actions such as create, edit or delete held on any one of the shared event instances, will be reflected on all other related instances visible on the UI.

**Example:** To edit all the resource events simultaneously,

{% aspTab template="schedule/resources/linked-events", sourceFiles="data.cs"  %}

{% endaspTab %}

## Simple resource header customization

It is possible to customize the resource header cells using built-in template option and change the look and appearance of it in both the vertical and timeline view modes. All the resource related fields and other information can be accessed within the resource header template option.

**Example:** To customize the resource header and display it along with designation field, refer the below code example.

{% aspTab template="schedule/resources/resource-header", sourceFiles="data.cs"  %}

{% endaspTab %}

> To customize the resource header in compact mode properly make use of the class `e-device` as in the code example.

![Resource header template in compact mode](../../schedule/images/header-template.png)

## Customizing resource header with multiple columns

It is possible to customize the resource headers to display with multiple columns such as Room, Type and Capacity. The following code example depicts the way to achieve it and is applicable only on timeline views.

{% aspTab template="schedule/resources/custom-resource-header", sourceFiles="data.cs"  %}

{% endaspTab %}

## Displaying tooltip for resource headers

It is possible to display tooltip over the resource headers showing the resource information. By default, there won't be any tooltip displayed on the resource headers, and to enable it, you need to assign the customized template design to the `HeaderTooltipTemplate` option within the `Group` property.

{% aspTab template="schedule/resources/tooltip", sourceFiles="data.cs"  %}

{% endaspTab %}

## Choosing between resource colors for appointments

By default, the colors defined on the top level resources collection will be applied for the events. In case, if you want to apply specific resource color to events irrespective of its top-level parent resource color, it can be achieved by defining `ResourceColorField` option within the `EventSettings` property.

In the following example, the colors mentioned in the second level will get applied over the events.

{% aspTab template="schedule/resources/resource-color", sourceFiles="data.cs"  %}

{% endaspTab %}

> The value of the `ResourceColorField` field should be mapped with the `Name` value given within the `Resources` property.

## Dynamically add and remove resources

It is possible to add or remove the resources dynamically to and from the Scheduler respectively. In the following example, when the checkbox is checked and unchecked, the respective resources gets added up or removed from the Scheduler layout. To add new resource dynamically, `addResource` method is used which accepts the arguments such as resource object, resource name (within which level, the resource object to be added) and index (position where the resource needs to be added).

To remove the resources dynamically, `removeResource` method is used which accepts the index (position from where the resource to be removed) and resource name (within which level, the resource object presents) as parameters.

{% aspTab template="schedule/resources/dynamic-resource", sourceFiles="data.cs"  %}

{% endaspTab %}

## Setting different working days and hours for resources

Each resource in the Scheduler can have different working hours as well as different working days set to it. There are default options available within the `Resources` collection, to customize the default working hours and days of the Scheduler.

### Set different work days

Different working days can be set for the resources of Scheduler using the `WorkDaysField` property which maps the working days field from the resource dataSource. This field accepts the collection of day indexes (from 0 to 6) of a week. By default, it is set to [1, 2, 3, 4, 5] and in the following example, each resource has been set with different values and therefore each of them will render only those working days. This option is applicable only on the calendar views and is not applicable on timeline views.

{% aspTab template="schedule/resources/custom-workdays", sourceFiles="data.cs"  %}

{% endaspTab %}

### Set different work hours

Working hours indicates the work hour duration of a day, which is highlighted visually with active color over the work cells. Each resource on the Scheduler can be defined with its own set of working hours as depicted in the following example.

* `StartHourField` - Denotes the start time of the working/business hour in a day.
* `EndHourField` - Denotes the end time limit of the working/business hour in a day.

{% aspTab template="schedule/resources/custom-hour", sourceFiles="data.cs"  %}

{% endaspTab %}

In this example, a resource named `Will Smith` is depicted with working hours ranging from 8.00 AM to 3.00 PM and is visually illustrated with active colors, whereas the other two resources have different working hours set.

## Compact view in mobile

Although the Scheduler views are designed keeping in mind the responsiveness of the control in mobile devices, however when using Scheduler with multiple resources - it is difficult to view all the resources and its relevant events at once on the mobile. Therefore, we have introduced a new compact mode specially for displaying multiple resources of Scheduler on mobile devices. By default, this mode is enabled while using Scheduler with multiple resources on mobile devices. If in case, you need to disable this compact mode, set `false` to the `EnableCompactView` option within the `Group` property. Disabling this option will display the exact desktop mode of Scheduler view on mobile devices.

With this compact view enabled on mobile, you can view only single resource at a time and to switch to other resources, there is a TreeView at the left listing out all other available resources - clicking on which will display that particular resource and its related appointments.

![Resources in compact mode](../../schedule/images/resource.png)

## Adaptive UI in desktop

By default, the Scheduler layout adapts automatically in the desktop and mobile devices with appropriate UI changes. In case, if the user wants to display the Adaptive scheduler in desktop mode with adaptive enhancements, then the property `EnableAdaptiveUI` can be set to true. Enabling this option will display the exact mobile mode of Scheduler view on desktop devices.

Some of the default changes made for compact Scheduler to render in desktop devices are as follows,
* View options displayed in the Navigation drawer.
* Plus icon is added to the header for new event creation.
* Today icon is added to the header instead of the Today button.
* With Multiple resources – only one resource has been shown to enhance the view experience of resource events details clearly. To switch to other resources, there is a TreeView on the left that lists all other available resources, clicking on which will display that particular resource and its related events.

{% aspTab template="schedule/resources/adaptive-ui", sourceFiles="data.cs"  %}

{% endaspTab %}

> You can refer to our [ASP.NET MVC Scheduler](https://www.syncfusion.com/aspnet-mvc-ui-controls/scheduler) feature tour page for its groundbreaking feature representations. You can also explore our [ASP.NET MVC Scheduler](https://ej2.syncfusion.com/aspnetmvc/Schedule/Overview#/material) example to knows how to present and manipulate data.
