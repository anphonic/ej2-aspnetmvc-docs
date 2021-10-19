# Customize the icons for pivot grid

You can customize the pivot button icons in the pivot grid by overriding the class **.pivot-button** with a custom property content as mentioned below.

```html

<style>
#PivotView_PivotFieldList .e-icons.e-toggle-field-list::before {
    content: '\e337';
}
</style>

```

In the below sample, pivot grid is rendered with a customized pivot button icons.

{% aspTab template="pivot-grid/icon-customize/customize", sourceFiles="IconCustomize.cs" %}

{% endaspTab %}
