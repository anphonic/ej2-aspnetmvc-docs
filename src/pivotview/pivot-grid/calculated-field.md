---
title: "Calculated Field"
component: "Pivot Grid"
description: "Calculated field allows the user to add a new field (user-defined) dynamically based on a simple mathematical formula."
---

# Calculated Field

Allows user to insert or add a new calculated field based on the available fields from the bound data source using basic arithmetic operators.

Calculated field can be included in pivot grid using the `calculatedFieldsSettings` property through code behind. The setting required for calculate field feature at code behind are:
* `name`: It allows to indicate the given calculated field with unique name.
* `formula`: It allows to set the formula base on the given data source.

Or else, calculated fields can be added at run time through the built-in dialog by just setting the `allowCalculatedField` property to **true** in Pivot Grid. You can see a button enabled in Field List UI to invoke the calculated field dialog.

> The calculated field is applicable only for value fields.

{% aspTab template="pivot-grid/calculatedfield", sourceFiles="calculatedfield.cs" %}

{% endaspTab %}

Meanwhile, you can also display the calculated field dialog independently through other means. For example, you can invoke the dialog on an external button click which is shown in the below code sample.

{% aspTab template="pivot-grid/getting-start-core/calculatedfield", sourceFiles="calculatedfield.cs" %}

{% endaspTab %}