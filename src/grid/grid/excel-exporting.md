---
title: "Excel Export"
component: "Grid"
description: "Documentation on exporting DataGrid content to Excel and customizing the exported document with multi-export, headers and footers, and file name changes."
---

# Excel Export

The excel export allows exporting Grid data to Excel document. You need to use the
 [`excelExport`](https://ej2.syncfusion.com/documentation/api/grid/#excelexport) method for exporting. To enable Excel export in the grid, set the [`AllowExcelExport`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_AllowExcelExport) property as true.

To use excel export, You need to define the **ExcelExport** in inbuild toolbar and define the [`ToolbarClick`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_ToolbarClick) event for exporting the Grid.

{% aspTab template="grid/excel-export/excel-export", sourceFiles="excel-export.cs" %}

{% endaspTab %}

## Multiple Grid exporting

The excel export provides an option to export multiple grid data in the same excel file.

### Same sheet

The excel export provides support to export multiple grids in same sheet. To export in same sheet, define [`multipleExport`](https://ej2.syncfusion.com/documentation/api/grid/excelExportProperties/#multipleexport) type as **AppendToSheet** in [`exportProperties`](https://ej2.syncfusion.com/documentation/api/grid/excelExportProperties/#excelexportproperties). It have an option to provide blank rows between grids. These blank rows count can be defined by using the [`multipleExport`](https://ej2.syncfusion.com/documentation/api/grid/excelExportProperties/#multipleexport) as blankRows.

{% aspTab template="grid/excel-export/same-sheet", sourceFiles="same-sheet.cs" %}

{% endaspTab %}

> By default, [`multipleExport`](https://ej2.syncfusion.com/documentation/api/grid/excelExportProperties/#multipleexport) blankRows value is 5.

### New Sheet

Excel exporting provides support to export multiple grids in new sheet. To export in new sheet, define  [`multipleExport`](https://ej2.syncfusion.com/documentation/api/grid/excelExportProperties/#multipleexport) type as **NewSheet** in [`exportProperties`](https://ej2.syncfusion.com/documentation/api/grid/excelExportProperties/#excelexportproperties).

{% aspTab template="grid/excel-export/new-sheet", sourceFiles="new-sheet.cs" %}

{% endaspTab %}

## To customize excel export

The excel export provides an option to customize mapping of the grid to excel document.

### Export current page

The excel export provides an option to export the current page into excel. To export current page, define [`exportType`](https://ej2.syncfusion.com/documentation/api/grid/excelExportProperties/#exporttype) to **currentpage**.

{% aspTab template="grid/excel-export/export-current", sourceFiles="export-current.cs" %}

{% endaspTab %}

### Export hidden columns

The excel export provides an option to export hidden columns of grid by defining [`includeHiddenColumn`](https://ej2.syncfusion.com/documentation/api/grid/excelExportProperties/#includehiddencolumn) as **true**.

{% aspTab template="grid/excel-export/export-hidden", sourceFiles="export-hidden.cs" %}

{% endaspTab %}

### Show or Hide columns on Exported Excel

You can show a hidden column or hide a visible column while printing the grid using [`ToolbarClick`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_ToolbarClick) and [`ExcelExportComplete`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_ExcelExportComplete) events.

In the [`ToolbarClick`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_ToolbarClick) event, based on **args.item.id** as **Grid_excelexport**. We can show or hide columns by setting [`Visible`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html#Syncfusion_EJ2_Grids_GridColumn_Visible) property of [`Column`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.GridColumn.html) to **true** or **false** respectively.

In the [`ExcelExportComplete`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_ExcelExportComplete) event, We have reversed the state back to the previous state.

In the below example, we have **CustomerID** as a hidden column in the grid. While exporting, we have changed **CustomerID** to visible column and **ShipCity** as hidden column.

{% aspTab template="grid/excel-export/show-hide", sourceFiles="show-hide.cs" %}

{% endaspTab %}

### Export with filter options

The excel export provides an option to export with filter option in excel by defining `enableFilter` as **true** .
It requires the [`allowFiltering`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_AllowFiltering) to be true.

{% aspTab template="grid/excel-export/enable-filter", sourceFiles="enable-filter.cs" %}

{% endaspTab %}

### Conditional Cell Formatting

Grid cells in the exported Excel can be customized or formatted using [`ExcelQueryCellInfo`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_ExcelQueryCellInfo) event. In this event, we can format the grid cells of exported PDF document based on the column cell value.

In the below sample, we have set the background color for **Freight** column in the exported excel by using the arguments of [`ExcelQueryCellInfo`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Grids.Grid.html#Syncfusion_EJ2_Grids_Grid_ExcelQueryCellInfo) event and **backColor** property.

{% aspTab template="grid/excel-export/cell-format", sourceFiles="cell-formats.cs" %}

{% endaspTab %}

### Theme

The excel export provides an option to include theme for exported excel document.

To apply theme in exported Excel, define the [`theme`](https://ej2.syncfusion.com/documentation/api/grid/excelExportProperties/#theme) in [`ExcelExportProperties`](https://ej2.syncfusion.com/documentation/api/grid/excelExportProperties/#properties).

{% aspTab template="grid/excel-export/theme", sourceFiles="theme.cs" %}

{% endaspTab %}

> By default, material theme is applied to exported excel document.

### To add header and footer

The excel export provides an option to include header and footer content for exported excel document.

{% aspTab template="grid/excel-export/header-footer", sourceFiles="header-footer.cs" %}

{% endaspTab %}

### File Name for Exported document

You can assign the file name for the exported document by defining [`fileName`](https://ej2.syncfusion.com/documentation/api/grid/excelExportProperties/#filename) property in [`ExcelExportProperties`](https://ej2.syncfusion.com/documentation/api/grid/excelExportProperties/#excelexportproperties).

{% aspTab template="grid/excel-export/export-filename", sourceFiles="export-filename.cs" %}

{% endaspTab %}

## Custom data source

The excel export provides an option to define datasource dynamically before exporting. To export data dynamically, define the [`dataSource`](https://ej2.syncfusion.com/documentation/api/grid/excelExportProperties/#datasource) in [`ExcelExportProperties`](https://ej2.syncfusion.com/documentation/api/grid/excelExportProperties/#excelexportproperties).

{% aspTab template="grid/excel-export/custom-data", sourceFiles="custom-data.cs" %}

{% endaspTab %}

## Exporting grouped records

The excel export provides outline option for grouped records which hides the detailed data for better viewing.
In grid, we have provided the outline option for the exported document when the data's are grouped.

{% aspTab template="grid/excel-export/excel-group", sourceFiles="excel-group.cs" %}

{% endaspTab %}

## Export the hierarchy grid

The grid have an option to export the hierarchy grid to excel document. By default, grid will exports the visible child grids in expanded state. you can change the exporting option by using the **hierarchyExportMode** property of [`ExcelExportProperties`](https://ej2.syncfusion.com/documentation/api/grid/excelExportProperties/#excelexportproperties). The available options are,

| Mode     | Behavior    |
|----------|-------------|
| Expanded | Exports the visible child grids in expanded state. |
| All      | Exports the all the child grids in expanded state. |
| None     | Exports all child grids in collapse state. |

{% aspTab template="grid/excel-export/hierarchy", sourceFiles="hierarchy.cs" %}

{% endaspTab %}

### Limitations

* Microsoft Excel permits up to seven nested levels in outlines. So that in the grid we can able to provide only up to seven nested levels
  and if it exceeds more than seven levels then the document will be exported without outline option.
  Please refer the [Microsoft Limitation](https://docs.microsoft.com/en-us/sql/reporting-services/report-builder/exporting-to-microsoft-excel-report-builder-and-ssrs?view=sql-server-2017#ExcelLimitations)

## Exporting Grid in server

The Grid have an option to export the data to Excel in server side using Grid server export library.

### Server Dependencies

The Server side export functionality is shipped in the Syncfusion.EJ2.GridExport package, which is available in Essential Studio and [nuget.org](https://www.nuget.org/).The following list of dependencies is required for Grid server side Excel exporting action.

* Syncfusion.EJ2
* Syncfusion.EJ2.GridExport
* Syncfusion.Compression.Base
* Syncfusion.XlsIO.Base

### Server Configuration

The following code snippets shows server configuration using ASP.NET MVC Controller Action.

To Export the Grid in server side, You need to call the
 [`serverExcelExport`](https://ej2.syncfusion.com/documentation/api/grid/#serverexcelexport) method for passing the Grid properties to server exporting action.

{% aspTab template="grid/excel-export/server-export", sourceFiles="server-exportMVC.cs" %}

{% endaspTab %}

> **Note:** Refer to the GitHub sample for quick implementation and testing from [here](https://github.com/SyncfusionExamples/MVC-EJ2-Grid-server-side-exporting).

### CSV Export in server

You can export the Grid to CSV format by using the [`serverCsvExport`](https://ej2.syncfusion.com/documentation/api/grid/#servercsvexport) method which will pass the Grid properties to server.

In the below demo, we have invoked the above method inside the [`toolbarClick`](https://ej2.syncfusion.com/documentation/api/grid/#toolbarclick) event. In server side, we have deserialized the Grid properties and passed to the `CsvExport` method which will export the properties to CSV format.

{% aspTab template="grid/excel-export/server-csv-export", sourceFiles="server-exportMVC.cs" %}

{% endaspTab %}

## See Also

* [Copy & paste excel](https://www.syncfusion.com/blogs/post/essential-js-2-copying-and-pasting-excel-sheet-data-to-grid-asp-net-mvc.aspx)

* [Copy and pasting excel sheet data to Grid](https://www.syncfusion.com/blogs/post/copy-and-pasting-excel-sheet-data-to-syncfusion-grid-for-mvc.aspx)