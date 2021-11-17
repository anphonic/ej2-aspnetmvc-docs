---
title: "Getting Started For Tooltip"
component: "Tooltip"
description: "Getting started with ASP.NET MVC Tooltip component."
---

# Getting Started

This section briefly explains about how to render Tooltip component in your ASP.NET MVC application. You can refer [ASP.NET MVC Getting Started documentation](../getting-started/) page for introduction part of the system requirements and configure the common specifications.

> Starting with `v16.2.0.x`, if you reference Syncfusion assemblies from trial setup or from the NuGet feed, you also have to include a license key in your projects. Please refer to this [link](https://help.syncfusion.com/common/essential-studio/licensing/license-key) to know about registering Syncfusion license key in your ASP .NET MVC application to use our components.

## Adding Tooltip component to the Application

Tooltip component can be rendered with the help of `@Html.EJS().Tooltip` tag helper. Add the below code to your `index.cshtml` page which is present under `Views/Home` folder, where the Tooltip is initialized.

```cs

@Html.EJS().Tooltip("Tooltip").Content("Lets go green & Save Earth !!!").ContentTemplate(@<span id='target'>Show Tooltip</span>).Render()

```

## Run the application

 After successful compilation of your application, simply press `F5` to run the application.

The following example shows a basic Tooltip.

{% aspTab template="tooltip/getting-started/mvc", sourceFiles="HomeController.cs" %}

{% endaspTab %}

> In the above sample code, `#target` is the `id` of the element in a page to which the `Tooltip` is initialized.

Output be like the below.

![Tooltip Sample](./images/tooltip.PNG)

## Initialize Tooltip within a container

You can create Tooltips on multiple targets within a container. To do so, you have to define specific target elements to the `target`
property so that the Tooltip is initialized only on matched targets within a container. In this case, the Tooltip content is assigned from the `title` attribute of the target element.

Refer to the following code example to create a Tooltip on multiple targets within a container.

{% aspTab template="tooltip/getting-started/multiple-target-mvc", sourceFiles="HomeController.cs" %}

{% endaspTab %}

Output be like the below.

![ASP .NET Core - Tooltip - Accessibility](./images/tooltip-container.png)

> In the above sample, `#details` refers to the container's id, and the target `.e-info` refers to the target elements available within that container.

## See Also

[Positioning Tooltip](./position)

[Tooltip Open Mode](./open-mode)

[Customize the Tooltip](./customization)