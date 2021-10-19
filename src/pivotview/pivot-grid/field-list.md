---
title: "Field List"
component: "Pivot Grid"
description: "Field list allows the user to add or remove fields and also re-arrange them between different axes."
---

# Pivot Field List

The Pivot Grid provides a built-in Field List similar to Microsoft Excel. It allows you to add or remove fields and also rearrange the fields between different axes, including column, row, value, and filter along with filter and sort options dynamically at runtime.

The field list can be displayed in three different formats to interact with pivot grid. They are:

* **In-built Field List (Popup)**: To display the field list icon in Pivot Grid UI to invoke the built-in dialog.
* **Stand-alone Field List (Fixed)**: To display the field list in a static position within a web page.
* **Invoking dynamic Field List (Customized)**: To display the field list by invoking the built-in dialog independently through other means, for example, on a button click.

## In-built Field List (Popup)

To display the field list icon in Pivot Grid UI, you need to set the `showFieldList` property to **true**. In order to display the field list dialog, click the field list icon at the top left corner of the Pivot Grid.

> The field list icon will be displayed at the top right corner of the Pivot Grid, when grouping bar is enabled.

{% aspTab template="pivot-grid/getting-start-mvc/fieldlist", sourceFiles="fieldlist.cs" %}

{% endaspTab %}

## Stand-alone Field List (Fixed)

The field list can be rendered in a static position, anywhere in web page layout, like a separate component. To do so, you need to set `renderMode` property to `Fixed`.

> Moreover, to make field list interact with pivot grid, you need to use the **updateView** and **update** methods for data source update in both field list and pivot grid simultaneously.

{% aspTab template="pivot-grid/field-list/static", sourceFiles="Static.cs" %}

{% endaspTab %}

## Invoking dynamic Field List (Customized)

Also, you can display the field list dialog independently through other means. For example, you can invoke the field list dialog on an external button click. To do so, set `renderMode` property to `Popup` and  since on button click, field list dialog will be invoked.

> * Meanwhile, you can display the field list dialog at specific target element within a webpage using `target` property. By default, the `target` value is null, which refers the `document.body` element.
> * Moreover, to make field list interact with pivot grid, you need to use the **updateView** and **update** methods for data source update in both field list and pivot grid simultaneously.

The below sample code illustrates the field list dialog invoked on an external button click.

{% aspTab template="pivot-grid/field-list/popup", sourceFiles="Popup.cs" %}

{% endaspTab %}

## See Also

* [Change load limited data in member editor](./how-to/change-load-limited-data-in-member-editor)
* [Customize the icons for pivot grid](./how-to/customize-the-icons-for-pivot-grid)