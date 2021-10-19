---
title: "Defer Layout Update"
component: "Pivot Grid"
description: "Defer update allows users to update the pivot table only on demand."
---

# Defer Layout Update

Defer layout update support allows you to update the pivot table only on demand. To enable deferred updates in the pivot grid, set the property `allowDeferLayoutUpdate` as **true**.

## Built-in Field List (Pop-up)

The Defer layout update support allows you to update the pivot table only on-demand. To enable Defer layout update in the pivot grid, set the `allowDeferLayoutUpdate` as **true**.

## In-built Field List (Popup)

{% aspTab template="pivot-grid/defer-update/popup", sourceFiles="DeferUpdate.cs" %}

{% endaspTab %}

## Stand-alone Field List (Fixed)

{% aspTab template="pivot-grid/defer-update/static", sourceFiles="Static.cs" %}

{% endaspTab %}