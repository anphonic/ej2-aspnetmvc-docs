---
title: "Data Binding"
component: "Pivot Grid"
description: "Learn about how to bind local and remote data source to the pivot grid."
---

# Data Binding

The Pivot Grid uses `DataManager`, which supports both RESTful JSON data service binding and local JavaScript object array binding. The `data` property can be assigned either with the instance of `DataManager` or JavaScript object array collection. It supports two kinds of data binding method:
* Local data
* Remote data

## Local Data

To bind local data to the pivot grid, you can assign a JavaScript object array to the `data` property under `dataSource` option. The local data source can also be provided as an instance of the `DataManager`.

{% aspTab template="pivot-grid/data-binding/local-data", sourceFiles="localdata.cs" %}

{% endaspTab %}

> By default, `DataManager` uses `JsonAdaptor` for local data-binding.

## Remote Data

To interact with remote data source, provide the endpoint `url` within `DataManager` along with appropriate `adaptor`. Now to bind remote data to pivot grid component, assign resultant JavaScript object array from the `DataManager` instance to the `data` property.

{% aspTab template="pivot-grid/data-binding/remote-data", sourceFiles="remotedata.cs" %}

{% endaspTab %}

> By default, `DataManager` uses `ODataAdaptor` for remote data-binding.

## Fields

The fields are used as `dataSource` schema in the Pivot Grid. The four major fields are `rows`, `columns`, `values` and `filters` under `dataSource` option which plays a vital role in rendering the entire widget in a desired format. Also, some of the major pivot grid features such as sorting, filtering and grouping, field list etc... can be performed on these fields. The settings required for each fields at code behind are:
* `name`: It allows to set the field name from the bound data source.
* `caption`: It allows to set the field caption, which is the alias name displayed in pivot grid.
* `type`: It allows to set the summary type of the field.

> The `name` property in each fields is necessary to map the data source values in the Pivot Grid. Moreover, if the field `name` is not properly specified, the pivot grid will be displayed as empty. Also, you will find more details about support summary type option [`here`](./aggregation).

{% aspTab template="pivot-grid/data-binding/local-data", sourceFiles="localdata.cs" %}

{% endaspTab %}

### Values in row axis

By default, the value fields are plotted in column axis. To plot those fields in row axis, use the `valueAxis` property by setting its value as `row`. By default, it holds the value `column`.

{% aspTab template="pivot-grid/data-binding/values-in-row", sourceFiles="valuesinrow.cs" %}

{% endaspTab %}

### Show 'no data' items

By default, the pivot grid only shows the field item if it has data in its row or column combination. To show the all items that do not have data in row and column combination in the pivot grid, use the `showNoDataItems` property by settings its value to `true` for the desired fields. In the following code example, rows of the County and State fields do not have data in all combination with columns(Date).

{% aspTab template="pivot-grid/data-binding/no-data", sourceFiles="nodata.cs" %}

{% endaspTab %}

## See Also

* [Aggregation](./aggregation)
* [Show/Hide Totals](./summary-customization)
* [Customize number, date, and time values](./how-to/customize-number-date-and-time-values)