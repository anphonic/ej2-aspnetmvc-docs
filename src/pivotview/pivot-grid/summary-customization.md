---
title: "Summary Customization"
component: "Pivot Grid"
description: "Show/hide sub-totals and grand totals for the pivot table"
---

# Summary Customization

## Show/hide grand totals

Allows you to show or hide grand totals in rows and columns by using the `showGrandTotals` property. To hide the grand totals in rows and columns, set the property `showGrandTotals` to **false**.
You can hide grand totals for row or columns individually by setting the property `showRowGrandSubTotals` or `showColumnGrandTotals` to **false**.

> By default, these properties are set as true.

{% aspTab template="pivot-grid/summary-customization/grand-total", sourceFiles="GrandTotal.cs" %}

{% endaspTab %}

## Show/hide sub-totals

Allows you to show or hide sub-totals in rows and columns by using the `showSubTotals` property. To hide all the sub-totals in rows and columns, set the property `showSubTotals` to **false**. You can hide sub-totals for rows and columns specifically by setting the property `showRowSubTotals` or `showColumnSubTotals` to **false**.

> By default, these properties are set as true.

{% aspTab template="pivot-grid/summary-customization/sub-total", sourceFiles="SubTotal.cs" %}

{% endaspTab %}

## Show/hide sub-totals for specific fields

Allows you to show or hide sub-totals for specific fields in rows and columns by using the `showSubTotals` property. To hide the sub-totals in a specific row or column, set the property `showSubTotals` to **false**.

> By default, this property is set as true.

{% aspTab template="pivot-grid/summary-customization/sub-total-specific", sourceFiles="SubTotalSpecific.cs" %}

{% endaspTab %}