---
title: "User interaction with form fields"
component: "PDF Viewer"
description: "Learn about the User interaction with form fields support in PDF Viewer."
---

# User interaction with form fields

The PDF viewer control provides the option for interaction with Form Fields such as Drag and resize. you can draw a Form Field dynamically by clicking the Form Field icon on the toolbar and draw it in the PDF document. The Form Fields type supported by the PDF Viewer Control are:

    * Textbox
    * Password
    * CheckBox
    * RadioButton
    * ListBox
    * DropDown
    * SignatureField
    * InitialField

## Enable or Disable form designer toolbar

We should inject FormDesigner module and set enableFormDesignerToolbar as true to enable the Form designer icon on the toolbar. By default, enableFormDesignerToolbar is set as true. Use the following code to inject FormDesigner module and to enable the enableFormDesignerToolbar property.

```html
    <div style="width:100%;height:600px">
        @Html.EJS().PdfViewer("pdfviewer").ServiceUrl(VirtualPathUtility.ToAbsolute("~/api/PdfViewer/")).EnableFormDesignerToolbar(true).DocumentPath("Hive_Succinctly.pdf").Render()
    </div>

```

## Add the form field dynamically

Click the Form Field icon on the toolbar and then click on to the PDF document to draw a Form Field. Refer the below GIF for further reference.

![Alt text](../../pdfviewer/images/addformfield.gif)

## Drag the form field

We provide options to drag the Form Field which is currently selected in the PDF document. Refer the below GIF for further reference.

![Alt text](../../pdfviewer/images/dragformfield.gif)

## Resize the form field

We provide options to resize the Form Field which is currently selected in the PDF document. Refer the below GIF for further reference.

![Alt text](../../pdfviewer/images/resizeformfield.gif)

## Edit or Update the form field dynamically

The properties of the Form Fields can be edited using the Form Field Properties window. It can be opened by selecting the Properties option in the context menu that appears on the right by clicking the Form Field object. Refer the below image for the properties available to customize the appearance of the Form Field.  

![Alt text](../../pdfviewer/images/generalproperties.png)

![Alt text](../../pdfviewer/images/appearanceproperties.png)

![Alt text](../../pdfviewer/images/dropdownproperties.png)

## Clipboard operation with form field

The PDF Viewer control supports the clipboard operations such as cut, copy and paste for Form Fields. You can right click on the Form Field object to view the context menu and select to the clipboard options that you would like to perform. Refer the below image for the options in the context menu.

![Alt text](../../pdfviewer/images/clipboardformfield.png)

## Undo and Redo

We provided support to undo/redo the Form Field actions that are performed at runtime. Use the following code example to perform undo/redo actions.

```html
    <button id="undo">Undo</button>
    <button id="redo">Redo</button>
    <div style="width:100%;height:600px">
         @Html.EJS().PdfViewer("pdfviewer").ServiceUrl(VirtualPathUtility.ToAbsolute("~/api/PdfViewer/")).DocumentPath("Hive_Succinctly.pdf").Render()
    </div>
    <script>
        document.getElementById('undo').addEventListener('click', function() {
            var pdfviewer = document.getElementById("pdfviewer").ej2_instances[0];
            pdfviewer.undo();
        });
         document.getElementById('redo').addEventListener('click', function() {
             var pdfviewer = document.getElementById("pdfviewer").ej2_instances[0];
            pdfviewer.redo();
        });
    </script>
```