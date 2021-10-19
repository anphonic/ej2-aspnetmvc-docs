---
title: "Editing"
component: "Pivot Grid"
description: "Editing allows to perform CRUD operation in the raw items of any cells of the pivot table."
---

# Editing

Cell edit allow to add, delete and update the raw items/detailed data of any cells of the pivot table. The aggregation will be performed for the updated values. The feature can be enabled by setting the `editSettings.allowEditing` property to `true`.

The raw items/detailed data of any value cell can view in new window on double-clicking. CRUD operations can be performed by double-clicking the cells or using toolbar options in newly opened report.

The available toolbar options are:

| Toolbar Button | Actions |
|----------------|---------|
| Add | Add a new row.|
| Edit | Edit the current row/cell.|
| Delete | Delete the current row.|
| Update | Update the edited row/cell.|
| Cancel | Cancel the edited state. |

It supports following edit types,

* Normal
* Dialog
* Batch
* Command Columns

## Normal

In Normal edit mode, when you start editing, the currently selected row is changed to edit state.
You can change the cell values and save it to the data source by clicking `Update` toolbar button.
To enable Normal edit, set the `editSettings.mode` as `Normal`.

{% aspTab template="pivot-grid/editing/normal", sourceFiles="Normal.cs" %}

{% endaspTab %}

> Normal edit mode is default mode of editing.

## Dialog

In Dialog edit mode, when you start editing the currently selected row data will be shown on a dialog.
You can change the cell values and save it to the data source by clicking `Save` button in the dialog.
To enable Dialog edit, set the `editSettings.mode` as `Dialog`.

{% aspTab template="pivot-grid/editing/dialog", sourceFiles="Dialog.cs" %}

{% endaspTab %}

## Batch

In Batch edit mode, when you double-click on the grid cell, then the target cell changed to edit state.
You can bulk save (added, changed and deleted data in the single request) to data source by click on the toolbar's `Update`
button.
To enable Batch edit, set the `editSettings.mode` as `Batch`.

{% aspTab template="pivot-grid/editing/batch", sourceFiles="Batch.cs" %}

{% endaspTab %}

## Command column

Here, an additional column appended in the grid layout which holds the command buttons to perform CRUD operation.
To enable Command columns, set the `editSettings.allowCommandColumns` as `true`.

The available built-in command buttons are:

| Command Button | Actions |
|----------------|---------|
| Edit | Edit the current row.|
| Delete | Delete the current row.|
| Save | Update the edited row.|
| Cancel | Cancel the edited state. |

{% aspTab template="pivot-grid/editing/cc", sourceFiles="CC.cs" %}

{% endaspTab %}
