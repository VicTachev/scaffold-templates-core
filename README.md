# scaffold-templates-core

This repository contains scaffold templates that are alternatives to the native .NET Core templates for web application with MVC and RazorPages.

## Getting Started

The scaffolding logic and tools are the same as with the ordinary .NET Core web applications. The main repository and logic for the scaffolding provided by Microsoft is in this repository:  [https://github.com/aspnet/Scaffolding](https://github.com/aspnet/Scaffolding). The original template files are located here: [https://github.com/aspnet/Scaffolding/tree/master/src/VS.Web.CG.Mvc/Templates](https://github.com/aspnet/Scaffolding/tree/master/src/VS.Web.CG.Mvc/Templates).

In order to use the scaffolding provided by Microsoft you can follow these resources:

- [Add a model to an ASP.NET Core MVC app](https://docs.microsoft.com/en-us/aspnet/core/tutorials/first-mvc-app/adding-model?view=aspnetcore-2.1)
- [Add a model to a Razor Pages app in ASP.NET Core](https://docs.microsoft.com/en-us/aspnet/core/tutorials/razor-pages/model?view=aspnetcore-2.1)

## Installing the Kendo UI for ASP.NET Core Scaffold templates

In order to install the scaffold templates from this repository just copy the **Templates** folder and include it in the root of the created project:

![adding templates](https://github.com/telerik/scaffold-templates-core/wiki/2018-11-19_0849.png)

Make sure to exclude the folder from the project so that those files are not compiled. Or you can include the exclude manually in the *.csproj* file:

```xml
  <ItemGroup>
    <Compile Remove="Templates\**" />
    <Content Remove="Templates\**" />
    <EmbeddedResource Remove="Templates\**" />
    <None Remove="Templates\**" />
  </ItemGroup>
```

Next, using the build-in scaffolding utility will output cshtml generated using the custom templates included. In this case, the inputs generated will be the Telerik UI for ASP.NET Core components corresponding to the type of the field.

* `String`: `input` element with Kendo styles;
* `String`(multiline): `textarea` element with Kendo styles;
* `Number`: `kendo-numerictextbox` tag helper;
* `DateTime`: `kendo-datetimepicker` tag helper;
* `Boolean`: `Html.Kendo().CheckBoxFor` helper.
