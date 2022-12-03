.Net Core:
Buit on top of .Net MVC and it is very robust.

Advantages of .Net Core:
- Fast and Open Source
- Cross Platform > Window, Linux
- Built In Dependency Injection
- Easy Update
- Cloud Friendly
- High Performance

Dependency Injection:
Dependency injection is a design pattern in which classes are not allowed to create dependencies. Rather, they request dependencies from external sources. This design pattern strongly holds that a class should not configure its dependencies statically.

It is an integral part of ASP .Net Core Architecture. .Net Core inject object of dependency classes to constructor using the built in IoC Container.

Advantages of DI:
- Loose Coupling / More flexibity
- Security
- Improves code reusability.
- Eases the unit testing of applications through mocking/stubbing injected dependencies.
- Makes it easier to extend the application classes.
- Enhances the configuration of applications

Note : We have to register the concrete class so that IoC container can inject object.

CsProj File:
- PropertyGroup
  Section define the target framework which we are using.
- ItemGroup
  ItemGroup contain all the Nuget packages which we will install and use in the project.

Properties
- launchSettings.json
  This file is containing different profiles through which we can run our application
  
  IIS Express Profile:
  Port: 44330
  Application Url: http://localhost:28792

  Default Profile:
  Launch command line and then launch the website.
  Application Url : "https://localhost:7129;http://localhost:5129"

wwwroot folder:
This will be containing the static web files.
- css
- js
- lib
- favicon.ico

appsettings.json
This file will be containing all the application secrets that are used in the application. Eg. API Keys, Connection String

We can create different app file for different environment.

Program.cs File
Responsible for running the application. 

If you want to register some concrete class/services you have to do in Program.cs file.(For Dependency Injection) (Before Build You need to add)

Pipeline:
A pipeline specify how web application should response to different web request. When an application receive a request from the browser it will go back and forth to the pipeline.

A pipeline is made up of different middlewares and MVC is type of middleware itself.

Middleware:
- MVC
- AUth
- Static Files

Note: Order of pipeline is very important. For instance authentication should alway come before autherization.

MVC - Model View Controller
- Model : Define shape of the data. Represent all the data in the application.
- View : Represents the User Interface.
- Controller : Handles the user request and acts as an interface between Model & View. Heart of the MVC Application.

Routing:
Consist of Controller and Action. The URL pattern for routing is considered after the domain name.
- https://localhost:55555/Category/Index/3
- https://localhost:55555/{Controller}/{Action}/{id}

Default Controller - Home Controller
Default Action - Index
Default Id - Null

Action Result:
Action Result is a result of action method/pages or return type of action methods/pages handlers.

IActionResult Interface
Abstraction layer for view. It is the parent for many of the derived classes that have associated helper. It is appropriate when multiple Action Result return type are possible in an action.

Below are the Concrete Classes for IActionResult are:
- ViewResult
- PartialViewResult
- JsonResult
- FileResult
- RedirectResult
- ContentResult
- EmptyResult
- RedirectToActionResult
- JavaScriptResult


Shared Folder:
For Partial View. View within a view.

- _Layout.cshtml : Default Master Page.
- _ValidationScriptsPartial.cshtml : View having the validation script.
- _Error.cshml : View for Errors


_ViewImports.cshtml
This file is for global import. Accessible in all the pages.

_ViewStart.cshtml
For defining the default Master Page.

Tag Helper
They are introduced in ASP .Net Core. Tag Helper enable server side code to participate in creating and rendering HTML Element in RAZOR files. Tag Helper are very focussed around the HTML elements and much more natural to use.

Some of the Tag Helper:
- asp-controller
- asp-action
- asp-for
- asp-page
- asp-area
- asp-route-id

Entity Framework Core
It is used to manipulate Data Layer.