---
title: "Aggregation"
component: "Pivot Grid"
description: "Aggregation allows user to summarize the measure values."
---

# Aggregation

Users can perform calculations over a group of values using the aggregation option. By default, values are added together. The other aggregation types are explained in below section.

## Aggregation through UI

Aggregation type can change simply with UI support, which option available in [`grouping bar`](./grouping-bar) and [`field list`](./field-list) at run time.

## Aggregation through code

It can be configured using `type` option for each value fields through code-behind. The settings required for summarize the value fields at initial rendering are:

* `type`: It allows to set the aggregate type of the field.
* `baseField`: It allows to set the base field to aggregate the values.
* `baseItem`: It allows to set the base item to aggregate the values.

> By default, the aggregation will be considered as `Sum` to the value fields which had number type and for the value fields which had string type, the aggregation type will be considered as `Count`. **DifferenceFrom** and **PercentageOfDifferenceFrom** can check for specific field of the specific item using `baseField` and `baseItem`. We can consider the **PercentageOfParentTotal** for specific field using `baseField`.

The following are the aggregate types used in value fields:

| Operator | Description |
|------|-------------|
| Sum| Displays the pivot grid values with sum.|
| Product| Displays the pivot grid values with product.|
| Count| Displays the pivot grid values with count.|
| DistinctCount| Displays the pivot grid values with distinct count.|
| Min| Displays the pivot grid with minimum value.|
| Max| Displays the pivot grid with maximum value.|
| Avg| Displays the pivot grid values with average.|
| Index| Displays the pivot grid values with index.|
| PopulationStDev| Displays the pivot grid values with standard deviation of population.|
| SampleStDev| Displays the pivot grid values with sample standard deviation.|
| PopulationVar| Displays the pivot grid values with variance of population.|
| SampleVar| Displays the pivot grid values with sample variance.|
| RunningTotals| Displays the pivot grid values with running totals.|
| DifferenceFrom| Displays the pivot grid values with difference from the value of the base item in the base field.|
| PercentageOfDifferenceFrom| Displays the pivot grid values with percentage difference from the value of the base item in the base field.|
| PercentageOfGrandTotal| Displays the pivot grid values with percentage of grand total of all values.|
| PercentageOfColumnTotal| Displays the pivot grid values in each column with percentage of total values for the column.|
| PercentageOfRowTotal| Displays the pivot grid values in each row with percentage of total values for the row.|
| PercentageOfParentTotal| Displays the pivot grid values with percentage of total of all values based on selected field.|
| PercentageOfParentColumnTotal| Displays the pivot grid values with percentage of its parent total in each column.|
| PercentageOfParentRowTotal| Displays the pivot grid values with percentage of its parent total in each row.|
| CalculatedField| Displays the pivot grid with calculated field values. It allows you to create a new calculated field alone.|

{% aspTab template="pivot-grid/aggregation/aggregation", sourceFiles="aggregation.cs" %}

{% endaspTab %}
