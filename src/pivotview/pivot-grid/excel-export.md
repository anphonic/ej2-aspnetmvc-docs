---
title: "Excel Exporting"
component: "Pivot Grid"
description: "Export pivot grid data to Excel document."
---

# Excel Export

The Excel export allows Pivot Grid data to export as Excel document. To enable Excel export in the pivot grid, set the `allowExcelExport` as **true**. You need to use the `excelExport` method for Excel exporting.

{% aspTab template="pivot-grid/excel-export/export", sourceFiles="Export.cs" %}

{% endaspTab %}

## Multiple pivot grid exporting

The Excel export provides an option to export multiple pivot grid data in the same Excel file.

### Same WorkSheet

The Excel export provides support to export multiple pivot grids in same sheet. To export in same sheet, define `multipleExport.type` as `AppendToSheet` in `excelExportProperties`. It has an option to provide blank rows between pivot grids and these blank row(s) count can be defined using the`multipleExport.blankRows` property.

>By default, `multipleExport.blankRows` value is 5 between pivot grid's within the same sheet.

{% aspTab template="pivot-grid/excel-export/samesheet-export", sourceFiles="SameSheetExport.cs" %}

{% endaspTab %}

### New WorkSheet

Excel export provides support to export multiple pivot grids into new sheets. To export in new sheets, define  `multipleExport.type` as `NewSheet` in `excelExportProperties`.

{% aspTab template="pivot-grid/excel-export/newsheet-export", sourceFiles="NewSheetExport.cs" %}

{% endaspTab %}

## Customization during excel export

The Excel export provides an option to customize mapping of the pivot grid to excel document.

### Theme

The Excel export provides an option to include theme for exported Excel document.

To apply theme in exported Excel, define the `theme` in `excelExportProperties`.

>By default, material theme is applied to exported Excel document.

{% aspTab template="pivot-grid/excel-export/theme-export", sourceFiles="ThemeExport.cs" %}

{% endaspTab %}

### To add header and footer

The Excel export provides an option to include header and footer content for the exported Excel document.

{% aspTab template="pivot-grid/excel-export/header-footer", sourceFiles="HeaderFooter.cs" %}

{% endaspTab %}

## CSV Export

Also, the Excel export allows Pivot Grid data to be exported in `CSV` file format. To export pivot grid in `CSV` file format, you need to use the `csvExport` method.

{% aspTab template="pivot-grid/excel-export/csv-export", sourceFiles="CSVExport.cs" %}

{% endaspTab %}

## See Also

* [PDF Exporting](./pdf-export)