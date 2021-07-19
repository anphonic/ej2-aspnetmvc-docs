---
title: "ASP.NET MVC Rich Text Editor Toolbar configuration"
component: "Rich Text Editor"
description: "This section for Syncfusion ASP.NET MVC Rich Text Editor control explains the toolbar which provides a set of commands for editing and formatting the content."
---

# Toolbar

The Rich Text Editor’s toolbar contains a collection of tools such as bold, italic and text alignment buttons that are used to format the content. However, in most integrations, it's desirable to change the toolbar configuration to suit needs. Fortunately, that's quite easy to do too.

To create Rich Text Editor with Markdown editing feature, it can be added by defining the Toolbar as a collection of built-in items.

The Rich Text Editor allows you to configure different types of toolbar using `Type` field in [`ToolbarSettings`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.RichTextEditor.RichTextEditor.html#Syncfusion_EJ2_RichTextEditor_RichTextEditor_ToolbarSettings) property. The types of toolbar are:

1. Expand
2. MultiRow

## Expand Toolbar

The default mode of [`Type`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.RichTextEditor.RichTextEditor.html#Syncfusion_EJ2_RichTextEditor_RichTextEditor_ToolbarSettings) is `Expand`, it will hide the overflowing items in the next row. By clicking the expand arrow, view the overflowing toolbar items.

{% aspTab template="rich-text-editor/toolbar-expand", sourceFiles="controller.cs" %}

{% endaspTab %}

## Multi-row Toolbar

Set the type as `MultiRow` in [`ToolbarSettings`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.RichTextEditor.RichTextEditor.html#Syncfusion_EJ2_RichTextEditor_RichTextEditor_ToolbarSettings) to moves the overflowing items in the next row. All toolbar items are visible.

{% aspTab template="rich-text-editor/toolbar-multi", sourceFiles="controller.cs" %}

{% endaspTab %}

## Floating Toolbar

By default, toolbar is float at the top of the Rich Text Editor on scrolling. By disabling the [`EnableFloating`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.RichTextEditor.RichTextEditor.html#Syncfusion_EJ2_RichTextEditor_RichTextEditor_ToolbarSettings), toolbar at the top of the content area of Rich Text Editor. Floating toolbar offset can be customize by specifies the offset of the floating toolbar from documents top position using [`FloatingToolbarOffset`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.RichTextEditor.RichTextEditor.html#Syncfusion_EJ2_RichTextEditor_RichTextEditor_FloatingToolbarOffset).

Enable or disable the floating toolbar using `EnableFloating` of `ToolbarSettings` property.

{% aspTab template="rich-text-editor/floating-toolbar", sourceFiles="controller.cs" %}

{% endaspTab %}

## Toolbar Items

The following table lists the available tools on the toolbar.

| Name | Summary | Initialization |
|----------------|---------|------------------------------------------|
| Undo | Allows to undo the actions.|toolbarSettings: { items: ['Undo']} |
| Redo | Allows to redo the actions.|toolbarSettings: { items: ['Redo']}|
| Alignment | Align the content with left, center, and right margin.|toolbarSettings: { items: ['Alignments']}|
| OrderedList | Create a new list item(numbered). |toolbarSettings: { items: ['OrderedList']}|
| UnorderedList | Create a new list item(bulleted). |toolbarSettings: { items: ['UnorderedList']}|
| Indent | Allows to increase the indent level of the content.|toolbarSettings: { items: ['Indent']}|
| Outdent | Allows to decrease the indent level of the content.|toolbarSettings: { items: ['Outdent']}|
| Hyperlink | Creates a hyperlink to a text or image to a specific location in the content.|toolbarSettings: { items: ['CreateLink']}|
| Images | Inserts an image from an online source or local computer. |toolbarSettings: { items: ['Image']}|
| LowerCase | Change the case of selected text to lower in the content. |toolbarSettings: { items: ['LowerCase']}|
| UpperCase | Change the case of selected text to upper  in the content.|toolbarSettings: { items: ['UpperCase’']}|
| SubScript | Makes the selected text as subscript (lower).|toolbarSettings: { items: ['SubScript']}|
| SuperScript | Makes the selected text as superscript (higher).|toolbarSettings: { items: ['SuperScript’']}|
| Print | Allows to print the editor content. |toolbarSettings: { items: ['Print']}|
| FontName | Defines the fonts that appear under the Font Family DropDownList from the Rich Text Editor's toolbar. |toolbarSettings: { items: ['FontName']}|
| FontSize | Defines the font sizes that appear under the Font Size DropDownList from the Rich Text Editor's toolbar.|toolbarSettings: { items: ['FontSize']}|
| FontColor | Specifies an array of colors can be used in the colors popup for font color.|toolbarSettings: { items: ['FontColor']}|
| BackgroundColor | Specifies an array of colors can be used in the colors popup for background color.|toolbarSettings: { items: ['BackgroundColor']}|
| Format | An Object with the options that will appear in the Paragraph Format dropdown from the toolbar. |toolbarSettings: { items: ['Formats']}|
| StrikeThrough | Apply double line strike through formatting for the selected text. |toolbarSettings: { items: ['StrikeThrough']}|
| ClearFormat | The clear format tool is useful to remove all formatting styles (such as bold, italic, underline, color, superscript, subscript, and more) from currently selected text. As a result, all the text formatting will be cleared and return to its default formatting styles.|toolbarSettings: { items: ['ClearFormat']}|
| FullScreen | Stretches the editor to the maximum width and height of the browser window.|toolbarSettings: { items: ['FullScreen']}|
| SourceCode | Rich Text Editor includes the ability for users to directly edit HTML code via “Source View”. If you made any modification in Source view directly, synchronize with Design view.|toolbarSettings: { items: ['SourceCode']}|
| Table | Creates a table to a specific location in the content |toolbarSettings: { items: ['CreateTable']}|
| NumberFormatList | Allows to create list items with various list style types(numbered)|toolbarSettings: { items: ['NumberFormatList']}|
| BulletFormatList | Allows to create list items with various list style types(bulleted)|toolbarSettings: { items: ['BulletFormatList']}|
| JustifyLeft | Allows each line to begin at the same distance from the editor’s left-hand side. | toolbarSettings: { items: ['JustifyLeft']} |
| JustifyCenter |There is an even space on each side of each line since the text is not aligned to the left or right margins. | toolbarSettings: { items: ['JustifyCenter']} |
| JustifyRight | Allows each line to end at the same distance from the editor’s right-hand side. | toolbarSettings: { items: ['JustifyRight']} |
| JustifyFull |The text is aligned with both right and left margins. | toolbarSettings: { items: ['JustifyFull']} |
| Bold | Text that is thicker and darker than usual. | toolbarSettings: { items: ['Bold']} |
| Italic |Shows a text that is leaned to the right. | toolbarSettings: { items: ['Italic']} |
| Underline | The underline is added to the selected text. | toolbarSettings: { items: ['Underline']} |
| ClearAll | Removes all styles that have been applied to the selected text.| toolbarSettings: { items: ['ClearAll']} |
| Cut | Removes the text from its current location and places it into the clipboard. | toolbarSettings: { items: ['Cut']} |
| Copy | The selected item is copied and pasted into the clipboard. | toolbarSettings: { items: ['Copy']} |
| Paste | Allows you to insert a clipboard item into a specific location. | toolbarSettings: { items: ['Paste']} |
| OpenLink | To open the URL link that is  attached to the selected text. | toolbarSettings: { items: ['OpenLink']} |
| EditLink | Allows you to change the URL that has been attached to a specific item. | toolbarSettings: { items: ['EditLink']} |
| CreateTable | Create a table with defined columns and rows. | toolbarSettings: { items: ['CreateTable']} |
| RemoveTable | Removes the selected table and its contents. | toolbarSettings: { items: ['RemoveTable']} |
| Replace | Replace the selected image with another image. | toolbarSettings: { items: ['Replace']} |
| Align | The image can be aligned to the right, left, or center. | toolbarSettings: { items: ['Align']} |
| Remove | Allows to remove the selected image from the editor. | toolbarSettings: { items: ['Remove']} |
| OpenImageLink | Opens the link that is attached to the selected image. | toolbarSettings: { items: ['OpenImageLink']} |
| EditImageLink | Allows to edit the link that is attached to the selected image. | toolbarSettings: { items: ['EditImageLink']} |
| RemoveImageLink | Removes the link that is attached to the selected image. | toolbarSettings: { items: ['RemoveImageLink']} |
| InsertLink |Allows users to add a link to a particular item. | toolbarSettings: { items: ['InsertLink']} |
| Display | Allows you to choose whether an image should be shown inline or as a block. | toolbarSettings: { items: ['Display']} |
| AltText | To display image description when an image on a Web page cannot be displayed. | toolbarSettings: { items: ['AltText']} |
| Dimension | Allows you to customize the image’s height and width. | toolbarSettings: { items: ['Dimension']} |
| Maximize | Stretches the editor to the maximum width and height of the browser window. | toolbarSettings: { items: ['Maximize']} |
| Minimize | Shrinks the editor to the default width and height. | toolbarSettings: { items: ['Minimize']} |
| Preview | Allows to see how the editor’s content looks in a browser. | toolbarSettings: { items: ['Preview']} |
| InsertCode |Represents preformatted text which is to be presented exactly as written in the HTML file. | toolbarSettings: { items: ['InsertCode']} |
| RemoveLink | Allows you to remove the applied link from the selected item. | toolbarSettings: { items: ['RemoveLink']} |
| TableHeader | Allows you to add a table header. | toolbarSettings: { items: ['TableHeader']} |
| TableColumns | Shows the dropdown to insert a column or delete the selected column. | toolbarSettings: { items: ['TableColumns']} |
| TableRows | Shows the dropdown to insert a row ors delete the selected row. | toolbarSettings: { items: ['TableRows']} |
| TableCellHorizontalAlign | Allows the table cell content to be aligned horizontally. | toolbarSettings: { items: ['TableCellHorizontalAlign']} |
| TableCellVerticalAlign | Allows the table cell content to be aligned vertically. | toolbarSettings: { items: ['TableCellVerticalAlign']} |
| TableEditProperties | Allows you to change the table width, padding, and cell spacing styles. | toolbarSettings: { items: ['TableEditProperties']} |

By default, tool will be arranged in following order.

> items: ['Bold', 'Italic', 'Underline', '|', 'Formats', 'Alignments', 'OrderedList', 'UnorderedList', '|', 'CreateLink', 'Image', '|', 'SourceCode', 'Undo', 'Redo']

We can customize the tools order as our application requirement. If you are not specifying any tools order, the editor will create the toolbar with default items.

## Custom Tool

The Rich Text Editor allows you to configure your own commands to its toolbar using [`ToolbarSettings`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.RichTextEditor.RichTextEditor.html#Syncfusion_EJ2_RichTextEditor_RichTextEditor_ToolbarSettings) property. The command can be plain text, icon, or HTML template. You can also define the order and group where the command should be included. Bind the action to the command by getting its instance.

This sample shows how to add your own commands to toolbar of the Rich Text Editor. The “Ω” command is added to insert special characters in the editor.

The below code snippet, for custom tool with tooltip text which will be included in `Items` field of `ToolbarSettings` property.

```csharp

    var tools = new {
        tooltipText = "Insert Symbol",
            template = "<button class='e-tbar-btn e-btn' tabindex='-1' id='custom_tbar'  style='width:100%'><div class='e-tbar-btn-text rtecustomtool' style='font-weight: 500;'> &#937;</div></button>"
    };
    ViewBag.items = new object[] { "Bold", "Italic", "Underline", "|", "Formats", "Alignments", "OrderedList",
        "UnorderedList", "|", "CreateLink", "Image", "|", "SourceCode", tools
        , "|", "Undo", "Redo"
    };

```

Click the “Ω” command to show the special characters list, and then choose the character to be inserted in the editor.

{% aspTab template="rich-text-editor/custom-tool", sourceFiles="controller.cs" %}

{% endaspTab %}

## Quick Inline Toolbar

Quick commands are opened as popup on clicking the corresponding element. The commands must be passed as string collection to image, text, and link attributes of the [`QuickToolbarSettings`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.RichTextEditor.RichTextEditor.html#Syncfusion_EJ2_RichTextEditor_RichTextEditor_QuickToolbarSettings) property.

| Target Element | Default Quick Toolbar items |
|----------------|---------|
| Image | 'Replace', 'Align', 'Caption', 'Remove', 'InsertLink', 'Display', 'AltText','Dimension'.|
| Link | 'Open', 'Edit', 'UnLink'.|
| Text  (`Deprecated`) | 'Cut', 'Copy', 'Paste'.|
| Table| 'TableHeader', 'TableRows', 'TableColumns', 'BackgroundColor', '-', 'TableRemove', 'Alignments', 'TableCellVerticalAlign', 'Styles'.|

Custom tool can be added to the corresponding quick toolbar, using [`QuickToolbarSettings`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.RichTextEditor.RichTextEditor.html#Syncfusion_EJ2_RichTextEditor_RichTextEditor_QuickToolbarSettings) property.

The below sample demonstrates the option to insert the image to the Rich Text Editor content as well as option to rotate the image through the quick toolbar.

{% aspTab template="rich-text-editor/quick-inline", sourceFiles="controller.cs" %}

{% endaspTab %}

## See Also

* [How to render the toolbar in inline mode](./inline-mode/)