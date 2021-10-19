# Perform cell selection and get selected cells information

You can select any cell/row by setting the property `gridSettings.allowSelection` as `true` where the selected cells can be highlighted. It can be done through mouse down or arrow keys.

## Selection mode

It supports three types of selection mode that can be set by the property `gridSettings.selectionSettings.mode`. They are,

* **`Row`**: The `Row` value is set by default, and allows you to select only rows.
* **`Cell`**: Allows you to select only cells.
* **`Both`**: Allows you to select rows and cells at the same time.

## Selection type

It supports two types of selection that can be set by the property `gridSettings.selectionSettings.type`. They are,

* **`Single`**: The `Single` value is set by default, and it only allows selection of a single row or a cell.
* **`Multiple`**: Allows you to select multiple rows or cells.
To perform the multi-selection, press and hold CTRL key and click the desired rows or cells. To select range of rows or cells, press and hold the SHIFT key and click the rows or cells.

## Event

The event `cellSelected` fires on every cell/row on selected/deselected operations and it provides the selected cells information with its corresponding column and row headers.

{% aspTab template="pivot-grid/pivot-selection", sourceFiles="PivotSelection.cs" %}

{% endaspTab %}
