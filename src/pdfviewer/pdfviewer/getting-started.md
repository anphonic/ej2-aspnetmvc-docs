---
title: "Getting Started"
component: "PDF Viewer"
description: "Learn how to get started using ASP.NET MVC PDF Viewer component through simple steps."
---

# Getting Started with ASP.NET MVC

> Starting with v16.4.0.x, if you reference Syncfusion assemblies from trial setup or from the NuGet feed, include a license key in your projects. Refer to this [link](https://help.syncfusion.com/common/essential-studio/licensing/license-key) to learn about registering Syncfusion license key in your ASP.NET MVC application to use Syncfusion components.

## Prerequisites

To get started with ASP.NET MVC application, ensure that the following software is installed on the machine.

* Visual Studio
* .Net Framework 4.5 and above.
* ASP.NET MVC 4 or ASP.NET MVC 5

## Preparing ASP.NET MVC application

The following steps are used to create ASP.NET MVC application.

**Step 1:** Create ASP.NET MVC web application with default template project in Visual Studio.

![Default Template](./images/default-template-mvc.png)

**Step 2:** After creating the project, add the following dependencies to your application by using `NuGet Package Manager`.

* Syncfusion.EJ2.MVC5
* Syncfusion.EJ2.PdfViewer.AspNet.Mvc5

Open the `NuGet` package manager.

![Solution Explorer](./images/solution-explorer-mvc.png)

Install the **Syncfusion.EJ2.MVC5** package to the application.

![Nuget Demo](./images/nuget_ej2_mvc.png)

Install the **Syncfusion.EJ2.PdfViewer.AspNet.Mvc5** package to the application.

**Step 3 :** Added the following assemblies in `Views\Shared\_Layout.cshtml` and `Index.cshtml` view page.

 ```html
@using Syncfusion.EJ2
@using Syncfusion.EJ2.PdfViewer

```

**Step 4:** Add client side resource through [`CDN`](http://ej2.syncfusion.com/15.4.23/documentation/base/deployment.html?lang=typescript#cdn) or local [`package`](https://www.npmjs.com/package/@syncfusion/ej2) in the layout page `Views\Shared\_Layout.cshtml`.

```html

<head>
@* Syncfusion Essential JS2 Scripts *@
<script src="https://cdn.syncfusion.com/ej2/dist/ej2.min.js"></script>
</head>

```

**Step 5:** Adding Script Manager in the layout page `_Layout.cshtml`.

```html

<body>
    @RenderBody()
    @RenderSection("scripts", required: false)
    @Html.EJS().ScriptManager()
</body>

```

**Step 6:** Add the following code to the Index.cshtml view page, which is presented under Views/Home folder, to initialize the PDF Viewer.

{% aspTab template="pdfviewer/getting-start-mvc", sourceFiles="PdfViewerController.cs" %}

{% endaspTab %}

> You can refer to our [ASP.NET MVC PDF Viewer](https://www.syncfusion.com/aspnet-mvc-ui-controls/pdf-viewer) feature tour page for its groundbreaking feature representations. You can also explore our [ASP.NET MVC PDF Viewer example](https://ej2.syncfusion.com/aspnetmvc/PdfViewer/Default#/material) to understand how to explains core features of PDF Viewer.