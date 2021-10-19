---
title: "Member Filtering"
component: "Pivot Grid"
description: "Member filtering allows user to view pivot grid with particular records based on selected members."
---

# Member filtering

Member filtering allows you to view Pivot Grid with particular records based on filter criteria.

## Filtering through UI

Filtering can also be performed through UI option available in [`grouping bar`](./grouping-bar) and [`field list`](./field-list) at run time.

## Filtering through code

It can be configured using the `filterSettings` option through code-behind. The settings required to filter at initial rendering are:
* `name`: It allows to set field name.
* `type`: It allows to set filter type as either "Include" or "Exclude" to the field.
* `items`: It allows to set the filter members of the field.

{% aspTab template="pivot-grid/filtering/member-filtering", sourceFiles="Filtering.cs" %}

{% endaspTab %}

## See Also

* [Label Filtering](./label-filtering)
* [Value Filtering](./value-filtering)