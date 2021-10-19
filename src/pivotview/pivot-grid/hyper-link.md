---
title: "Hyperlink"
component: "Pivot Grid"
description: "User allows to show hyperlink option to the link data for individual cells."
---

# Hyperlink

Pivot Grid allows you to show hyperlink option to the link data for individual cells that display in the pivot grid. Also, the hyperlink can be enabled separately for row header, column header, value, and summary cells using the `hyperlinkSettings`. It can be configured through code behind, during initial rendering. The settings available to show hyperlink to the cells are:

* `showHyperlink`: It allows to set the visibility of hyperlink in all cells.
* `showRowHeaderHyperlink`: It allows to set the visibility of hyperlink in row headers.
* `showColumnHeaderHyperlink`: It allows to set the visibility of hyperlink in column headers.
* `showValueCellHyperlink`: It allows to set the visibility of hyperlink in value cells.
* `showSummaryCellHyperlink`: It allows to set the visibility of hyperlink in summary cells.
* `headerText`: It allows to set the visibility of hyperlink based on header text.
* `conditionalSettings`: It allows to set the visibility of hyperlink based on specific condition.

> By default, the hyperlink options are disabled for all cells in the pivot grid.

## Hyperlink for all cells

The Pivot Grid has an option to show hyperlink option to all the cells that are currently displaying. To show hyperlink option, you need to set `showHyperlink` to **true**.

{% aspTab template="pivot-grid/hyper-link/all-cells", sourceFiles="AllCells.cs" %}

{% endaspTab %}

## Hyperlink for row headers

The Pivot Grid has an option to show hyperlink option to row header cells that are currently displaying. To show hyperlink option for row headers alone, you need to set `showRowHeaderHyperlink` to **true**.

{% aspTab template="pivot-grid/hyper-link/row-header", sourceFiles="RowHeader.cs" %}

{% endaspTab %}

## Hyperlink for column headers

The Pivot Grid has an option to show hyperlink option to columns header cells that are currently displaying. To show hyperlink option for column headers alone, you need to set `showColumnHeaderHyperlink` to **true**.

{% aspTab template="pivot-grid/hyper-link/column-header", sourceFiles="ColumnHeader.cs" %}

{% endaspTab %}

## Hyperlink for value cells

The Pivot Grid has an option to show hyperlink option to value cells that are currently displaying. To show hyperlink option for values alone, you need to set `showValueCellHyperlink` to **true**.

{% aspTab template="pivot-grid/hyper-link/value-cells", sourceFiles="ValueCells.cs" %}

{% endaspTab %}

## Hyperlink for summary cells

The Pivot Grid has an option to show hyperlink option to summary value cells that are currently displaying. To show hyperlink option for summary values alone, you need to set `showSummaryCellHyperlink` to **true**.

{% aspTab template="pivot-grid/hyper-link/summary-cells", sourceFiles="SummaryCells.cs" %}

{% endaspTab %}

## Condition based hyperlink

The Pivot Grid has an option to show hyperlink option to the cells based on specific conditions. It can be configured using the `conditionalSettings` option through code behind, during initial rendering. The settings required to sort are:

* `measure`: Specifies the value field name to get visibility of hyperlink option for specific measure.
* `condition`: Specifies the operator type such as equals, greater than, less than, etc.
* `value1`: Specifies the start value.
* `value2`: Specifies the end value.

{% aspTab template="pivot-grid/hyper-link/conditions", sourceFiles="Conditions.cs" %}

{% endaspTab %}

## Header based hyperlink

The Pivot Grid has an option to show hyperlink option to the cells based on specific row or column. It can be configured using the `headerText` option through code behind, during initial rendering.

{% aspTab template="pivot-grid/hyper-link/headers", sourceFiles="Headers.cs" %}

{% endaspTab %}

## See Also

* [Apply condition based hyperlink for specific row or column](./how-to/apply-condition-based-hyper-link-for-specific-row-or-column)