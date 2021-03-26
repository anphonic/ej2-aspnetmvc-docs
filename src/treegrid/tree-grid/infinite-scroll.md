---
title: "Infinite Scrolling"
component: "Tree Grid"
description: "Learn how to improve performance in the Essential JS 2 Tree Grid control by using infinite scroll feature. Also learn about the limitations of this feature."
---

# Infinite scrolling

Infinite scrolling is used to load a huge amount of data without degrading the Tree Grid performance. This feature works like the lazy loading concept, which means the buffer data is loaded only when the scrollbar reaches the end of the scroller.

To use Infinite scrolling, set `EnableInfiniteScrolling` property as true.

> * In this feature, Tree Grid will not make a new data request when you visit the same page again.

{% aspTab template="tree-grid/infinite-scroll/infinite", sourceFiles="infinitescroll.cs" %}

{% endaspTab %}

## InitialBlocks

You can define the initial loading pages count by using `InitialBlocks` property of `InfiniteScrollSettings`. By default, this feature loads three pages in initial rendering.

In the below demo, we have changed this property value to load five page records instead of three.

{% aspTab template="tree-grid/infinite-scroll/initialblocks", sourceFiles="infinitescroll.cs" %}

{% endaspTab %}

## Cache Mode

Cache is used to store the loaded rows object in the Tree Grid instance which can be reused for creating the row elements whenever you scroll to already visited page. Also, this mode maintains row elements based on the `MaxBlocks` count value of `InfiniteScrollSettings`, once this limit exceeds then it will remove row elements from DOM for new rows.

To enable the cache mode in Infinite scrolling, set `EnableCache` property of `InfiniteScrollSettings` as true.

{% aspTab template="tree-grid/infinite-scroll/cache", sourceFiles="infinitescroll.cs" %}

{% endaspTab %}

## Limitations for Infinite Scrolling

* Due to the element height limitation in browsers, the maximum number of records loaded by the tree grid is limited due to the browser capability.
* Initial loading rows total height must be greater than the viewport height.
* Cell selection will not be persisted in cache mode.
* Infinite scrolling is not compatible with batch editing, detail template and hierarchy features.
* The aggregated information and total group items are displayed based on the current view items. To get these information regardless of the view items, refer to the
* Programmatic selection using the [`selectRows`](../api/treegrid/#selectrows) and [`selectRow`](../api/treegrid/#selectrow) method is not supported in infinite scrolling.