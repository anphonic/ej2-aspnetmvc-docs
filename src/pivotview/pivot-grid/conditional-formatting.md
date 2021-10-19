---
title: "Conditional Formatting"
component: "Pivot Grid"
description: "Conditional formatting allowing the users to highlighting the value cells based on its value."
---

# Conditional Formatting

Conditional formatting allows users to change the appearance of pivot grid value cells with its background color, font color, font family, and font size based on specific conditions. To achieve this, set the `allowConditionalFormatting` to `true` and use the `conditionalFormatSettings` object in the pivot grid widget along with the following properties.

* `measure`: Specifies the value field name for which style will be applied.
* `condition`: Specifies the operator type such as equals, greater than, less than, etc.
* `value1`: Specifies the start value.
* `value2`: Specifies the end value.
* `style`: Specifies the style for the cell.

{% aspTab template="pivot-grid/conditional-formatting/code-behind", sourceFiles="Formatting.cs" %}

{% endaspTab %}

Meanwhile, you can also achieve this in UI by invoking `showConditionalFormattingDialog` method on an external button click which is shown in the below code sample.

{% aspTab template="pivot-grid/conditional-formatting/ui", sourceFiles="Formatting.cs" %}

{% endaspTab %}

## See Also

* [Apply conditional formatting for specific row or column](./how-to/apply-conditional-formatting-for-specific-row-or-column)
