---
title: "Drill Through"
component: "Pivot Grid"
description: "Drill Through allows to view the detailed data of the summarized cell."
---

# Drill Through

Allows the user to view the detailed data or an original values of the summarized cell of the pivot table. It can be enabled by setting the `allowDrillThrough` property to `true`. On double clicking any value cell, you can view detailed report in new window. In this reports, user can get the row and column headers and summary value(measure) of the clicked cell.
Also, user can include/exclude the fields which available in the data source using column chooser option. By default, detailed reports showing for bounded fields in the pivot report.

{% aspTab template="pivot-grid/drill-through", sourceFiles="DrillThrough.cs" %}

{% endaspTab %}
