# Customize number, date, and time values

You can format the number, date, and time values for each field using `formatSettings` option under `dataSource`. It can be configured through code behind, during initial rendering.

## Number formatting

For numbers, the formatting settings required to apply through code behind are:

* `name`: It allows to set the field name.
* `format`: It allows to set the format of the respective field.

> Also, you can customize the applied number format by setting the [`NumberFormatOptions`](https://ej2.syncfusion.com/documentation/common/intl.html?lang=typescript#manipulating-numbers) options in `formatSettings` itself.

{% aspTab template="pivot-grid/formatting/number", sourceFiles="Number.cs" %}

{% endaspTab %}

## Date and time formatting

For date and time, the formatting settings required to apply through code behind are:

* `name`: It allows to set the field name.
* `format`: It allows to set the format of the respective field.
* `type`: It allows to set the type of format to be used for the respective field.

> Also, you can customize the applied date format by setting [`DateFormatOptions`](https://ej2.syncfusion.com/documentation/common/intl.html?lang=typescript#manipulating-datetime) options in `formatSettings` itself.

{% aspTab template="pivot-grid/formatting/date", sourceFiles="Date.cs" %}

{% endaspTab %}
