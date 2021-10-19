---
title: "Grouping Bar"
component: "Pivot Grid"
description: "Grouping bar allows the user to drag and drop fields between different axes at runtime."
---

# Grouping Bar

The Grouping Bar option in Pivot Grid automatically populates fields from the bound data source and allows end users to drag fields between different axes such as columns, rows, values, and filters, and create pivot views at runtime. It can be enabled by setting the `showGroupingBar` property to **true**.

To use grouping bar, You need to inject the `GroupingBar` module in pivot grid.

{% aspTab template="pivot-grid/getting-start-mvc/groupingbar", sourceFiles="groupingbar.cs" %}

{% endaspTab %}

The grouping bar provides some additional options to customize it's UI using `groupingBarSettings` property.

## Show/hide filter icon

The Grouping Bar has an option to filter members of particular fields at runtime in Pivot Grid. In order to filter members in a field, click the filter icon in the pivot button and check/uncheck the members that needs to be displayed. To disable the filter icon, you need to set `showFilterIcon` to **false**.

> By default, the filter icon is enabled in the grouping bar.

{% aspTab template="pivot-grid/grouping-bar/show-filter", sourceFiles="ShowFilter.cs" %}

{% endaspTab %}

## Show/hide sort icon

The Grouping Bar has an option to order members of a particular fields either in ascending or descending at run time. In order to sort a field, click the sort icon available in the respective pivot button. To reverse the sort direction, click the same sort icon again. To disable the sort option, you need to set the `showSortIcon` to **false**.

> By default, the sort icon is enabled in the grouping bar.

{% aspTab template="pivot-grid/grouping-bar/show-sort", sourceFiles="ShowSort.cs" %}

{% endaspTab %}

## Show/hide remove icon

In order to filter members in a field, click the filter icon in the pivot button and check/uncheck the members that needs to be displayed. To disable the filter icon, you need to set `showFilterIcon` to **false**.

The Grouping Bar has an option to remove a particular field at run time. In order to remove a field, click the remove icon in the pivot button. To disable the remove icon, you need to set the `showRemoveIcon` to **false**.

> By default, the remove icon is enabled in the grouping bar.

{% aspTab template="pivot-grid/grouping-bar/show-remove", sourceFiles="ShowRemove.cs" %}

{% endaspTab %}

## See Also

* [Change load limited data in member editor](./how-to/change-load-limited-data-in-member-editor)
* [Customize the icons for pivot grid](./how-to/customize-the-icons-for-pivot-grid)