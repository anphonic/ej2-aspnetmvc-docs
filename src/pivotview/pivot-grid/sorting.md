---
title: "Sorting"
component: "Pivot Grid"
description: "Sorting allows user to order the field headers either in ascending or descending."
---

# Sorting

Sorting allows you to order the field header in rows and columns either in ascending or descending. Sorting can been enabled by setting the `enableSorting` property to **true**.

> By default, field headers in rows and columns are in ascending order.

## Sorting through UI

Sorting can also be performed through UI option available in [`grouping bar`](./grouping-bar) and [`field list`](./field-list) at run time.

## Sorting through code

Sorting can be configured using the `sortSettings` option through code behind, during initial rendering. The settings required to sort are:
* `name`: It allows to set the field name.
* `order`: It allows to set the sort direction of the respective field.

{% aspTab template="pivot-grid/sorting", sourceFiles="Sorting.cs" %}

{% endaspTab %}

## See Also

* [Value Sorting](./value-sorting)