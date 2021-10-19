---
title: "Drill Operation"
component: "Pivot Grid"
description: "Expand or collapse headers displayed in rows and columns."
---

# Drill Operation

## Expand All

Pivot Grid allows you to either expand or collapse all headers that are displayed in rows and columns using `expandAll` property. To display Pivot Grid with all headers at collapsed state, set the property `expandAll` to **false**.

> By default, all headers in rows and columns are in expanded state.

{% aspTab template="pivot-grid/drill-down/expand-all", sourceFiles="ExpandAll.cs" %}

{% endaspTab %}

## Drill Up/Down

Also, you can expand/collapse specific header(s) in each fields under row and column using the `drilledMembers` property through code behind. The settings required to expand/collapse specific header(s) during initial rendering are:
* `name`: It allows to set the field name, whose members needs to be drilled.
* `items`: It allows to set the members which needs to be drilled.

> The **drilledMembers** option always work in vice-versa manner with respect to the property **expandAll** in Pivot Grid. For example, if **expandAll** is set to true, then the **drilledMembers** will be set in collapsed state.

{% aspTab template="pivot-grid/drill-down/drilled-members", sourceFiles="DrilledMembers.cs" %}

{% endaspTab %}