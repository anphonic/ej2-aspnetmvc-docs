---
title: "Columns"
component: "Grid"
description: "Documentation on column reordering, resizing, header templates (custom header content), and column templates (custom cell content) in the Essential JS 2 DataGrid control."
---

# Columns

The column definitions are used as the [`DataSource`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_DataSource) schema in the Grid. This plays a vital role in rendering column values in the required format.

The grid operations such as sorting, filtering and grouping etc. are performed based on column definitions. The [`Field`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_Field) property of the [`Columns`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html)
is necessary to map the data source values in Grid columns.

> 1. If the column [`Field`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_Field) is not specified in the dataSource, the column values will be empty.
> 2. If the [`Field`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_Field) name contains “dot” operator, it is considered as complex binding.

## Auto generation

The [`Columns`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html) are automatically generated when
[`Columns`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html) declaration is empty or undefined while initializing the grid. All the columns in the [`DataSource`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_DataSource) are bound as grid columns.

{% aspTab template="grid/columns/auto", sourceFiles="auto.cs" %}

{% endaspTab %}

> When columns are auto-generated, the column [`Type`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_Type) will be determined from the first record of the [`DataSource`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_DataSource).

### Set Primary key column for auto generated columns when editing is enabled

Primary key can be defined in the declaration of column object of the grid. When you did not declare the columns, the grid will generate the columns automatically. For these auto generated columns, you can set [`IsPrimaryKey`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_IsPrimaryKey) column property as true by using the following ways,

If Primary key "column index" is known then refer the following example

{% aspTab template="grid/columns/primary", sourceFiles="primary.cs" %}

{% endaspTab %}

> If Primary key "column fieldname" is known then you can get the column by using **var column = grid.getColumnByField('OrderID')** and then set primary key by defining **Column.IsPrimaryKey = 'true'**

### Set column options to auto generated columns

You can set column options such as [`Format`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_Format), [`Width`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_Width) to the auto generated columns by using [`DataBound`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_DataBound) event of the grid.

In the below example, [`Width`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_Width) is set for **OrderID** column, date type is set for **OrderDate** column and numeric type is set for **Freight** column.

{% aspTab template="grid/columns/autocolumnformat", sourceFiles="autocolumnformat.cs" %}

{% endaspTab %}

## Complex data binding

You can achieve complex data binding in the grid by using the dot(.) operator in the [`Field`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_Field).

{% aspTab template="grid/columns/complexbinding", sourceFiles="complexbinding.cs" %}

{% endaspTab %}

## Foreign Key Column

Foreign key column can be enabled by using [`DataSource`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_DataSource), [`ForeignKeyField`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_ForeignKeyField) and [`ForeignKeyValue`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_ForeignKeyValue) properties of [`Column`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html).

* [`DataSource`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_DataSource) - Defines the foreign data.
* [`ForeignKeyField`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_ForeignKeyField) - Defines the mapping column name to the foreign data.
* [`ForeignKeyValue`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_ForeignKeyValue) - Defines the display field from the foreign data.

In the following example, **Employee Name** is a foreign column which shows **FirstName** column from foreign data.

{% aspTab template="grid/columns/foreign", sourceFiles="foreign.cs,employeeView.cs" %}

{% endaspTab %}

> For remote data, the sorting and grouping is done based on [`ForeignKeyField`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_ForeignKeyField) instead of [`ForeignKeyValue`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_ForeignKeyValue).
> If [`ForeignKeyField`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_ForeignKeyField) is not defined, then the column uses [`Field`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumnBuilder-1.html#Syncfusion_EJ2_Grids_GridColumnBuilder_1_Field_System_String_).

## Header Template

You can customize the header element by using the [`HeaderTemplate`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_HeaderTemplate) property. In this demo, the custom element is rendered for both EmployeeID and BirthDate column headers.

{% aspTab template="grid/columns/headertemplate", sourceFiles="headertemplate.cs" %}

{% endaspTab %}

## Header text

By default, column header title is displayed from column [`Field`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_Field) value. To override the default header title, you have to define the [`HeaderText`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_HeaderText) value.

{% aspTab template="grid/columns/headertext", sourceFiles="headertext.cs" %}

{% endaspTab %}

> If both the [`Field`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_Field) and [`HeaderText`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_HeaderText)
are not defined in the column, the column renders with empty header text.

## Format

To format cell values based on specific culture, use the [`Format`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_Format) property of [`Columns`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html). The grid uses Internalization library to format number and date values.

{% aspTab template="grid/columns/format", sourceFiles="format.cs" %}

{% endaspTab %}

> By default, the number and date values are formatted in **en-US** locale.

### Number formatting

The number or integer values can be formatted using the below format strings.

Format |Description |Remarks
-----|-----|-----
N | Denotes numeric type. | The numeric format is followed by integer value as N2, N3. etc which denotes the number of precision to be allowed.
C | Denotes currency type. | The currency format is followed by integer value as C2, C3. etc which denotes the number of precision to be allowed.
P | Denotes percentage type | The percentage format expects the input value to be in the range of 0 to 1. For example the cell value **0.2** is formatted as **20%**. The percentage format is followed by integer value as P2, P3. etc which denotes the number of precision to be allowed.

### Date formatting

You can format date values either using built-in date format string or custom format string.

For built-in date format you can specify [`Format`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_Format) property as string(Example: `yMd`).

You can also use custom format string to format the date values. Some of the custom formats and the formatted date values are given in the below table.

Format | Formatted value
-----|-----
{ type:'date', format:'dd/MM/yyyy' } | 04/07/1996
{ type:'date', format:'dd.MM.yyyy' } | 04.07.1996
{ type:'date', skeleton:'short' } | 7/4/96
{ type: 'dateTime', format: 'dd/MM/yyyy hh:mm a' } | 04/07/1996 12:00 AM
{ type: 'dateTime', format: 'MM/dd/yyyy hh:mm:ss a' } | 07/04/1996 12:00:00 AM

{% aspTab template="grid/columns/dateformat", sourceFiles="format.cs" %}

{% endaspTab %}

## Visibility

You can hide any particular column in Grid before rendering by defining [`Visible`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_Visible) property as false. In the below sample **ShipCity** column is defined as visible false.

{% aspTab template="grid/columns/Visibility", sourceFiles="Visibility.cs" %}

{% endaspTab %}

## AutoFit specific columns

The [`autoFitColumns`](https://ej2.syncfusion.com/documentation/api/grid/#autofitcolumns) method resizes the column to fit the widest cell's content without wrapping. You can autofit a specific column at initial rendering by invoking the [`autoFitColumns`](https://ej2.syncfusion.com/documentation/api/grid/#autofitcolumns) method in [`DataBound`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_DataBound) event.

{% aspTab template="grid/columns/autofit", sourceFiles="autofit.cs" %}

{% endaspTab %}

> You can autofit all the columns by invoking the [`autoFitColumns`](https://ej2.syncfusion.com/documentation/api/grid/#autofitcolumns) method without column names.

## Reorder

Reordering can be done by drag and drop of a particular column header from one index to another index within the grid. To enable reordering, set the [`AllowReordering`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_AllowReordering) to true.

{% aspTab template="grid/columns/reorder", sourceFiles="reorder.cs" %}

{% endaspTab %}

> You can disable reordering a particular column by setting the [`AllowReordering`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_AllowReordering) property of [`Columns`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html) to false.

### Reorder Single Column

Grid have option to reorder Columns either by Interaction or by using the **reorderColumns** method. In the below sample, **Name** column is reordered to last column position by using the method.

{% aspTab template="grid/columns/reordercols", sourceFiles="reordercols.cs" %}

{% endaspTab %}

### Reorder Multiple Columns

User can reorder a single column at a time by Interaction. Sometimes we need to have reorder multiple columns at the same time, It can be achieved through programmatically by using **reorderColumns** method.

In the below sample, **Ship City** and **Ship Region** column is reordered to last column position.

{% aspTab template="grid/columns/reordercolumns", sourceFiles="reordercols.cs" %}

{% endaspTab %}

### Reorder Events

During the reorder action, the grid component triggers the below three events.

1. The [`ColumnDragStart`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_ColumnDragStart) event triggers when column header element drag (move) starts.
2. The [`ColumnDrag`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_ColumnDrag) event triggers when column header element is dragged (moved) continuously.
3. The [`ColumnDrop`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_ColumnDrop) event triggers when a column header element is dropped on the target column.

{% aspTab template="grid/columns/reorderevents", sourceFiles="reorderevents.cs" %}

{% endaspTab %}

## Lock Columns

You can lock columns by using [`LockColumn`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_LockColumn) property. The locked columns will be moved to the first position. Also you cannot reorder its position.

In the below example, Ship City column is locked and its reordering functionality is disabled.

{% aspTab template="grid/columns/lock", sourceFiles="lock.cs" %}

{% endaspTab %}

## Column resizing

Column width can be resized by clicking and dragging the right edge of the column header. While dragging, the width of the respective column will be resized immediately. Each column can be auto resized by double-clicking the right edge of the column header to fit the width of that column based on the widest cell content. To enable column resize, set the [`AllowResizing`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_AllowResizing) property to true.

{% aspTab template="grid/columns/resize", sourceFiles="resize.cs" %}

{% endaspTab %}

> You can disable resizing for a particular column by setting the [`AllowResizing`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_AllowResizing) property of [`Columns`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html) to false.
> In RTL mode, you can click and drag the left edge of the header cell to resize the column.

### Column Resizing by using method

To resize a column, set width to that particular column and then refresh the grid header by using the **refreshHeader** method. Please refer the below code

```typescript

var grid = document.getElementById('Grid').ej2_instances[0]; //Grid Instance

var columns = grid.columns;

columns[0].width = 150;

grid.refreshHeader();

```

### Min and max width

Column resize can be restricted between minimum and maximum width by defining the [`MinWidth`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_MinWidth) and [`MaxWidth`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_MaxWidth) properties of [`Columns`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html).

In the following sample, minimum and maximum width are defined for **OrderID**, **Ship Name**, and **Ship Country** columns.

{% aspTab template="grid/columns/min", sourceFiles="min.cs" %}

{% endaspTab %}

### Resize Stacked Column

Stacked columns can be resized by clicking and dragging the right edge of the stacked column header. While dragging, the width of the respective child columns will be resized at the same time. You can disable resize for any particular stacked column by setting [`AllowResizing`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_AllowResizing) as **false** to its columns.

In this example, we have disabled resize for Ship City column.

{% aspTab template="grid/columns/stacked", sourceFiles="stacked.cs" %}

{% endaspTab %}

### Touch interaction

When the right edge of the header cell is tapped, a floating handler will be visible over the right border of the column. To resize the column, tap and drag the floating handler as needed. You can autoFit a column by using the Column menu of the grid.

The following screenshot represents the column resizing in touch device.

![Touch interaction](./images/column-resizing.jpg)

### Resizing Events

During the resizing action, the grid component triggers the below three events.

1. The [`ResizeStart`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_ResizeStart) event triggers when column resize starts.
2. The [`Resizing`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_Resizing) event triggers when column header element is dragged (moved) continuously..
3. The [`ResizeStop`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_ResizeStop) event triggers when column resize ends.

{% aspTab template="grid/columns/resizeevents", sourceFiles="resizeevents.cs" %}

{% endaspTab %}

## Column template

The column [`Template`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_Template) has options to display custom element instead of a field value in the column.

{% aspTab template="grid/columns/template", sourceFiles="template.cs" %}

{% endaspTab %}

> Grid actions such as editing, grouping, filtering and sorting etc. will depend upon the column [`Field`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_Field). If the [`Field`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_Field) is not specified in the template column, the grid actions cannot be performed.

### Using condition template

You can render the template elements based on condition.

In the following code, checkbox is rendered based on **Discontinued** field value.

{% aspTab template="grid/columns/condition-template", sourceFiles="template.cs" %}

{% endaspTab %}

## Column type

Column type can be specified using the [`Type`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_Type) property of [`Columns`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html). It specifies the type of data the column binds.

If the [`Format`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_Format) is defined for a column, the column uses [`Type`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_Type) to select the appropriate format option **number** or **date**.

Grid column supports the following types:
* string
* number
* boolean
* date
* datetime

> If the [`Type`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_Type) is not defined, it will be determined from the first record of the [`DataSource`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_DataSource).
> Incase if the first record of the [`DataSource`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_DataSource) is null/blank value for a column then it is necessary to define the [`Type`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_Type) for that column.

## Column chooser

The column chooser has options to show or hide columns dynamically. It can be enabled by defining the
[`ShowColumnChooser`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_ShowColumnChooser) as true.

{% aspTab template="grid/columns/columnchooser", sourceFiles="columnchooser.cs" %}

{% endaspTab %}

> You can hide the column names in column chooser by defining the [`ShowInColumnChooser`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_ShowInColumnChooser) as false.

### Open column chooser by external button

The Column chooser can be displayed on a page through external button by invoking
the **openColumnChooser** method with X and Y axis positions.

{% aspTab template="grid/columns/externalbutton", sourceFiles="externalbutton.cs" %}

{% endaspTab %}

## Column menu

The column menu has options to integrate features like sorting, grouping, filtering, column chooser, and autofit. It will show a menu with the integrated feature when users click on multiple icon of the column. To enable column menu, you need to define the [`ShowColumnMenu`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_ShowColumnMenu) property as true.

The default items are displayed in following table.

| Item | Description |
|-----|-----|
| `SortAscending` | Sort the current column in ascending order. |
| `SortDescending` | Sort the current column in descending order. |
| `Group` | Group the current column. |
| `Ungroup` | Ungroup the current column. |
| `AutoFit` | Auto fit the current column. |
| `AutoFitAll` | Auto fit all columns. |
| `ColumnChooser` | Choose the column visibility. |
| `Filter` | Show the filter option as given in `FilterSettings.Type` |

{% aspTab template="grid/column/columnmenu", sourceFiles="columnmenu.cs" %}

{% endaspTab %}

> You can disable column menu for a particular column by defining the [`ShowColumnMenu`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_ShowColumnMenu) property of [`Columns`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html) as false.
> You can customize the default items by defining the [`ColumnMenuItems`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_ColumnMenuItems) with required items.

### Column menu Events

During the resizing action, the grid component triggers the below two events.

1. The [`ColumnMenuOpen`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_ColumnMenuOpen) event triggers before the column menu opens.
2. The [`ColumnMenuClick`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_ColumnMenuClick) event triggers when the user clicks the column menu of the grid.

{% aspTab template="grid/column/columnmenuevents", sourceFiles="columnmenuevents.cs" %}

{% endaspTab %}

### Custom Column Menu Item

Custom column menu items can be added by defining the [`ColumnMenuItems`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_ColumnMenuItems) as collection of
the ColumnMenuItemModel.

Actions for this customized items can be defined in the [`ColumnMenuClick`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_ColumnMenuClick) event.

{% aspTab template="grid/columns/customcolumnmenu", sourceFiles="customcolumnmenu.cs" %}

{% endaspTab %}

### Customize menu items for particular columns

Sometimes, you have a scenario that to hide an item from column menu for particular columns. In that case, you need to define the **hide** as true in the arguments of [`ColumnMenuOpen`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_ColumnMenuOpen) event.

The following sample, **Filter** item was hidden in column menu when opens for the **OrderID** column.

{% aspTab template="grid/columns/customizecolumnmenu", sourceFiles="customizecolumnmenu.cs" %}

{% endaspTab %}

## Column spanning

The grid has option to span the adjacent cells. You need to define the **colSpan** attribute to span cells in the [`QueryCellInfo`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_QueryCellInfo) event.

In the following demo, employee **Davolio** is doing testing from 9.00 A.M. to 10.00 A.M. so that the cells have been spanned.

{% aspTab template="grid/columns/columnspanning", sourceFiles="columnspanning.cs" %}

{% endaspTab %}

## Responsive columns

You can toggle column visibility based on media queries which are defined
at the [`HideAtMedia`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_HideAtMedia).
The [`HideAtMedia`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_HideAtMedia) accepts valid
[Media Queries]( http://cssmediaqueries.com/what-are-css-media-queries.html ).In the below sample, for **OrderID** column, [`HideAtMedia`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_HideAtMedia) property value is set as **(min-width: 700px)** so that **OrderID** column will gets hidden when the browser screen width is lessthan 700px.

{% aspTab template="grid/columns/responsivecolumns", sourceFiles="responsivecolumns.cs" %}

{% endaspTab %}

## Controlling Grid actions

You can enable or disable grid action for a particular column by setting the [`AllowFiltering`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_AllowFiltering),
[`AllowGrouping`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_AllowGrouping), [`AllowEditing`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_AllowEditing),[`AllowReordering`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_AllowReordering), and [`AllowSorting`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_AllowSorting) properties.

{% aspTab template="grid/columns/controllingactions", sourceFiles="controllingactions.cs" %}

{% endaspTab %}

## ValueAccessor

The **valueAccessor** is used to access/manipulate the value of display data. You can achieve custom value formatting by using the valueAccessor.

{% aspTab template="grid/columns/valueaccessor", sourceFiles="valueaccessor.cs" %}

{% endaspTab %}

## Show/hide columns by external button

You can show or hide grid columns dynamically using external buttons by invoking the **showColumns** or **hideColumns** method.

{% aspTab template="grid/columns/showhide", sourceFiles="showhide.cs" %}

{% endaspTab %}

## How to render boolean values as checkbox

To render boolean values as checkbox in columns, you need to set [`DisplayAsCheckBox`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_DisplayAsCheckBox) property as **true**.

{% aspTab template="grid/columns/booleanascheckbox", sourceFiles="booleanascheckbox.cs" %}

{% endaspTab %}

## See Also

* [How to Change Column Header Text Dynamically](./how-to/change-header-text-dynamically)
* [Customize Column Styles](./how-to/customize-column-styles)
* [Custom Tooltip for Columns](how-to/display-custom-tool-tip-for-columns-in-grid)
* [How to Render Other Component in a Column](how-to/render-other-components-in-column)
* [How to change the Orientation of Header Text](./how-to/change-orientation-of-header-text)
* [Group Column by Format](./grouping#group-by-format)
* [How to Use Edit Template in Foreign Key Column](./how-to/use-edit-template-in-foreign-key-column)
* [How to Create and use custom Filter UI in Foreign Key Column](./how-to/customize-filter-ui-in-foreign-key)
* [How to Use Filter Bar Template in Foreign Key Column](./how-to/use-filter-bar-template-in-foreign-key-column)
* [How to Perform aggregation in Foreign Key Column](./how-to/perform-aggregation-in-foreign-key-column)
* [How to set complex column as Foreignkey column](./how-to/complex-column-as-foreign-key-column)
* [Complex Data Binding with list of Array Of Objects](./how-to/list-of-array-of-objects)
* [How to add primaryKey after column rendered in ASP.NET MVC  Grid](https://www.syncfusion.com/forums/138439/how-to-add-primarykey-after-column-rendered-in-asp-net-mvc-grid)
* [Drag and drop between two Grids in ASP.NET MVC Grid](https://www.syncfusion.com/forums/138154/drag-and-drop-between-two-grids-in-asp-net-mvc-grid)
* [How can I put a Sparkline in a child grid that is on a Grid with hierarchy in ASP.NET MVC Grid](https://www.syncfusion.com/forums/145389/how-can-i-put-a-sparkline-in-a-child-grid-that-is-on-a-grid-with-hierarchy-in-asp-net-mvc)
* [How can I enable or disable a menu option that is inside a template in ASP.NET MVC Grid](https://www.syncfusion.com/forums/153923/how-can-i-enable-or-disable-a-menu-option-that-is-inside-a-template-in-asp-net-mvc-grid)