---
title: "Virtual Scrolling"
component: "Pivot Grid"
description: "Virtual Scrolling allows user to load large amount of data without performance degradation."
---

# Virtual Scrolling

The virtual scrolling option allows you to load the large amounts of data without performance degradation by rendering rows and columns only in the content viewport. The data will refresh dynamically on vertical or horizontal scroll. This feature can be enabled by setting the `enableVirtualization` property to **true**.

{% aspTab template="pivot-grid/virtual-scrolling", sourceFiles="VirtualScrolling.cs" %}

{% endaspTab %}

> The `height` and `width` properties should be set for virtual scrolling. If it is not defined then the pivot grid will consider its value as `300px` and `800px` respectively.

## Limitations for virtual scrolling

* In virtual scrolling, the column width should be in pixel and percentage values are not accepted.
* Due to the element height limitation in browsers, the maximum number of records loaded by the pivot grid is limited by the browser capability.
