---
title: "Editor Window and Quick Popup of Scheduler"
component: "Scheduler"
description: "This topic demonstrates how to customize the default event editor and quick pop-up using templates and also explains how to design the custom modal popup."
---

# Editor window and quick popups

Scheduler makes use of popups and dialog to display the required notifications, as well as includes an editor window with event fields for making the appointment creation and editing process easier. You can also easily customize the editor window and the fields present in it, and can also apply validations on those fields.

## Event editor

The editor window usually opens on the Scheduler, when a cell or event is double clicked. When a cell is double clicked, the detailed editor window opens in "Add new" mode, whereas when an event is double clicked, the same is opened in an "Edit" mode.

In mobile devices, you can open the detailed editor window in edit mode by clicking the edit icon on the popup, that opens on single tapping an event. You can also open it in add mode by single tapping a cell, which will display a `+` indication, clicking on it again will open the editor window.

> You can also prevent the editor window from opening, by rendering Scheduler in a `Readonly` mode or by doing code customization within the `PopupOpen` event.

### How to change the editor window header title and text of footer buttons

You can change the header title and the text of buttons displayed at the footer of the editor window by changing the appropriate localized word collection used in the Scheduler.

{% aspTab template="schedule/editor-template/local-word", sourceFiles="data.cs"  %}

{% endaspTab %}

### How to change the label text of default editor fields

To change the default labels such as Subject, Location and other field names in the editor window, make use of the `Title` property available within the field option of `EventSettings`.

{% aspTab template="schedule/editor-template/field-label", sourceFiles="data.cs"  %}

{% endaspTab %}

### Field validation

It is possible to validate the required fields of the editor window from client-side before submitting it, by adding appropriate validation rules to each field. The appointment fields have been extended to accept both `string` and `object` type values. To perform validations, it is necessary to specify object values for the event fields.

{% aspTab template="schedule/editor-template/field-validation", sourceFiles="data.cs"  %}

{% endaspTab %}

> Applicable validation rules can be referred from [form validation](http://ej2.syncfusion.com/documentation/form-validator/#validation-rules) documentation.

### Add additional fields to the default editor

The additional fields can be added to the default event editor by making use of the `PopupOpen` event which gets triggered before the event editor opens on the Scheduler. The `PopupOpen` is a client-side event that triggers before any of the generic popups opens on the Scheduler. The additional field (any of the form elements) should be added with a common class name `e-field`, so as to handle and process those additional data along with the default event object. In the following example, an additional field `Event Type` has been added to the default event editor and its value is processed accordingly.

{% aspTab template="schedule/editor-template/additional-field", sourceFiles="data.cs"  %}

{% endaspTab %}

### Customizing the default time duration in editor window

In default event editor window, start and end time duration are processed based on the `interval` value set within the `TimeScale` property. By default, `interval` value is set to 30, and therefore the start/end time duration within the event editor will be in a 30 minutes time difference. You can change this duration value by changing the `duration` option within the `PopupOpen` event as shown in the following code example.

{% aspTab template="schedule/editor-template/duration", sourceFiles="data.cs"  %}

{% endaspTab %}

### How to prevent the display of editor and quick popups

It is possible to prevent the display of editor and quick popup windows by passing the value `true` to `cancel` option within the `PopupOpen` event.

{% aspTab template="schedule/editor-template/prevention", sourceFiles="data.cs"  %}

{% endaspTab %}

In case, if you need to prevent only specific popups on Scheduler, then you can check the condition based on the popup type. The types of the popup that can be checked within the `PopupOpen` event are as follows.

| Type | Description |
|-----|-----|
| `Editor` | For Detailed editor window.|
| `QuickInfo` | For Quick popup which opens on cell click.|
| `EditEventInfo` | For  Quick popup which opens on event click.|
| `ViewEventInfo` | For Quick popup which opens on responsive mode.|
| `EditorContainer` | For more event indicator popup.|

## Quick popups

The quick info popups are the ones that gets opened, when a cell or appointment is single clicked on the desktop mode. On single clicking a cell, you can simply provide a subject and save it. Also, while single clicking on an event, a popup will be displayed where you can get the overview of the event information. You can also edit or delete those events through the options available in it.

By default, these popups are displayed over cells and appointments of Scheduler and to disable this action, set `false` to `ShowQuickInfo` property.

{% aspTab template="schedule/editor-template/hide-quick-info", sourceFiles="data.cs"  %}

{% endaspTab %}

> The quick popup that opens while single clicking on the cells are not applicable on mobile devices.

### How to open Quick Info popup on multiple cell selection

By default the `QuickInfo` popup will open on single click of the cell. To open the quick info popup on multiple cell selection, you need to select the cells and press `enter` key. You can open this popup immediately after multiple cell selection by setting up `true` to `QuickInfoOnSelectionEnd` property where as its default value is `false`.

{% aspTab template="schedule/editor-template/show-quick-info", sourceFiles="data.cs"  %}

{% endaspTab %}

### How to change the watermark text of quick popup subject

By default, `Add Title` text is displayed on the subject field of quick popup. To change the default watermark text, change the value of the appropriate localized word collection used in the Scheduler.

```csharp
var L10n = ej.base.L10n;
L10n.load({
    'en-US': {
        'schedule': {
          'addTitle' : 'New Title'
        }
    }
});
```

### Customizing quick popups

The look and feel of the built-in quick popup window, which opens when single clicked on the cells or appointments can be customized by making use of the `QuickInfoTemplates` property of the Scheduler. There are 3 sub-options available to customize them easily,

* header - Accepts the template design that customizes the header part of the quick popup.
* content - Accepts the template design that customizes the content part of the quick popup.
* footer - Accepts the template design that customizes the footer part of the quick popup.

{% aspTab template="schedule/editor-template/custom-quick-popup", sourceFiles="data.cs"  %}

{% endaspTab %}

> The quick popup in adaptive mode can also be customized using `QuickInfoTemplates` using `e-device` class.

## Customizing event editor using template

The event editor window can be customized by making use of the `EditorTemplate` option. Here, the custom window design is built with the required fields using the script template and its type should be of **text/x-template**.

Each field defined within template should contain the **e-field** class, so as to allow the processing of those field values internally. The ID of this customized script template section is assigned to the `EditorTemplate` option, so that these customized fields will be replaced onto the default editor window.

As we are using our Syncfusion sub-components within our editor using template in the following example, the custom defined form elements needs to be configured as required Syncfusion components such as **DropDownList** and **DateTimePicker** within the `PopupOpen` event. This particular step can be skipped, if the user needs to simply use the usual form elements.

{% aspTab template="schedule/editor-template/custom-editor-template", sourceFiles="data.cs"  %}

{% endaspTab %}

### How to add resource options within editor template

The resource field can be added within editor template with MultiSelect control for allow multiple resources.

{% aspTab template="schedule/editor-template/editor-resource", sourceFiles="data.cs"  %}

{% endaspTab %}

### Apply validations on editor template fields

In the following code example, validation has been added to the status field.

{% aspTab template="schedule/editor-template/editor-template-validation", sourceFiles="data.cs"  %}

{% endaspTab %}

### How to save the customized event editor using template

The **e-field** class is not added to each field defined within the template, so you should allow to set those field values externally by using the `popupClose` event.

Note: You can allow to retrieve the data only on the `save` and `delete` option. Data cannot be retrieved on the `close` and `cancel` options in the editor window.

The following code example shows how to save the customized event editor using a template by the `popupClose` event.

{% aspTab template="schedule/editor-template/custom-event-editor", sourceFiles="data.cs"  %}

{% endaspTab %}

In case, if you need to prevent only specific popups on Scheduler, then you can check the condition based on the popup type. The types of the popup that can be checked within the `popupClose` event are as follows.

| Type | Description |
|------|-------------|
| `Editor` | For Detailed editor window.|
| `QuickInfo` | For Quick popup which opens on cell click.|
| `EditEventInfo` |For  Quick popup which opens on event click.|
| `ViewEventInfo` | For Quick popup which opens on responsive mode.|
| `EventContainer` | For more event indicator popup.|
| `RecurrenceAlert` | For edit recurrence event alert popup.|
| `DeleteAlert` | For delete confirmation popup.|
| `ValidationAlert` | For validation alert popup.|
| `RecurrenceValidationAlert` | For recurrence validation alert popup.|

## More events indicator and popup

When the number of appointments count that lies on a particular time range * default appointment height exceeds the default height of a cell in month view and all other timeline views, a `+ more` text indicator will be displayed at the bottom of those cells. This indicator denotes that the cell contains few more appointments in it and clicking on that will display a popup displaying all the appointments present on that day.

> To disable this option of showing popup with all hidden appointments, while clicking on the text indicator, you can do code customization within the `PopupOpen` event.

The same indicator is displayed on all-day row in calendar views such as day, week and work week views alone, when the number of appointment count present in a cell exceeds three. Clicking on the text indicator here will not open a popup, but will allow the expand/collapse option for viewing the remaining appointments present in the all-day row.

The following code example shows how to disable the display of such popups while clicking on the more text indicator.

{% aspTab template="schedule/editor-template/more-indicator", sourceFiles="data.cs"  %}

{% endaspTab %}

### How to customize the popup that opens on more indicator

The following code example shows you how to customize the default more indicator popup in which number of events rendered count on the day has been shown in the header.

{% aspTab template="schedule/editor-template/more-indicator-custom", sourceFiles="data.cs"  %}

{% endaspTab %}

### How to prevent the display of popup when clicking on the more text indicator

It is possible to prevent the display of popup window by passing the value `true` to `cancel` option within the `MoreEventsClick` event.

{% aspTab template="schedule/editor-template/more-event-popup", sourceFiles="data.cs"  %}

{% endaspTab %}

### How to navigate Day view when clicking on more text indicator

The following code example shows you how to customize the `moreEventsClick` property to navigate to the Day view when clicking on the more text indicator.

{% aspTab template="schedule/editor-template/more-event-edit", sourceFiles="data.cs"  %}

{% endaspTab %}

> You can refer to our [ASP.NET MVC Scheduler](https://www.syncfusion.com/aspnet-mvc-ui-controls/scheduler) feature tour page for its groundbreaking feature representations. You can also explore our [ASP.NET MVC Scheduler](https://ej2.syncfusion.com/aspnetmvc/Schedule/Overview#/material) example to knows how to present and manipulate data.