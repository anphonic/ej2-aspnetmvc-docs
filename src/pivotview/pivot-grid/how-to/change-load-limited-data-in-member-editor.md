# Improve filter dialog performance when handling large data

In the filter dialog, user can set the limit to display field values while loading the large data. Based on this limit, the initial loading will complete quickly without any performance constraint. And user can use search option to refining the field values from exceeded limit. You can refine the data further by using search option and a message with the remaining data count will be displayed in member editor. The data limit can be set in the property `maxNodeLimitInEditor`.

By default, the property holds the value `1000`.

> The property is available in both Pivot Grid and Field List components.

In the below example, the data in the member editor limits to 100. So, the member editor of the field `ProductID` shows only its first 100 members from its 1000 members.

{% aspTab template="pivot-grid/limit-data/limit-data", sourceFiles="LimitData.cs" %}

{% endaspTab %}
