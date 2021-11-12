# Open Editor Window in different ways

## Open Editor Window Manually

Scheduler allows the user to manually open the event editor on specific time or on certain events using `openEditor` method. To open the editor on specific range of time, user need to pass the cell details as first argument and **Add** as second argument whereas to open it on event pass that event detail and **Save** as arguments. In the following code example, on clicking the respective button will open the respective editor window manually.

{% aspTab template="schedule/how-to/event-editor", sourceFiles="data.cs"  %}

{% endaspTab %}

## Open editor window on single click

By default, Scheduler Editor window will open when double clicking the cells or appointments. You can also open the editor window with single click by using `openEditor` method in `EventClick` and `CellClick` events of scheduler and setting false to `ShowQuickInfo`. The following example shows how to open editor window on single click of cells and appointments.

{% aspTab template="schedule/how-to/single-click-editor", sourceFiles="data.cs"  %}

{% endaspTab %}
