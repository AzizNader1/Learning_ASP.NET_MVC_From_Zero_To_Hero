# Mastering ASP.NET Core MVC — From Zero to Hero

### A Step-by-Step, Line-by-Line Guided Journey from Absolute Beginner to Mastery

> **Repository status:** This is a complete rewrite of the original `README.md` for `AzizNader1/Learning_ASP.NET_MVC_From_Zero_To_Hero`. The original was a dense reference; this version is a *teaching* document — every chapter assumes nothing more than what the previous chapter taught, every code block is explained line by line, and every concept is built from the ground up.

---

## How To Use This Guide

This guide is not a reference book. It is a **guided course**. Read it top to bottom, in order. Every chapter assumes you have read and understood the previous chapter. If you skip ahead, you will see code and concepts that have not yet been explained, and the explanations will appear terse — because they were written for someone who followed the path.

Each chapter follows the same structure:

1. **What you will learn** — the goal of the chapter in one paragraph.
2. **Why it matters** — the motivation, with concrete examples.
3. **The theory** — concepts explained in plain English, with analogies.
4. **The code** — every line we type, with an explanation for each line.
5. **What just happened** — a recap of what the code did and why.
6. **Try it yourself** — a small exercise to lock the concept in.
7. **Common mistakes** — pitfalls you will hit, and how to fix them.

By the end of Part V you will have built a complete, production-quality MVC application called **TaskManager** — a real task-tracking app with categories, due dates, priorities, authentication, validation, an API surface, tests, and a deployment story. Every chapter from Chapter 12 onward adds one piece of TaskManager. You will end with the full source tree in your head and a portfolio app on your disk.

### Who this guide is for

- You have **never** written ASP.NET code, and you want to learn it properly from the ground up.
- You have used other web frameworks (Django, Laravel, Rails, Express) and want to understand the .NET way.
- You have used ASP.NET Web Forms or Razor Pages and want to understand MVC specifically.
- You want every line of code explained — not just "and now add this code" with no context.

### What you need before you start

- A computer running Windows, macOS, or Linux. ASP.NET Core is fully cross-platform.
- The ability to install software on that computer (admin rights are convenient but not strictly required on most systems).
- About 30 to 60 hours of focused reading and typing, depending on your starting point. This is not a 30-minute skim.

### Conventions used in this guide

- A line of code we are about to discuss is always followed by an explanation block that begins with `// →` for C# code or `<!-- → -->` for HTML/Razor. Read the explanation immediately after reading the line.
- When we add code to an existing file, we **show the surrounding context** so you can find where to insert the new lines.
- When a command is to be typed in a terminal, it appears in a `bash` code block and starts with `$` for Windows PowerShell, or `>` for macOS/Linux shells. Do not type the `$` or `>`.
- Terms being defined for the first time are written in **bold** the first time they appear.

---

## Table of Contents

### Part I — Foundations (Chapters 1–6)
1. [Introduction: What Is ASP.NET MVC and Why Does It Exist?](#part-i--chapter-1--introduction-what-is-aspnet-mvc-and-why-does-it-exist)
2. [The MVC Pattern: History, Theory, and Architecture](#part-i--chapter-2--the-mvc-pattern-history-theory-and-architecture)
3. [Setting Up Your Development Environment](#part-i--chapter-3--setting-up-your-development-environment)
4. [C# Crash Course for MVC Beginners](#part-i--chapter-4--c-crash-course-for-mvc-beginners)
5. [Your First ASP.NET Core MVC Project](#part-i--chapter-5--your-first-aspnet-core-mvc-project)
6. [Anatomy of the Request Pipeline: Program.cs Line by Line](#part-i--chapter-6--anatomy-of-the-request-pipeline-programcs-line-by-line)

### Part II — The Core of MVC (Chapters 7–11)
7. [Controllers: The Heart of MVC](#part-ii--chapter-7--controllers-the-heart-of-mvc)
8. [Routing: How URLs Reach Your Controllers](#part-ii--chapter-8--routing-how-urls-reach-your-controllers)
9. [Views and Razor Syntax](#part-ii--chapter-9--views-and-razor-syntax)
10. [Layouts, Sections, and View Organization](#part-ii--chapter-10--layouts-sections-and-view-organization)
11. [Models, ViewModels, and Data Annotations](#part-ii--chapter-11--models-viewmodels-and-data-annotations)

### Part III — Data with Entity Framework Core (Chapters 12–16)
12. [Introducing Our Sample Project: TaskManager](#part-iii--chapter-12--introducing-our-sample-project-taskmanager)
13. [Entity Framework Core: The ORM That Powers Your Data Layer](#part-iii--chapter-13--entity-framework-core-the-orm-that-powers-your-data-layer)
14. [Migrations: Evolving Your Database Schema](#part-iii--chapter-14--migrations-evolving-your-database-schema)
15. [Relationships: One-to-Many, Many-to-Many, and Eager Loading](#part-iii--chapter-15--relationships-one-to-many-many-to-many-and-eager-loading)
16. [The Repository Pattern and Dependency Injection](#part-iii--chapter-16--the-repository-pattern-and-dependency-injection)

### Part IV — Real-World Application Features (Chapters 17–22)
17. [Forms: Capturing User Input the Right Way](#part-iv--chapter-17--forms-capturing-user-input-the-right-way)
18. [Validation: Server-Side, Client-Side, and Custom](#part-iv--chapter-18--validation-server-side-client-side-and-custom)
19. [Authentication and Authorization with ASP.NET Core Identity](#part-iv--chapter-19--authentication-and-authorization-with-aspnet-core-identity)
20. [Security Essentials: CSRF, XSS, SQL Injection, and Over-Posting](#part-iv--chapter-20--security-essentials-csrf-xss-sql-injection-and-over-posting)
21. [Filters: Cross-Cutting Concerns the Clean Way](#part-iv--chapter-21--filters-cross-cutting-concerns-the-clean-way)
22. [Async Programming in MVC](#part-iv--chapter-22--async-programming-in-mvc)

### Part V — Mastery and Production (Chapters 23–30, plus appendices)
23. [View Components: Reusable UI Logic Beyond Partials](#part-v--chapter-23--view-components-reusable-ui-logic-beyond-partials)
24. [Areas: Organizing Large Applications](#part-v--chapter-24--areas-organizing-large-applications)
25. [Building REST APIs Alongside MVC](#part-v--chapter-25--building-rest-apis-alongside-mvc)
26. [Logging, Error Handling, and Observability](#part-v--chapter-26--logging-error-handling-and-observability)
27. [Testing MVC Applications](#part-v--chapter-27--testing-mvc-applications)
28. [Deployment: From Local to Production](#part-v--chapter-28--deployment-from-local-to-production)
29. [Best Practices, Design Patterns, and Clean Architecture](#part-v--chapter-29--best-practices-design-patterns-and-clean-architecture)
30. [Common Mistakes and How to Avoid Them](#part-v--chapter-30--common-mistakes-and-how-to-avoid-them)

### Appendices
- [Appendix A — Quick Reference Cheatsheet](#appendix-a--quick-reference-cheatsheet)
- [Appendix B — Additional Resources and Next Steps](#appendix-b--additional-resources-and-next-steps)

---

## Part I · Chapter 1 — Introduction: What Is ASP.NET MVC and Why Does It Exist?

### What you will learn in this chapter
You will learn what ASP.NET is, what MVC is, how ASP.NET MVC came to exist, what it provides to you as a developer, and why — in 2026, when there are dozens of web frameworks to choose from — learning ASP.NET Core MVC is still one of the highest-leverage skills you can build.

### What is ASP.NET, exactly?

**ASP.NET** is the name Microsoft gives to its server-side web framework — the part of .NET that runs on a web server and produces HTML (or JSON, or anything else) in response to HTTP requests from browsers. The first version of ASP.NET shipped in January 2002 as part of the original **.NET Framework 1.0**, and it was designed to bring rapid web development to Windows developers coming from Visual Basic and classic ASP.

The original ASP.NET shipped one primary model for building web user interfaces, called **Web Forms**. Web Forms tried to make building a web page feel like building a Windows desktop form: you dragged a button onto a designer, double-clicked it, and wrote a click handler. The framework hid the stateless nature of HTTP behind a mechanism called **View State**, which serialized the entire state of every control on the page into a hidden form field. Click the button, the page posts back to the server, the framework deserializes the state, fires your handler, re-serializes the state, and ships the page back to the browser.

This was enormously productive for line-of-business apps — internal CRUD apps, admin panels, data entry forms. But it had a serious cost: the developer had almost no control over the HTML the framework produced. The rendered markup was full of `id="ctl00_MainContent_Button1"` style names, page sizes ballooned from the view-state field, and the abstraction leaked badly the moment you tried to do anything modern with JavaScript, AJAX, or responsive design.

### Enter ASP.NET MVC

In March 2009, Microsoft shipped **ASP.NET MVC 1.0** as an alternative to Web Forms. It was built by a team led by **Phil Haack**, **Scott Hanselman**, and others, and it was heavily inspired by the Ruby on Rails framework and the broader MVC movement in the Java and Python communities. The pitch was simple: *give the developer full control over the HTML, the URLs, and the request lifecycle, and structure the application using the Model-View-Controller pattern.*

MVC did not replace Web Forms — both shipped side-by-side for years. But it gave developers who wanted to write clean, testable, RESTful, HTML-controlled web applications a first-class option in the .NET ecosystem.

### From ASP.NET MVC to ASP.NET Core MVC

In 2016 Microsoft shipped **.NET Core 1.0** — a complete rewrite of .NET that runs on Windows, macOS, and Linux, and a complete rewrite of ASP.NET called **ASP.NET Core**. ASP.NET Core MVC is the spiritual successor to ASP.NET MVC 5: same patterns, same controller-and-views idea, but rebuilt on a much faster, cross-platform, cloud-friendly runtime.

The version line looks like this:

| Year | Release | What changed |
|------|---------|--------------|
| 2002 | ASP.NET 1.0 (Web Forms) | First release of ASP.NET. |
| 2009 | ASP.NET MVC 1.0 | MVC pattern added as an alternative to Web Forms. |
| 2013 | ASP.NET MVC 5 | Last release on the old .NET Framework. Still widely used in legacy enterprise apps. |
| 2016 | ASP.NET Core MVC 1.0 | Complete rewrite, cross-platform, much faster. |
| 2018 | ASP.NET Core 2.0 / 2.1 | Razor Pages added; Identity consolidated. |
| 2020 | ASP.NET Core 3.0 / 3.1 | Dropped legacy .NET Framework support; endpoint routing. |
| 2020 | ASP.NET Core 5.0 | Began unifying the version numbers with .NET. |
| 2021 | ASP.NET Core 6.0 | LTS. Minimal APIs introduced. Top-level statements in `Program.cs`. |
| 2022 | ASP.NET Core 7.0 | Rate limiting, output caching. |
| 2023 | ASP.NET Core 8.0 | LTS. Native AOT improvements, server-sent events. |
| 2024 | ASP.NET Core 9.0 | Static asset delivery improvements. |
| 2025 | ASP.NET Core 10.0 | LTS. Latest release as of this guide. |

This guide targets **ASP.NET Core 8.0**, the current Long-Term Support release. Everything you learn here transfers cleanly to 9.0 and 10.0. The differences between 5.0 and 8.0 are mostly additive — the chapters in this guide will note when a feature is version-specific.

### What does ASP.NET Core MVC provide to you?

When you write `dotnet new mvc`, here is what you get, out of the box, for free:

1. **A web server.** ASP.NET Core ships with **Kestrel**, a high-performance HTTP server written entirely in C#. You do not need IIS, Apache, or Nginx to run your app locally — Kestrel is the server. In production, Kestrel is usually placed behind IIS or Nginx as a reverse proxy, but Kestrel is the actual HTTP listener.

2. **A routing engine.** You describe URL patterns like `{controller=Home}/{action=Index}/{id?}`, and the engine routes incoming requests to the right controller method. You never write `if (path == "/products") { ... }` chains.

3. **A model binder.** When a request comes in for `/products/details/5`, the framework parses the `5` from the URL, converts it to an `int`, and passes it as an argument to your action method. When a POST request comes in with a JSON body, the binder deserializes it into a C# object for you.

4. **A view engine called Razor.** You write `.cshtml` files that mix HTML and C#. Razor compiles them at runtime into in-memory C# classes that render the final HTML. Razor is fast (views are compiled, not interpreted), type-safe, and integrates with C# 12 features.

5. **A dependency injection container.** You write your classes as if their dependencies were handed to them — and the framework hands them. This makes your code testable, modular, and easy to refactor.

4. **An authentication and authorization system.** **ASP.NET Core Identity** is a complete user-management subsystem — registration, login, password hashing, lockout, two-factor auth, external login (Google, Facebook, Microsoft Account), role-based and claim-based authorization. It is built in, free, configurable, and replaceable.

5. **Entity Framework Core**, the Microsoft-supported object-relational mapper. You write C# classes; EF Core creates the database schema, generates SQL for you, tracks changes, and saves them efficiently.

6. **Middleware pipeline.** You compose your application's HTTP pipeline as a series of small, focused components — each one looks at the request, does its job (logging, authentication, routing, error handling), and either short-circuits or passes the request to the next component. This is a fundamentally cleaner model than the old `global.asax` event hooks.

7. **Cross-platform runtime.** The same code that runs on your Windows laptop will run on a Mac, on a Linux container in Kubernetes, on an Azure App Service, on AWS Elastic Beanstalk, or on a Raspberry Pi.

8. **Industry-grade performance.** ASP.NET Core routinely places in the top tier of the TechEmpower benchmarks, ahead of Express, Django, Rails, and (depending on the test) ahead of Go and Java frameworks. Performance is not an accident — it was a primary design goal of the rewrite.

### Why should you learn ASP.NET Core MVC?

There are dozens of web frameworks. You could learn Django, Rails, Laravel, Express, NestJS, Phoenix, Spring Boot, or a dozen others. Why pick this one?

**For employment.** The .NET ecosystem is one of the largest in enterprise software. Banks, insurance companies, hospitals, governments, and the majority of the Fortune 500 have .NET codebases. There are jobs. The skills in this guide will map to a large slice of the "back-end developer" job market globally.

**For the architecture.** ASP.NET Core is opinionated enough to keep you out of trouble, but flexible enough to scale to very large applications. The middleware pipeline, the DI container, and the controller-and-views model compose cleanly into architectures like Clean Architecture, CQRS, and event-driven systems. Learning MVC the right way teaches you patterns you will reuse in every other framework.

**For the tooling.** Visual Studio is the most powerful IDE in the .NET world, but Visual Studio Code with the C# Dev Kit extension is excellent on Mac and Linux. The `dotnet` CLI is scriptable, fast, and works in CI pipelines. NuGet has 400,000+ packages. The tooling is mature.

**For the language.** C# is one of the most pleasant mainstream programming languages. It has evolved from a Java clone in 2002 into a language with records, pattern matching, source generators, nullable reference types, and async streams. Learning C# through MVC is a great way to learn a modern, well-designed language.

**For the long-term.** Microsoft has committed to a yearly major release of .NET, with LTS releases every two years. The LTS releases are supported for three years. The framework is not going anywhere. Your skills will not be obsolete in three years.

### Real-world apps built on ASP.NET MVC

To make this concrete, here are some well-known systems that run on ASP.NET MVC, either as ASP.NET MVC 5 or as ASP.NET Core MVC:

- **Stack Overflow** — the entire Q&A site, including the tag engine, is ASP.NET MVC. The Stack Exchange network runs on a customized fork of the same codebase.
- **Microsoft's own websites** — docs.microsoft.com, azure.com, and large parts of office.com — are ASP.NET Core.
- **Visual Studio Marketplace** — Microsoft's extension store.
- **Orchard CMS** and **Umbraco** — two of the most popular .NET open-source content management systems, both built on MVC.
- **nopCommerce** — a popular open-source e-commerce platform.
- Many banks, insurance providers, and government portals that you use regularly run on ASP.NET MVC and ASP.NET Core MVC under the hood. It is one of the dominant back-end technologies in enterprise IT.

### What you will be able to build by the end of this guide

You will be able to take a blank project, design a domain model, build controllers and views, wire up a database with EF Core, add user authentication and authorization, validate input on both client and server, expose a REST API alongside the HTML pages, write unit and integration tests, containerize the app, and deploy it to a Linux server, an Azure App Service, or any cloud that runs containers.

You will also understand **why** each piece exists and **when** to deviate from the default conventions. That last part — understanding the *why* — is what separates someone who has followed a tutorial from someone who can architect a system.

### Summary of Chapter 1

- **ASP.NET** is Microsoft's server-side web framework, originally shipped in 2002.
- **Web Forms** was the original UI model, productive but hid HTML and HTTP from the developer.
- **ASP.NET MVC**, released in 2009, gave developers control over HTML, URLs, and the request lifecycle.
- **ASP.NET Core MVC**, the modern cross-platform rewrite, shipped in 2016 and continues to evolve.
- This guide targets **ASP.NET Core 8.0**, the current LTS release.
- Learning MVC gives you employment options, a clean architecture to learn, mature tooling, the modern C# language, and a long-term future.

In the next chapter, we step back from the framework and study the **MVC pattern itself** — where it came from, what it actually is, and why it maps so cleanly to HTTP. We will not write any code in Chapter 2 — the goal is to give your brain a clear mental model before we put a single line of code in front of it.

---

## Part I · Chapter 2 — The MVC Pattern: History, Theory, and Architecture

### What you will learn in this chapter
You will learn the **history** of the Model-View-Controller pattern, the **three components** in depth, how they communicate, why this pattern maps so cleanly onto the HTTP request/response cycle, and the **benefits and trade-offs** of building applications this way. We will not write any code in this chapter. The goal is to give you a mental model that will make every line of code in later chapters feel obvious.

### A short history of MVC

The **Model-View-Controller** pattern is much older than the web. It was invented in **1979** by a Norwegian computer scientist named **Trygve Reenskaug**, while he was working at Xerox PARC on the **Smalltalk-80** system. Reenskaug was trying to figure out how to structure graphical desktop applications — the kind with windows, menus, and buttons — so that the data model, the screen presentation, and the user input handling could each evolve independently. His original note, titled *"Models-Views-Controllers"* (December 1979), is still on his personal website.

In that original formulation:

- **Model** was "the knowledge of the application" — the data and the operations on it.
- **View** was "the visual representation of the model" — what the user saw.
- **Controller** was "the user input mechanism" — what translated keyboard and mouse events into actions on the model.

The pattern sat in the Smalltalk world for a long time. Then in the late 1990s and early 2000s, web developers noticed something: the request/response cycle of HTTP maps beautifully onto the MVC triad. A request comes in (input, like a controller event), the application does some work (touches the model), and the application returns HTML (a view). This insight spread through the Java community (Struts, Spring MVC), the Python community (Django, Pylons), the Ruby community (Rails), and eventually reached .NET in 2009 with ASP.NET MVC 1.0.

### The three components, in depth

#### The Model

The **Model** is the part of your application that knows about *what the application is*, not about *how it is shown*. In a to-do app, the Model is everything about tasks, categories, due dates, priorities — the rules that say a task can be marked complete, that a high-priority task must have a due date, that a category has a name and a color. The Model knows about tasks; it does not know about HTML, JSON, browsers, or HTTP.

In ASP.NET Core MVC, the Model is mostly expressed as **plain C# classes** (called **POCOs** — Plain Old CLR Objects) plus the business rules that operate on them. Sometimes those rules live inside the classes themselves, sometimes in separate services, sometimes in the database via constraints and triggers. The shape of the model is up to you; what matters is that the model is independent of the presentation.

A model class can be as simple as:

```csharp
public class TodoItem
{
    public int Id { get; set; }
    public string Title { get; set; } = string.Empty;
    public bool IsCompleted { get; set; }
}
```

We will explain every word of this in Chapter 4. For now, the point is: this class describes a *thing in the domain* (a to-do item). It does not describe how the to-do item appears on a web page. It does not import anything related to ASP.NET. It is a pure domain object.

A model can also be a **view model** — a class designed specifically to carry data between a controller and a view. We will see view models in Chapter 11. For now, treat "model" as "the C# classes that describe the domain."

#### The View

The **View** is the part of your application that turns data into something the user can see. In a web app, that "something" is HTML. The view takes data handed to it by the controller and renders it as HTML. It does *not* fetch its own data, *not* execute business logic, and *not* decide what to do next based on user input. Those are the controller's job.

In ASP.NET Core MVC, views are `.cshtml` files written in the **Razor** syntax — a mix of HTML and C# that compiles into a class that produces HTML when called. A trivial view:

```cshtml
@model TodoItem

<h1>@Model.Title</h1>
@if (Model.IsCompleted)
{
    <p>This task is done.</p>
}
else
{
    <p>This task is still pending.</p>
}
```

We will explain every symbol here in Chapter 9. The point is: this view *only* cares about rendering. It is given a `TodoItem` and it produces HTML. It does not query the database, it does not call any service, it does not know about HTTP requests.

#### The Controller

The **Controller** is the orchestrator. When a request arrives, the controller decides what to do: which model classes to talk to, what business operations to perform, and which view to render. The controller is the *verb* of the application — it receives the user's intent ("create a new task", "show me task 5", "mark task 7 as complete") and dispatches it.

In ASP.NET Core MVC, a controller is a class that inherits from `Microsoft.AspNetCore.Mvc.Controller` and contains **action methods**. Each action method handles one URL pattern. A controller for to-do items looks like:

```csharp
public class TodoController : Controller
{
    public IActionResult Index()
    {
        var items = new List<TodoItem>
        {
            new() { Id = 1, Title = "Buy milk", IsCompleted = false },
            new() { Id = 2, Title = "Walk dog",  IsCompleted = true  }
        };
        return View(items);
    }
}
```

We will go through this line by line in Chapter 7. The point for now: this controller is a class. It has a method called `Index`. The method builds some data (in real apps, by calling services or repositories, not by hard-coding), and returns a view. The framework takes the data and the view, renders the HTML, and ships it to the browser.

### How the three components communicate

Here is the canonical request flow in an MVC web application, from browser to browser:

```
1.  User types https://yourapp.com/todo/index in the browser.
2.  Browser sends an HTTP GET request to that URL.
3.  The web server (Kestrel) receives the request.
4.  The middleware pipeline runs (logging, authentication, routing).
5.  The routing engine inspects the URL and decides:
       controller = "Todo", action = "Index".
6.  The framework instantiates TodoController (fresh, per request).
7.  The framework calls the Index() method.
8.  Index() asks a service or repository for the data:
       var items = _todoService.GetAll();
9.  The service talks to the database via EF Core.
10. The database returns rows; EF Core materializes them as objects.
11. Index() passes the data to a view:
       return View(items);
12. The view engine finds /Views/Todo/Index.cshtml.
13. The view engine compiles and executes the view, passing `items`.
14. The view produces HTML.
15. The framework wraps the HTML in an HTTP response.
16. Kestrel sends the response back to the browser.
17. The browser renders the HTML.
```

This is the entire MVC request lifecycle. Every chapter after this one zooms in on one part of this flow. Controllers (Chapter 7) are steps 6–8 and 11. Routing (Chapter 8) is step 5. Views (Chapter 9) are steps 12–14. EF Core (Chapters 13–16) is steps 9–10. Middleware (Chapter 6) is step 4. Authentication (Chapter 19) is part of step 4. Filters (Chapter 21) wrap steps 6–11. Async (Chapter 22) is the threading model of steps 6–14.

When you understand this diagram, you understand ASP.NET Core MVC at a structural level. The rest of this guide fills in each box.

### The diagram, rendered as ASCII

```
 ┌──────────┐  HTTP request  ┌──────────────┐  route      ┌────────────┐
 │ Browser  │ ─────────────▶ │ Kestrel +    │ ──────────▶ │  Routing   │
 │          │                 │ Middleware   │             │  Engine    │
 └──────────┘                 └──────────────┘             └────────────┘
       ▲                                                           │
       │                                                           ▼
       │ HTTP response                                    ┌──────────────┐
       │                                                   │  Controller  │
       │                                                   │  (action)    │
       │                                                   └──────────────┘
       │                                                           │
       │                                                           ▼
       │                                            ┌──────────────────────────┐
       │                                            │ Model layer (services,  │
       │                                            │ repositories, EF Core)   │
       │                                            └──────────────────────────┘
       │                                                           │
       │                                                           ▼
       │     ┌──────────────┐   model data   ┌──────────────┐
       └────│  View Engine │ ◀───────────── │   View       │
             │  (Razor)     │                │  (.cshtml)   │
             └──────────────┘                └──────────────┘
```

Read this diagram a few times. Trace one request through it. When you can read this diagram without thinking, you have the model in your head.

### The benefits of MVC

Why bother with the separation at all? Why not just write a single file that does everything, like classic PHP or classic ASP?

**Testability.** Because the model is plain C# code, you can test it without a web server, a database, or a browser. Because controllers are plain C# classes, you can unit-test them by instantiating them and calling their methods directly — no HTTP needed. Views are harder to unit test, but you rarely need to; you test that a controller returns the right data for a view, and you visually inspect the rendered HTML.

**Parallel work.** A designer can edit `.cshtml` files and CSS without touching C#. A back-end developer can add a new controller action without touching HTML. A database engineer can change the schema without touching either. They work in different files, with different mental models, and they merge cleanly in source control.

**Control over HTML.** Unlike Web Forms, MVC does not generate weird `id` attributes or hide view-state in the page. The HTML you write in the view is the HTML the browser receives. You can validate it, style it, script it, and ship it.

**Clean URLs.** MVC's default routing produces `/todo/details/5` instead of `/todo.aspx?id=5` or `/index.php?page=todo&action=details&id=5`. Clean URLs matter for SEO, for sharing, and for user trust.

**Extensibility.** Every step in the request pipeline can be replaced. Don't like the default view engine? Write your own. Don't like the default JSON serializer? Replace it. Want to add a custom caching layer? There's a hook for that. The framework is built as a set of composable pieces, not a monolith.

**Separation of concerns.** This is not just a buzzword. When your business logic lives in one place, your data access in another, your HTML in a third, and your request handling in a fourth, you can change any one of them with a predictable blast radius. A change to the way you query the database does not touch HTML. A change to HTML does not touch business rules. This pays off enormously as an application grows.

### The trade-offs

No pattern is free. MVC has costs:

**More files.** A single Web Forms page could be one `.aspx` file. The same functionality in MVC is a controller method, a view file, possibly a view model, and a model class. This is more files to keep track of. It is also why the separation works — each file has one job.

**Steeper learning curve.** To build your first useful MVC page, you need to understand routing, controllers, action methods, view discovery, Razor syntax, and model binding. The first day is harder. The thousandth day is much easier.

**Not the only option.** **Razor Pages**, introduced in ASP.NET Core 2.0, is a page-centric alternative to MVC that combines the controller action and the view into a single "page" unit. For some apps (especially content sites with a few forms per page), Razor Pages is simpler. **Blazor** lets you write interactive UI in C# instead of JavaScript. **Minimal APIs** let you build HTTP APIs without controllers at all. We will not cover these in depth; this guide is about MVC, but you should know they exist.

### When MVC is the wrong choice

- A small marketing site with three static pages and a contact form. Use Razor Pages or a static site generator.
- A highly interactive single-page app where the server is just a JSON API. Use Minimal APIs or controllers-as-API, plus a JS framework on the front.
- A real-time application where the UI is driven by server push (live chat, multiplayer games). Use SignalR or Blazor Server.

For everything else — content sites, admin dashboards, CRUD apps, e-commerce back ends, SaaS portals, internal tools — MVC is a strong default and a great foundation.

### Summary of Chapter 2

- MVC was invented by Trygve Reenskaug in 1979 for desktop GUIs, and was adopted by web frameworks because the HTTP request/response cycle maps naturally onto it.
- The **Model** is the domain; the **View** is the rendering; the **Controller** is the orchestration.
- The request flow is: browser → Kestrel → middleware → routing → controller → model → view → response.
- Benefits: testability, parallel work, HTML control, clean URLs, extensibility, separation of concerns.
- Costs: more files, steeper curve, and it is not always the right choice for every kind of app.

In the next chapter, we get practical: we install the tools you need, verify they work, and prepare your machine for writing ASP.NET Core MVC code.

---

## Part I · Chapter 3 — Setting Up Your Development Environment

### What you will learn in this chapter
You will install the .NET 8 SDK, install a code editor (Visual Studio 2022 on Windows, or Visual Studio Code with the C# Dev Kit extension on Mac/Linux/Windows), and verify that everything works by running `dotnet --version` and creating a tiny "hello world" console app. By the end of the chapter you will have a fully functional .NET development environment, and we will be ready to write ASP.NET Core MVC code in Chapter 5.

### Why we set up the environment carefully

The single most common reason new .NET learners give up is a broken environment — the SDK is not on `PATH`, the IDE does not see the SDK, the SDK is a slightly older version, the wrong runtime is installed. We will go slowly here, because every later chapter depends on this one being right.

### 3.1 Installing the .NET 8 SDK

The **.NET SDK** (Software Development Kit) is the package that contains everything you need to build, run, and publish .NET apps: the compiler (`csc`/`Roslyn`), the runtime (`CoreCLR`), the base libraries, the `dotnet` command, and the project templates.

#### On Windows

1. Open a browser and go to **https://dotnet.microsoft.com/download/dotnet/8.0**.
2. Under **.NET SDK 8.0.x**, click **Windows x64** (or **Windows ARM64** if you are on an ARM device like the Surface Pro X).
3. Run the downloaded installer. Accept the license, click Install, wait. The installer adds the SDK to your `PATH` automatically.
4. **Open a new terminal** — this is important. Terminals that were already open before the install will not see the new `PATH` entry.
5. Verify:

```powershell
dotnet --version
```

You should see something like `8.0.404` (the patch version changes over time). If you see `command not found` or `not recognized`, close every terminal window, reopen one, and try again. If it still fails, you need to add `C:\Program Files\dotnet\` to your `PATH` manually (search Windows for "Environment Variables" and edit the `Path` variable for your user).

Also list the installed SDKs:

```powershell
dotnet --list-sdks
```

You should see at least one entry starting with `8.0.`.

#### On macOS

The cleanest way to install .NET on macOS is via **Homebrew**, the macOS package manager.

1. If you do not have Homebrew, install it by following the instructions at **https://brew.sh**. The install is one line in Terminal.
2. Install the .NET 8 SDK:

```bash
brew install --cask dotnet-sdk
```

3. Verify:

```bash
dotnet --version
dotnet --list-sdks
```

If you prefer not to use Homebrew, you can download the installer from **https://dotnet.microsoft.com/download/dotnet/8.0** under **.NET SDK 8.0.x → macOS x64** (or **macOS ARM64** on Apple Silicon).

#### On Linux

The install procedure varies by distribution. The authoritative instructions for every distribution are at **https://learn.microsoft.com/dotnet/core/install/linux**. The short version for the most common distributions:

**Ubuntu 22.04 / 24.04** (and derivatives):

```bash
# Add the Microsoft package repository
wget https://packages.microsoft.com/config/ubuntu/$(lsb_release -rs)/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
rm packages-microsoft-prod.deb

# Install the SDK
sudo apt-get update
sudo apt-get install -y dotnet-sdk-8.0
```

**Fedora**:

```bash
sudo dnf install dotnet-sdk-8.0
```

**Arch / Manjaro** (community package):

```bash
sudo pacman -S dotnet-sdk
```

After installation, verify:

```bash
dotnet --version
dotnet --list-sdks
```

#### What is the difference between the SDK and the Runtime?

The **SDK** is what you need to *build* apps — it includes the compiler. The **Runtime** is what you need to *run* apps on a machine that does not develop them (a production server, for example). The SDK includes the runtime, so as a developer you only need the SDK. On a production server, you typically install just the runtime (`dotnet-runtime-8.0`), which is much smaller.

You can verify both with:

```bash
dotnet --list-runtimes
```

You should see at least `Microsoft.NETCore.App 8.0.x` and `Microsoft.AspNetCore.App 8.0.x`. The first is the base runtime; the second is the ASP.NET Core runtime on top of it.

### 3.2 Installing an editor

You have two main choices. Both are free.

#### Option A: Visual Studio 2022 (Windows only, the heavy IDE)

Visual Studio is the most powerful .NET IDE, with a visual designer, excellent debugger, integrated SQL Server Explorer, built-in performance profiler, and rich refactoring tools. The **Community** edition is free for individuals, open-source projects, and small teams.

1. Go to **https://visualstudio.microsoft.com/vs/community/** and download the installer.
2. Run the installer. The "Visual Studio Installer" appears.
3. In the **Workloads** tab, check **ASP.NET and web development**. This workload includes the .NET SDK, Razor tooling, web project templates, and the IIS Express local web server.
4. Optionally also check **.NET desktop development** if you want to build desktop apps later, and **Data storage and processing** if you want the SQL Server Object Explorer.
5. Click **Install**. The download is several GB. Make coffee.
6. After install, launch Visual Studio, sign in with a Microsoft account (optional but recommended — it syncs settings across machines), and pick a theme.

#### Option B: Visual Studio Code (Windows, Mac, Linux, lightweight)

Visual Studio Code is a free, lightweight, cross-platform code editor with first-class C# support through the **C# Dev Kit** extension. This is the most popular choice for Mac and Linux users, and a perfectly valid choice on Windows too.

1. Download VS Code from **https://code.visualstudio.com/** and install it.
2. Open VS Code. Open the Extensions panel (the icon on the left sidebar that looks like four squares).
3. Search for **C# Dev Kit** (published by Microsoft). Click **Install**.
4. The C# Dev Kit installs several sub-extensions: **C#** (the language server, OmniSharp or Roslyn-based), **C# Base Language Server**, and others. Accept any prompts.
5. Restart VS Code if prompted.

The C# Dev Kit gives you: IntelliSense, go-to-definition, find-all-references, refactoring (rename, extract method), in-editor debugging (set breakpoints, step, watch), and the **Solution Explorer** view in the sidebar — the part of VS Code that shows your projects and files like Visual Studio does.

### 3.3 Optional: a database

For most of this guide we will use **SQLite** as the database, because it requires zero setup — it is a single file on disk. ASP.NET Core and EF Core support SQLite out of the box; the SQLite engine is bundled inside the `Microsoft.Data.Sqlite` package, which EF Core uses automatically.

If you would rather use **SQL Server** (Microsoft's flagship database):

- **Windows**: install **SQL Server 2022 Express** (free) from **https://www.microsoft.com/sql-server/sql-server-downloads**. Choose "Express" (the free, lightweight edition). Also install **SQL Server Management Studio (SSMS)** for a graphical database browser.
- **macOS / Linux**: use the **SQL Server in Docker** image (`mcr.microsoft.com/mssql/server:2022-latest`). You need Docker Desktop installed. We will cover this in Chapter 14.

For now, you do not need to do anything — we will install database tooling when we get to EF Core in Chapter 13.

### 3.4 Optional: Git

You will want source control. Most developers already have it. Check:

```bash
git --version
```

If it is not installed, get it from **https://git-scm.com/downloads**. This guide does not teach Git — that is a topic for a separate book — but every code change we make in later chapters should live in a Git commit so you can roll back if you break something.

### 3.5 Verifying the environment end-to-end

Let us build a tiny console app to prove your SDK and editor work together.

Open a terminal, navigate to a folder where you want to keep your code (for example `~/Code` or `C:\Code`), and run:

```bash
dotnet new console -o HelloDotNet
cd HelloDotNet
dotnet run
```

You should see `Hello, World!` printed in the terminal.

What just happened, line by line:

- `dotnet new console -o HelloDotNet` — `dotnet new` is the template engine. `console` is the template name (a console app, no web). `-o HelloDotNet` says "create the project in a new folder called `HelloDotNet`". The template generates two files: `HelloDotNet.csproj` (the project file, XML) and `Program.cs` (the entry point, C#).
- `cd HelloDotNet` — move into the new folder.
- `dotnet run` — this is shorthand for "build the project and execute the resulting binary". It does the equivalent of `dotnet build` followed by `dotnet HelloDotNet.dll`. The output of the default console template is `Hello, World!`.

Now open `Program.cs` in your editor. With the default template in .NET 8, it should look like this:

```csharp
// See https://aka.ms/new-console-template for more information
Console.WriteLine("Hello, World!");
```

This is **top-level statements** — a C# 9 feature. The compiler wraps this in a generated `Program.Main` method for you. In older C# (pre-9.0) the template generated the full ceremony:

```csharp
using System;

namespace HelloDotNet
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello, World!");
        }
    }
}
```

Both forms compile to the same IL. The new top-level form is just less typing. We will see this pattern again in Chapter 6 — the `Program.cs` of an ASP.NET Core app is also top-level statements.

Change the line to:

```csharp
Console.WriteLine("Hello from my first .NET app!");
```

Save the file. Run `dotnet run` again. You should see your new message.

If you saw your new message, your environment is fully working. You have a compiler, a runtime, an editor, and the ability to make changes and see them. We are ready for real work.

### 3.6 Common mistakes

- **"dotnet is not recognized"** on Windows: the SDK installer did not update your `PATH`. Close all terminals, reopen one. If still broken, add `C:\Program Files\dotnet\` to your user `PATH` manually.
- **"dotnet --version shows an older version"**: you have an older SDK on the system and it is taking precedence. Run `dotnet --list-sdks` to see all installed SDKs. The SDK chosen depends on a `global.json` file if one exists in the folder tree — if you see a `global.json` specifying an older version, delete it.
- **VS Code IntelliSense does not work**: open the Command Palette (Ctrl+Shift+P / Cmd+Shift+P) and run `.NET: Restart Language Server`. If it still does not work, run `dotnet restore` in the project folder to make sure the NuGet packages are restored.
- **Visual Studio does not see the .NET 8 SDK**: restart Visual Studio after installing the SDK. If still missing, run the Visual Studio Installer and click "Modify" — make sure the latest SDK is checked under "Individual components".

### Summary of Chapter 3

- The .NET 8 SDK is the one thing you must install; it is available from Microsoft's website for Windows, macOS, and most Linux distributions.
- Your editor is either Visual Studio 2022 (Windows, full IDE) or Visual Studio Code with the C# Dev Kit (any OS, lightweight).
- We will use SQLite in this guide — no setup needed. SQL Server is optional.
- Verify the environment with `dotnet new console -o HelloDotNet && cd HelloDotNet && dotnet run`. If `Hello, World!` appears, you are ready.
- Common install issues are PATH-related and easy to fix.

In the next chapter, we take a 30-minute crash course in C#. You do not need to be a C# expert to start learning MVC, but you do need a working vocabulary — classes, methods, properties, generics, async, LINQ — so that the code in later chapters does not throw unfamiliar syntax at you. If you already know C# reasonably well, you can skim Chapter 4 and move to Chapter 5.

---

## Part I · Chapter 4 — C# Crash Course for MVC Beginners

### What you will learn in this chapter
A working C# vocabulary: types, variables, classes, properties, methods, constructors, access modifiers, inheritance, interfaces, generics, collections, LINQ, async/await, nullable reference types, and records. We will not go deep on any one topic — this is the minimum you need to read every line of code in later chapters without getting stuck on syntax. By the end, you will be able to read and write small C# programs confidently.

This chapter is long because C# is a large language. If you already know Java, TypeScript, or Kotlin, much of this will be familiar — skim the parts you recognize. If you are coming from Python or JavaScript, pay close attention to the type system parts: C# is statically typed, and the compiler is your friend but also your gatekeeper.

### 4.1 Types and variables

C# is **statically typed**: every variable has a type known at compile time. The compiler will refuse to compile code that mixes types in ways that lose information.

```csharp
int age = 30;            // int: a 32-bit signed integer
long big = 9_000_000_000L; // long: a 64-bit signed integer
double pi = 3.14159;     // double: a 64-bit floating point
decimal price = 19.99m;  // decimal: a 128-bit high-precision decimal (use for money)
bool isDone = true;      // bool: true or false
char grade = 'A';        // char: a single Unicode character
string name = "Sara";   // string: an immutable sequence of chars
```

Line by line:

- `int age = 30;` — declares a variable named `age` of type `int` (32-bit integer) and assigns it the value `30`. The semicolon ends the statement.
- `long big = 9_000_000_000L;` — the `L` suffix tells the compiler "this literal is a `long`, not an `int`". The underscores in `9_000_000_000` are digit separators — they make large numbers easier to read and are ignored by the compiler.
- `double pi = 3.14159;` — a 64-bit IEEE 754 floating point. Use for scientific calculations where small rounding errors are acceptable.
- `decimal price = 19.99m;` — the `m` suffix means `decimal`. `decimal` is a 128-bit type with much greater precision and no floating-point rounding artifacts. **Always use `decimal` for money**, never `double`.
- `bool isDone = true;` — booleans can only be `true` or `false`.
- `char grade = 'A';` — single quotes for `char`, double quotes for `string`.
- `string name = "Sara";` — `string` (lowercase) is a C# keyword alias for `System.String`. They are the same type.

#### `var` — let the compiler infer the type

```csharp
var name = "Sara";   // compiler infers: string
var count = 42;      // compiler infers: int
var items = new List<int>(); // compiler infers: List<int>
```

`var` is a convenience, not a dynamic type. The variable is still statically typed — the compiler just figures out the type for you from the right-hand side. Use `var` when the type is obvious (`var name = "Sara";`) and use the explicit type when it is not (`List<int> items = GetItems();` makes the type clear to the reader).

### 4.2 Classes, properties, methods

A **class** is a blueprint for objects. An **object** is an instance of a class.

```csharp
public class Person
{
    public string Name { get; set; }
    public int Age { get; set; }

    public Person(string name, int age)
    {
        Name = name;
        Age = age;
    }

    public string Describe() => $"{Name} is {Age} years old.";
}
```

Line by line:

- `public class Person` — `public` means "any other code can see this class". `class Person` declares the class.
- `public string Name { get; set; }` — this is an **auto-property**. Behind the scenes, the compiler generates a private backing field and `get`/`set` methods. Reading `person.Name` calls the getter; assigning `person.Name = "Bob"` calls the setter.
- `public Person(string name, int age)` — this is a **constructor**. It runs when you write `new Person("Sara", 30)`. The parameters (`name`, `age`) are passed in by the caller and assigned to the properties.
- `public string Describe() => $"{Name} is {Age} years old.";` — this is a **method** using an **expression-bodied member** (the `=>` syntax). It is shorthand for:

```csharp
public string Describe()
{
    return $"{Name} is {Age} years old.";
}
```

The `$"..."` is an **interpolated string**. The `{Name}` and `{Age}` placeholders are replaced with the values of the corresponding properties.

#### Creating objects

```csharp
var p = new Person("Sara", 30);
Console.WriteLine(p.Describe()); // Sara is 30 years old.
```

`new Person("Sara", 30)` allocates a new `Person` object on the heap and calls the constructor. The reference to that object is stored in `p`.

#### `record` — a class designed for data

C# 9 introduced **records**, which are classes auto-generated to be value-equal and immutable by default. Perfect for DTOs and view models:

```csharp
public record Person(string Name, int Age);

var a = new Person("Sara", 30);
var b = new Person("Sara", 30);
Console.WriteLine(a == b); // True — records compare by value
```

With a `record`, two instances with the same data are considered equal. With a regular `class`, they are only equal if they are the same object in memory. We will use records for view models in Chapter 11.

### 4.3 Access modifiers

- `public` — anyone can see it.
- `private` — only this class can see it. Default for members.
- `protected` — this class and any class that inherits from it.
- `internal` — any code in the same assembly (project) can see it. Default for top-level types.
- `protected internal` — this assembly OR derived classes.
- `private protected` — this assembly AND derived classes (rare).

In MVC, controllers are `public` (the framework needs to find them). Action methods are `public` (the framework needs to call them). Helper methods on a controller should be `private`. Models are usually `public`. View models are `public`.

### 4.4 Inheritance and interfaces

```csharp
public class Animal
{
    public string Name { get; set; }
    public virtual string Speak() => "...";
}

public class Dog : Animal
{
    public override string Speak() => "Woof!";
}

public interface IThing
{
    void DoIt();
}

public class Thing : IThing
{
    public void DoIt() { /* ... */ }
}
```

- `class Dog : Animal` — `Dog` inherits from `Animal`. `Dog` *is an* `Animal`.
- `virtual` — a method that derived classes are allowed to override.
- `override` — actually overriding a virtual method in a derived class.
- `interface IThing` — a contract: any class implementing `IThing` must provide a `DoIt` method.
- `class Thing : IThing` — `Thing` promises to implement `IThing`.

In ASP.NET Core MVC, controllers inherit from `Microsoft.AspNetCore.Mvc.Controller`, which itself inherits from `ControllerBase`. The `Controller` base class provides helper methods like `View()`, `Redirect()`, `Json()`, and gives you access to `HttpContext`, `User`, `Request`, `Response`.

### 4.5 Generics

**Generics** let you write code that works with any type, while keeping type safety.

```csharp
public class Stack<T>
{
    private List<T> _items = new();
    public void Push(T item) => _items.Add(item);
    public T Pop() { var i = _items[^1]; _items.RemoveAt(_items.Count - 1); return i; }
}

var s = new Stack<int>();
s.Push(1);
s.Push(2);
int x = s.Pop(); // x is 2 — type-safe, no cast needed
```

`<T>` is a **type parameter**. When you write `new Stack<int>()`, `T` becomes `int`. The compiler enforces that you can only push `int`s onto this stack and `Pop` returns an `int`.

You will see generics everywhere in ASP.NET Core:

- `List<T>`, `Dictionary<TKey, TValue>`, `Task<T>` — the base class library.
- `IRepository<T>` — generic repositories (Chapter 16).
- `ActionResult<T>` — typed controller return values (Chapter 7).
- `ILogger<T>` — typed logger categories (Chapter 26).
- `DbContext` sets: `DbSet<TodoItem>` (Chapter 13).

### 4.6 Collections

```csharp
// Arrays — fixed size
int[] nums = { 1, 2, 3 };

// List<T> — growable array
var list = new List<int> { 1, 2, 3 };
list.Add(4);
list.Remove(2);

// Dictionary<TKey, TValue> — key/value
var map = new Dictionary<string, int>();
map["one"] = 1;
int one = map["one"];

// HashSet<T> — unique items
var set = new HashSet<int> { 1, 2, 3 };
set.Add(1); // no-op, already present
```

`List<T>` is what you will use 90% of the time. `Dictionary<K,V>` for lookups by key. `HashSet<T>` when you need fast uniqueness checks.

### 4.7 LINQ

**LINQ** (Language Integrated Query) is C#'s query language for collections. It is one of the best features in C# and you will use it constantly in MVC, especially in controller methods that query the database.

```csharp
var people = new List<Person>
{
    new("Sara", 30),
    new("Bob",  17),
    new("Joe",  25),
    new("Amy",  16),
};

// Where: filter
var adults = people.Where(p => p.Age >= 18);

// Select: project
var names = people.Select(p => p.Name);

// OrderBy: sort
var byAge = people.OrderBy(p => p.Age);

// First / FirstOrDefault: get one
var first = people.First();         // throws if empty
var firstOr = people.FirstOrDefault(); // returns default (null) if empty

// Any / All: boolean checks
bool anyAdults = people.Any(p => p.Age >= 18);
bool allAdults = people.All(p => p.Age >= 18);

// Count: count
int adultsCount = people.Count(p => p.Age >= 18);

// GroupBy: group
var byAgeGroup = people.GroupBy(p => p.Age >= 18 ? "Adult" : "Minor");
```

The `p => p.Age >= 18` syntax is a **lambda expression**: "given a `p`, return `p.Age >= 18`". Lambdas are tiny inline functions.

When you use LINQ on an EF Core `DbSet<T>`, the LINQ expression is translated into SQL and executed in the database. The same code, against an in-memory `List<T>`, executes locally. This is one of the magical things about EF Core — your data access code looks the same whether the data is in memory or in a database.

### 4.8 Async / await

Modern web apps do a lot of I/O: database queries, HTTP calls, file reads. If a request blocks the calling thread while waiting for the database, the thread sits idle — and threads are expensive. **Async/await** lets the thread do other work while waiting for I/O, dramatically increasing how many requests your server can handle.

```csharp
public async Task<string> FetchAsync()
{
    using var client = new HttpClient();
    string body = await client.GetStringAsync("https://example.com");
    return body;
}
```

- `async` — marks the method as async. Required to use `await` inside it.
- `Task<string>` — the return type. A `Task` represents "work that will produce a value later". `Task<string>` is "a task that will produce a string". The caller can `await` it too, or use `.Result` (avoid `.Result` — it can deadlock).
- `await` — suspends the method until the task finishes, then resumes with the result. The thread is free to do other work during the wait.
- `using var client = new HttpClient();` — `using` ensures `client.Dispose()` is called when the variable goes out of scope. This pattern (the `using` declaration, no braces) was added in C# 8.

In ASP.NET Core MVC, controller actions are very commonly async:

```csharp
public async Task<IActionResult> Index()
{
    var items = await _db.TodoItems.ToListAsync();
    return View(items);
}
```

We will dive deeper in Chapter 22. The key takeaway for now: **whenever you call a database or a remote API from a controller, make the action `async Task<IActionResult>` and `await` the call.**

### 4.9 Nullable reference types

Starting in C# 8 (and enabled by default in .NET 6+ projects), **nullable reference types** are a compile-time feature that warns you when a `string` (or any reference type) might be `null` and you have not handled it.

```csharp
string name = "Sara";   // non-nullable reference: compiler assumes never null
string? maybeName = null; // nullable reference: explicitly allowed to be null
```

The `?` after the type means "this can be null". Without it, the compiler will warn you if you assign `null` or if you do not initialize the variable.

This feature catches a huge class of bugs (`NullReferenceException`) before runtime. In this guide we will write all reference-type properties as nullable when they are allowed to be null:

```csharp
public string Title { get; set; } = string.Empty; // non-nullable, but starts empty
public string? Description { get; set; }            // nullable
```

### 4.10 Pattern matching and switch expressions

C# has powerful pattern matching, especially in switch expressions:

```csharp
string DescribeAge(int age) => age switch
{
    < 0    => "Invalid",
    < 13   => "Child",
    < 20   => "Teenager",
    < 65   => "Adult",
    >= 65  => "Senior",
};
```

This is much cleaner than a chain of `if/else if`. We will use switch expressions occasionally in later chapters.

### 4.11 Putting it together

Here is a tiny complete C# program that uses everything from this chapter. Read it through; if you understand every line, you are ready for MVC.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;

var people = new List<Person>
{
    new("Sara", 30),
    new("Bob",  17),
    new("Joe",  25),
};

var adults = people
    .Where(p => p.Age >= 18)
    .OrderBy(p => p.Name)
    .Select(p => p.Name);

foreach (var name in adults)
{
    Console.WriteLine(name);
}

public record Person(string Name, int Age);
```

Output:

```
Joe
Sara
```

What this does: creates a list of three people, filters to those 18 or older, sorts by name, projects to just the name, and prints each one.

### Summary of Chapter 4

- C# is statically typed; the compiler enforces type rules at build time.
- Classes are blueprints, objects are instances. Properties are auto-backed fields.
- `record` types are value-equal data classes, great for view models.
- Access modifiers control visibility; controllers and actions are `public`.
- Inheritance (`:`) and interfaces (`interface`) provide polymorphism.
- Generics (`<T>`) let you write reusable, type-safe code.
- `List<T>` and `Dictionary<K,V>` are the workhorse collections.
- LINQ is the query language for collections and EF Core.
- `async/await` lets your server handle many more requests without blocking threads.
- Nullable reference types (`string?`) help you avoid null-reference bugs.
- Pattern matching (`switch` expressions) makes branching code clean.

You will not be an expert in C# after one chapter. But you now have the vocabulary to read the MVC code in the next chapters, and you can fill in the gaps by re-reading this chapter as needed. In the next chapter, we finally create an ASP.NET Core MVC project and start building real things.

---

## Part I · Chapter 5 — Your First ASP.NET Core MVC Project

### What you will learn in this chapter
You will create your first ASP.NET Core MVC project using the `dotnet new mvc` template, run it, see it in the browser, and then walk through every file the template generates. By the end you will understand what each file in a default MVC project does, and we will be ready in Chapter 6 to dissect `Program.cs` line by line.

### 5.1 Creating the project

Open a terminal in your code folder (`~/Code` or `C:\Code` — wherever you keep your projects). Run:

```bash
dotnet new mvc -o TaskManager
cd TaskManager
```

What just happened:

- `dotnet new mvc` — uses the `mvc` template (an ASP.NET Core MVC project).
- `-o TaskManager` — creates the project in a new folder called `TaskManager`. The folder name also becomes the project name and the default namespace.
- `cd TaskManager` — move into the project folder.

The template generates this structure:

```
TaskManager/
├── Controllers/
│   └── HomeController.cs
├── Models/
│   ├── ErrorViewModel.cs
│   └── ErrorViewModel.cs
├── Views/
│   ├── Home/
│   │   ├── Index.cshtml
│   │   └── Privacy.cshtml
│   ├── Shared/
│   │   ├── Error.cshtml
│   │   ├── _Layout.cshtml
│   │   ├── _Layout.cshtml.css
│   │   ├── _ValidationScriptsPartial.cshtml
│   │   └── _ViewImports.cshtml
│   ├── _ViewStart.cshtml
│   └── appsettings.json
├── wwwroot/
│   ├── css/
│   │   └── site.css
│   ├── js/
│   │   └── site.js
│   ├── lib/                (Bootstrap, jQuery from LibMan)
│   └── favicon.ico
├── Properties/
│   └── launchSettings.json
├── Program.cs
├── appsettings.json
├── appsettings.Development.json
├── TaskManager.csproj
└── .gitignore
```

We will look at each of these files in detail shortly.

### 5.2 Running the project

```bash
dotnet run
```

You should see output similar to:

```
Building...
info: Microsoft.Hosting.Lifetime[14] Now listening on: http://localhost:5000
info: Microsoft.Hosting.Lifetime[14] Application started. Press Ctrl+C to shut down.
info: Microsoft.Hosting.Lifetime[0] Hosting environment: Development
```

Open a browser to **http://localhost:5000** (or whatever port the output says — it might be 5001, 5000, or 5171 depending on your version and OS).

You should see the default ASP.NET Core MVC welcome page — a Bootstrap-styled page with three nav links (Home, Privacy, and the docs link) and an "ASP.NET Core" header.

**Stop the server** with `Ctrl+C` in the terminal.

### 5.3 The `TaskManager.csproj` file

Open `TaskManager.csproj` in your editor. It looks like:

```xml
<Project Sdk="Microsoft.NET.Sdk.Web">

  <PropertyGroup>
    <TargetFramework>net8.0</TargetFramework>
    <Nullable>enable</Nullable>
    <ImplicitUsings>enable</ImplicitUsings>
  </PropertyGroup>

</Project>
```

Line by line:

- `<Project Sdk="Microsoft.NET.Sdk.Web">` — every .NET project is an MSBuild project. The `Sdk` attribute tells MSBuild which SDK to use. `Microsoft.NET.Sdk.Web` is the web SDK — it includes the right defaults for ASP.NET Core apps (as opposed to `Microsoft.NET.Sdk` for class libraries, or `Microsoft.NET.Sdk.Worker` for background services).
- `<TargetFramework>net8.0</TargetFramework>` — this project targets .NET 8.0. You cannot run it on .NET 7. The target framework is the "platform version" the project compiles against.
- `<Nullable>enable</Nullable>` — turns on nullable reference types for this project. We saw this in Chapter 4.
- `<ImplicitUsings>enable</ImplicitUsings>` — enables **implicit usings**, a C# 10 feature. The most common `using System;` style namespaces are imported automatically so you do not need to type them at the top of every file. The list includes `System`, `System.Collections.Generic`, `System.IO`, `System.Linq`, `System.Net.Http`, `System.Threading.Tasks`, plus a few ASP.NET-specific ones for web projects.

If you add NuGet packages later, they appear as `<PackageReference>` elements in this file. We will see that in Chapter 13 when we install EF Core.

### 5.4 The `Program.cs` file

Open `Program.cs`. In .NET 8, it looks like this (lightly reformatted for clarity):

```csharp
var builder = WebApplication.CreateBuilder(args);

// Add services to the container.
builder.Services.AddControllersWithViews();

var app = builder.Build();

// Configure the HTTP request pipeline.
if (!app.Environment.IsDevelopment())
{
    app.UseExceptionHandler("/Home/Error");
    // The default HSTS value is 30 days. You may want to change this for production scenarios, see https://aka.ms/aspnetcore-hsts.
    app.UseHsts();
}

app.UseHttpsRedirection();
app.UseStaticFiles();

app.UseRouting();

app.UseAuthorization();

app.MapControllerRoute(
    name: "default",
    pattern: "{controller=Home}/{action=Index}/{id?}");

app.Run();
```

This is the entire entry point of your application. **Twelve meaningful lines of code**, and they run an MVC web app. We will dissect every line of this in Chapter 6 — for now, here is the summary:

- `WebApplication.CreateBuilder(args)` — creates the configuration host that knows about command-line args, environment variables, and `appsettings.json`.
- `builder.Services.AddControllersWithViews()` — registers MVC services in the DI container: the controller factory, the view engine, the model binder, the tag helper system.
- `var app = builder.Build();` — produces the runnable `WebApplication`.
- `app.Use*()` calls add middleware to the request pipeline.
- `app.MapControllerRoute(...)` — registers the default route.
- `app.Run()` — starts the web server and blocks until shutdown.

### 5.5 The `appsettings.json` and `appsettings.Development.json` files

Open `appsettings.json`:

```json
{
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft.AspNetCore": "Warning"
    }
  },
  "AllowedHosts": "*"
}
```

- `Logging:LogLevel:Default: Information` — by default, log everything at "Information" level or higher (Warning, Error, Critical).
- `Microsoft.AspNetCore: Warning` — except for the ASP.NET Core infrastructure logs, which should be at Warning or higher. This keeps the console output focused on *your* logs, not the framework's internal chatter.
- `AllowedHosts: "*"` — accept requests regardless of the `Host` header.

Open `appsettings.Development.json`:

```json
{
  "DetailedErrors": true,
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft.AspNetCore": "Warning"
    }
  }
}
```

This file overrides `appsettings.json` when the environment is `Development`. The `DetailedErrors` flag turns on detailed exception pages — the famous "developer exception page" with the stack trace and the source code snippet. We will see it in Chapter 6.

The environment is set by the `ASPNETCORE_ENVIRONMENT` environment variable. The default is `Development` when you run locally with `dotnet run`, and `Production` everywhere else.

### 5.6 The `HomeController.cs` file

Open `Controllers/HomeController.cs`:

```csharp
using System.Diagnostics;
using Microsoft.AspNetCore.Mvc;
using TaskManager.Models;

namespace TaskManager.Controllers
{
    public class HomeController : Controller
    {
        private readonly ILogger<HomeController> _logger;

        public HomeController(ILogger<HomeController> logger)
        {
            _logger = logger;
        }

        public IActionResult Index()
        {
            return View();
        }

        public IActionResult Privacy()
        {
            return View();
        }

        [ResponseCache(Duration = 0, Location = ResponseCacheLocation.None, NoStore = true)]
        public IActionResult Error()
        {
            return View(new ErrorViewModel { RequestId = Activity.Current?.Id ?? HttpContext.TraceIdentifier });
        }
    }
}
```

Line by line:

- `using System.Diagnostics;` — needed for the `Activity` class used in the `Error` action.
- `using Microsoft.AspNetCore.Mvc;` — the namespace containing `Controller`, `IActionResult`, `[ResponseCache]`, etc.
- `using TaskManager.Models;` — the project's own `Models` namespace, where `ErrorViewModel` lives.
- `namespace TaskManager.Controllers` — puts this class in the `TaskManager.Controllers` namespace.
- `public class HomeController : Controller` — the controller class. Inheriting from `Controller` gives you access to `View()`, `Json()`, `Redirect()`, `HttpContext`, `User`, and many more helpers.
- `private readonly ILogger<HomeController> _logger;` — a logger, typed by the controller's own type. The framework injects one for you (Chapter 26).
- `public HomeController(ILogger<HomeController> logger)` — **constructor injection**: the DI container sees that `HomeController` needs an `ILogger<HomeController>` and gives it one when instantiating the controller. This is the dependency injection pattern, and it is everywhere in ASP.NET Core.
- `_logger = logger;` — store the dependency in a field.
- `public IActionResult Index()` — an action method. The route `/` and `/Home` and `/Home/Index` all reach this method.
- `return View();` — "render the default view for this action". The default view is at `Views/Home/Index.cshtml`.
- `public IActionResult Privacy()` — the action for the `/Home/Privacy` URL.
- `[ResponseCache(Duration = 0, Location = ResponseCacheLocation.None, NoStore = true)]` — disables all caching for this action. We do not want error responses to be cached.
- `public IActionResult Error()` — the action invoked when an unhandled exception happens (because `Program.cs` configured `UseExceptionHandler("/Home/Error")`).
- `return View(new ErrorViewModel { RequestId = Activity.Current?.Id ?? HttpContext.TraceIdentifier });` — passes a model to the view with the current request ID, so the error page can show it to the user (and they can quote it to support).

The pattern you should notice: **every public method on a controller is an action** that responds to a URL. The `[ResponseCache]` and `[NonAction]` attributes are the only things that change this default.

### 5.7 The `Index.cshtml` view

Open `Views/Home/Index.cshtml`:

```cshtml
@{
    ViewData["Title"] = "Home Page";
}

<div class="text-center">
    <h1 class="display-4">Welcome</h1>
    <p>Learn about <a href="https://learn.microsoft.com/aspnet/core">building Web apps with ASP.NET Core</a>.</p>
</div>
```

Line by line:

- `@{ ... }` — a Razor code block. Code inside runs server-side and does not produce output directly. Here, it sets `ViewData["Title"]` to "Home Page". The layout (Chapter 10) reads this and uses it as the `<title>` tag in the rendered HTML.
- `<div class="text-center">...</div>` — literal HTML. Razor passes it through unchanged.

Notice there is no `@model` directive here — this view does not receive a model. The `View()` call in the controller passed nothing, so this view is "untyped".

### 5.8 The `_Layout.cshtml` view

Open `Views/Shared/_Layout.cshtml`. This is the **layout** — the master template that wraps every page. It is mostly HTML with some Razor. The key parts are:

```cshtml
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>@ViewData["Title"] - TaskManager</title>
    <link rel="stylesheet" href="~/lib/bootstrap/dist/css/bootstrap.min.css" />
    <link rel="stylesheet" href="~/css/site.css" asp-append-version="true" />
</head>
<body>
    <header>
        <nav class="navbar navbar-expand-sm navbar-toggleable-sm navbar-light bg-white border-bottom box-shadow">
            <!-- nav links here, including asp-controller / asp-action tag helpers -->
        </nav>
    </header>
    <div class="container">
        <main role="main" class="pb-3">
            @RenderBody()
        </main>
    </div>
    <footer class="border-top footer text-muted">
        <div class="container">
            &copy; 2025 - TaskManager - <a asp-area="" asp-controller="Home" asp-action="Privacy">Privacy</a>
        </div>
    </footer>
    <script src="~/lib/jquery/dist/jquery.min.js"></script>
    <script src="~/lib/bootstrap/dist/js/bootstrap.bundle.min.js"></script>
    <script src="~/js/site.js" asp-append-version="true"></script>
    @await RenderSectionAsync("Scripts", required: false)
</body>
</html>
```

Key lines:

- `@ViewData["Title"]` — reads the value that `Index.cshtml` set. This is how a page communicates its title (and any other metadata) to its layout.
- `asp-append-version="true"` — appends a SHA256 of the file as a query string, e.g. `site.css?v=abc123`. This forces browsers to re-fetch when the file changes (cache busting).
- `asp-controller="Home" asp-action="Privacy"` — these are **tag helpers** (Chapter 9). They generate URLs based on your routes. If the route changes, the URL updates automatically.
- `@RenderBody()` — this is where the view that uses this layout gets injected. `Index.cshtml` is rendered right here.
- `@await RenderSectionAsync("Scripts", required: false)` — a layout section. A view can add a `@section Scripts { ... }` block, and the contents are injected here. We will use this in Chapter 17 when we add per-page JavaScript.

### 5.9 The `_ViewStart.cshtml` file

Open `Views/_ViewStart.cshtml`:

```cshtml
@{
    Layout = "_Layout";
}
```

This file runs *before* every view in the same folder (and subfolders). It sets the default layout to `_Layout.cshtml`. If a view wants to use a different layout, or no layout, it can override this. But by default, every view gets wrapped by `_Layout.cshtml`.

### 5.10 The `_ViewImports.cshtml` file

Open `Views/_ViewImports.cshtml`:

```cshtml
@using TaskManager
@using TaskManager.Models
@addTagHelper *, Microsoft.AspNetCore.Mvc.TagHelpers
```

This file is also processed before every view. Its job is to import namespaces and enable tag helpers globally so each view does not have to repeat them.

- `@using TaskManager` and `@using TaskManager.Models` — make these namespaces available in every view, so you can reference model classes without typing `TaskManager.Models.TodoItem`.
- `@addTagHelper *, Microsoft.AspNetCore.Mvc.TagHelpers` — enables all the built-in ASP.NET Core tag helpers (`asp-action`, `asp-for`, `asp-controller`, etc.) in every view. Without this, `asp-action="Privacy"` would just be a literal HTML attribute.

### 5.11 The `wwwroot` folder

This is the **web root**. Files here are served as static content by Kestrel (after the `app.UseStaticFiles()` middleware runs). The default template has:

- `wwwroot/css/site.css` — your site's CSS overrides.
- `wwwroot/js/site.js` — your site's JavaScript.
- `wwwroot/lib/...` — Bootstrap and jQuery, installed via LibMan (Library Manager). These are static CSS/JS files you can include in your views.
- `wwwroot/favicon.ico` — the browser tab icon.

Any file you put in `wwwroot` is accessible by URL. A file at `wwwroot/images/logo.png` is served at `/images/logo.png`. This is the *only* place the web server serves files from by default — everything else is hidden.

### 5.12 The `launchSettings.json` file

Open `Properties/launchSettings.json`:

```json
{
  "profiles": {
    "http": {
      "commandName": "Project",
      "dotnetRunMessages": true,
      "launchBrowser": true,
      "applicationUrl": "http://localhost:5000",
      "environmentVariables": {
        "ASPNETCORE_ENVIRONMENT": "Development"
      }
    },
    "https": {
      "commandName": "Project",
      "dotnetRunMessages": true,
      "launchBrowser": true,
      "applicationUrl": "https://localhost:7146;http://localhost:5000",
      "environmentVariables": {
        "ASPNETCORE_ENVIRONMENT": "Development"
      }
    }
  }
}
```

This file is used by `dotnet run` and Visual Studio to know how to launch the app. Each "profile" is a launch configuration:

- `applicationUrl` — the URL(s) the app listens on.
- `environmentVariables` — environment variables set when launching.
- `launchBrowser` — whether to open a browser automatically.

The `ASPNETCORE_ENVIRONMENT=Development` setting is what makes `app.Environment.IsDevelopment()` return `true` in `Program.cs`, which is what turns on the developer exception page.

In production you do not use `launchSettings.json` — the hosting environment (IIS, Nginx, Azure, Docker) sets these values.

### 5.13 The `ErrorViewModel` model

Open `Models/ErrorViewModel.cs`:

```csharp
namespace TaskManager.Models
{
    public class ErrorViewModel
    {
        public string? RequestId { get; set; }

        public bool ShowRequestId => !string.IsNullOrEmpty(RequestId);
    }
}
```

- `public string? RequestId { get; set; }` — a nullable string for the request ID.
- `public bool ShowRequestId => !string.IsNullOrEmpty(RequestId);` — a read-only computed property. The error view uses this to decide whether to show the request ID section.

This is a **view model** — a class whose only purpose is to carry data from a controller to a view. We will study view models in depth in Chapter 11.

### 5.14 Try it yourself

1. Modify `Index.cshtml` to say "Welcome to TaskManager!" instead of "Welcome".
2. Run the app and verify your change appears.
3. Add a new action method to `HomeController` called `About()` that returns `View()`.
4. Create a new file `Views/Home/About.cshtml` with some HTML.
5. Run the app and visit `/Home/About`. You should see your new page.
6. Notice you did not have to change any routing configuration — the conventional route picked up the new action automatically.

### 5.15 Common mistakes

- **"The view 'About' was not found"** — you forgot to create the `.cshtml` file, or you put it in the wrong folder. The view for the `About` action of `HomeController` must be at `Views/Home/About.cshtml`.
- **Changes to `.cshtml` do not appear** — you are running the published (compiled) version, not the source. Make sure `dotnet run` is running in your project folder. Razor views are compiled at runtime by default in .NET 8, so changes should appear on refresh; if they do not, restart `dotnet run`.
- **"Cannot find controller"** — the controller class must be `public`, must end in `Controller`, must inherit from `Controller` or `ControllerBase`, and must be in a namespace that starts with the assembly's default namespace (or it will not be discovered by the framework's controller discovery).

### Summary of Chapter 5

- `dotnet new mvc -o TaskManager` creates a working MVC app from a template.
- The project structure follows conventions: `Controllers/`, `Views/`, `Models/`, `wwwroot/`.
- The default `Program.cs` is 12 lines and runs the whole framework.
- A controller is a class inheriting from `Controller`; its public methods are actions.
- A view is a `.cshtml` file in `Views/{ControllerName}/{ActionName}.cshtml`.
- `_Layout.cshtml` wraps every page; `_ViewStart.cshtml` sets the default layout; `_ViewImports.cshtml` imports namespaces and tag helpers for every view.
- `wwwroot` is the only folder served as static files.

In Chapter 6 we take `Program.cs` apart line by line and learn how the entire request pipeline actually works.

---

## Part I · Chapter 6 — Anatomy of the Request Pipeline: Program.cs Line by Line

### What you will learn in this chapter
You will learn every line of `Program.cs` in detail — what each method does, why the order of calls matters, what the DI container is doing, and what the middleware pipeline is. After this chapter you will not be confused by `Program.cs` files you find in real projects, even when they include dozens of `Add*` and `Use*` calls.

### 6.1 The complete file, again

```csharp
var builder = WebApplication.CreateBuilder(args);

builder.Services.AddControllersWithViews();

var app = builder.Build();

if (!app.Environment.IsDevelopment())
{
    app.UseExceptionHandler("/Home/Error");
    app.UseHsts();
}

app.UseHttpsRedirection();
app.UseStaticFiles();

app.UseRouting();

app.UseAuthorization();

app.MapControllerRoute(
    name: "default",
    pattern: "{controller=Home}/{action=Index}/{id?}");

app.Run();
```

### 6.2 Line 1 — `WebApplication.CreateBuilder(args)`

```csharp
var builder = WebApplication.CreateBuilder(args);
```

- `args` — the command-line arguments passed to your program (the string array from the implicit `Main` method). The builder uses them to add command-line configuration to the app's configuration system.
- `WebApplication.CreateBuilder(args)` — this is a **factory method** that returns a `WebApplicationBuilder`. The builder is responsible for two things:
  1. **Configuration** — it reads `appsettings.json`, `appsettings.{Environment}.json`, environment variables, and command-line args, and exposes them via `builder.Configuration`.
  2. **Services** — it exposes a DI container via `builder.Services` where you register everything your app needs.

Under the hood this method:
- Sets up the Kestrel web server.
- Sets up logging to console, debug, and event source.
- Reads configuration files in priority order.
- Sets up the default hosting environment (`Development`, `Staging`, `Production`).

### 6.3 Line 3 — `builder.Services.AddControllersWithViews()`

```csharp
builder.Services.AddControllersWithViews();
```

- `builder.Services` — the **service collection**. This is where you register all the services your application needs, plus their lifetimes (transient, scoped, singleton). The framework builds this collection into an actual DI container when you call `builder.Build()`.
- `AddControllersWithViews()` — a method that registers everything MVC needs:
  - The controller activator and factory.
  - The view engine (Razor).
  - The model binder (parses route values, query strings, JSON bodies into C# objects).
  - The tag helper system.
  - The view component system.
  - The validation system (based on data annotations).
  - The anti-forgery token generator (CSRF protection).
  - Client-side validation support (jQuery unobtrusive validation).

This single line is what turns a generic ASP.NET Core app into an MVC app. If you called `AddControllers()` instead (without `WithViews`), you would get an API-only app — controllers but no Razor view engine. If you called `AddRazorPages()`, you would get Razor Pages instead of MVC.

### 6.4 Line 5 — `var app = builder.Build();`

```csharp
var app = builder.Build();
```

- This builds the actual `WebApplication` from the `WebApplicationBuilder`. After this line, the service collection is "frozen" — you cannot add more services. The `app` variable is your running application: it has the configured DI container, the configuration object, the environment, the logging pipeline, and the middleware pipeline you are about to build.

### 6.5 Lines 7–10 — Environment-specific middleware

```csharp
if (!app.Environment.IsDevelopment())
{
    app.UseExceptionHandler("/Home/Error");
    app.UseHsts();
}
```

- `app.Environment` — an `IHostEnvironment` object. Its `EnvironmentName` property is `"Development"` if `ASPNETCORE_ENVIRONMENT=Development` is set, otherwise `"Production"` (or `"Staging"` if you set that).
- `IsDevelopment()` — returns true if the environment name is `"Development"`.
- `!IsDevelopment()` — true in Production and Staging.
- `app.UseExceptionHandler("/Home/Error")` — registers the **exception handler middleware**. This middleware catches unhandled exceptions thrown by later middleware, logs them, and re-executes the pipeline at the `/Home/Error` URL (so the user sees your friendly error page instead of a stack trace). It only runs in non-Development environments, because in Development you want the developer exception page (which shows the stack trace and source code snippet) to help you debug.
- `app.UseHsts()` — registers the **HSTS** middleware. HSTS stands for **HTTP Strict Transport Security**. It tells browsers (via a response header) "always use HTTPS for this domain for the next 30 days". This protects against man-in-the-middle attacks where a user on a hostile network is downgraded to HTTP. It must not be enabled in Development because you do not have a valid cert there.

In Development, the framework auto-registers the **developer exception page** for you (because `AddControllersWithViews` includes it). You would normally add it explicitly with `app.UseDeveloperExceptionPage();` inside an `if (app.Environment.IsDevelopment())` block, but the template leaves it implicit. We will make it explicit later.

### 6.6 Line 12 — `app.UseHttpsRedirection()`

```csharp
app.UseHttpsRedirection();
```

This middleware redirects any HTTP request to its HTTPS equivalent. If a user types `http://localhost:5000/home`, they are 302-redirected to `https://localhost:7146/home`. The redirect URL is constructed from the configured HTTPS port (read from `launchSettings.json` or the `ASPNETCORE_HTTPS_PORT` env var).

This is important for security: it ensures no user accidentally sends form data over plain HTTP.

### 6.7 Line 13 — `app.UseStaticFiles()`

```csharp
app.UseStaticFiles();
```

This middleware serves files from `wwwroot` at the matching URL path. Without this line, `https://localhost:5000/css/site.css` would 404 — the framework would not know to look in `wwwroot/css/site.css`. With this line, the middleware intercepts the request, finds the file, and serves it with the right content type.

If you want to serve files from a different folder, you can configure it: `app.UseStaticFiles(new StaticFileOptions { FileProvider = new PhysicalFileProvider(Path.Combine(builder.Environment.ContentRootPath, "MyStaticFiles")), RequestPath = "/StaticFiles" });`.

### 6.8 Line 15 — `app.UseRouting()`

```csharp
app.UseRouting();
```

This middleware turns on **endpoint routing**. Endpoint routing is the system that matches incoming URLs to controller actions (or Razor Pages, or Minimal API endpoints, or Health Checks, etc.). After `UseRouting()` runs, the request has a `Endpoint` property attached that says "this request is going to match the `Index` action on `HomeController`". The actual *execution* of the matched endpoint happens later, after `UseAuthorization()` and any other middleware that needs to know the endpoint but should run before it.

The two phases (match → execute) are split so that middleware between `UseRouting()` and the endpoint can see which endpoint was chosen and decide whether to allow it. Authorization works this way: it needs to know *which* action is being called so it can check the `[Authorize]` attributes on that specific action.

### 6.9 Line 17 — `app.UseAuthorization()`

```csharp
app.UseAuthorization();
```

This middleware enforces `[Authorize]` and `[AllowAnonymous]` attributes on controllers and actions. If a request reaches an action marked `[Authorize]` and the user is not signed in, the middleware redirects them to the login page (or returns 401/403 for API requests). If the action has a role requirement (`[Authorize(Roles = "Admin")]`), the middleware checks the user's roles.

`UseAuthorization()` must run *after* `UseRouting()` (so it knows which endpoint was matched) and *before* the endpoint execution (so it can block unauthorized requests before they reach the controller).

Note: this middleware only does authorization, not authentication. Authentication must be added separately, typically via `AddAuthentication()` in the services section and `app.UseAuthentication()` in the pipeline. The template does not include authentication by default; we will add it in Chapter 19.

### 6.10 Lines 19–21 — The default route

```csharp
app.MapControllerRoute(
    name: "default",
    pattern: "{controller=Home}/{action=Index}/{id?}");
```

This is where the URL pattern is defined. Let us break the pattern apart:

- `{controller=Home}` — a route parameter. The URL's first segment is the controller name. If the URL is just `/`, the controller defaults to `Home`.
- `{action=Index}` — the second segment is the action name. If absent, defaults to `Index`.
- `{id?}` — the third segment is an optional `id` parameter. The `?` makes it optional.

So:
- `/` → `HomeController.Index()`
- `/Home` → `HomeController.Index()`
- `/Home/Index` → `HomeController.Index()`
- `/Home/Privacy` → `HomeController.Privacy()`
- `/Todo/Details/5` → `TodoController.Details(5)` (the `5` becomes the `int id` argument of the action)
- `/Todo/Create` → `TodoController.Create()`

The `name: "default"` is just a label for the route — useful for generating URLs from route names, but not strictly required.

After this call, the framework knows the URL pattern. Now when a request comes in:
1. `UseRouting()` matches the URL against this pattern.
2. The endpoint is "execute the matched controller action".
3. `UseAuthorization()` checks the action's authorization attributes.
4. The endpoint finally executes (the framework instantiates the controller, calls the action, and returns the response).

### 6.11 Line 23 — `app.Run()`

```csharp
app.Run();
```

This starts the web server (`Kestrel`), binds to the configured URLs (from `launchSettings.json` or environment), and starts processing requests. The call **blocks** until the application is shut down (Ctrl+C, SIGTERM, or `app.Lifetime.StopApplication()`).

If you forget `app.Run()`, your program will exit immediately without serving anything.

### 6.12 The order matters

Let me emphasize this: **the order of `Use*` calls matters**. Middleware runs in the order it is registered, both for the request (top to bottom) and for the response (bottom to top). Putting middleware in the wrong order produces subtle bugs.

The canonical order is:

```csharp
app.UseExceptionHandler("/Home/Error");     // catch all errors from later middleware
app.UseHsts();                                // HSTS header on all responses
app.UseHttpsRedirection();                   // redirect HTTP → HTTPS
app.UseStaticFiles();                         // serve wwwroot files
app.UseRouting();                             // match URL to endpoint
app.UseCors();                                // CORS headers (if any)
app.UseAuthentication();                       // identify the user
app.UseAuthorization();                        // check user is allowed
app.UseSession();                             // session middleware (if used)
// app.MapControllerRoute(...) here           // define the routes
app.MapHealthChecks("/health");               // additional endpoints
app.Run();                                    // start
```

This is the order the ASP.NET Core team recommends. Deviate only when you understand the implications.

### 6.13 The middleware pipeline diagram

Here is the visual model of the pipeline:

```
 Request in
    │
    ▼
 ┌───────────────────────────────────────────┐
 │ UseExceptionHandler  (catches downstream) │  ← top middleware
 └───────────────────────────────────────────┘
    │
    ▼
 ┌───────────────────────────────────────────┐
 │ UseHttpsRedirection (HTTP→HTTPS)          │
 └───────────────────────────────────────────┘
    │
    ▼
 ┌───────────────────────────────────────────┐
 │ UseStaticFiles (serve wwwroot)            │
 └───────────────────────────────────────────┘
    │
    ▼
 ┌───────────────────────────────────────────┐
 │ UseRouting (match endpoint)               │
 └───────────────────────────────────────────┘
    │
    ▼
 ┌───────────────────────────────────────────┐
 │ UseAuthorization (allow/deny)             │
 └───────────────────────────────────────────┘
    │
    ▼
 ┌───────────────────────────────────────────┐
 │ Endpoint (Controller action)              │
 │   ├─ Model binding                         │
 │   ├─ Action method execution               │
 │   ├─ View rendering                        │
 │   └─ Result writing                        │
 └───────────────────────────────────────────┘
    │
    ▼
 Response out
```

Each box is a middleware. The request flows down; the response flows back up. The `UseExceptionHandler` middleware wraps the entire downstream pipeline in a `try/catch`, so any exception from `UseAuthorization` or the controller is caught and turned into the friendly `/Home/Error` response.

### 6.14 The DI container and lifetimes

You will see code like this in later chapters:

```csharp
builder.Services.AddSingleton<ITimeService, TimeService>();
builder.Services.AddScoped<ITodoRepository, TodoRepository>();
builder.Services.AddTransient<IEmailSender, EmailSender>();
```

These three calls register three services with three different **lifetimes**:

- **Singleton** — one instance for the entire application. All requests share it. Use for stateless, thread-safe services like a clock or a configuration cache.
- **Scoped** — one instance per **request**. All components handling a single HTTP request share the same instance. New request = new instance. Use for things like database contexts (so all repository calls in one request share the same `DbContext` and the same transaction).
- **Transient** — a new instance every time something asks for it. Use for lightweight, stateless, cheap services.

The default `AddControllersWithViews()` already registers many services. We will add our own as we need them.

### 6.15 Try it yourself

1. In your `Program.cs`, before `app.Run();`, add:
   ```csharp
   app.Use(async (context, next) =>
   {
       Console.WriteLine($"Request: {context.Request.Method} {context.Request.Path}");
       await next();
       Console.WriteLine($"Response: {context.Response.StatusCode}");
   });
   ```
2. Run the app and visit a few pages.
3. Watch the console output: every request prints two lines, one before the downstream pipeline runs, one after. You can see the middleware pipeline wrapping the request.

### 6.16 Common mistakes

- **Adding `UseAuthentication()` after `UseAuthorization()`**: authorization will not know who the user is, and every `[Authorize]` request will fail.
- **Adding `UseRouting()` after `UseStaticFiles()`**: static files will still work, but routing will run on every request including static files, which is wasteful. The conventional order has `UseStaticFiles()` short-circuit before routing is even consulted.
- **Forgetting `UseRouting()`**: `MapControllerRoute` will throw an exception at startup telling you to add it.
- **Calling `builder.Services.Add*` after `builder.Build()`**: the service collection is frozen. You will get an `InvalidOperationException`.

### Summary of Chapter 6

- `WebApplication.CreateBuilder` sets up the host, configuration, and DI container.
- `AddControllersWithViews` registers the entire MVC pipeline.
- Middleware order matters: exceptions → HTTPS → static files → routing → auth → endpoint.
- The default route is `{controller=Home}/{action=Index}/{id?}`.
- Service lifetimes are Singleton, Scoped, Transient.
- `app.Run()` starts the server and blocks.

In the next chapter, we finally write our own controllers and actions in depth — the most important building block of an MVC application.

---

## Part II · Chapter 7 — Controllers: The Heart of MVC

### What you will learn in this chapter
What a controller is, how the framework discovers it, how action methods are invoked, what `IActionResult` is and the most common result types, how parameters are bound from the URL/query string/form/body, how to use HTTP verb attributes, and how to return JSON instead of a view. By the end you can write a controller that handles any URL pattern, reads any input, and returns any kind of response.

### 7.1 What is a controller?

A **controller** in ASP.NET Core MVC is a class that:

1. Inherits from `Microsoft.AspNetCore.Mvc.Controller` (or `ControllerBase` if it is an API controller with no view support).
2. Lives in a namespace that the framework's controller discovery can find (by default, any class ending in `Controller` in the assembly's default namespace or a sub-namespace).
3. Has public methods called **actions** that respond to HTTP requests.

A controller is instantiated by the framework **per request**. It is disposed after the response is sent. Controllers are cheap to create; do not worry about performance.

A well-designed controller is **thin**: it receives input, validates it, calls a service or repository, and returns a result. Business logic lives in services, not in controllers.

### 7.2 The minimal controller

```csharp
using Microsoft.AspNetCore.Mvc;

namespace TaskManager.Controllers
{
    public class HelloController : Controller
    {
        public string Index()
        {
            return "Hello from HelloController!";
        }
    }
}
```

Save this as `Controllers/HelloController.cs`. Run the app. Visit `http://localhost:5000/Hello`.

What happens:
1. The URL `/Hello` matches the default route pattern `{controller=Home}/{action=Index}/{id?}` with `controller=Hello`, `action=Index` (default).
2. The framework instantiates `HelloController`.
3. The framework calls `Index()`.
4. The method returns a string. The framework wraps the string in a `ContentResult` and sends it as the response body with `Content-Type: text/plain`.

You should see "Hello from HelloController!" as plain text in the browser.

This demonstrates that controllers can return any type — strings, objects, files. But the common case is to return `IActionResult`, which is a polymorphic result that can be a view, a redirect, JSON, a file, etc.

### 7.3 `IActionResult` and `ActionResult<T>`

`IActionResult` is an interface in `Microsoft.AspNetCore.Mvc`. The framework ships many implementations:

| Result type | Returned via | What it does |
|-------------|--------------|--------------|
| `ViewResult` | `View()` | Renders a Razor view as HTML. |
| `ContentResult` | `Content("text")` | Returns plain text. |
| `JsonResult` | `Json(data)` | Serializes data as JSON. |
| `RedirectResult` | `Redirect("url")` | 302 redirect to a URL. |
| `RedirectToActionResult` | `RedirectToAction("Index")` | 302 redirect to another action. |
| `RedirectToRouteResult` | `RedirectToRoute(...)` | 302 redirect using a named route. |
| `FileResult` | `File(bytes, contentType)` | Returns binary data. |
| `NotFoundResult` | `NotFound()` | 404. |
| `BadRequestResult` | `BadRequest()` | 400. |
| `UnauthorizedResult` | `Unauthorized()` | 401. |
| `ForbidResult` | `Forbid()` | 403. |
| `StatusCodeResult` | `StatusCode(418)` | Custom status code. |
| `EmptyResult` | `new EmptyResult()` | No response body. |
| `PartialViewResult` | `PartialView()` | Renders a partial view. |

A controller action that returns `IActionResult` can return any of these:

```csharp
public IActionResult Index(int id)
{
    if (id == 0) return NotFound();
    if (id == 1) return BadRequest("id cannot be 1");
    if (id == 2) return RedirectToAction("Other");
    if (id == 3) return Content("plain text");
    if (id == 4) return Json(new { name = "Sara" });
    return View();
}
```

In .NET Core 2.1+ there is also `ActionResult<T>` — a generic wrapper that lets you return either an `ActionResult` or a `T` directly. This is mainly useful in API controllers (Chapter 25).

### 7.4 Action methods and HTTP verbs

By default, an action responds to any HTTP verb. To restrict it, use attributes:

```csharp
public class TodoController : Controller
{
    [HttpGet]
    public IActionResult Index() { /* ... */ }

    [HttpPost]
    public IActionResult Create() { /* ... */ }

    [HttpPut]
    public IActionResult Update(int id) { /* ... */ }

    [HttpDelete]
    public IActionResult Delete(int id) { /* ... */ }
}
```

The framework will reject requests with the wrong verb. For example, a POST to `/Todo/Index` will get a 405 Method Not Allowed.

A common pattern is to have two actions with the same name — one GET to show a form, one POST to process it:

```csharp
[HttpGet]
public IActionResult Create()
{
    return View();
}

[HttpPost]
[ValidateAntiForgeryToken]
public IActionResult Create(TodoItem item)
{
    if (ModelState.IsValid)
    {
        _db.TodoItems.Add(item);
        _db.SaveChanges();
        return RedirectToAction(nameof(Index));
    }
    return View(item);
}
```

`[ValidateAntiForgeryToken]` adds CSRF protection (Chapter 20) — required for any POST that mutates state.

### 7.5 Action selectors

- `[ActionName("Edit")]` — changes the URL the action responds to. The method can be named anything; the URL uses "Edit".
- `[NonAction]` — marks a public method as **not** an action. Use it for helper methods that happen to be public.
- `[Route("custom/url")]` — gives the action a specific URL (attribute routing, Chapter 8).

Example:

```csharp
public class TodoController : Controller
{
    // GET /Todo/Show/5
    [ActionName("Show")]
    public IActionResult Details(int id) { ... }

    // Helper method - not callable via URL
    [NonAction]
    public string FormatItem(TodoItem item) => $"{item.Title}";
}
```

### 7.6 Parameters and model binding

When a request comes in, the framework's **model binder** takes data from various sources and binds it to the parameters of the action method.

Sources, in order:

1. **Route data** — values captured from the URL pattern.
2. **Query string** — values in `?key=value` after the URL.
3. **Form data** — values from a POSTed form (`application/x-www-form-urlencoded` or `multipart/form-data`).
4. **Request body** — JSON deserialized into an object (typically for APIs).

You can be explicit:

```csharp
public IActionResult Search(
    [FromRoute] int id,
    [FromQuery] string? term,
    [FromForm] TodoItem item,
    [FromBody] TodoItem bodyItem,
    [FromServices] ILogger<TodoController> logger)
{
    // ...
}
```

- `[FromRoute]` — bind from the route (`{id}` in the URL).
- `[FromQuery]` — bind from the query string.
- `[FromForm]` — bind from posted form values.
- `[FromBody]` — deserialize the JSON body into the type.
- `[FromServices]` — resolve the parameter from the DI container. Useful when a service is only needed by one action and you do not want it in the constructor.

For simple types (int, string, bool), you usually do not need the attributes — the binder figures out where to look. For complex types (your own classes), the binder by default uses form data in MVC and JSON in API controllers; you should be explicit.

### 7.7 Async actions

Database calls and HTTP calls should be async. Make the action return `Task<IActionResult>` and `await` the I/O:

```csharp
public class TodoController : Controller
{
    private readonly AppDbContext _db;

    public TodoController(AppDbContext db) => _db = db;

    public async Task<IActionResult> Index()
    {
        var items = await _db.TodoItems.ToListAsync();
        return View(items);
    }

    public async Task<IActionResult> Details(int id)
    {
        var item = await _db.TodoItems.FirstOrDefaultAsync(t => t.Id == id);
        if (item is null) return NotFound();
        return View(item);
    }
}
```

`ToListAsync` and `FirstOrDefaultAsync` are EF Core's async extension methods. We will dive deep in Chapter 22.

### 7.8 Returning JSON

For an API-style endpoint inside an MVC controller, return `Json`:

```csharp
public IActionResult Stats()
{
    var data = new { Total = 100, Done = 30, Pending = 70 };
    return Json(data);
}
```

`Json(data)` serializes the data with `System.Text.Json` and returns a `JsonResult` with `Content-Type: application/json`. A JavaScript front-end can call this URL and parse the JSON.

In Chapter 25 we will see how to build a fully separate API surface alongside MVC controllers.

### 7.9 Putting it together: a complete CRUD controller

Here is a complete controller for a simple `TodoItem` resource, using all the patterns from this chapter. We will study each piece in detail in later chapters (EF Core in Chapter 13, validation in Chapter 18, etc.), but you should be able to read this and understand the structure now.

```csharp
using Microsoft.AspNetCore.Mvc;
using Microsoft.EntityFrameworkCore;
using TaskManager.Data;
using TaskManager.Models;

namespace TaskManager.Controllers
{
    public class TodoController : Controller
    {
        private readonly AppDbContext _db;
        public TodoController(AppDbContext db) => _db = db;

        // GET /Todo
        public async Task<IActionResult> Index()
        {
            var items = await _db.TodoItems.OrderByDescending(t => t.Id).ToListAsync();
            return View(items);
        }

        // GET /Todo/Details/5
        public async Task<IActionResult> Details(int id)
        {
            var item = await _db.TodoItems.FirstOrDefaultAsync(t => t.Id == id);
            if (item is null) return NotFound();
            return View(item);
        }

        // GET /Todo/Create
        [HttpGet]
        public IActionResult Create() => View();

        // POST /Todo/Create
        [HttpPost]
        [ValidateAntiForgeryToken]
        public async Task<IActionResult> Create(TodoItem item)
        {
            if (!ModelState.IsValid) return View(item);

            _db.TodoItems.Add(item);
            await _db.SaveChangesAsync();
            return RedirectToAction(nameof(Index));
        }

        // GET /Todo/Edit/5
        [HttpGet]
        public async Task<IActionResult> Edit(int id)
        {
            var item = await _db.TodoItems.FirstOrDefaultAsync(t => t.Id == id);
            if (item is null) return NotFound();
            return View(item);
        }

        // POST /Todo/Edit/5
        [HttpPost]
        [ValidateAntiForgeryToken]
        public async Task<IActionResult> Edit(int id, TodoItem item)
        {
            if (id != item.Id) return BadRequest();
            if (!ModelState.IsValid) return View(item);

            _db.TodoItems.Update(item);
            await _db.SaveChangesAsync();
            return RedirectToAction(nameof(Index));
        }

        // GET /Todo/Delete/5
        [HttpGet]
        public async Task<IActionResult> Delete(int id)
        {
            var item = await _db.TodoItems.FirstOrDefaultAsync(t => t.Id == id);
            if (item is null) return NotFound();
            return View(item);
        }

        // POST /Todo/Delete/5
        [HttpPost, ActionName("Delete")]
        [ValidateAntiForgeryToken]
        public async Task<IActionResult> DeleteConfirmed(int id)
        {
            var item = await _db.TodoItems.FindAsync(id);
            if (item is not null)
            {
                _db.TodoItems.Remove(item);
                await _db.SaveChangesAsync();
            }
            return RedirectToAction(nameof(Index));
        }
    }
}
```

Notice:
- Two `Create` methods, one for GET (show form) and one for POST (process form). The framework picks the right one based on the HTTP verb.
- `[ActionName("Delete")]` on `DeleteConfirmed` — the URL is `/Todo/Delete`, but the C# method name is `DeleteConfirmed` (because you cannot have two `Delete` methods with the same signature in C#).
- `ModelState.IsValid` checks all data annotation rules on the model (Chapter 18).
- `await _db.SaveChangesAsync()` writes changes to the database.
- `RedirectToAction(nameof(Index))` sends the user back to the list, avoiding the "double-submit on refresh" problem (PRG pattern — Post/Redirect/Get).

### 7.10 Try it yourself

1. Add a `HelloController` with an action `Index` that returns `Content("Hello")`.
2. Add an action `Greet` that takes a `string name` from the query string and returns `$"Hello, {name}!"` as plain text.
3. Add an action `Json` that returns `Json(new { message = "hi" })`.
4. Add an action `Random` that returns `Redirect("https://example.com")`.
5. Visit each URL and observe the response in your browser's dev tools.

### 7.11 Common mistakes

- **Returning a string from an action that should return a view**: the framework returns the string as plain text, not as HTML. If you want HTML, use `Content("<h1>Hi</h1>", "text/html")` or, better, return a view.
- **Calling a non-existent view**: `return View("Foo")` throws an exception if `Views/{Controller}/Foo.cshtml` and `Views/Shared/Foo.cshtml` do not exist.
- **Putting business logic in the controller**: do not. The controller should be thin. Move business logic into a service class and inject it (Chapter 16).
- **Using `.Result` or `.Wait()` on async methods**: this can deadlock. Always `await` async methods.

### Summary of Chapter 7

- A controller is a `public` class inheriting from `Controller`.
- Every public method is an action.
- Actions return `IActionResult` (or `Task<IActionResult>` for async).
- The framework provides many result types: `View`, `Json`, `Content`, `Redirect`, `NotFound`, `BadRequest`, etc.
- HTTP verbs are restricted with `[HttpGet]`, `[HttpPost]`, etc.
- Parameters are bound from route data, query string, form, body, and services.
- Controllers are per-request, thin, and delegate business logic to services.

In Chapter 8, we look at how URLs are mapped to controllers — the routing system — in much more detail.

---

## Part II · Chapter 8 — Routing: How URLs Reach Your Controllers

### What you will learn in this chapter
How the routing engine matches URLs to controller actions, the difference between **conventional routing** and **attribute routing**, what route constraints are, how to define route defaults, how to generate URLs from your code instead of hard-coding them, and how to debug routing when a URL does not behave as you expect.

### 8.1 The two styles of routing

ASP.NET Core MVC supports two styles:

1. **Conventional routing** — you define URL patterns in `Program.cs` with `MapControllerRoute`. URLs are matched to controllers and actions based on those patterns. This is what the default template uses.
2. **Attribute routing** — you put `[Route]` and `[HttpGet]` attributes directly on controllers and actions. The route for each action is declared right next to the action itself.

You can mix them in the same project. Most MVC apps use conventional routing for the main pages and attribute routing for special cases.

### 8.2 Conventional routing in depth

The default route is:

```csharp
app.MapControllerRoute(
    name: "default",
    pattern: "{controller=Home}/{action=Index}/{id?}");
```

Let us dissect every symbol:

- `name: "default"` — every route has a name. You can use this name to generate URLs with `Url.RouteUrl("default", new { controller = "Todo", action = "Index" })`. The name is optional; it can be empty.
- `pattern: "{controller=Home}/{action=Index}/{id?}"` — the URL pattern.
  - `{controller=Home}` — a route parameter named `controller` with a default of `Home`.
  - `{action=Index}` — a route parameter named `action` with a default of `Index`.
  - `{id?}` — a route parameter named `id`, made optional by the `?`.

When a request arrives at `/`, the route has no segments. The defaults kick in: `controller=Home`, `action=Index`, `id` is absent. The framework instantiates `HomeController` and calls `Index()`.

When a request arrives at `/Todo/Details/5`, the route matches: `controller=Todo`, `action=Details`, `id=5`. The framework instantiates `TodoController`, calls `Details(5)`, with the `5` bound to the `int id` parameter.

#### Multiple conventional routes

You can register multiple patterns:

```csharp
app.MapControllerRoute(
    name: "blog",
    pattern: "Blog/{year}/{month}/{slug}",
    defaults: new { controller = "Blog", action = "Post" });

app.MapControllerRoute(
    name: "default",
    pattern: "{controller=Home}/{action=Index}/{id?}");
```

The framework tries the routes **in order**. The first match wins. So `/Blog/2025/10/hello-world` matches the `blog` route and reaches `BlogController.Post(year: 2025, month: 10, slug: "hello-world")`.

If no pattern matches, the response is 404.

#### Route defaults, inline

The `{controller=Home}` syntax is shorthand for "default value if no segment". You can also write defaults separately:

```csharp
app.MapControllerRoute(
    name: "default",
    pattern: "{controller}/{action}/{id?}",
    defaults: new { controller = "Home", action = "Index" });
```

Both forms are equivalent.

### 8.3 Route constraints

A route **constraint** restricts what values can match a route parameter. For example, you can require `id` to be an integer:

```csharp
app.MapControllerRoute(
    name: "default",
    pattern: "{controller=Home}/{action=Index}/{id:int}");
```

The `:int` is a constraint. Common constraints:

- `:int` — integer.
- `:long`, `:float`, `:double`, `:decimal` — numeric types.
- `:bool` — boolean.
- `:guid` — GUID.
- `:datetime` — date/time.
- `:alpha` — only alphabetic characters.
- `:length(5)` — exactly 5 characters.
- `:minlength(3)`, `:maxlength(10)`.
- `:min(0)`, `:max(100)` — numeric range.
- `:regex(^\\d{4}-\\d{2}-\\d{2}$)` — custom regex.

Example:

```csharp
app.MapControllerRoute(
    name: "blog",
    pattern: "Blog/{year:int:min(2000)}/{month:int:range(1,12)}/{slug:alpha:minlength(3)}",
    defaults: new { controller = "Blog", action = "Post" });
```

This route requires `year` to be an integer at least 2000, `month` to be an integer between 1 and 12, and `slug` to be at least 3 alphabetic characters. If any constraint fails, the route does not match and the framework moves to the next route (or 404 if no more routes).

### 8.4 Attribute routing in depth

In **attribute routing**, you put the URL pattern directly on the controller or action:

```csharp
[Route("api/[controller]")]
[ApiController]
public class TodoApiController : ControllerBase
{
    [HttpGet]
    public IActionResult List() { ... }

    [HttpGet("{id}")]
    public IActionResult Get(int id) { ... }

    [HttpPost]
    public IActionResult Create(TodoItem item) { ... }

    [HttpPut("{id}")]
    public IActionResult Update(int id, TodoItem item) { ... }

    [HttpDelete("{id}")]
    public IActionResult Delete(int id) { ... }
}
```

- `[Route("api/[controller]")]` on the class — sets a prefix. `[controller]` is a token that is replaced with the controller name (without "Controller"). So this controller responds to `/api/TodoApi`.
- `[HttpGet]` on `List()` — handles GET to `/api/TodoApi`.
- `[HttpGet("{id}")]` on `Get(int id)` — handles GET to `/api/TodoApi/5`. The `{id}` part is appended to the prefix.
- `[HttpPost]` on `Create` — handles POST to `/api/TodoApi`.
- `[HttpPut("{id}")]` — handles PUT to `/api/TodoApi/5`.
- `[HttpDelete("{id}")]` — handles DELETE to `/api/TodoApi/5`.

Attribute routing is **required** when you use `[ApiController]` (Chapter 25). It is most commonly used for APIs, but you can also use it in MVC views if you want.

#### Combining class and method routes

The class-level `[Route]` is a prefix. The method-level `[HttpGet]` adds to it. If the method's attribute starts with `/`, it overrides the prefix:

```csharp
[Route("api/[controller]")]
public class TodoApiController : ControllerBase
{
    [HttpGet("list")]           // GET /api/TodoApi/list
    [HttpGet("/todos")]         // GET /todos  (overrides prefix)
    ...
}
```

### 8.5 Token replacement

Inside `[Route]` patterns, you can use these tokens:

- `[controller]` — replaced with the controller name (without "Controller").
- `[action]` — replaced with the action name.
- `[area]` — replaced with the area name (Chapter 24).

Example:

```csharp
[Route("[controller]/[action]")]
public class AdminController : Controller
{
    public IActionResult Dashboard() { ... }   // GET /Admin/Dashboard
    public IActionResult Reports()   { ... }   // GET /Admin/Reports
}
```

### 8.6 Generating URLs in views and controllers

Hard-coding URLs in HTML is fragile: if the route changes, the URL breaks. Instead, use the URL helpers:

In a Razor view, with tag helpers:

```cshtml
<a asp-controller="Todo" asp-action="Details" asp-route-id="5">View task 5</a>
```

This generates `<a href="/Todo/Details/5">View task 5</a>` (or the equivalent based on the current routing configuration). If the route changes, the URL updates automatically.

In a controller:

```csharp
public IActionResult Create()
{
    // ...
    var url = Url.Action("Details", "Todo", new { id = 5 });
    // url is "/Todo/Details/5"
}
```

`Url.Action(action, controller, routeValues)` returns a string URL.

`Url.RouteUrl("default", new { controller = "Todo", action = "Details", id = 5 })` returns the URL for a named route.

This is called **URL generation** or **link generation**, and it is one of the most powerful features of routing — your links stay correct as you refactor your routes.

### 8.7 Debugging routing

If a URL does not behave as expected:

1. Add this to `Program.cs` after `app.UseRouting();`:

```csharp
app.Use(async (context, next) =>
{
    var endpoint = context.GetEndpoint();
    if (endpoint is not null)
    {
        Console.WriteLine($"Matched endpoint: {endpoint.DisplayName}");
        foreach (var md in endpoint.Metadata)
            Console.WriteLine($"  metadata: {md}");
    }
    await next();
});
```

This prints the matched endpoint before the action runs. You can see exactly which action the routing system chose.

2. Check the route order. Routes are tried in registration order; the first match wins. If you have a catch-all like `"{*catch}"`, put it last.

3. Check the verb. The URL might match, but the verb might not. For example, a `[HttpPost]` action does not respond to GET.

4. Check the parameter binding. If the action signature is `public IActionResult Details(int id)` but the URL is `/Todo/Details/abc`, the `:int` constraint (if used) will not match, but if no constraint, the binder fails to convert "abc" to int and `id` becomes 0 (the default for `int`).

### 8.8 Try it yourself

1. In your app, add a new route before the default route:

```csharp
app.MapControllerRoute(
    name: "todo",
    pattern: "tasks/{action=Index}/{id?}",
    defaults: new { controller = "Todo" });
```

2. Now `/tasks/Details/5` reaches `TodoController.Details(5)` (notice the URL does not contain "Todo").
3. Use the tag helper `<a asp-controller="Todo" asp-action="Details" asp-route-id="5">` in a view — it will generate `/tasks/Details/5`, because the new route is registered first.

### 8.9 Common mistakes

- **Route order**: catch-all routes first eat everything. Always put specific routes before general ones.
- **Mixing `[Route]` on some actions of a controller but not others**: when you use attribute routing on a controller, you must use it on every action you want to be reachable. The conventional routes will not apply to a controller that has any `[Route]` or `[HttpGet]` attributes at the class level.
- **`[ApiController]` without attribute routing**: at runtime the framework throws, demanding `[Route]` or `[ApiController]`-compatible routing.

### Summary of Chapter 8

- Two styles: conventional (URL patterns in `Program.cs`) and attribute (`[Route]` on controllers/actions).
- Default route is `{controller=Home}/{action=Index}/{id?}`.
- Constraints (`:int`, `:min()`, `:regex()`) restrict what matches.
- Tokens `[controller]`, `[action]`, `[area]` are replaced at startup.
- Generate URLs with tag helpers (`asp-controller`, `asp-action`) or `Url.Action()`.
- Routes are tried in order; first match wins.

In Chapter 9, we look at views and the Razor syntax in depth.

---

## Part II · Chapter 9 — Views and Razor Syntax

### What you will learn in this chapter
What Razor is and how it compiles, the basic syntax (`@` and code blocks), directives (`@model`, `@inject`, `@using`, `@functions`, `@page`), how to render data, conditionals, loops, comments, HTML helpers and tag helpers (the modern way), and how to escape HTML safely. By the end you can read and write any `.cshtml` file you encounter.

### 9.1 What is Razor?

**Razor** is a template syntax that mixes HTML and C#. Razor files have the `.cshtml` (C# HTML) extension. At compile time, the Razor view engine converts each `.cshtml` file into a real C# class that inherits from `Microsoft.AspNetCore.Mvc.Razor.RazorPage<TModel>`. The generated class has a method called `ExecuteAsync()` that writes HTML and C# output to a `TextWriter`. When you call `return View(model)`, the framework invokes `ExecuteAsync()` on the generated class, captures the output, and ships it as the HTTP response.

This is important to understand: **Razor is compiled, not interpreted**. There is no runtime parsing on each request. The first request to a view triggers compilation; subsequent requests use the compiled class. This makes Razor fast.

### 9.2 The basic syntax

The `@` symbol is the trigger for switching from HTML to C#. A single value after `@` is rendered:

```cshtml
<p>The current date is @DateTime.Now.ToString("yyyy-MM-dd").</p>
```

What gets sent to the browser:

```html
<p>The current date is 2025-10-04.</p>
```

Notice that the result of the C# expression is automatically HTML-encoded before being written. This is a security feature (Chapter 20): if `@Model.Title` is `<script>alert('xss')</script>`, the browser receives `&lt;script&gt;alert(&#x27;xss&#x27;)&lt;/script&gt;` — the script does not run.

If you want to render raw HTML (and you know the content is trusted), use `@Html.Raw(...)`:

```cshtml
@Html.Raw("<b>Bold</b>")
```

This outputs `<b>Bold</b>` as-is. Never use `@Html.Raw` on untrusted user input — it is an XSS vulnerability.

### 9.3 Code blocks: `@{ ... }`

To run multiple statements without output:

```cshtml
@{
    var now = DateTime.Now;
    var greeting = now.Hour < 12 ? "Good morning" : "Good afternoon";
    ViewData["Title"] = "Home";
}

<h1>@greeting!</h1>
<p>It is @now.ToString("HH:mm").</p>
```

Inside `@{ ... }`, you can write any C#: variable declarations, assignments, `if` statements, loops, method calls. To render output from inside the block, use `@:` (single line) or `<text>...</text>` (multi-line):

```cshtml
@if (items.Any())
{
    <text>We have items!</text>
}
else
{
    @:No items.
}
```

### 9.4 Conditionals and loops

```cshtml
@if (Model.IsCompleted)
{
    <p class="done">Done!</p>
}
else
{
    <p class="pending">Pending...</p>
}
```

```cshtml
<ul>
@foreach (var item in Model.Items)
{
    <li>@item.Title — @item.DueAt.ToString("d")</li>
}
</ul>
```

```cshtml
@for (var i = 0; i < Model.Items.Count; i++)
{
    <p>Item @i: @Model.Items[i].Title</p>
}
```

The `@if`, `@foreach`, `@for`, `@while`, `@switch` are the same C# keywords prefixed with `@`.

### 9.5 Comments

Razor comments are `@* ... *@` and are not sent to the browser:

```cshtml
@* This is a Razor comment. It is removed before HTML is sent. *@
```

HTML comments `<!-- ... -->` are sent to the browser and visible in the page source. Use them only for things you want users to see (or be able to debug).

### 9.6 The `@model` directive

The `@model` directive declares what type the view expects from the controller:

```cshtml
@model TaskManager.Models.TodoItem

<h1>@Model.Title</h1>
```

The view is now strongly typed: `Model` is of type `TodoItem`, and the compiler checks that `Model.Title` actually exists. If you typed `Model.Titel` by mistake, you get a compile error.

If a view does not need a model, omit the directive. `Model` will be `null` and `@Model.Something` will throw.

### 9.7 The `@using` and `@namespace` directives

```cshtml
@using TaskManager.Models
@model TodoItem
```

The `@using` is the C# `using` — it imports the namespace so you can write `@model TodoItem` instead of `@model TaskManager.Models.TodoItem`.

You will typically put common `@using` directives in `Views/_ViewImports.cshtml` so every view inherits them:

```cshtml
@using TaskManager
@using TaskManager.Models
@addTagHelper *, Microsoft.AspNetCore.Mvc.TagHelpers
```

`@namespace` declares the namespace of the generated class. Use only in special scenarios.

### 9.8 The `@inject` directive — dependency injection in views

You can inject a service into a view directly:

```cshtml
@inject TaskManager.Services.IStatusService StatusService

<p>System status: @StatusService.GetCurrentStatus()</p>
```

The framework sees the `@inject` directive and adds a constructor parameter to the generated class. When the view is executed, the service is resolved from DI and assigned to the property named (`StatusService` here).

Use `@inject` sparingly — it is a temptation to put logic in views. Legitimate use cases include accessing the current user, reading configuration, or rendering a small piece of dynamic content like a notification badge. For complex logic, use a view component (Chapter 23).

### 9.9 The `@functions` directive

You can define methods inside a view:

```cshtml
@functions
{
    string FormatDate(DateTime d) => d.ToString("yyyy-MM-dd");
}

<p>Due: @FormatDate(Model.DueAt)</p>
```

Again, use sparingly. If a function is non-trivial, put it in a service and inject it.

### 9.10 Tag helpers — the modern way

**Tag helpers** are the modern, HTML-friendly way to generate HTML from Razor. They look like normal HTML tags with custom attributes that the framework recognizes. The most common ones:

#### `asp-action`, `asp-controller` — generating URLs

```cshtml
<a asp-controller="Todo" asp-action="Details" asp-route-id="@Model.Id">View</a>
```

Generates:

```html
<a href="/Todo/Details/5">View</a>
```

If the route changes, the URL updates automatically.

#### `asp-for` — binding form fields to a model

```cshtml
<input asp-for="Title" />
```

This:
1. Sets the `id` to `Title`.
2. Sets the `name` to `Title` (so model binding can pick it up on POST).
3. Sets the `value` to `Model.Title` (current value).
4. Adds validation attributes (`data-val`, `data-val-required`, etc.) based on data annotations, for client-side validation.

Use `asp-for` inside a `<form asp-controller="Todo" asp-action="Create">` and the form is wired up correctly with minimal effort. We will see this in detail in Chapter 17.

#### `asp-items` — dropdown lists

```cshtml
<select asp-for="CategoryId" asp-items="Model.AvailableCategories"></select>
```

This populates the `<select>` with `<option>` elements from `Model.AvailableCategories` (a `List<SelectListItem>`).

#### `asp-route-*` — route values

```cshtml
<a asp-action="Search" asp-route-term="hello" asp-route-page="2">Search</a>
```

Generates `<a href="/Todo/Search?term=hello&page=2">Search</a>`.

### 9.11 HTML helpers — the older way

Before tag helpers existed, Razor used **HTML helpers** — methods called with `@Html.Something(...)`. They still work, and you will see them in older code:

```cshtml
@Html.ActionLink("View", "Details", "Todo", new { id = Model.Id }, null)
@Html.TextBoxFor(m => m.Title)
@Html.EditorFor(m => m.Title)
@Html.LabelFor(m => m.Title)
@Html.DisplayNameFor(m => m.Title)
@Html.ValidationSummary()
```

For new code, prefer tag helpers — they produce cleaner HTML, are easier to read, and integrate with Bootstrap-style class names more naturally. We will use tag helpers throughout this guide.

### 9.12 Razor directives you should know

- `@model T` — declare the view's model type.
- `@using Ns` — import a namespace.
- `@inject IService Name` — inject a service.
- `@functions { ... }` — define methods on the view class.
- `@page` — turn the file into a Razor Page (not MVC; out of scope).
- `@layout "Foo"` — set the layout (overriding `_ViewStart`).
- `@addTagHelper *, AssemblyName` — enable tag helpers from an assembly.
- `@section Scripts { ... }` — define a section for the layout to render.
- `@attribute [Authorize]` — add an attribute to the generated class.

### 9.13 A complete view example

```cshtml
@model IEnumerable<TaskManager.Models.TodoItem>

@{
    ViewData["Title"] = "All Tasks";
}

<h1>@ViewData["Title"]</h1>

@if (!Model.Any())
{
    <p>You have no tasks. <a asp-action="Create" asp-controller="Todo">Add one now</a>.</p>
}
else
{
    <table class="table table-striped">
        <thead>
            <tr>
                <th>ID</th>
                <th>Title</th>
                <th>Status</th>
                <th>Actions</th>
            </tr>
        </thead>
        <tbody>
        @foreach (var item in Model)
        {
            <tr>
                <td>@item.Id</td>
                <td>@item.Title</td>
                <td>
                    @if (item.IsCompleted)
                    {
                        <span class="badge bg-success">Done</span>
                    }
                    else
                    {
                        <span class="badge bg-warning">Pending</span>
                    }
                </td>
                <td>
                    <a asp-action="Details" asp-route-id="@item.Id" class="btn btn-sm btn-info">Details</a>
                    <a asp-action="Edit"    asp-route-id="@item.Id" class="btn btn-sm btn-primary">Edit</a>
                    <a asp-action="Delete"   asp-route-id="@item.Id" class="btn btn-sm btn-danger">Delete</a>
                </td>
            </tr>
        }
        </tbody>
    </table>
}
```

Read this view line by line and make sure you understand every line. This is what a typical "list" view looks like in real ASP.NET Core MVC apps.

### 9.14 Try it yourself

1. Create a `TodoController` with an `Index` action that returns a list of three hard-coded `TodoItem` objects.
2. Create `Views/Todo/Index.cshtml` based on the example above.
3. Visit `/Todo` and observe the table.
4. Add `@inject Microsoft.AspNetCore.Http.IHttpContextAccessor HttpContext` and use `@Context.Request.Headers["User-Agent"]` to display the browser's user agent in the page.

### 9.15 Common mistakes

- **Forgetting `@model`**: `Model` becomes `dynamic` and you lose IntelliSense. You also lose compile-time checks.
- **`Model` vs `model`**: `@model` declares the type, `@Model` accesses the instance. They are case-sensitive.
- **`@Html.Raw` on user input**: XSS hole. Always use `@variable` (encoded) unless you have a specific reason not to.
- **Logic in views**: keep it out. If you have an `@if` with more than three branches or a loop with complex body, move it into a view component or a service.

### Summary of Chapter 9

- Razor is a template syntax that compiles to C#.
- `@` switches from HTML to C#.
- `@{ ... }` is a code block; `@variable` renders a value (HTML-encoded).
- `@model T` makes the view strongly typed.
- `@inject` brings a service into a view.
- Tag helpers (`asp-controller`, `asp-action`, `asp-for`) are the modern way to generate HTML.
- HTML helpers (`@Html.*`) are older but still work.

In Chapter 10, we look at layouts, partial views, and how to organize many views in a real application.

---

## Part II · Chapter 10 — Layouts, Sections, and View Organization

### What you will learn in this chapter
How layouts work, what `_ViewStart` and `_ViewImports` do, how to define and render sections, how to use partial views for reuse, and how to keep a growing view folder clean. By the end you can structure the views of a 100-page MVC app without losing your mind.

### 10.1 Layouts

A **layout** is a master template that wraps a view. Every page that uses the layout shares the same navbar, footer, and HTML skeleton, and only the body changes.

The default layout lives at `Views/Shared/_Layout.cshtml`. Files starting with `_` are conventionally "private" — they are not served as full pages; they are included by other pages. This is just convention; the framework does not enforce it, but tools and developers respect it.

A minimal layout:

```cshtml
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8" />
    <title>@ViewData["Title"] - My App</title>
    <link rel="stylesheet" href="~/css/site.css" asp-append-version="true" />
</head>
<body>
    <header>
        <nav>
            <a asp-controller="Home" asp-action="Index">Home</a>
            <a asp-controller="Todo" asp-action="Index">Tasks</a>
        </nav>
    </header>
    <main>
        @RenderBody()
    </main>
    <footer>&copy; @DateTime.Now.Year - My App</footer>
    @await RenderSectionAsync("Scripts", required: false)
</body>
</html>
```

The two critical calls:

- `@RenderBody()` — the view that uses this layout is rendered here.
- `@await RenderSectionAsync("Scripts", required: false)` — a placeholder where a view can inject page-specific JavaScript. The `required: false` makes it optional; if no view defines a `Scripts` section, the layout does not throw.

### 10.2 Using the layout from a view

The default `Views/_ViewStart.cshtml` does:

```cshtml
@{
    Layout = "_Layout";
}
```

This runs before every view, setting `Layout = "_Layout"`. The view does not need to repeat this.

To use a different layout for one page, override it in the view:

```cshtml
@{
    Layout = "_PrintLayout";
}
```

To render without any layout (e.g. for a partial response or a printable page):

```cshtml
@{
    Layout = null;
}
```

### 10.3 Sections

A view can define content for a layout section using `@section`:

```cshtml
@section Scripts {
    <script src="~/js/chart.js"></script>
    <script>
        $(function () {
            // page-specific JS
        });
    </script>
}
```

The layout's `@await RenderSectionAsync("Scripts", required: false)` picks this up and renders it where the layout says. The result: a page with both the shared scripts (from the layout) and the page-specific scripts (from the section).

You can have multiple sections in a layout, with any name:

```cshtml
<head>
    <meta charset="utf-8" />
    <title>@ViewData["Title"]</title>
    @await RenderSectionAsync("Head", required: false)
</head>
<body>
    @RenderBody()
    @await RenderSectionAsync("Scripts", required: false)
</body>
```

If `required: true` and a view does not define the section, an exception is thrown. Use `required: false` for optional sections.

### 10.4 `_ViewStart.cshtml`

`Views/_ViewStart.cshtml` runs before every view in the same folder and any subfolder. Its job is to set up defaults: the layout, typically. You can also have `_ViewStart.cshtml` files in subfolders to override the layout for that subfolder:

```
Views/
├── _ViewStart.cshtml          // sets Layout = "_Layout"
├── _ViewImports.cshtml
├── Home/
│   └── _ViewStart.cshtml       // (optional) overrides for Home views
├── Todo/
└── Admin/
    └── _ViewStart.cshtml       // overrides Layout = "_AdminLayout"
```

### 10.5 `_ViewImports.cshtml`

`Views/_ViewImports.cshtml` runs before every view too, but its purpose is to import common directives. It supports:

- `@using Namespace` — import namespaces.
- `@inject IService Name` — make a service available in all views.
- `@addTagHelper *, AssemblyName` — enable tag helpers.
- `@removeTagHelper` — disable a previously enabled tag helper.

A typical `_ViewImports.cshtml`:

```cshtml
@using TaskManager
@using TaskManager.Models
@inject TaskManager.Services.ICurrentUserService CurrentUser
@addTagHelper *, Microsoft.AspNetCore.Mvc.TagHelpers
```

With this, every view can use `TodoItem` directly, can access `@CurrentUser.DisplayName`, and has the built-in tag helpers enabled.

Like `_ViewStart`, `_ViewImports` is hierarchical — subfolders can add or remove imports.

### 10.6 Partial views

A **partial view** is a reusable chunk of view code. It does not have its own layout; it is meant to be embedded inside other views.

Create `Views/Shared/_TodoItemRow.cshtml`:

```cshtml
@model TaskManager.Models.TodoItem

<tr>
    <td>@Model.Id</td>
    <td>@Model.Title</td>
    <td>
        @if (Model.IsCompleted)
        {
            <span class="badge bg-success">Done</span>
        }
        else
        {
            <span class="badge bg-warning">Pending</span>
        }
    </td>
</tr>
```

Use it from a parent view:

```cshtml
<table class="table">
    @foreach (var item in Model.Items)
    {
        <partial name="_TodoItemRow" model="item" />
    }
</table>
```

The `<partial>` tag helper is the modern way to render a partial. Older syntax is `@await Html.PartialAsync("_TodoItemRow", item)`. Both do the same thing.

Use partials when:
- The same chunk of HTML appears in multiple views (DRY).
- A view is getting too long and you want to break it up.

For more complex reuse (with logic, dependencies, async), use **view components** (Chapter 23).

### 10.7 Organizing a large Views folder

As your app grows:

```
Views/
├── _ViewStart.cshtml
├── _ViewImports.cshtml
├── Shared/
│   ├── _Layout.cshtml
│   ├── _Layout.cshtml.css
│   ├── _LoginPartial.cshtml
│   ├── _TodoItemRow.cshtml
│   └── Error.cshtml
├── Home/
│   ├── Index.cshtml
│   └── Privacy.cshtml
├── Todo/
│   ├── Index.cshtml
│   ├── Details.cshtml
│   ├── Create.cshtml
│   ├── Edit.cshtml
│   └── Delete.cshtml
├── Account/
│   ├── Login.cshtml
│   └── Register.cshtml
└── Admin/
    ├── Dashboard.cshtml
    └── Reports.cshtml
```

Rules of thumb:
- One folder per controller (matched by name).
- Shared content goes in `Shared/`.
- Sub-views that are tiny and used once can be inlined; if used twice or more, extract a partial.

### 10.8 Try it yourself

1. Modify `_Layout.cshtml` to add a footer with your name.
2. Create a `Views/Shared/_StatusBadge.cshtml` partial that takes a `TodoItem` and renders the "Done"/"Pending" badge.
3. Use the partial in your `Views/Todo/Index.cshtml` instead of the inline `@if` block.
4. Add a `@section Scripts { <script>console.log('hello');</script> }` to a view and observe that the script appears at the bottom of the page.

### 10.9 Common mistakes

- **Layout cycles**: layout A references layout B references layout A. The framework throws an exception.
- **Forgetting `@RenderBody()`**: the layout looks fine but no page content ever appears.
- **Using a partial that requires a model but not passing one**: `Model` is `null` and the partial throws a `NullReferenceException`.

### Summary of Chapter 10

- Layouts wrap views with shared HTML; `@RenderBody()` is the placeholder.
- Sections let views inject content into specific places in the layout.
- `_ViewStart.cshtml` sets defaults for every view.
- `_ViewImports.cshtml` imports namespaces and tag helpers for every view.
- Partials (`<partial name="..." model="..." />`) are reusable view fragments.

In Chapter 11, we look at models, view models, and data annotations — the third pillar of MVC.

---

## Part II · Chapter 11 — Models, ViewModels, and Data Annotations

### What you will learn in this chapter
The difference between an entity model, a view model, and a DTO; how to use data annotations to drive validation and rendering; how to write custom validation attributes; how to keep your data layer and presentation layer separate. By the end you can design a model layer that is clean, secure, and easy to evolve.

### 11.1 The three flavors of "model"

In ASP.NET Core MVC, the word "model" is overloaded. Three different things are all called "models":

1. **Entity models** — C# classes that map to database tables. They are managed by Entity Framework Core and live in your `Models/` folder or in a separate `Domain` project. They represent the persistent state of your application.

2. **View models** — C# classes designed specifically to carry data from a controller to a view (or back from a form). They are the "shape" of the data a view needs. They include only the fields the view needs, plus computed properties and dropdown lists.

3. **DTOs** (Data Transfer Objects) — C# classes used for serialization across API boundaries. In ASP.NET Core, view models and DTOs are often the same class, but conceptually they are different: a view model is for a view, a DTO is for a JSON response.

This separation is important. The same database entity can be displayed in many different views, each needing a different subset of fields. Trying to render a view directly from an entity leads to:
- **Over-posting** attacks — a malicious user adds extra fields to a POST and binds to properties they should not be able to set (e.g. `IsAdmin`).
- **Tight coupling** — changing the database schema breaks every view that uses that entity.
- **Awkward rendering** — the entity does not have a "list of categories for the dropdown" property, so the view has to fetch it from somewhere.

The right answer: have entity classes for the database, and view model classes for the views. Map between them in the controller (or a service).

### 11.2 An entity model

```csharp
namespace TaskManager.Models
{
    public class TodoItem
    {
        public int Id { get; set; }

        [Required(ErrorMessage = "Title is required.")]
        [StringLength(200, MinimumLength = 3, ErrorMessage = "Title must be 3–200 characters.")]
        public string Title { get; set; } = string.Empty;

        [StringLength(2000)]
        public string? Description { get; set; }

        public DateTime CreatedAt { get; set; } = DateTime.UtcNow;

        public DateTime? DueAt { get; set; }

        public bool IsCompleted { get; set; }

        [Range(1, 5, ErrorMessage = "Priority must be between 1 and 5.")]
        public int Priority { get; set; } = 3;

        public int? CategoryId { get; set; }
        public Category? Category { get; set; }
    }
}
```

Line by line:

- `public int Id { get; set; }` — the primary key. EF Core will auto-increment it by convention.
- `[Required]` — the field must be set. For reference types like `string`, this is enforced at the validation layer; for value types like `int`, you do not need it (they are never null).
- `[StringLength(200, MinimumLength = 3)]` — the string must be between 3 and 200 characters.
- `ErrorMessage = "..."` — overrides the default error message. If you omit it, the framework uses a generic message like "The field Title must be a string with a minimum length of 3 and a maximum length of 200."
- `public DateTime CreatedAt { get; set; } = DateTime.UtcNow;` — initialized to the current UTC time. Using UTC avoids timezone bugs.
- `public DateTime? DueAt { get; set; }` — `DateTime?` is `Nullable<DateTime>`, so the field can be null.
- `[Range(1, 5)]` — numeric range.
- `public int? CategoryId { get; set; }` — foreign key to a `Category` entity (nullable, since a task can have no category).
- `public Category? Category { get; set; }` — navigation property (Chapter 15).

### 11.3 A view model

For a create form, we might want:

```csharp
namespace TaskManager.ViewModels
{
    public class TodoCreateViewModel
    {
        [Required]
        [StringLength(200, MinimumLength = 3)]
        public string Title { get; set; } = string.Empty;

        [StringLength(2000)]
        public string? Description { get; set; }

        [Display(Name = "Due date")]
        [DataType(DataType.Date)]
        public DateTime? DueAt { get; set; }

        [Range(1, 5)]
        public int Priority { get; set; } = 3;

        [Display(Name = "Category")]
        public int? CategoryId { get; set; }

        public IEnumerable<SelectListItem>? AvailableCategories { get; set; }
    }
}
```

- `[Display(Name = "...")]` — what label the tag helper `<label asp-for="...">` will render. The form will say "Due date" instead of "DueAt".
- `[DataType(DataType.Date)]` — tells the view engine to render an `<input type="date">` rather than a text input.
- `IEnumerable<SelectListItem>? AvailableCategories` — populated by the controller before the view renders, used by `asp-items` in the `<select>` for the category dropdown.

### 11.4 Mapping between entity and view model

The controller takes form input as a view model, validates, and converts to an entity:

```csharp
[HttpGet]
public async Task<IActionResult> Create()
{
    var vm = new TodoCreateViewModel
    {
        AvailableCategories = await _db.Categories
            .Select(c => new SelectListItem { Value = c.Id.ToString(), Text = c.Name })
            .ToListAsync()
    };
    return View(vm);
}

[HttpPost]
[ValidateAntiForgeryToken]
public async Task<IActionResult> Create(TodoCreateViewModel vm)
{
    if (!ModelState.IsValid)
    {
        vm.AvailableCategories = await _db.Categories
            .Select(c => new SelectListItem { Value = c.Id.ToString(), Text = c.Name })
            .ToListAsync();
        return View(vm);
    }

    var item = new TodoItem
    {
        Title = vm.Title,
        Description = vm.Description,
        DueAt = vm.DueAt,
        Priority = vm.Priority,
        CategoryId = vm.CategoryId,
        CreatedAt = DateTime.UtcNow
    };

    _db.TodoItems.Add(item);
    await _db.SaveChangesAsync();
    return RedirectToAction(nameof(Index));
}
```

Notice:
- The GET version populates `AvailableCategories` so the dropdown has something to show.
- If POST validation fails, the controller re-populates `AvailableCategories` before returning the view — otherwise the dropdown is empty and the page looks broken.
- The `TodoItem` entity is created only after validation passes. `Id` and `IsCompleted` are not set from the view model — the user cannot set them from a public form. This is the **over-posting defense** (Chapter 20).

### 11.5 The full data annotation catalog

Here is every commonly-used data annotation. All live in the `System.ComponentModel.DataAnnotations` namespace unless noted.

#### Validation attributes

- `[Required]` — must be set.
- `[StringLength(max)]` — string length limit. Optional `MinimumLength`.
- `[MaxLength(n)]`, `[MinLength(n)]` — array / list length.
- `[Range(min, max)]` — numeric range.
- `[EmailAddress]` — valid email format.
- `[Url]` — valid URL.
- `[Phone]` — phone-like string.
- `[CreditCard]` — credit card number (with Luhn check).
- `[Compare(nameof(Password)]` — must equal another property.
- `[RegularExpression(pattern)]` — match a regex.
- `[EnumDataType(typeof(MyEnum))]` — must be a valid enum value.
- `[DataType(DataType.X)]` — declares the type, drives the editor: `Date`, `Time`, `DateTime`, `EmailAddress`, `Url`, `Password`, `MultilineText`, `PhoneNumber`, `Currency`, `PostalCode`, `Duration`, `CreditCard`, `Image`, `Upload`, etc.

#### Display attributes

- `[Display(Name = "...")]` — label text.
- `[DisplayFormat(DataFormatString = "{0:d}", ApplyFormatInEditMode = true)]` — how to format the value when rendered.
- `[DisplayName("...")]` — older form of `Display(Name)`.
- `[ScaffoldColumn(false)]` — skip when auto-scaffolding.
- `[HiddenInput]` — render as `<input type="hidden">`.
- `[ReadOnly(true)]` — render as read-only.

#### Database-mapping attributes (used by EF Core)

EF Core mostly uses **Fluent API** (Chapter 13) for mapping, but supports a few attributes for common cases:

- `[Key]` — primary key.
- `[ForeignKey]` — foreign key.
- `[Column(name)]` — column name.
- `[Table(name)]` — table name.
- `[NotMapped]` — exclude from database.
- `[DatabaseGenerated(DatabaseGeneratedOption.Identity)]` — auto-increment.
- `[ConcurrencyCheck]` — optimistic concurrency column.
- `[Timestamp]` — row version (for optimistic concurrency).

### 11.6 Custom validation attributes

When the built-in annotations are not enough, write your own:

```csharp
public class NotInPastAttribute : ValidationAttribute
{
    public override bool IsValid(object? value)
    {
        if (value is DateTime dt)
        {
            return dt >= DateTime.Today;
        }
        return true; // null is OK; use [Required] to forbid null
    }
}
```

Use it like any annotation:

```csharp
public class TodoItem
{
    // ...
    [NotInPast(ErrorMessage = "Due date cannot be in the past.")]
    public DateTime? DueAt { get; set; }
}
```

For cross-field validation, implement `IValidatableObject`:

```csharp
public class TodoCreateViewModel : IValidatableObject
{
    public DateTime? StartAt { get; set; }
    public DateTime? DueAt  { get; set; }

    public IEnumerable<ValidationResult> Validate(ValidationContext validationContext)
    {
        if (StartAt.HasValue && DueAt.HasValue && StartAt > DueAt)
        {
            yield return new ValidationResult(
                "Start date cannot be after due date.",
                new[] { nameof(StartAt), nameof(DueAt) });
        }
    }
}
```

The framework calls `Validate` after running all attribute-based rules, and adds any results to `ModelState`.

### 11.7 Try it yourself

1. Add a `Category` entity: `public class Category { public int Id { get; set; } [Required] public string Name { get; set; } public string? Color { get; set; } }`.
2. Add a `TodoCreateViewModel` with all the fields above and a `NotInPast` validation on `DueAt`.
3. Write the controller actions to map between them.
4. Use the `[Display]` and `[DataType]` attributes so the form labels and input types are friendly.

### 11.8 Common mistakes

- **Binding the entity directly to the form**: opens you to over-posting. Always use a view model for the form.
- **Setting `AvailableCategories` only in the GET, not in the POST on validation failure**: the re-rendered form's dropdown is empty.
- **Forgetting `[Required]` on reference types when using nullable reference types**: with `Nullable<T>` enabled, the compiler will warn you, but `[Required]` is still needed for *runtime* validation.
- **Putting UI concerns in entities**: `Display(Name)` on an entity means the entity now knows about how it is shown. Put it on the view model.

### Summary of Chapter 11

- **Entities** map to database tables.
- **View models** carry data to views and back.
- **DTOs** cross API boundaries.
- Use data annotations for validation, display, and (occasionally) mapping.
- Custom validation attributes for unusual rules.
- `IValidatableObject` for cross-field validation.
- Never bind entities directly to forms — use view models to defend against over-posting.

In Chapter 12, we start building our real sample project, TaskManager, which we will use for the rest of the guide.

---

## Part III · Chapter 12 — Introducing Our Sample Project: TaskManager

### What you will learn in this chapter
You will be introduced to the TaskManager application — the sample project we will build through the rest of this guide. We will lay out the entities, the relationships, and the features we will add chapter by chapter. From this point onward, every chapter adds a piece of TaskManager, and by the end you will have a complete, deployable app.

### 12.1 What is TaskManager?

**TaskManager** is a personal task-tracking application. The user logs in, creates tasks with a title, description, due date, priority, and category, marks them as completed, edits them, deletes them, and views a dashboard of upcoming and overdue tasks. Tasks can be filtered by category and status. The data lives in a SQLite database. The app exposes both an HTML UI (MVC) and a JSON API surface. It has tests, logging, and a deployment story.

### 12.2 Domain model

```
Category               TodoItem                ApplicationUser (from Identity)
─────────              ──────────              ──────────────────
Id (PK)                Id (PK)                 Id (PK, string)
Name (req, 50)         Title (req, 3–200)      UserName (req)
Color (opt, 20)        Description (opt, 2000) Email (req)
Todos (1→many)         CreatedAt (req)         PasswordHash
                       DueAt (opt)             LockoutEnd
                       IsCompleted            ...
                       Priority (1–5)
                       CategoryId (FK, opt)
                       Category (nav)
                       OwnerId (FK → User, opt)
                       Owner (nav)
```

### 12.3 Features by chapter

| Chapter | Adds |
|---------|------|
| 13      | `AppDbContext`, `Category` and `TodoItem` entities, SQLite connection. |
| 14      | First migration, seed data. |
| 15      | `Owner` navigation, `Category` one-to-many with eager loading. |
| 16      | `IRepository<T>`, repository implementation, DI registration. |
| 17      | `Create` and `Edit` forms with tag helpers, anti-forgery, file upload for an attachment. |
| 18      | Data annotations on entities, custom `NotInPast` validator, client-side validation. |
| 19      | ASP.NET Core Identity: registration, login, logout, role-based access. |
| 20      | Security review: CSRF tokens, XSS hardening, over-posting protection. |
| 21      | `LogActionFilter` global filter; `[RequireHttps]`; admin-only area. |
| 22      | Async actions throughout; cancellation tokens on long queries. |
| 23      | `CategorySidebarViewComponent` rendered in the layout. |
| 24      | `Admin` area with its own controllers and views. |
| 25      | REST API for `/api/todos` alongside the MVC UI. |
| 26      | `ILogger<T>` structured logging; custom error page. |
| 27      | xUnit tests for controllers; integration tests for routes. |
| 28      | `dotnet publish`; Dockerfile; deploy to a Linux container. |
| 29      | Refactor into Clean Architecture layers. |

### 12.4 Setting up the project

If you have already created the `TaskManager` project in Chapter 5, continue with it. If not:

```bash
dotnet new mvc -o TaskManager
cd TaskManager
git init
dotnet new gitignore
```

Add the `Data` and `ViewModels` folders:

```bash
mkdir Data ViewModels Services
```

Your project should look like:

```
TaskManager/
├── Controllers/
├── Data/                  ← NEW
├── Models/
├── Services/              ← NEW
├── ViewModels/            ← NEW
├── Views/
├── wwwroot/
└── Program.cs
```

### 12.5 The plan for the next few chapters

In Chapter 13 we install EF Core and write our `DbContext`. In Chapter 14 we run our first migration and create the schema. In Chapter 15 we add relationships and learn how to load related data. In Chapter 16 we wrap the data access in repositories and inject them into our controllers. By the end of Part III we have a fully functional data layer and can build the rest of the app on top.

### Summary of Chapter 12

- TaskManager is a personal task tracker.
- Two main entities: `TodoItem` and `Category`.
- One user entity from ASP.NET Core Identity.
- We will build the data layer in Chapter 13–16.
- We will add UI, validation, auth, security, filters, async, areas, API, tests, and deployment in subsequent chapters.

---

## Part III · Chapter 13 — Entity Framework Core: The ORM That Powers Your Data Layer

### What you will learn in this chapter
What an ORM is and why we use one, how to install EF Core, how to write a `DbContext`, the three ways to configure entity mappings (conventions, data annotations, Fluent API), and how to register a `DbContext` with the DI container. By the end you can persist C# objects to a SQLite database.

### 13.1 What is an ORM, and why EF Core?

An **Object-Relational Mapper (ORM)** is a layer that sits between your object-oriented code and a relational database. You work with C# objects; the ORM translates between those objects and database rows. The ORM writes SQL for you, executes it, and materializes the rows back into objects when you read.

The promise: you focus on the domain model, not on SQL strings. The reality: ORMs make common cases trivial and rare cases annoying — but for 80% of business apps, the common cases are what you write most of the time, and an ORM saves enormous amounts of boilerplate.

**Entity Framework Core** (EF Core) is Microsoft's ORM. EF Core 8 is the current version. It supports SQL Server, SQLite, PostgreSQL, MySQL, Azure Cosmos DB, and in-memory (for testing). It is open source, fast, and well-supported.

Why use EF Core instead of writing raw SQL?

- **Type safety**: your queries are checked at compile time. A typo in a column name is a build error, not a runtime crash.
- **LINQ integration**: write queries in C# with LINQ; the provider translates them to SQL.
- **Change tracking**: when you load an entity and modify it, calling `SaveChanges` issues the right UPDATE. You do not write the UPDATE by hand.
- **Migrations**: schema changes are code. You commit them to source control; your team and your production database stay in sync.
- **Cross-database**: write your code against SQLite in dev, switch to SQL Server in production by changing one line.

The downsides:

- **Performance**: a hand-written SQL query is faster than what the ORM generates, in extreme cases. For most apps, the difference is negligible; for hot paths, you can always drop down to raw SQL via `FromSqlRaw`.
- **Learning curve**: EF Core has many features. You will not learn them all in one chapter.

### 13.2 Installing EF Core

In your `TaskManager` folder, run:

```bash
dotnet add package Microsoft.EntityFrameworkCore.Sqlite --version 8.0.*
dotnet add package Microsoft.EntityFrameworkCore.Design  --version 8.0.*
dotnet add package Microsoft.EntityFrameworkCore.Tools   --version 8.0.*
```

What you just installed:

- `Microsoft.EntityFrameworkCore.Sqlite` — the SQLite provider. Includes the EF Core runtime and the SQLite-specific ADO.NET layer. You only need one provider per project (you can install `Microsoft.EntityFrameworkCore.SqlServer` instead, or alongside, for SQL Server).
- `Microsoft.EntityFrameworkCore.Design` — design-time components needed by the EF Core tooling (migrations, scaffolding). Required to run `dotnet ef migrations add`.
- `Microsoft.EntityFrameworkCore.Tools` — adds PowerShell commands for Visual Studio's Package Manager Console (`Add-Migration`, `Update-Database`). Not strictly required if you only use the `dotnet ef` CLI, but useful.

Verify the install:

```bash
dotnet restore
dotnet build
```

### 13.3 The entity classes

Create `Models/Category.cs`:

```csharp
using System.ComponentModel.DataAnnotations;

namespace TaskManager.Models
{
    public class Category
    {
        public int Id { get; set; }

        [Required]
        [StringLength(50)]
        public string Name { get; set; } = string.Empty;

        [StringLength(20)]
        public string? Color { get; set; }

        // Navigation property (Chapter 15)
        public List<TodoItem> Todos { get; set; } = new();
    }
}
```

Create `Models/TodoItem.cs`:

```csharp
using System.ComponentModel.DataAnnotations;

namespace TaskManager.Models
{
    public class TodoItem
    {
        public int Id { get; set; }

        [Required]
        [StringLength(200, MinimumLength = 3)]
        public string Title { get; set; } = string.Empty;

        [StringLength(2000)]
        public string? Description { get; set; }

        public DateTime CreatedAt { get; set; } = DateTime.UtcNow;

        public DateTime? DueAt { get; set; }

        public bool IsCompleted { get; set; }

        [Range(1, 5)]
        public int Priority { get; set; } = 3;

        public int? CategoryId { get; set; }
        public Category? Category { get; set; }
    }
}
```

Notice the navigation property pattern:
- `TodoItem` has `CategoryId` (foreign key) and `Category` (navigation).
- `Category` has a collection `List<TodoItem> Todos` (the other side of the relationship).

EF Core will detect this pattern by convention (Chapter 15).

### 13.4 The `DbContext`

Create `Data/AppDbContext.cs`:

```csharp
using Microsoft.EntityFrameworkCore;
using TaskManager.Models;

namespace TaskManager.Data
{
    public class AppDbContext : DbContext
    {
        public AppDbContext(DbContextOptions<AppDbContext> options) : base(options) { }

        public DbSet<TodoItem> TodoItems => Set<TodoItem>();
        public DbSet<Category> Categories => Set<Category>();

        protected override void OnModelCreating(ModelBuilder modelBuilder)
        {
            base.OnModelCreating(modelBuilder);

            modelBuilder.Entity<TodoItem>(entity =>
            {
                entity.HasKey(t => t.Id);
                entity.Property(t => t.Title).IsRequired().HasMaxLength(200);
                entity.Property(t => t.Description).HasMaxLength(2000);
                entity.Property(t => t.CreatedAt).HasDefaultValueSql("CURRENT_TIMESTAMP");
                entity.Property(t => t.Priority).HasDefaultValue(3);

                entity.HasOne(t => t.Category)
                      .WithMany(c => c.Todos)
                      .HasForeignKey(t => t.CategoryId)
                      .OnDelete(DeleteBehavior.SetNull);
            });

            modelBuilder.Entity<Category>(entity =>
            {
                entity.HasKey(c => c.Id);
                entity.Property(c => c.Name).IsRequired().HasMaxLength(50);
                entity.Property(c => c.Color).HasMaxLength(20);
                entity.HasIndex(c => c.Name).IsUnique();
            });
        }
    }
}
```

Line by line:

- `public class AppDbContext : DbContext` — a `DbContext` is the EF Core unit of work. It tracks entity changes, manages connections, and writes them to the database on `SaveChanges`.
- `public AppDbContext(DbContextOptions<AppDbContext> options) : base(options) { }` — the constructor takes options (which include the connection string and provider). The DI container provides these options to the constructor.
- `public DbSet<TodoItem> TodoItems => Set<TodoItem>();` — a `DbSet<T>` is a typed table accessor. `Set<T>()` returns the set; the `=>` makes it a computed property. The name `TodoItems` becomes the table name by convention (pluralized).
- `protected override void OnModelCreating(ModelBuilder modelBuilder)` — the **Fluent API** method. This is where you configure entities, properties, indexes, relationships, constraints. It is called once when the context is first used; the configuration is cached.

In `OnModelCreating`:

- `entity.HasKey(t => t.Id)` — declares `Id` as the primary key. EF Core does this by convention anyway, but being explicit is clearer.
- `entity.Property(t => t.Title).IsRequired().HasMaxLength(200)` — column is `NOT NULL` and `VARCHAR(200)`.
- `entity.Property(t => t.CreatedAt).HasDefaultValueSql("CURRENT_TIMESTAMP")` — SQLite function that returns the current timestamp. The column has a default at the database level, so you can insert without setting `CreatedAt` (the database fills it in). We have `= DateTime.UtcNow` on the C# property too — for in-memory tests, you want the C# default; for production, you want the database default.
- `entity.HasOne(t => t.Category).WithMany(c => c.Todos).HasForeignKey(t => t.CategoryId).OnDelete(DeleteBehavior.SetNull)` — declares the one-to-many relationship. `HasOne` says a `TodoItem` has one `Category`. `WithMany` says a `Category` has many `TodoItems`. `HasForeignKey` identifies the FK column. `OnDelete(SetNull)` says when a category is deleted, the `CategoryId` on its tasks is set to NULL (instead of cascading the delete, which would lose the task).
- `entity.HasIndex(c => c.Name).IsUnique()` — creates a unique index on `Name`.

### 13.5 Registering the DbContext

Edit `appsettings.json` to add a connection string:

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Data Source=taskmanager.db"
  },
  "Logging": { ... },
  "AllowedHosts": "*"
}
```

The `Data Source=taskmanager.db` connection string tells SQLite to use a file called `taskmanager.db` in the project's working directory.

Edit `Program.cs` to register the context:

```csharp
using Microsoft.EntityFrameworkCore;
using TaskManager.Data;

var builder = WebApplication.CreateBuilder(args);

builder.Services.AddControllersWithViews();

builder.Services.AddDbContext<AppDbContext>(options =>
    options.UseSqlite(
        builder.Configuration.GetConnectionString("DefaultConnection")));

var app = builder.Build();
// ... (rest unchanged)
```

Line by line:

- `using Microsoft.EntityFrameworkCore;` — for `UseSqlite`.
- `using TaskManager.Data;` — for `AppDbContext`.
- `builder.Services.AddDbContext<AppDbContext>(options => options.UseSqlite(...))` — registers `AppDbContext` in the DI container with **scoped** lifetime (one instance per request). The options factory builds the connection configuration. `UseSqlite` tells EF Core to use the SQLite provider with the given connection string.

To switch to SQL Server in production, change `UseSqlite(...)` to `options.UseSqlServer(...)` and change the connection string. The rest of the code is unchanged — that is the portability promise.

### 13.6 Three configuration styles, summarized

You can configure an entity in three ways. They are not mutually exclusive — they layer.

1. **Conventions** — EF Core has default rules. A property named `Id` or `EntityNameId` is the primary key. A `string` becomes `TEXT` (SQLite) or `NVARCHAR(MAX)` (SQL Server). A navigation property of type `T` with a `TId` property on the parent is a one-to-many relationship.

2. **Data annotations** — attributes on the class: `[Required]`, `[MaxLength]`, `[Column]`, `[Table]`. Quick to write, lives next to the property.

3. **Fluent API** — the `OnModelCreating` method. Most powerful; lets you do things annotations cannot (e.g. configuring relationships in detail, defining indexes, seeding).

For simple properties, annotations are fine. For relationships, indexes, seeds, and any non-trivial configuration, prefer the Fluent API. We will use both in this guide.

### 13.7 Try it yourself

1. Add the EF Core packages as above.
2. Create `Category` and `TodoItem` entities.
3. Create `AppDbContext` with the configuration shown.
4. Register the context in `Program.cs`.
5. Add the connection string to `appsettings.json`.
6. Build the project (`dotnet build`). It should compile cleanly.

We will create the database itself (migrations) in Chapter 14.

### 13.8 Common mistakes

- **Two providers**: `UseSqlite` and `UseSqlServer` both in `AddDbContext`. The framework throws. Pick one.
- **Connection string not in `appsettings.json`**: `GetConnectionString` returns `null`, EF Core throws a confusing null reference. Verify the section name (`ConnectionStrings`) and the key name (`DefaultConnection`) match exactly.
- **DbContext not registered**: controller takes `AppDbContext` but `AddDbContext` was forgotten. The DI container throws "no service for type AppDbContext".
- **Forgetting `using Microsoft.EntityFrameworkCore;`**: `UseSqlite` is not found. The compiler error is helpful here.

### Summary of Chapter 13

- EF Core is Microsoft's ORM; it translates C# objects to/from database rows.
- A `DbContext` is the unit of work; `DbSet<T>` is a table accessor.
- Configure entities with conventions, annotations, or Fluent API.
- Register the context with `AddDbContext<T>(options => options.UseSqlite(...))`.
- The connection string lives in `appsettings.json` under `ConnectionStrings`.

In Chapter 14, we generate the database schema with migrations.

---

## Part III · Chapter 14 — Migrations: Evolving Your Database Schema

### What you will learn in this chapter
What migrations are, how to install the EF Core CLI tooling, how to create your first migration, how to apply it to the database, how to read the generated files, how to seed the database, and how to evolve the schema as your model changes.

### 14.1 What is a migration?

A **migration** is a code file that describes a change to the database schema. Each migration has an `Up` method (apply the change) and a `Down` method (revert the change). The framework keeps a table called `__EFMigrationsHistory` in your database that tracks which migrations have been applied. When you run `dotnet ef database update`, EF Core looks at the pending migrations, runs their `Up` methods, and updates the history table.

Migrations are **source-controlled**: you commit the migration files alongside your C# code. Your teammates get the latest, run `dotnet ef database update`, and their database has the same schema as yours. Production runs the same command and stays in sync.

### 14.2 Installing the EF Core CLI

The `dotnet ef` command is a global tool. Install it once per machine:

```bash
dotnet tool install --global dotnet-ef
```

If you already have it but it is old, update:

```bash
dotnet tool update --global dotnet-ef
```

Verify:

```bash
dotnet ef --version
```

You should see something like `8.0.x`.

### 14.3 Creating the first migration

In your project folder, run:

```bash
dotnet ef migrations add InitialCreate
```

This produces three files under a new `Migrations/` folder:

- `Migrations/{timestamp}_InitialCreate.cs` — the migration itself. Contains `Up` and `Down`.
- `Migrations/{timestamp}_InitialCreate.Designer.cs` — a snapshot of the model at the time the migration was created. Used internally for the next migration to compute the diff.
- `Migrations/AppDbContextModelSnapshot.cs` — the current snapshot. Updated on every new migration.

Let us look at the generated `Up` method:

```csharp
public partial class InitialCreate : Migration
{
    protected override void Up(MigrationBuilder migrationBuilder)
    {
        migrationBuilder.CreateTable(
            name: "Categories",
            columns: table => new
            {
                Id = table.Column<int>(type: "INTEGER", nullable: false)
                    .Annotation("Sqlite:Autoincrement", true),
                Name = table.Column<string>(type: "TEXT", maxLength: 50, nullable: false),
                Color = table.Column<string>(type: "TEXT", maxLength: 20, nullable: true)
            },
            constraints: table =>
            {
                table.PrimaryKey("PK_Categories", x => x.Id);
            });

        migrationBuilder.CreateTable(
            name: "TodoItems",
            columns: table => new
            {
                Id = table.Column<int>(type: "INTEGER", nullable: false)
                    .Annotation("Sqlite:Autoincrement", true),
                Title = table.Column<string>(type: "TEXT", maxLength: 200, nullable: false),
                Description = table.Column<string>(type: "TEXT", maxLength: 2000, nullable: true),
                CreatedAt = table.Column<DateTime>(type: "TEXT", nullable: false),
                DueAt = table.Column<DateTime>(type: "TEXT", nullable: true),
                IsCompleted = table.Column<bool>(type: "INTEGER", nullable: false),
                Priority = table.Column<int>(type: "INTEGER", nullable: false),
                CategoryId = table.Column<int>(type: "INTEGER", nullable: true)
            },
            constraints: table =>
            {
                table.PrimaryKey("PK_TodoItems", x => x.Id);
                table.ForeignKey(
                    name: "FK_TodoItems_Categories_CategoryId",
                    column: x => x.CategoryId,
                    principalTable: "Categories",
                    principalColumn: "Id",
                    onDelete: ReferentialAction.SetNull);
            });

        migrationBuilder.CreateIndex(
            name: "IX_Categories_Name",
            table: "Categories",
            column: "Name",
            unique: true);

        migrationBuilder.CreateIndex(
            name: "IX_TodoItems_CategoryId",
            table: "TodoItems",
            column: "CategoryId");
    }

    protected override void Down(MigrationBuilder migrationBuilder)
    {
        migrationBuilder.DropTable(name: "TodoItems");
        migrationBuilder.DropTable(name: "Categories");
    }
}
```

This is C# code that uses the `MigrationBuilder` fluent API to describe what tables, columns, primary keys, foreign keys, and indexes to create. The `Down` method drops the tables.

### 14.4 Applying the migration

```bash
dotnet ef database update
```

This:
1. Reads the connection string from `appsettings.json`.
2. Connects to the SQLite database (creates `taskmanager.db` if it does not exist).
3. Checks the `__EFMigrationsHistory` table — empty, so no migrations applied yet.
4. Finds the pending migration `InitialCreate` and runs its `Up`.
5. Inserts a row into `__EFMigrationsHistory` recording the migration was applied.

You should now see `taskmanager.db` in your project folder. (Open it with any SQLite browser like DB Browser for SQLite or the VS Code SQLite extension.)

### 14.5 Seeding data

You often want to populate the database with some initial data when it is created. Two ways:

#### Seeding via `OnModelCreating` (built-in)

Add this to the end of `OnModelCreating`:

```csharp
modelBuilder.Entity<Category>().HasData(
    new Category { Id = 1, Name = "Personal", Color = "#4287f5" },
    new Category { Id = 2, Name = "Work",     Color = "#42f57b" },
    new Category { Id = 3, Name = "Urgent",  Color = "#f54242" }
);
```

The `HasData` seeds are added to the migration as INSERT statements. Run:

```bash
dotnet ef migrations add SeedCategories
dotnet ef database update
```

The new migration inserts the three rows into `Categories`. The seed is part of the schema; if you change the data, you create a new migration that updates it. This is great for lookup tables (categories, statuses, etc.) that should always exist.

#### Seeding at startup (custom)

For larger seed data or data that should only be inserted if not present:

```csharp
public static class DbSeeder
{
    public static async Task SeedAsync(AppDbContext db)
    {
        await db.Database.MigrateAsync();

        if (!db.TodoItems.Any())
        {
            db.TodoItems.Add(new TodoItem
            {
                Title = "Welcome to TaskManager!",
                Description = "Edit or delete this task to get started.",
                Priority = 5
            });
            await db.SaveChangesAsync();
        }
    }
}
```

Call it from `Program.cs`:

```csharp
using (var scope = app.Services.CreateScope())
{
    var db = scope.ServiceProvider.GetRequiredService<AppDbContext>();
    await DbSeeder.SeedAsync(db);
}
```

This pattern is useful for inserting a default admin user, sample data in development, etc. The `await db.Database.MigrateAsync()` ensures the database schema is up to date at startup — handy for production deployments.

### 14.6 Evolving the schema

When you change your entities, you create a new migration. Example: add a `Tags` column to `TodoItem`.

1. Edit `Models/TodoItem.cs`:

```csharp
[StringLength(500)]
public string? Tags { get; set; }
```

2. Create the migration:

```bash
dotnet ef migrations add AddTagsToTodoItem
```

3. Apply:

```bash
dotnet ef database update
```

The new migration contains:

```csharp
migrationBuilder.AddColumn<string>(
    name: "Tags",
    table: "TodoItems",
    type: "TEXT",
    maxLength: 500,
    nullable: true);
```

### 14.7 Dropping and starting over

During development you might want to wipe the database and start fresh:

```bash
dotnet ef database drop
dotnet ef database update
```

In production, never use `database drop`. Schema changes are always migrations.

### 14.8 Try it yourself

1. Create the `InitialCreate` migration.
2. Apply it with `dotnet ef database update`.
3. Add a `Tags` column to `TodoItem` and create a migration for it.
4. Apply the new migration.
5. Inspect the `taskmanager.db` file in a SQLite browser.

### 14.9 Common mistakes

- **Forgetting to run `dotnet ef database update`**: you have the migration file, but the database does not. The app runs but every query throws "no such table".
- **Editing a migration after applying it**: never. The history table says the migration was applied, but the code now describes something else. Always create a new migration instead.
- **Forgetting to add new entities to the `DbContext`**: a `public DbSet<T>` is required for EF Core to track the entity. If you forget it, `dotnet ef migrations add` does not see your new entity and produces an empty migration.

### Summary of Chapter 14

- Migrations are source-controlled descriptions of schema changes.
- Install the `dotnet-ef` global tool once.
- `dotnet ef migrations add <name>` creates a new migration.
- `dotnet ef database update` applies pending migrations.
- Seed via `HasData` (in `OnModelCreating`) or custom code in `Program.cs`.
- Never edit applied migrations. Always create new ones.

In Chapter 15, we look at how to load related data — how to navigate from a `TodoItem` to its `Category` and back, and the three loading patterns EF Core supports.

---

## Part III · Chapter 15 — Relationships: One-to-Many, Many-to-Many, and Eager Loading

### What you will learn in this chapter
The three kinds of relationships EF Core supports (one-to-one, one-to-many, many-to-many), how to define them, the difference between eager loading, explicit loading, and lazy loading, how to choose between them for performance, and how to configure cascading deletes.

### 15.1 The one-to-many we already have

Our `Category` ↔ `TodoItem` relationship is one-to-many: one `Category` has many `TodoItem`s. We defined it like this:

```csharp
public class Category
{
    public int Id { get; set; }
    public string Name { get; set; } = string.Empty;
    public List<TodoItem> Todos { get; set; } = new();
}

public class TodoItem
{
    public int Id { get; set; }
    public string Title { get; set; } = string.Empty;
    public int? CategoryId { get; set; }
    public Category? Category { get; set; }
}
```

The configuration in `OnModelCreating`:

```csharp
entity.HasOne(t => t.Category)
      .WithMany(c => c.Todos)
      .HasForeignKey(t => t.CategoryId)
      .OnDelete(DeleteBehavior.SetNull);
```

This is the canonical pattern: a foreign key property (`CategoryId`) and a navigation property (`Category`) on the dependent side, a collection navigation property (`Todos`) on the principal side.

### 15.2 Loading related data

When you query `var items = await _db.TodoItems.ToListAsync();`, you get the `TodoItem` rows but the `Category` navigation is **not** populated — it is `null`. To get the category data, you have three options.

#### Option 1: Eager loading with `Include`

```csharp
var items = await _db.TodoItems
    .Include(t => t.Category)
    .ToListAsync();
```

`Include` tells EF Core to join the `Categories` table and populate the `Category` navigation. The generated SQL is a LEFT JOIN, so tasks without a category still come back, with `Category = null`.

You can include multiple:

```csharp
var items = await _db.TodoItems
    .Include(t => t.Category)
    .Include(t => t.Owner)
    .ToListAsync();
```

And nest:

```csharp
var items = await _db.TodoItems
    .Include(t => t.Category)
        .ThenInclude(c => c.Todos)
    .ToListAsync();
```

Eager loading is the most common and the safest. You know exactly what data you are loading.

#### Option 2: Explicit loading

```csharp
var item = await _db.TodoItems.FindAsync(id);
await _db.Entry(item).Reference(t => t.Category).LoadAsync();
```

Explicit loading is when you load the principal entity first, then explicitly tell EF Core to load a navigation. Useful when you only sometimes need the related data and want to save a query when you don't.

#### Option 3: Lazy loading

Lazy loading loads navigation properties on demand — the moment you access `item.Category`, EF Core issues a query.

To enable it:

```bash
dotnet add package Microsoft.EntityFrameworkCore.Proxies --version 8.0.*
```

```csharp
builder.Services.AddDbContext<AppDbContext>(options =>
    options.UseSqlite(connStr)
           .UseLazyLoadingProxies());
```

And your navigation properties must be `virtual`:

```csharp
public class TodoItem
{
    // ...
    public virtual Category? Category { get; set; }
}
```

**Lazy loading is convenient but dangerous.** It can produce the **N+1 problem**: you query 100 tasks, then loop through and access `.Category` on each one, generating 100 extra SQL queries. Always prefer eager loading with `Include` unless you have a specific reason.

### 15.3 One-to-one

A one-to-one relationship is configured like a one-to-many, but with a unique foreign key and a reference (not a collection) on both sides.

Example: each `TodoItem` has one `Reminder`:

```csharp
public class Reminder
{
    public int Id { get; set; }
    public DateTime RemindAt { get; set; }
    public int TodoItemId { get; set; }
    public TodoItem? TodoItem { get; set; }
}

public class TodoItem
{
    // ...
    public Reminder? Reminder { get; set; }
}

// In OnModelCreating:
modelBuilder.Entity<TodoItem>()
    .HasOne(t => t.Reminder)
    .WithOne(r => r.TodoItem!)
    .HasForeignKey<Reminder>(r => r.TodoItemId);
```

The `HasForeignKey<Reminder>` says the FK lives on `Reminder`, not on `TodoItem`. This is how EF Core knows which side is the dependent.

### 15.4 Many-to-many

In EF Core 5+, many-to-many is configured automatically when you have collections on both sides:

```csharp
public class TodoItem
{
    // ...
    public List<Tag> Tags { get; set; } = new();
}

public class Tag
{
    public int Id { get; set; }
    public string Name { get; set; } = string.Empty;
    public List<TodoItem> Todos { get; set; } = new();
}
```

EF Core creates a join table `TagTodoItem` automatically. You never see the join table in your code; you just add tags to a task and save.

If you want to add extra columns to the join table (e.g. a `CreatedAt` on the link), define the join entity explicitly:

```csharp
public class TodoTag
{
    public int TodoItemId { get; set; }
    public TodoItem TodoItem { get; set; } = null!;

    public int TagId { get; set; }
    public Tag Tag { get; set; } = null!;

    public DateTime AssignedAt { get; set; } = DateTime.UtcNow;
}

modelBuilder.Entity<TodoTag>()
    .HasKey(tt => new { tt.TodoItemId, tt.TagId });

modelBuilder.Entity<TodoTag>()
    .HasOne(tt => tt.TodoItem)
    .WithMany(t => t.Tags)
    .HasForeignKey(tt => tt.TodoItemId);

modelBuilder.Entity<TodoTag>()
    .HasOne(tt => tt.Tag)
    .WithMany(t => t.Todos)
    .HasForeignKey(tt => tt.TagId);
```

### 15.5 Cascading deletes

When a `Category` is deleted, what happens to its `TodoItem`s? EF Core's cascade behaviors:

- `DeleteBehavior.Cascade` — dependent entities are also deleted. Default for required relationships.
- `DeleteBehavior.SetNull` — dependent FK is set to NULL. Requires nullable FK. We used this for `CategoryId`.
- `DeleteBehavior.Restrict` — the delete is blocked. You must delete the children first.
- `DeleteBehavior.NoAction` — like `Restrict` but at the database level (no FK constraint enforcement at the EF layer).
- `DeleteBehavior.ClientSetNull` — EF Core sets the FK to null in memory; the database might still have a constraint.

Choose `SetNull` for soft relationships (deleting a category should not delete tasks). Choose `Cascade` for ownership (deleting an order should delete its items).

### 15.6 Eager loading and the N+1 problem

The classic pitfall:

```csharp
var items = await _db.TodoItems.ToListAsync(); // 1 query
foreach (var item in items)
{
    Console.WriteLine($"{item.Title} - {item.Category?.Name}");
}
// If lazy loading is enabled, this generates N+1 queries:
// 1 query for the items, plus 1 per item to fetch the Category.
```

The fix is `Include`:

```csharp
var items = await _db.TodoItems.Include(t => t.Category).ToListAsync();
// 1 query with a JOIN. Much faster for large lists.
```

Always use `Include` when you know you'll need the related data.

### 15.7 Try it yourself

1. Add a `Tag` entity and the many-to-many with `TodoItem`.
2. Create a migration for it.
3. Modify the `TodoController.Index` to use `Include(t => t.Category)` and `Include(t => t.Tags)`.
4. In the view, render the tags as small badges.

### 15.8 Common mistakes

- **Forgetting `Include`**: a view that needs `item.Category.Name` blows up with a null reference because `Category` was not loaded.
- **Lazy loading with N+1**: easy to miss in dev with a few rows; painful in prod with thousands. Use eager loading as the default.
- **Cascade delete surprising you**: deleting a `Category` deletes all its `TodoItems` because the default behavior for required relationships is `Cascade`. If `CategoryId` is `int?` (nullable), the default is `SetNull`, which is what we want.

### Summary of Chapter 15

- Relationships are defined by FK + navigation on the dependent, collection on the principal.
- Three loading patterns: eager (`Include`), explicit (`Entry().Reference().Load()`), lazy (with proxies).
- Eager is the safest default; lazy is dangerous because of N+1.
- One-to-one uses `HasOne().WithOne().HasForeignKey<T>()`.
- Many-to-many in EF Core 5+ is automatic; for extra columns, define the join entity explicitly.
- Choose cascade behavior per relationship: `SetNull` for soft, `Cascade` for ownership.

In Chapter 16, we wrap our data access in a repository pattern and inject it into controllers.

---

## Part III · Chapter 16 — The Repository Pattern and Dependency Injection

### What you will learn in this chapter
The repository pattern — what it is, why people use it, and why some people argue against it with EF Core. We will implement a simple generic `IRepository<T>` for TaskManager, register it in DI, and use it in a controller. By the end you can decide for yourself whether you need repositories in your project.

### 16.1 The pattern, in plain terms

A **repository** is an abstraction over data access. Instead of writing:

```csharp
public async Task<IActionResult> Index()
{
    var items = await _db.TodoItems.ToListAsync();
    return View(items);
}
```

you write:

```csharp
public async Task<IActionResult> Index()
{
    var items = await _repo.GetAllAsync();
    return View(items);
}
```

The controller no longer knows about EF Core, `DbContext`, or `DbSet<T>`. It only knows about `IRepository<TodoItem>`.

The promise:
- **Testability**: you can mock the repository in unit tests; the controller is tested without a database.
- **Swap-ability**: you can replace the EF Core implementation with a MongoDB or REST-backed implementation without touching the controller.
- **Encapsulation**: complex queries live in the repository, not scattered across controllers.

### 16.2 The case against

Critics argue:
- EF Core's `DbSet<T>` **is** a repository. `DbContext` **is** a unit of work. Wrapping them adds a layer with no benefit.
- Real projects rarely swap the database, so the "swap-ability" argument is theoretical.
- The repository hides EF Core features (e.g. `Include`, `AsNoTracking`, raw SQL) behind an abstraction, leading to leaky interfaces or extra methods.

Both sides have a point. The pragmatic choice:

- For small apps, use `DbContext` directly.
- For larger apps where you want testable controllers and a single place to put query logic, use repositories, but keep them thin. Do not try to recreate EF Core's API; just expose the operations you actually use.

We will use the repository pattern in TaskManager because it teaches DI and unit testing, both of which are valuable skills. You can decide for yourself in real projects.

### 16.3 A generic repository interface

Create `Repositories/IRepository.cs`:

```csharp
using System.Linq.Expressions;
using TaskManager.Models;

namespace TaskManager.Repositories
{
    public interface IRepository<T> where T : class
    {
        Task<IEnumerable<T>> GetAllAsync();
        Task<IEnumerable<T>> FindAsync(Expression<Func<T, bool>> predicate);
        Task<T?> GetByIdAsync(int id);
        Task AddAsync(T entity);
        void Update(T entity);
        void Remove(T entity);
        Task<int> SaveChangesAsync();
    }
}
```

This is a generic interface — `T` is any entity type. The methods are CRUD basics. The `Expression<Func<T, bool>>` parameter on `FindAsync` lets callers pass a lambda like `t => t.IsCompleted == false`.

### 16.4 The implementation

Create `Repositories/Repository.cs`:

```csharp
using System.Linq.Expressions;
using Microsoft.EntityFrameworkCore;
using TaskManager.Data;
using TaskManager.Models;

namespace TaskManager.Repositories
{
    public class Repository<T> : IRepository<T> where T : class
    {
        protected readonly AppDbContext _db;
        protected readonly DbSet<T> _set;

        public Repository(AppDbContext db)
        {
            _db = db;
            _set = db.Set<T>();
        }

        public async Task<IEnumerable<T>> GetAllAsync() => await _set.ToListAsync();

        public async Task<IEnumerable<T>> FindAsync(Expression<Func<T, bool>> predicate)
            => await _set.Where(predicate).ToListAsync();

        public async Task<T?> GetByIdAsync(int id) => await _set.FindAsync(id);

        public async Task AddAsync(T entity) => await _set.AddAsync(entity);

        public void Update(T entity) => _set.Update(entity);

        public void Remove(T entity) => _set.Remove(entity);

        public async Task<int> SaveChangesAsync() => await _db.SaveChangesAsync();
    }
}
```

Line by line:
- `where T : class` — `T` must be a reference type (a class). This is required because `DbSet<T>` only works with classes.
- `protected readonly AppDbContext _db;` — the context. `protected` so derived classes (e.g. `TodoItemRepository`) can access it for special queries.
- `_set = db.Set<T>();` — gets the `DbSet<T>` for the entity type.
- `await _set.FindAsync(id)` — looks in the change tracker first, then queries the database. Fast for repeated lookups of the same key.
- `await _set.AddAsync(entity)` — adds the entity to the change tracker (does not save yet).
- `_set.Update(entity)` — marks the entity as modified.
- `_set.Remove(entity)` — marks for deletion.
- `await _db.SaveChangesAsync()` — actually writes the changes to the database.

### 16.5 Specialized repository for `TodoItem`

The generic repository is fine for basic CRUD. For queries specific to `TodoItem`, create a specialized interface:

```csharp
public interface ITodoItemRepository : IRepository<TodoItem>
{
    Task<IEnumerable<TodoItem>> GetRecentAsync(int count);
    Task<IEnumerable<TodoItem>> GetWithCategoryAsync();
    Task<IEnumerable<TodoItem>> GetOverdueAsync();
}
```

Implementation:

```csharp
public class TodoItemRepository : Repository<TodoItem>, ITodoItemRepository
{
    public TodoItemRepository(AppDbContext db) : base(db) { }

    public async Task<IEnumerable<TodoItem>> GetRecentAsync(int count) =>
        await _set.OrderByDescending(t => t.CreatedAt).Take(count).ToListAsync();

    public async Task<IEnumerable<TodoItem>> GetWithCategoryAsync() =>
        await _set.Include(t => t.Category).ToListAsync();

    public async Task<IEnumerable<TodoItem>> GetOverdueAsync() =>
        await _set.Where(t => t.DueAt.HasValue && t.DueAt.Value < DateTime.UtcNow && !t.IsCompleted)
                  .ToListAsync();
}
```

### 16.6 Registering in DI

In `Program.cs`:

```csharp
builder.Services.AddScoped<IRepository<Category>, Repository<Category>>();
builder.Services.AddScoped<ITodoItemRepository, TodoItemRepository>();
```

The DI container now knows: when a controller asks for `ITodoItemRepository`, give it a `TodoItemRepository` instance, scoped to the current request.

### 16.7 Using it in a controller

```csharp
public class TodoController : Controller
{
    private readonly ITodoItemRepository _todos;
    private readonly IRepository<Category> _categories;

    public TodoController(ITodoItemRepository todos, IRepository<Category> categories)
    {
        _todos = todos;
        _categories = categories;
    }

    public async Task<IActionResult> Index()
    {
        var items = await _todos.GetWithCategoryAsync();
        return View(items);
    }

    public async Task<IActionResult> Details(int id)
    {
        var item = await _todos.GetByIdAsync(id);
        if (item is null) return NotFound();
        return View(item);
    }
}
```

The controller depends on abstractions, not on `AppDbContext`. In a unit test, we can inject a mock repository.

### 16.8 Try it yourself

1. Create the `Repositories/` folder and the `IRepository<T>` interface.
2. Implement the generic `Repository<T>`.
3. Create `ITodoItemRepository` and `TodoItemRepository` with the specialized methods.
4. Register both in `Program.cs`.
5. Rewrite `TodoController` to use `ITodoItemRepository` instead of `AppDbContext`.

### 16.9 Common mistakes

- **Using `AddScoped` instead of `AddTransient` or vice versa**: for repositories that wrap a scoped `DbContext`, the repository must be scoped too. Mixing lifetimes throws "scope validation" errors at startup.
- **Forgetting to register the repository**: DI throws "no service for type ITodoItemRepository".
- **Calling `SaveChangesAsync` too eagerly**: each call is a database round-trip. Group related changes and save once.

### Summary of Chapter 16

- The repository pattern abstracts data access behind an interface.
- A generic `IRepository<T>` plus specialized repositories is a common structure.
- Register repositories in DI; inject them into controllers.
- Decide for yourself whether to use it — both choices are defensible.
- We will use it in TaskManager to keep controllers testable (Chapter 27).

In Chapter 17, we start building the user-facing UI — the forms that capture user input.

---

## Part IV · Chapter 17 — Forms: Capturing User Input the Right Way

### What you will learn in this chapter
How to build forms in Razor views using tag helpers, how the model binder reconstructs your object on POST, how to handle file uploads, how to use the anti-forgery token, and how to render validation errors. By the end you can build a create/edit form for any entity in your app.

### 17.1 The anatomy of a form

A typical create form in ASP.NET Core MVC looks like this:

```cshtml
@model TaskManager.ViewModels.TodoCreateViewModel

<form asp-controller="Todo" asp-action="Create" method="post" class="form">
    @Html.AntiForgeryToken()

    <div class="mb-3">
        <label asp-for="Title" class="form-label"></label>
        <input asp-for="Title" class="form-control" />
        <span asp-validation-for="Title" class="text-danger"></span>
    </div>

    <div class="mb-3">
        <label asp-for="Description" class="form-label"></label>
        <textarea asp-for="Description" class="form-control" rows="4"></textarea>
        <span asp-validation-for="Description" class="text-danger"></span>
    </div>

    <div class="mb-3">
        <label asp-for="DueAt" class="form-label"></label>
        <input asp-for="DueAt" class="form-control" type="date" />
        <span asp-validation-for="DueAt" class="text-danger"></span>
    </div>

    <div class="mb-3">
        <label asp-for="Priority" class="form-label"></label>
        <input asp-for="Priority" class="form-control" type="number" min="1" max="5" />
        <span asp-validation-for="Priority" class="text-danger"></span>
    </div>

    <div class="mb-3">
        <label asp-for="CategoryId" class="form-label"></label>
        <select asp-for="CategoryId" asp-items="Model.AvailableCategories" class="form-control">
            <option value="">— None —</option>
        </select>
    </div>

    <button type="submit" class="btn btn-primary">Save</button>
</form>
```

Line by line:

- `@model TaskManager.ViewModels.TodoCreateViewModel` — the view's model type.
- `<form asp-controller="Todo" asp-action="Create" method="post">` — the form will POST to `/Todo/Create`. The tag helper reads the route and produces the correct `action` attribute.
- `@Html.AntiForgeryToken()` — emits a hidden `<input>` containing an anti-CSRF token. The `[ValidateAntiForgeryToken]` attribute on the action (Chapter 20) verifies it on POST.
- `<label asp-for="Title" class="form-label">` — generates a `<label for="Title">Title</label>`. The label text comes from `[Display(Name = "...")]` on the property (or the property name itself).
- `<input asp-for="Title" class="form-control" />` — generates an `<input>` with `id="Title" name="Title" value="..."` (the current value of `Model.Title`). When data annotations have validation rules, validation attributes like `data-val-required` are added for client-side validation.
- `<span asp-validation-for="Title" class="text-danger"></span>` — a placeholder where the validation error message for `Title` will be inserted.
- `<textarea asp-for="Description">` — a textarea that binds to `Description`.
- `<input asp-for="DueAt" type="date">` — the `[DataType(DataType.Date)]` would already produce `type="date"`; specifying it explicitly does no harm.
- `<select asp-for="CategoryId" asp-items="Model.AvailableCategories">` — a dropdown. `asp-items` is the list of `<option>`s to render, as `IEnumerable<SelectListItem>`.
- `<option value="">— None —</option>` — a placeholder option for "no category". Without it, the select would default to the first option.
- `<button type="submit">Save</button>` — the submit button.

When the user fills in this form and clicks Save, the browser POSTs to `/Todo/Create` with a body like:

```
Title=Buy+milk&Description=2L+of+whole+milk&DueAt=2025-10-15&Priority=3&CategoryId=2&__RequestVerificationToken=xxxxx
```

### 17.2 The POST handler

```csharp
[HttpPost]
[ValidateAntiForgeryToken]
public async Task<IActionResult> Create(TodoCreateViewModel vm)
{
    if (!ModelState.IsValid)
    {
        vm.AvailableCategories = await GetCategoryListAsync();
        return View(vm);
    }

    var item = new TodoItem
    {
        Title = vm.Title,
        Description = vm.Description,
        DueAt = vm.DueAt,
        Priority = vm.Priority,
        CategoryId = vm.CategoryId,
        CreatedAt = DateTime.UtcNow
    };

    await _todos.AddAsync(item);
    await _todos.SaveChangesAsync();

    return RedirectToAction(nameof(Index));
}
```

Line by line:
- `[ValidateAntiForgeryToken]` — verifies the anti-forgery token in the POST matches. Without it, an attacker could craft a malicious form that submits to this URL and trick the user into clicking it.
- `if (!ModelState.IsValid)` — checks the validation rules. If any rule fails, `ModelState` has errors and `IsValid` is false.
- `vm.AvailableCategories = await GetCategoryListAsync();` — repopulate the dropdown before returning the view, since the view needs it.
- `return View(vm);` — return the same view with the same model. The validation errors in `ModelState` are rendered by the `<span asp-validation-for>` helpers.
- Otherwise, build the entity, save it, redirect to Index. This is the **Post/Redirect/Get pattern** — after a successful POST, redirect so that the user cannot accidentally re-submit by refreshing.

### 17.3 The edit form

The edit form is nearly identical to the create form, but with an `Id` hidden field:

```cshtml
@model TaskManager.ViewModels.TodoEditViewModel

<form asp-action="Edit" method="post">
    <input asp-for="Id" type="hidden" />
    <!-- same fields as Create -->
</form>
```

The controller:

```csharp
[HttpGet]
public async Task<IActionResult> Edit(int id)
{
    var item = await _todos.GetByIdAsync(id);
    if (item is null) return NotFound();

    var vm = new TodoEditViewModel
    {
        Id = item.Id,
        Title = item.Title,
        Description = item.Description,
        DueAt = item.DueAt,
        Priority = item.Priority,
        CategoryId = item.CategoryId,
        AvailableCategories = await GetCategoryListAsync()
    };

    return View(vm);
}

[HttpPost]
[ValidateAntiForgeryToken]
public async Task<IActionResult> Edit(int id, TodoEditViewModel vm)
{
    if (id != vm.Id) return BadRequest();
    if (!ModelState.IsValid)
    {
        vm.AvailableCategories = await GetCategoryListAsync();
        return View(vm);
    }

    var item = await _todos.GetByIdAsync(id);
    if (item is null) return NotFound();

    item.Title = vm.Title;
    item.Description = vm.Description;
    item.DueAt = vm.DueAt;
    item.Priority = vm.Priority;
    item.CategoryId = vm.CategoryId;

    _todos.Update(item);
    await _todos.SaveChangesAsync();

    return RedirectToAction(nameof(Index));
}
```

Note the **manual mapping from view model to entity** — we load the entity from the database, set only the fields the form is allowed to change, then save. We never call `_todos.Update(vm)` directly. This protects against over-posting (Chapter 20): even if an attacker adds `IsCompleted=true` to the POST body, our code never reads that field.

### 17.4 File uploads

For a form that uploads a file, set `enctype="multipart/form-data"` and use `IFormFile` in the view model:

```cshtml
<form asp-action="Upload" method="post" enctype="multipart/form-data">
    <input asp-for="Attachment" type="file" />
    <button type="submit">Upload</button>
</form>
```

```csharp
public class UploadViewModel
{
    [Required]
    [Display(Name = "Attachment")]
    public IFormFile? Attachment { get; set; }
}

[HttpPost]
[ValidateAntiForgeryToken]
public async Task<IActionResult> Upload(UploadViewModel vm)
{
    if (vm.Attachment is null || vm.Attachment.Length == 0)
    {
        ModelState.AddModelError(nameof(vm.Attachment), "Please select a file.");
        return View(vm);
    }

    if (vm.Attachment.Length > 5 * 1024 * 1024)
    {
        ModelState.AddModelError(nameof(vm.Attachment), "Max 5 MB.");
        return View(vm);
    }

    var fileName = Path.GetFileName(vm.Attachment.FileName);
    var savePath = Path.Combine(_env.ContentRootPath, "Uploads", fileName);
    await using var stream = System.IO.File.Create(savePath);
    await vm.Attachment.CopyToAsync(stream);

    return RedirectToAction(nameof(Index));
}
```

The `_env` here is `IWebHostEnvironment`, injected via the constructor.

### 17.5 Try it yourself

1. Create the `TodoCreateViewModel` from Chapter 11 with `AvailableCategories`.
2. Implement the GET and POST `Create` actions in `TodoController`.
3. Build the `Views/Todo/Create.cshtml` form.
4. Submit it with valid and invalid data; observe validation errors.
5. Add an `Upload` action and view to accept a file.

### 17.6 Common mistakes

- **Forgetting `enctype="multipart/form-data"` on a file upload form**: `IFormFile` will be null.
- **Forgetting to repopulate dropdown lists when validation fails**: the re-rendered form has no options.
- **Forgetting `ValidateAntiForgeryToken`**: opens the form to CSRF attacks.
- **`return View()` instead of `RedirectToAction`**: breaks the PRG pattern; refreshing the page re-submits the form.

### Summary of Chapter 17

- Use tag helpers: `<form asp-controller asp-action>`, `<input asp-for>`, `<label asp-for>`, `<select asp-for asp-items>`, `<span asp-validation-for>`.
- Add `@Html.AntiForgeryToken()` to the form and `[ValidateAntiForgeryToken]` to the action.
- On POST validation failure, repopulate dropdown lists before returning the view.
- On POST success, redirect (PRG pattern).
- File uploads use `IFormFile` and `enctype="multipart/form-data"`.

In Chapter 18, we look at validation in depth — server-side, client-side, and custom.

---

## Part IV · Chapter 18 — Validation: Server-Side, Client-Side, and Custom

### What you will learn in this chapter
How server-side validation works (data annotations + `ModelState`), how to write a custom validation attribute, how to use `IValidatableObject` for cross-field rules, how to enable and customize client-side validation, and what to do when server and client validation disagree. By the end you can validate any user input with confidence.

### 18.1 Server-side validation

When a POST arrives, the model binder fills the action's parameters, then runs validation by inspecting the data annotations on the type. Each rule that fails adds a key/message to `ModelState`. After binding, `ModelState.IsValid` is `true` if no errors, `false` otherwise.

```csharp
[HttpPost]
public IActionResult Create(TodoCreateViewModel vm)
{
    if (!ModelState.IsValid)
    {
        // ModelState has errors; the view will render them via <span asp-validation-for>
        return View(vm);
    }
    // ...
}
```

You can add errors manually:

```csharp
ModelState.AddModelError(nameof(vm.DueAt), "Due date is on a weekend.");
```

The key matches the field name; the message is what gets displayed next to that field. Use `string.Empty` for a model-level error shown in the summary, not on a specific field.

### 18.2 Custom validation attribute

For a reusable rule:

```csharp
public class NotInPastAttribute : ValidationAttribute
{
    public override bool IsValid(object? value)
    {
        if (value is null) return true; // use [Required] for null check
        if (value is DateTime dt) return dt >= DateTime.Today;
        return false;
    }
}
```

Use:

```csharp
[NotInPast(ErrorMessage = "Due date cannot be in the past.")]
public DateTime? DueAt { get; set; }
```

### 18.3 Cross-field validation with `IValidatableObject`

```csharp
public class TodoEditViewModel : IValidatableObject
{
    public int Id { get; set; }
    public string Title { get; set; } = string.Empty;
    public DateTime? DueAt { get; set; }
    public bool IsCompleted { get; set; }

    public IEnumerable<ValidationResult> Validate(ValidationContext ctx)
    {
        if (IsCompleted && DueAt is null)
            yield return new ValidationResult("Completed tasks must have a due date.",
                new[] { nameof(DueAt) });
    }
}
```

The framework calls `Validate` after running attribute-based rules, and adds any `ValidationResult`s to `ModelState`.

### 18.4 Client-side validation

ASP.NET Core ships with **unobtrusive jQuery validation**. It is wired up by `_ValidationScriptsPartial.cshtml`, which the template includes in `_Layout`. The script file is `jquery.validate.unobtrusive.min.js`.

When you use `asp-for` on an input with a data annotation, the tag helper emits `data-val-*` attributes that the unobtrusive validation library reads:

```html
<input type="text" id="Title" name="Title"
       data-val="true"
       data-val-required="Title is required."
       data-val-length="Title must be 3–200 characters."
       data-val-length-min="3"
       data-val-length-max="200"
       data-val-length-max="200" />
```

The library reads these and runs the same rules in the browser, showing the error messages next to the inputs before the form is submitted. The server still validates, because attackers can bypass client-side validation.

### 18.5 Custom client-side validation

For custom rules, you write a small JavaScript function or use the `IClientModelValidator` interface (advanced; we won't cover it here). Most of the time, the server-side annotation is enough, and the user just sees the error after a server round-trip. That is fine.

### 18.6 The validation summary

```cshtml
@Html.ValidationSummary(false, "", new { @class = "text-danger" })
```

Or with tag helpers:

```cshtml
<div asp-validation-summary="All" class="text-danger"></div>
```

Modes:
- `All` — show all errors.
- `ModelOnly` — show only model-level errors (added with empty key).
- `None` — show nothing (still emits the container).

Place the summary at the top of the form to give the user a quick overview of what went wrong.

### 18.7 Try it yourself

1. Add the `NotInPast` attribute to `DueAt` on `TodoCreateViewModel`.
2. Submit the create form with a date in the past; you should see the error.
3. Implement `IValidatableObject` on `TodoEditViewModel` to require `DueAt` when `IsCompleted` is true.
4. Test client-side validation by disabling JavaScript in your browser; the form should still validate server-side.

### 18.8 Common mistakes

- **Relying only on client-side validation**: never. Server-side is the source of truth.
- **Forgetting to repopulate dropdowns on validation failure**: empty dropdowns confuse users.
- **Adding errors with the wrong key**: `ModelState.AddModelError("Title", "bad")` attaches the error to the Title field; `AddModelError("", "bad")` is a model-level error.

### Summary of Chapter 18

- Server-side validation uses data annotations and `ModelState`.
- Custom validation attributes inherit `ValidationAttribute`.
- `IValidatableObject` is for cross-field rules.
- Client-side validation is jQuery-based, automatic via `asp-for` tag helpers.
- The server is the source of truth; client-side is just UX.

In Chapter 19, we add user accounts with ASP.NET Core Identity.

---

## Part IV · Chapter 19 — Authentication and Authorization with ASP.NET Core Identity

### What you will learn in this chapter
What Identity is, how to install it, how to wire up the database, how to add registration and login pages, how to require authentication on a controller or action, how to use roles for authorization, and how to extend the user class with custom properties.

### 19.1 What is ASP.NET Core Identity?

**ASP.NET Core Identity** is the built-in membership system. It provides:
- User registration with email/password.
- Password hashing (PBKDF2 by default).
- Login, logout, profile management.
- Lockout (after N failed attempts, the account is locked for a period).
- Two-factor authentication (TOTP, SMS, email).
- External login (Google, Facebook, Microsoft Account, etc.).
- Role-based and claim-based authorization.
- Token providers (email confirmation, password reset).

Identity uses a `DbContext` (`IdentityDbContext<TUser>`) and several tables (`AspNetUsers`, `AspNetRoles`, `AspNetUserRoles`, `AspNetUserClaims`, `AspNetUserLogins`, etc.). You can either use Identity's own context or merge it into your `AppDbContext`.

### 19.2 Installing Identity

Add the package:

```bash
dotnet add package Microsoft.AspNetCore.Identity.EntityFrameworkCore --version 8.0.*
```

Or, simpler approach: scaffold Identity into your project. The scaffolder adds the views, controllers, and configuration:

```bash
dotnet add package Microsoft.VisualStudio.Web.CodeGeneration.Design --version 8.0.*
dotnet add package Microsoft.EntityFrameworkCore.Design --version 8.0.*
dotnet tool install --global dotnet-aspnet-codegenerator
```

Then scaffold the Identity files you need:

```bash
dotnet aspnet-codegenerator identity --useDefaultUI --files "Account.Register;Account.Login;Account.Logout"
```

But for teaching, let us wire Identity up manually.

### 19.3 Extending `AppDbContext`

Modify `AppDbContext` to inherit from `IdentityDbContext<ApplicationUser>` instead of `DbContext`:

```csharp
public class ApplicationUser : IdentityUser
{
    public string? DisplayName { get; set; }
}

public class AppDbContext : IdentityDbContext<ApplicationUser>
{
    public AppDbContext(DbContextOptions<AppDbContext> options) : base(options) { }

    public DbSet<TodoItem> TodoItems => Set<TodoItem>();
    public DbSet<Category> Categories => Set<Category>();

    protected override void OnModelCreating(ModelBuilder modelBuilder)
    {
        base.OnModelCreating(modelBuilder); // MUST be called for Identity tables
        // ... your existing configuration
    }
}
```

### 19.4 Registering Identity services

In `Program.cs`:

```csharp
builder.Services.AddIdentity<ApplicationUser, IdentityRole>(options =>
{
    options.Password.RequiredLength = 8;
    options.Password.RequireDigit = true;
    options.Password.RequireUppercase = false;
    options.Lockout.MaxFailedAccessAttempts = 5;
    options.Lockout.DefaultLockoutTimeSpan = TimeSpan.FromMinutes(15);
    options.User.RequireUniqueEmail = true;
    options.SignIn.RequireConfirmedEmail = false;
})
.AddEntityFrameworkStores<AppDbContext>();

builder.Services.ConfigureApplicationCookie(options =>
{
    options.LoginPath = "/Account/Login";
    options.LogoutPath = "/Account/Logout";
    options.AccessDeniedPath = "/Account/AccessDenied";
    options.ExpireTimeSpan = TimeSpan.FromDays(7);
    options.SlidingExpiration = true;
});
```

The options configure password policy, lockout, user uniqueness, and the cookie that identifies the logged-in user.

### 19.5 Adding the middleware

In `Program.cs` pipeline, before `UseAuthorization`:

```csharp
app.UseAuthentication();
app.UseAuthorization();
```

`UseAuthentication` reads the cookie (or other auth scheme), validates it, and sets `HttpContext.User`. `UseAuthorization` then checks `[Authorize]` attributes.

### 19.6 Creating a migration

```bash
dotnet ef migrations add AddIdentity
dotnet ef database update
```

The migration creates the Identity tables alongside your `Categories` and `TodoItems`.

### 19.7 A simple `AccountController`

```csharp
public class AccountController : Controller
{
    private readonly UserManager<ApplicationUser> _userManager;
    private readonly SignInManager<ApplicationUser> _signInManager;

    public AccountController(UserManager<ApplicationUser> userManager,
                             SignInManager<ApplicationUser> signInManager)
    {
        _userManager = userManager;
        _signInManager = signInManager;
    }

    [HttpGet]
    public IActionResult Register() => View();

    [HttpPost]
    [ValidateAntiForgeryToken]
    public async Task<IActionResult> Register(RegisterViewModel vm)
    {
        if (!ModelState.IsValid) return View(vm);

        var user = new ApplicationUser { UserName = vm.Email, Email = vm.Email, DisplayName = vm.DisplayName };
        var result = await _userManager.CreateAsync(user, vm.Password);

        if (!result.Succeeded)
        {
            foreach (var error in result.Errors)
                ModelState.AddModelError("", error.Description);
            return View(vm);
        }

        await _signInManager.SignInAsync(user, isPersistent: false);
        return RedirectToAction("Index", "Home");
    }

    [HttpGet]
    public IActionResult Login() => View();

    [HttpPost]
    [ValidateAntiForgeryToken]
    public async Task<IActionResult> Login(LoginViewModel vm)
    {
        if (!ModelState.IsValid) return View(vm);

        var result = await _signInManager.PasswordSignInAsync(vm.Email, vm.Password, vm.RememberMe, lockoutOnFailure: true);
        if (!result.Succeeded)
        {
            ModelState.AddModelError("", "Invalid login attempt.");
            return View(vm);
        }
        return RedirectToAction("Index", "Home");
    }

    [HttpPost]
    [ValidateAntiForgeryToken]
    public async Task<IActionResult> Logout()
    {
        await _signInManager.SignOutAsync();
        return RedirectToAction("Index", "Home");
    }
}
```

### 19.8 Authorization

Add `[Authorize]` to require login:

```csharp
[Authorize]
public class TodoController : Controller
{
    // All actions require authentication.
}

[Authorize(Roles = "Admin")]
public class AdminController : Controller
{
    // Only users in the "Admin" role.
}

[AllowAnonymous]
public IActionResult About() { /* anyone can access */ }
```

You can also authorize via policy (more flexible):

```csharp
builder.Services.AddAuthorization(options =>
{
    options.AddPolicy("CanDelete", policy => policy.RequireRole("Admin"));
});

[Authorize(Policy = "CanDelete")]
public IActionResult Delete(int id) { ... }
```

### 19.9 Getting the current user in a controller

```csharp
public class TodoController : Controller
{
    public async Task<IActionResult> Index()
    {
        var userId = User.FindFirstValue(ClaimTypes.NameIdentifier)!;
        var items = await _todos.FindAsync(t => t.OwnerId == userId);
        return View(items);
    }
}
```

`User` is a `ClaimsPrincipal` set by the authentication middleware. `ClaimTypes.NameIdentifier` is the user ID claim.

### 19.10 Try it yourself

1. Add Identity to TaskManager.
2. Create the `AccountController` with Register, Login, Logout.
3. Add `[Authorize]` to `TodoController`.
4. Add a `_LoginPartial.cshtml` that shows the user's email and a Logout button when logged in, or Register/Login links when not.

### 19.11 Common mistakes

- **Forgetting `app.UseAuthentication()` before `app.UseAuthorization()`**: `[Authorize]` always fails because `User` is anonymous.
- **Calling `base.OnModelCreating()` after your own config**: Identity tables do not get created. Always call `base.OnModelCreating()` first.
- **Re-using the same `DbContext` for two different `IdentityDbContext` types**: throws at startup.

### Summary of Chapter 19

- Identity is the built-in user-management system.
- Extend `IdentityUser` to add custom fields; inherit `AppDbContext` from `IdentityDbContext<T>`.
- `AddIdentity<TUser, TRole>().AddEntityFrameworkStores<TContext>()` registers everything.
- Add `UseAuthentication()` before `UseAuthorization()`.
- Use `[Authorize]` to require login; `[Authorize(Roles = "Admin")]` for roles; `[Authorize(Policy = "...")]` for custom policies.
- `User` (a `ClaimsPrincipal`) gives access to the current user.

In Chapter 20, we cover the rest of the security essentials — CSRF, XSS, SQL injection, over-posting.

---

## Part IV · Chapter 20 — Security Essentials: CSRF, XSS, SQL Injection, and Over-Posting

### What you will learn in this chapter
The four most common web app vulnerabilities and how ASP.NET Core MVC defends against each. By the end you can answer the interview question "How would you secure an MVC app?" with concrete framework features.

### 20.1 CSRF — Cross-Site Request Forgery

**What it is.** An attacker tricks a logged-in user into submitting a malicious form. The form points to your app's `/Todo/Delete/5`. Since the user's browser automatically attaches the auth cookie, your app thinks the user clicked the delete button and executes the delete.

**The defense.** Anti-forgery tokens. The server emits a random token in the form, and the server stores a matching token in a cookie. On POST, the server checks both match. An attacker cannot forge both because they cannot read your domain's cookie.

In Razor:

```cshtml
<form asp-action="Delete">
    @Html.AntiForgeryToken()
    <button type="submit">Delete</button>
</form>
```

In the controller:

```csharp
[HttpPost]
[ValidateAntiForgeryToken]
public IActionResult Delete(int id) { ... }
```

The `[ValidateAntiForgeryToken]` attribute checks the form token matches the cookie. With tag helpers, the `@Html.AntiForgeryToken()` is emitted automatically when you use `<form asp-action>` and `method="post"`.

For AJAX POSTs, you must add the token manually:

```cshtml
@inject Microsoft.AspNetCore.Antiforgery.IAntiforgery Xsrf
@{
    var token = Xsrf.GetAndStoreTokens(Context).RequestToken;
}

<script>
    fetch('@Url.Action("Delete")', {
        method: 'POST',
        headers: { 'RequestVerificationToken': '@token' },
        body: new URLSearchParams({ id: 5 })
    });
</script>
```

### 20.2 XSS — Cross-Site Scripting

**What it is.** A user enters `<script>...</script>` in a field. You save it. You render it back to them (or to other users) without escaping. The browser sees the `<script>` and runs it, leaking cookies or doing actions on behalf of the victim.

**The defense.** Razor escapes by default. `@Model.Title` produces HTML-encoded text — `<script>` becomes `&lt;script&gt;`. The browser sees text, not tags.

The only way to inject raw HTML is `@Html.Raw(...)`:

```cshtml
@Html.Raw(Model.UserProvidedHtml)   // DANGEROUS if not sanitized
```

Never call `@Html.Raw` on user-provided content. If you must render rich text from users, sanitize it first (use a library like HtmlSanitizer).

### 20.3 SQL injection

**What it is.** You concatenate user input into a SQL string:

```csharp
string sql = $"SELECT * FROM TodoItems WHERE Title = '{title}'";
```

A user submits `'; DROP TABLE TodoItems;--`. The SQL becomes:

```sql
SELECT * FROM TodoItems WHERE Title = ''; DROP TABLE TodoItems;--'
```

Game over.

**The defense.** EF Core parameterizes every query by default. The following is safe:

```csharp
var items = await _db.TodoItems.Where(t => t.Title == title).ToListAsync();
```

The `title` becomes a parameter in the generated SQL, not a concatenated value.

If you ever need raw SQL, use `FromSqlInterpolated`:

```csharp
var items = await _db.TodoItems.FromSqlInterpolated($"SELECT * FROM TodoItems WHERE Title = {title}").ToListAsync();
```

The `$"..."` is a **FormattableString**, and EF Core converts the interpolated values into parameters. Never use `FromSqlRaw` with string concatenation.

### 20.4 Over-posting (mass assignment)

**What it is.** Your action binds to the entity directly:

```csharp
[HttpPost]
public IActionResult Create(TodoItem item) { ... }
```

A malicious user adds extra fields to the POST: `IsAdmin=true`, `OwnerId=someoneElse`, `CreatedAt=2000-01-01`. The model binder happily fills them. You save. Now `TodoItem.IsAdmin` is true even though your form never had that field.

**The defense.** Bind to a view model that has only the fields the form is allowed to set. Map explicitly from view model to entity:

```csharp
[HttpPost]
public IActionResult Create(TodoCreateViewModel vm)
{
    var item = new TodoItem
    {
        Title = vm.Title,
        Description = vm.Description,
        // never set IsCompleted, OwnerId, CreatedAt from the form
    };
    _db.TodoItems.Add(item);
    _db.SaveChanges();
    return RedirectToAction(nameof(Index));
}
```

If you must bind directly to an entity for some reason, use `[Bind]` to whitelist fields:

```csharp
public IActionResult Create([Bind("Title,Description,DueAt")] TodoItem item) { ... }
```

But this is more error-prone than a view model.

### 20.5 Open redirect

**What it is.** Your action redirects to a URL passed as a query parameter:

```csharp
public IActionResult Login(string returnUrl)
{
    return Redirect(returnUrl);  // DANGEROUS
}
```

An attacker emails a link like `https://yoursite.com/Account/Login?returnUrl=https://evil.com/`. The user logs in, and is redirected to the attacker's site. The attacker can now phish further.

**The defense.** Validate `returnUrl` is local:

```csharp
public IActionResult Login(string? returnUrl)
{
    if (!Url.IsLocalUrl(returnUrl))
        returnUrl = "/";

    return Redirect(returnUrl);
}
```

### 20.6 Security headers

Add headers via middleware:

```csharp
app.Use(async (context, next) =>
{
    context.Response.Headers["X-Frame-Options"] = "DENY";
    context.Response.Headers["X-Content-Type-Options"] = "nosniff";
    context.Response.Headers["Referrer-Policy"] = "strict-origin-when-cross-origin";
    context.Response.Headers["Content-Security-Policy"] = "default-src 'self'";
    await next();
});
```

These headers tell the browser to refuse iframes, refuse to "sniff" content types, limit referrer info, and only load resources from your own domain. Strong defense against XSS, clickjacking, and content injection.

### 20.7 HTTPS, HSTS, secrets

We already enabled `UseHttpsRedirection` and `UseHsts` in `Program.cs`. For secrets (connection strings, API keys), use the **user secrets** tool in development:

```bash
dotnet user-secrets init
dotnet user-secrets set "ConnectionStrings:DefaultConnection" "your-secret-conn-str"
```

In production, use environment variables or Azure Key Vault.

### 20.8 Summary

| Threat | Defense |
|--------|---------|
| CSRF | Anti-forgery token in form, `[ValidateAntiForgeryToken]` on action |
| XSS | Razor auto-encodes; never `@Html.Raw` user input |
| SQL injection | EF Core parameterizes; use `FromSqlInterpolated` for raw SQL |
| Over-posting | Use view models; map manually to entities |
| Open redirect | `Url.IsLocalUrl(returnUrl)` before redirect |
| Various headers | Middleware to add `X-Frame-Options`, `X-Content-Type-Options`, CSP |
| Secrets in dev | `dotnet user-secrets` |
| Secrets in prod | Env vars, Azure Key Vault |

In Chapter 21, we look at filters — a clean way to add cross-cutting behavior like logging, authorization, or caching.

---

## Part IV · Chapter 21 — Filters: Cross-Cutting Concerns the Clean Way

### What you will learn in this chapter
What filters are, the five kinds of filters (authorization, resource, action, exception, result), the built-in attributes, how to write a custom filter, and how to apply it globally, per controller, or per action. By the end you can add behaviors like "log every action call" or "wrap responses in a standard envelope" without repeating the code in each action.

### 21.1 What is a filter?

A **filter** is a piece of code that runs at a specific stage of the request pipeline, allowing you to add behavior to many actions without modifying each action. Filters are the clean way to handle **cross-cutting concerns**: logging, validation, caching, error handling, authorization.

The filter pipeline has five stages, in this order:

1. **Authorization filters** — run first, decide whether the request is allowed. If they short-circuit (return a 401/403), no further pipeline runs. Example: `[Authorize]`.
2. **Resource filters** — run before and after model binding. Good for caching (if the cache has the response, return it without running the action). Example: `[ResponseCache]`.
3. **Action filters** — run immediately before and after the action method. They can inspect and modify the action's arguments and return value.
4. **Exception filters** — run when an unhandled exception is thrown by an action or another filter. Use for converting exceptions to friendly responses. Example: `[ExceptionHandler]`.
5. **Result filters** — run before and after the action result executes (e.g., before the view is rendered). Use for modifying the response. Example: `[FormatResponse]`.

### 21.2 The built-in filter attributes

You have already seen several:

- `[Authorize]`, `[AllowAnonymous]` — authorization filters.
- `[ResponseCache(Duration = 60)]` — resource filter for output caching.
- `[ValidateAntiForgeryToken]` — adds anti-forgery check, an IActionFilter.
- `[RequireHttps]` — enforces HTTPS, an IAuthorizationFilter.
- `[Route]`, `[HttpGet]`, etc. — these are not filters but action selectors; they do not run as pipeline stages.

### 21.3 A custom action filter

Let us write a filter that logs every action call.

```csharp
public class LogActionFilter : IActionFilter
{
    private readonly ILogger<LogActionFilter> _logger;

    public LogActionFilter(ILogger<LogActionFilter> logger)
    {
        _logger = logger;
    }

    public void OnActionExecuting(ActionExecutingContext context)
    {
        var action = $"{context.RouteData.Values["controller"]}.{context.RouteData.Values["action"]}";
        _logger.LogInformation("Starting {Action}", action);
    }

    public void OnActionExecuted(ActionExecutedContext context)
    {
        var action = $"{context.RouteData.Values["controller"]}.{context.RouteData.Values["action"]}";
        _logger.LogInformation("Finished {Action}", action);
    }
}
```

`OnActionExecuting` runs **before** the action. `OnActionExecuted` runs **after** the action. The `context` object lets you read route data, arguments, the result, and even short-circuit by setting `context.Result`.

Register it globally in `Program.cs`:

```csharp
builder.Services.AddControllersWithViews(options =>
{
    options.Filters.Add<LogActionFilter>();
});
```

Now every action call is logged.

### 21.4 An async action filter

```csharp
public class LogActionFilterAsync : IAsyncActionFilter
{
    private readonly ILogger<LogActionFilterAsync> _logger;

    public LogActionFilterAsync(ILogger<LogActionFilterAsync> logger) => _logger = logger;

    public async Task OnActionExecutionAsync(ActionExecutingContext context, ActionExecutionDelegate next)
    {
        var action = $"{context.RouteData.Values["controller"]}.{context.RouteData.Values["action"]}";
        _logger.LogInformation("Starting {Action}", action);

        await next();  // calls the action and any subsequent filters

        _logger.LogInformation("Finished {Action}", action);
    }
}
```

`next` is a delegate that runs the rest of the pipeline. Always call `await next();` — if you forget, the action does not run.

### 21.5 A custom exception filter

```csharp
public class AppExceptionFilter : IExceptionFilter
{
    private readonly ILogger<AppExceptionFilter> _logger;

    public AppExceptionFilter(ILogger<AppExceptionFilter> logger) => _logger = logger;

    public void OnException(ExceptionContext context)
    {
        _logger.LogError(context.Exception, "Unhandled exception in {Action}",
            context.RouteData.Values["action"]);

        if (context.HttpContext.Request.IsAjaxRequest())
        {
            context.Result = new ObjectResult(new { error = "An error occurred." }) { StatusCode = 500 };
        }
        else
        {
            context.Result = new RedirectToActionResult("Error", "Home", null);
        }

        context.ExceptionHandled = true;  // mark as handled so it does not propagate
    }
}
```

### 21.6 Filter scopes

A filter can be applied at three scopes:

1. **Globally** — registered in `Program.cs` as above. Runs for every action.
2. **Per controller** — decorated on the controller class:

```csharp
[LogActionFilter]
public class TodoController : Controller { ... }
```

Wait — to apply a filter as an attribute, it must inherit from `Attribute` and the appropriate filter interface. The common way is to inherit from `ActionFilterAttribute`:

```csharp
public class LogActionAttribute : ActionFilterAttribute
{
    public override void OnActionExecuting(ActionExecutingContext context)
    {
        Console.WriteLine($"Before {context.ActionDescriptor.DisplayName}");
    }

    public override void OnActionExecuted(ActionExecutedContext context)
    {
        Console.WriteLine($"After {context.ActionDescriptor.DisplayName}");
    }
}

[LogAction]
public class TodoController : Controller { ... }
```

3. **Per action** — same attribute on a single method:

```csharp
[LogAction]
public IActionResult Index() { ... }
```

The order of execution for filters is: **global filters run first, then controller-level, then action-level**.

### 21.7 Try it yourself

1. Write `LogActionFilter` and register it globally.
2. Run the app and watch the console output as you click around.
3. Write a `RequireHttps` style attribute (or use the built-in one) on a controller.
4. Write an exception filter that catches `DbUpdateException` and shows a friendly "Database error" page.

### 21.8 Common mistakes

- **Forgetting to call `await next()` in an async filter**: the pipeline stops.
- **Forgetting to set `context.ExceptionHandled = true` in an exception filter**: the exception propagates.
- **Using DI on an attribute-based filter**: by default, attribute-based filters are singletons and cannot have scoped dependencies. Use `[ServiceFilter(typeof(T))]` or `[TypeFilter(typeof(T))]` to inject scoped services.

### Summary of Chapter 21

- Five filter types: authorization, resource, action, exception, result.
- Built-in attributes like `[Authorize]` and `[ResponseCache]` are filters.
- Custom filters implement `IActionFilter`, `IAsyncActionFilter`, `IExceptionFilter`, etc.
- Register globally or decorate at controller/action level.
- Attribute filters can use `[ServiceFilter(typeof(T))]` for DI.

In Chapter 22, we go deep on async programming in MVC.

---

## Part IV · Chapter 22 — Async Programming in MVC

### What you will learn in this chapter
Why async matters in a web server, how to write async actions, the EF Core async extension methods, how to use cancellation tokens, and the most common async pitfalls. By the end you can make your controllers efficient and avoid the typical mistakes that cause thread pool starvation in production.

### 22.1 Why async matters

A web server has a thread pool — typically 25 to 100 threads. When a request comes in, a thread is taken from the pool to handle it. The thread runs the controller, the controller queries the database, the database takes 200ms to respond, the thread is **blocked waiting**. During those 200ms, the thread is doing nothing — but it cannot be used for another request.

If 50 simultaneous requests all hit a slow database, all 50 threads sit waiting. The 51st request queues up. The user sees latency. The server is not actually doing 50 things at once — it is doing 50 waits at once.

**Async/await** changes this. When a thread awaits an I/O operation, it is **returned to the pool**. The I/O is handled by the OS / network stack. When the I/O completes, a thread is taken from the pool again to resume the method. The thread is only "occupied" while doing CPU work, not while waiting.

The practical effect: a server with 50 threads can handle hundreds of simultaneous requests if most of them are mostly waiting. The thread pool can be much smaller for the same throughput.

### 22.2 Async controller actions

```csharp
public async Task<IActionResult> Index()
{
    var items = await _todos.GetAllAsync();
    return View(items);
}
```

- `async` — marks the method as async. Required to use `await`.
- `Task<IActionResult>` — the return type. `Task` is "work that will produce a value later"; `Task<IActionResult>` is "work that will produce an `IActionResult` later". The framework awaits the task to get the result.
- `await _todos.GetAllAsync();` — `await` suspends the method until the task finishes, then resumes with the result. While suspended, the thread returns to the pool.

### 22.3 EF Core async methods

EF Core provides async equivalents for almost every LINQ method:

| Sync | Async |
|------|-------|
| `ToList()` | `ToListAsync()` |
| `ToArray()` | `ToArrayAsync()` |
| `First()` | `FirstAsync()` |
| `FirstOrDefault()` | `FirstOrDefaultAsync()` |
| `Single()` | `SingleAsync()` |
| `SingleOrDefault()` | `SingleOrDefaultAsync()` |
| `Count()` | `CountAsync()` |
| `LongCount()` | `LongCountAsync()` |
| `Any()` | `AnyAsync()` |
| `All()` | `AllAsync()` |
| `Max`/`Min`/`Sum`/`Average` | `…Async()` versions |
| `Find()` | `FindAsync()` |
| `SaveChanges()` | `SaveChangesAsync()` |

These methods build the LINQ expression (synchronously) and execute it asynchronously against the database.

```csharp
var item = await _db.TodoItems
    .Where(t => t.IsCompleted == false)
    .OrderBy(t => t.DueAt)
    .FirstOrDefaultAsync();
```

`Where` and `OrderBy` are synchronous (they just build the expression). `FirstOrDefaultAsync` is the actual query execution.

### 22.4 Cancellation tokens

For long-running operations, you can pass a `CancellationToken` so the user (or framework) can cancel the request:

```csharp
public async Task<IActionResult> Index(CancellationToken ct)
{
    var items = await _db.TodoItems
        .ToListAsync(ct);
    return View(items);
}
```

The framework automatically passes a token for the request; if the client disconnects or the request times out, the token is cancelled and EF Core stops the query. Pass the token to EF Core methods; it is good practice.

### 22.5 Common pitfalls

**`.Result` and `.Wait()`** — never. These block the calling thread, defeating the purpose of async, and can deadlock in ASP.NET (the request thread waits for itself). Always `await`.

```csharp
// WRONG
var items = _db.TodoItems.ToListAsync().Result;

// RIGHT
var items = await _db.TodoItems.ToListAsync();
```

**`async void`** — never. `async void` is for event handlers only. Use `async Task` everywhere else. `async void` exceptions cannot be caught and crash the process.

**Mixing sync and async** — if your action is async, make every call inside it async. A single sync database call inside an async action blocks the thread.

**`ConfigureAwait(false)`** — in library code, you should use `ConfigureAwait(false)` to avoid capturing the sync context. In ASP.NET Core, there is no sync context (since 1.0), so `ConfigureAwait(false)` is unnecessary in your app code. Use it in libraries you publish, not in your MVC controllers.

### 22.6 Try it yourself

1. Make every action in `TodoController` async with `Task<IActionResult>` and `await`.
2. Pass `CancellationToken ct` to each action and pass it to EF Core calls.
3. Watch the response times with multiple concurrent requests — async scales much better.

### 22.7 Summary of Chapter 22

- Async/await lets the thread return to the pool while waiting for I/O.
- Use `async Task<IActionResult>` for async actions.
- EF Core has async equivalents for every LINQ method.
- Pass `CancellationToken` for cancellable operations.
- Never use `.Result` or `.Wait()`; never `async void`.
- `ConfigureAwait(false)` is unnecessary in ASP.NET Core app code.

In Chapter 23, we add view components — a more powerful alternative to partial views.

---

## Part V · Chapter 23 — View Components: Reusable UI Logic Beyond Partials

### What you will learn in this chapter
What a view component is, when to use one instead of a partial view, how to write and call one, and how to inject services into it. By the end you can extract reusable UI chunks that have their own data-fetching logic, without putting that logic in the parent view.

### 23.1 What is a view component?

A **view component** is a small controller-like class that produces a fragment of HTML. Like a controller, it has methods and is instantiated by the framework per request. Like a partial view, it renders a `.cshtml` file. Unlike a partial, it has its own logic — it does not depend on the parent view's model.

Use a partial when:
- You are reusing a chunk of pure presentation.
- The data needed is already in the parent view's model.

Use a view component when:
- The UI fragment needs its own data that the parent does not have.
- The fragment has logic (filtering, formatting) that does not belong in the parent.
- The fragment appears on every page (like a sidebar) and you do not want to fetch its data in every controller action.

### 23.2 A view component for the category sidebar

In TaskManager, we want a sidebar on every page showing the categories with their task counts. We do not want every controller action to fetch this data. We write a view component.

```csharp
using Microsoft.AspNetCore.Mvc;
using Microsoft.EntityFrameworkCore;
using TaskManager.Data;
using TaskManager.Models;

namespace TaskManager.ViewComponents
{
    public class CategorySidebarViewComponent : ViewComponent
    {
        private readonly AppDbContext _db;

        public CategorySidebarViewComponent(AppDbContext db) => _db = db;

        public async Task<IViewComponentResult> InvokeAsync()
        {
            var categories = await _db.Categories
                .Select(c => new CategoryWithCount
                {
                    Id = c.Id,
                    Name = c.Name,
                    Color = c.Color,
                    Count = c.Todos.Count
                })
                .ToListAsync();

            return View(categories);
        }
    }

    public class CategoryWithCount
    {
        public int Id { get; set; }
        public string Name { get; set; } = "";
        public string? Color { get; set; }
        public int Count { get; set; }
    }
}
```

- `ViewComponent` — the base class.
- `InvokeAsync` — the method the framework calls. The signature can have parameters (`InvokeAsync(int count)`).
- `return View(model)` — renders the default view for this component, at `Views/Shared/Components/CategorySidebar/Default.cshtml`.

### 23.3 The view component's view

Create `Views/Shared/Components/CategorySidebar/Default.cshtml`:

```cshtml
@model IEnumerable<TaskManager.ViewComponents.CategoryWithCount>

<div class="sidebar">
    <h4>Categories</h4>
    <ul class="nav nav-pills flex-column">
        @foreach (var c in Model)
        {
            <li class="nav-item">
                <a asp-controller="Todo" asp-action="Index" asp-route-categoryId="@c.Id" class="nav-link">
                    <span class="badge" style="background-color:@c.Color">@c.Count</span>
                    @c.Name
                </a>
            </li>
        }
    </ul>
</div>
```

### 23.4 Invoking the view component from a layout

In `_Layout.cshtml`:

```cshtml
<aside class="col-md-3">
    @await Component.InvokeAsync("CategorySidebar")
</aside>
```

`Component.InvokeAsync("Name")` instantiates the view component, calls `InvokeAsync`, and renders the result. You can also use the tag helper:

```cshtml
<vc:category-sidebar />
```

The tag helper name is `vc:<kebab-case-name-of-class>`. For `CategorySidebarViewComponent`, the name is `category-sidebar`.

### 23.5 Parametrized view components

```csharp
public async Task<IViewComponentResult> InvokeAsync(int maxCount = 10)
{
    var categories = await _db.Categories
        .Select(c => new CategoryWithCount { ... })
        .Where(c => c.Count < maxCount)
        .ToListAsync();
    return View(categories);
}
```

Invoke with the parameter:

```cshtml
@await Component.InvokeAsync("CategorySidebar", new { maxCount = 5 })
```

### 23.6 Try it yourself

1. Add `CategorySidebarViewComponent`.
2. Add the `Default.cshtml`.
3. Invoke it from `_Layout.cshtml` and observe the sidebar on every page.
4. Add a `RecentTasksViewComponent` that shows the five most recent tasks.

### 23.7 Common mistakes

- **Wrong folder name**: the view must be at `Views/Shared/Components/{NameWithoutSuffix}/Default.cshtml`. For `CategorySidebarViewComponent`, it is `Views/Shared/Components/CategorySidebar/Default.cshtml`.
- **Wrong class name**: the class must end in `ViewComponent` (or be decorated with `[ViewComponent(Name="...")]`).
- **Calling `View()` with no model**: the view receives `null` and breaks.

### Summary of Chapter 23

- View components are mini-controllers that render a fragment of HTML.
- Use them when a fragment needs its own data.
- They live in `ViewComponents/` and have an `InvokeAsync` method.
- Their views live at `Views/Shared/Components/{Name}/Default.cshtml`.
- Invoke with `@await Component.InvokeAsync(...)` or `<vc:name />`.

In Chapter 24, we organize large apps with **areas**.

---

## Part V · Chapter 24 — Areas: Organizing Large Applications

### What you will learn in this chapter
What an area is, how to create one, how areas affect routing, and how to organize controllers and views inside an area. By the end you can split a large app into logical sections (Admin, Customer, Vendor, etc.) without everything living in the root `Controllers` and `Views` folders.

### 24.1 What is an area?

An **area** is a way to group controllers and views into a logical section of the app. The default convention places each area's files under `Areas/{AreaName}/Controllers/` and `Areas/{AreaName}/Views/`. Routes can include an `{area}` segment so URLs like `/Admin/Users/Index` reach an `Admin` area's `UsersController`.

### 24.2 Creating an area manually

Create the folder structure:

```
Areas/
└── Admin/
    └── Controllers/
    └── Views/
```

Add a controller:

```csharp
namespace TaskManager.Areas.Admin.Controllers
{
    [Area("Admin")]
    [Authorize(Roles = "Admin")]
    public class DashboardController : Controller
    {
        public IActionResult Index() => View();
    }
}
```

The `[Area("Admin")]` attribute marks this controller as belonging to the Admin area. The `namespace` should also follow the convention `Project.Areas.{Area}.Controllers` so controller discovery works.

Add the view at `Areas/Admin/Views/Dashboard/Index.cshtml`.

### 24.3 Routing with areas

In `Program.cs`, add an area route **before** the default route:

```csharp
app.MapControllerRoute(
    name: "areas",
    pattern: "{area:exists}/{controller=Home}/{action=Index}/{id?}");

app.MapControllerRoute(
    name: "default",
    pattern: "{controller=Home}/{action=Index}/{id?}");
```

`:exists` is a constraint — it only matches if the area actually exists (i.e. has a controller with `[Area("...")]`). Without it, any first URL segment would be treated as an area.

Now `/Admin/Dashboard/Index` reaches `DashboardController.Index` in the Admin area.

### 24.4 Linking to area actions

```cshtml
<a asp-area="Admin" asp-controller="Dashboard" asp-action="Index">Admin Dashboard</a>
```

The `asp-area` attribute adds the area to the generated URL.

For links from inside an area to a non-area page, set `asp-area=""`:

```cshtml
<a asp-area="" asp-controller="Home" asp-action="Index">Home</a>
```

### 24.5 Scaffolding an area

If you have the aspnet-codegenerator installed:

```bash
dotnet aspnet-codegenerator area Admin
```

This generates the folder structure for you.

### 24.6 Try it yourself

1. Create an `Admin` area.
2. Add a `DashboardController` with an `Index` action.
3. Add the `Index.cshtml` view.
4. Add the area route.
5. Visit `/Admin/Dashboard/Index` and verify it works.

### 24.7 Common mistakes

- **Forgetting the area route**: without it, URLs with an area segment do not match.
- **Wrong namespace**: the controller must be in `Project.Areas.{Area}.Controllers` or area discovery fails.
- **Forgetting `[Area("...")]`**: the controller is treated as a non-area controller.

### Summary of Chapter 24

- Areas group controllers and views into logical sections.
- Controllers in an area use `[Area("Name")]` and live in `Areas/{Name}/Controllers/`.
- Routes use an `{area:exists}` segment.
- Links use `asp-area="..."`.

In Chapter 25, we expose a JSON API alongside our MVC views.

---

## Part V · Chapter 25 — Building REST APIs Alongside MVC

### What you will learn in this chapter
How to add a REST API surface to an existing MVC app, the `[ApiController]` attribute and what it does, how to version an API, and how to generate OpenAPI / Swagger documentation. By the end your app serves both HTML pages for users and JSON endpoints for clients.

### 25.1 Adding an API controller

```csharp
using Microsoft.AspNetCore.Mvc;
using TaskManager.Data;
using TaskManager.Models;

namespace TaskManager.Controllers.Api
{
    [ApiController]
    [Route("api/[controller]")]
    public class TodosController : ControllerBase
    {
        private readonly AppDbContext _db;
        public TodosController(AppDbContext db) => _db = db;

        [HttpGet]
        public async Task<ActionResult<IEnumerable<TodoItem>>> GetAll()
        {
            var items = await _db.TodoItems.Include(t => t.Category).ToListAsync();
            return Ok(items);
        }

        [HttpGet("{id}")]
        public async Task<ActionResult<TodoItem>> GetById(int id)
        {
            var item = await _db.TodoItems.FindAsync(id);
            if (item is null) return NotFound();
            return item;
        }

        [HttpPost]
        public async Task<ActionResult<TodoItem>> Create(TodoItem item)
        {
            _db.TodoItems.Add(item);
            await _db.SaveChangesAsync();
            return CreatedAtAction(nameof(GetById), new { id = item.Id }, item);
        }

        [HttpPut("{id}")]
        public async Task<IActionResult> Update(int id, TodoItem item)
        {
            if (id != item.Id) return BadRequest();
            _db.Entry(item).State = EntityState.Modified;
            try { await _db.SaveChangesAsync(); }
            catch (DbUpdateConcurrencyException) { if (!await _db.TodoItems.AnyAsync(t => t.Id == id)) return NotFound(); throw; }
            return NoContent();
        }

        [HttpDelete("{id}")]
        public async Task<IActionResult> Delete(int id)
        {
            var item = await _db.TodoItems.FindAsync(id);
            if (item is null) return NotFound();
            _db.TodoItems.Remove(item);
            await _db.SaveChangesAsync();
            return NoContent();
        }
    }
}
```

- `[ApiController]` — enables API conventions: automatic model validation (400 if invalid), `[FromBody]` by default for complex parameters, attribute routing required.
- `[Route("api/[controller]")]` — sets a base URL.
- Inherits from `ControllerBase` (no view helpers; saves memory for API-only controllers).
- `ActionResult<T>` — return either an `ActionResult` or a `T` directly. The framework wraps it.
- `CreatedAtAction(nameof(GetById), new { id = item.Id }, item)` — returns 201 with a `Location` header pointing to the new resource. REST conventions.

### 25.2 Calling the API from JavaScript

```html
<button onclick="loadTodos()">Load</button>
<ul id="todo-list"></ul>

<script>
async function loadTodos() {
    const res = await fetch('/api/todos');
    const todos = await res.json();
    document.querySelector('#todo-list').innerHTML =
        todos.map(t => `<li>${t.title}</li>`).join('');
}
</script>
```

### 25.3 Swagger / OpenAPI

Install:

```bash
dotnet add package Swashbuckle.AspNetCore --version 6.*
```

In `Program.cs`:

```csharp
builder.Services.AddEndpointsApiExplorer();
builder.Services.AddSwaggerGen();

// In the pipeline:
if (app.Environment.IsDevelopment())
{
    app.UseSwagger();
    app.UseSwaggerUI();
}
```

Visit `https://localhost:5001/swagger` and you get an interactive API explorer. You can call each endpoint from the browser.

### 25.4 Versioning

For larger APIs, versioning matters. The package `Asp.Versioning.Mvc`:

```bash
dotnet add package Asp.Versioning.Mvc
```

```csharp
builder.Services.AddApiVersioning(opts =>
{
    opts.DefaultApiVersion = new ApiVersion(1, 0);
    opts.AssumeDefaultVersionWhenUnspecified = true;
    opts.ReportApiVersions = true;
});
```

Decorate controllers with `[ApiVersion("1.0")]` and route with `{version:apiVersion}`.

### 25.5 Try it yourself

1. Add the `TodosController` API.
2. Add a "Show as JSON" link on the `Todo/Index` view that calls `/api/todos` and renders the list.
3. Install Swashbuckle and visit `/swagger`.

### 25.6 Common mistakes

- **Inheriting from `Controller` instead of `ControllerBase`**: you get view helpers you don't need; not an error, just wasteful.
- **Forgetting `[ApiController]`**: model validation returns no 400; complex parameters expect form data not JSON.
- **Returning the entity directly to a public API**: serializes the whole entity including potentially sensitive fields. Use a DTO.

### Summary of Chapter 25

- API controllers inherit from `ControllerBase`, are decorated with `[ApiController]`, and use attribute routing.
- `ActionResult<T>` lets you return either an action result or a `T`.
- Swashbuckle generates Swagger / OpenAPI documentation.
- Consider versioning for public APIs.

In Chapter 26, we cover logging, error handling, and observability.

---

## Part V · Chapter 26 — Logging, Error Handling, and Observability

### What you will learn in this chapter
How to use `ILogger<T>` for structured logging, how to configure log levels and providers, how to use the developer exception page, how to write a custom error page, and how to handle errors gracefully in production. By the end you can observe your application in development and diagnose problems in production.

### 26.1 The `ILogger<T>` interface

ASP.NET Core uses **structured logging**. Instead of string interpolation, you pass a message template and the parameters:

```csharp
public class TodoController : Controller
{
    private readonly ILogger<TodoController> _logger;

    public TodoController(ILogger<TodoController> logger) => _logger = logger;

    public IActionResult Details(int id)
    {
        _logger.LogInformation("Looking up todo {Id}", id);
        // ...
    }
}
```

The `{Id}` is a placeholder, not interpolated. The logging framework passes both the template and the parameters, so a structured logging provider (like Serilog or Application Insights) can store `Id` as a separate field you can query. If you interpolate, the template is the final string and you lose the structure.

Log levels:
- `LogTrace` — very detailed, usually off.
- `LogDebug` — useful for debugging, usually off in prod.
- `LogInformation` — normal flow.
- `LogWarning` — something abnormal but handled.
- `LogError` — an error.
- `LogCritical` — a critical failure.

### 26.2 Configuring logging

`appsettings.json`:

```json
{
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft.AspNetCore": "Warning",
      "Microsoft.EntityFrameworkCore": "Warning"
    }
  }
}
```

Each category (typically a namespace or `ILogger<T>` type name) can have its own level. Use `Default` for the catch-all.

### 26.3 Logging providers

The default provider is the **Console** provider (prints to stdout). For production:

- **Debug** provider — prints to the debug output window.
- **EventSource** provider — emits ETW events on Windows.
- **Serilog** (third-party) — file, rolling file, Seq, Elasticsearch, etc.
- **Application Insights** — Azure's full observability platform.

To add Serilog:

```bash
dotnet add package Serilog.AspNetCore
dotnet add package Serilog.Sinks.File
```

```csharp
using Serilog;

Log.Logger = new LoggerConfiguration()
    .MinimumLevel.Information()
    .WriteTo.Console()
    .WriteTo.File("logs/app.log", rollingInterval: RollingInterval.Day)
    .CreateLogger();

builder.Host.UseSerilog();
```

### 26.4 The developer exception page

In `Program.cs`:

```csharp
if (app.Environment.IsDevelopment())
{
    app.UseDeveloperExceptionPage();
}
else
{
    app.UseExceptionHandler("/Home/Error");
    app.UseHsts();
}
```

The developer exception page shows the full stack trace, the source code snippet, request headers, route data, cookies, and more. Invaluable in development, dangerous in production.

### 26.5 A custom error page

The default `/Home/Error` action and view show a generic message. Customize it:

```csharp
public IActionResult Error()
{
    var requestId = Activity.Current?.Id ?? HttpContext.TraceIdentifier;
    return View(new ErrorViewModel { RequestId = requestId });
}
```

```cshtml
@model ErrorViewModel

<h1>Oops!</h1>
<p>Something went wrong. Reference: @Model.RequestId</p>
```

In production, the user sees this friendly message; the actual exception is logged via `UseExceptionHandler` which catches the exception and logs it.

### 26.6 Status code pages

For 404s and other status codes:

```csharp
app.UseStatusCodePagesWithReExecute("/Home/Error", "?code={0}");
```

This re-executes the pipeline at `/Home/Error?code=404` when a 404 happens.

### 26.7 Try it yourself

1. Add a `LogInformation` call to each `TodoController` action.
2. Install Serilog and write to a file.
3. Trigger an exception (throw a `NotImplementedException` from an action) and observe the developer exception page.
4. Switch to Production environment and observe the friendly error page.

### 26.8 Common mistakes

- **String interpolation in log messages**: loses the structured-logging benefit. Always use placeholders.
- **Catching and swallowing exceptions**: log them, then rethrow or convert to a friendly response. Never silently swallow.
- **Logging sensitive data (passwords, tokens)**: don't.

### Summary of Chapter 26

- Use `ILogger<T>` with placeholders for structured logging.
- Configure log levels in `appsettings.json`.
- Use the developer exception page in dev; `UseExceptionHandler` in prod.
- Serilog is a popular third-party provider.
- Never log secrets.

In Chapter 27, we add tests.

---

## Part V · Chapter 27 — Testing MVC Applications

### What you will learn in this chapter
How to set up a unit test project, how to mock repositories and test controllers in isolation, and how to write integration tests with `WebApplicationFactory` that exercises the full pipeline. By the end you have a small test suite for TaskManager.

### 27.1 A unit test project

In the solution root (above the TaskManager folder):

```bash
dotnet new xunit -o TaskManager.Tests
cd TaskManager.Tests
dotnet add reference ../TaskManager/TaskManager.csproj
dotnet add package Moq
dotnet add package Microsoft.AspNetCore.Mvc
```

This creates an xUnit project, references your main project, and installs Moq (a mocking library) and the MVC package (for `Controller` types).

### 27.2 A controller unit test

```csharp
public class TodoControllerTests
{
    private readonly Mock<ITodoItemRepository> _todos = new();
    private readonly Mock<IRepository<Category>> _categories = new();
    private readonly TodoController _controller;

    public TodoControllerTests()
    {
        _controller = new TodoController(_todos.Object, _categories.Object);
    }

    [Fact]
    public async Task Index_ReturnsViewWithItems()
    {
        var data = new List<TodoItem>
        {
            new() { Id = 1, Title = "A" },
            new() { Id = 2, Title = "B" }
        };
        _todos.Setup(r => r.GetWithCategoryAsync()).ReturnsAsync(data);

        var result = await _controller.Index();

        var view = Assert.IsType<ViewResult>(result);
        var model = Assert.IsAssignableFrom<IEnumerable<TodoItem>>(view.Model);
        Assert.Equal(2, model.Count());
    }

    [Fact]
    public async Task Details_ReturnsNotFound_WhenMissing()
    {
        _todos.Setup(r => r.GetByIdAsync(99)).ReturnsAsync((TodoItem?)null);

        var result = await _controller.Details(99);

        Assert.IsType<NotFoundResult>(result);
    }
}
```

- `Mock<ITodoItemRepository>` — Moq creates a fake repository.
- `Setup(...).ReturnsAsync(...)` — when the controller calls `GetWithCategoryAsync()`, the mock returns the data we provided.
- `Assert.IsType<ViewResult>(result)` — the result is a `ViewResult`.
- `view.Model` — the model passed to the view.

Run:

```bash
dotnet test
```

### 27.3 Integration tests with `WebApplicationFactory`

For end-to-end tests:

```bash
dotnet add package Microsoft.AspNetCore.Mvc.Testing
```

```csharp
public class TodoIntegrationTests : IClassFixture<WebApplicationFactory<Program>>
{
    private readonly HttpClient _client;

    public TodoIntegrationTests(WebApplicationFactory<Program> factory)
    {
        _client = factory.WithWebHostBuilder(builder =>
        {
            builder.ConfigureServices(services =>
            {
                // replace AppDbContext with an in-memory database
                services.RemoveAll<DbContextOptions<AppDbContext>>();
                services.AddDbContext<AppDbContext>(o => o.UseInMemoryDatabase("test"));
            });
        }).CreateClient();
    }

    [Fact]
    public async Task Index_ReturnsHtmlWithTasksHeader()
    {
        var response = await _client.GetAsync("/Todo");
        response.EnsureSuccessStatusCode();
        var html = await response.Content.ReadAsStringAsync();
        Assert.Contains("All Tasks", html);
    }
}
```

`WebApplicationFactory<Program>` boots the entire app in-memory. You can override services (like the database) for testing.

### 27.4 Try it yourself

1. Create the test project.
2. Write tests for `TodoController.Index`, `Details`, `Create`, `Edit`, `Delete`.
3. Write one integration test that boots the app and asserts a page contains specific text.

### 27.5 Common mistakes

- **Testing the mock instead of the controller**: only mock what you need to control. The controller is the system under test.
- **Forgetting to seed the in-memory database**: integration tests fail because there's no data.
- **Calling `Assert.Equal(a, b)` with the wrong argument order**: `expected, actual`. Get it backwards and the failure message is misleading.

### Summary of Chapter 27

- Unit tests use Moq to replace the repository.
- xUnit is the most popular test framework for .NET.
- Integration tests use `WebApplicationFactory<Program>` to boot the app in-memory.
- Replace the database with EF Core's InMemory provider for fast, isolated tests.

In Chapter 28, we ship the app to production.

---

## Part V · Chapter 28 — Deployment: From Local to Production

### What you will learn in this chapter
How to publish a release build, what self-contained vs framework-dependent means, how to containerize with Docker, and how to deploy to a Linux server, Azure App Service, or any container host. By the end you can take TaskManager live.

### 28.1 Publish

The `dotnet publish` command compiles the project, copies all dependencies, and produces a folder you can deploy:

```bash
dotnet publish -c Release -o ./publish
```

The output in `./publish` contains:
- `TaskManager.dll` — your compiled code.
- All dependency DLLs.
- `appsettings.json` and `appsettings.Development.json`.
- `wwwroot/` — static files.
- `TaskManager.exe` (Windows) or `TaskManager` (Linux) — a launcher.

To run it:

```bash
cd publish
dotnet TaskManager.dll
```

Or, on Windows, double-click the `.exe`.

### 28.2 Self-contained vs framework-dependent

**Framework-dependent** (default): the deployment assumes the .NET 8 runtime is installed on the target machine. Smaller deployment.

**Self-contained**: the deployment includes the runtime. Bigger, but works on a machine with nothing installed:

```bash
dotnet publish -c Release -r linux-x64 --self-contained -o ./publish
```

`-r linux-x64` is the runtime identifier. Common ones: `win-x64`, `linux-x64`, `linux-musl-x64` (Alpine), `linux-arm64`, `osx-x64`, `osx-arm64`.

### 28.3 Single-file publish

```bash
dotnet publish -c Release -r linux-x64 --self-contained -p:PublishSingleFile=true -o ./publish
```

Produces a single executable with everything bundled. Slower first start (it extracts to a temp folder) but very easy to deploy.

### 28.4 Docker

Create `Dockerfile`:

```dockerfile
FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build
WORKDIR /src
COPY . .
RUN dotnet restore
RUN dotnet publish -c Release -o /app

FROM mcr.microsoft.com/dotnet/aspnet:8.0
WORKDIR /app
COPY --from=build /app .
EXPOSE 80
ENTRYPOINT ["dotnet", "TaskManager.dll"]
```

Build and run:

```bash
docker build -t taskmanager .
docker run -p 8080:80 taskmanager
```

Visit `http://localhost:8080`.

### 28.5 Behind a reverse proxy

In production, Kestrel is usually placed behind Nginx or IIS. The proxy handles TLS termination, rate limiting, and serves static files efficiently. Kestrel listens on `localhost:5000`; the proxy listens on `:80/:443` and forwards to Kestrel.

A minimal Nginx config:

```nginx
server {
    listen 80;
    server_name yourapp.com;
    location / {
        proxy_pass http://localhost:5000;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
    }
}
```

In `Program.cs`, add:

```csharp
app.UseForwardedHeaders(new ForwardedHeadersOptions
{
    ForwardedHeaders = ForwardedHeaders.XForwardedFor | ForwardedHeaders.XForwardedProto
});
```

So the app respects the `X-Forwarded-*` headers from the proxy.

### 28.6 Azure App Service

`dotnet publish` directly to Azure:

```bash
dotnet publish -c Release /p:PublishProfile=Azure -p:Configuration=Release
```

Or use Visual Studio's "Publish" wizard. The deployment uses Azure App Service's Linux container runtime.

### 28.7 Environment-specific configuration

`appsettings.Production.json` overrides `appsettings.json` when `ASPNETCORE_ENVIRONMENT=Production`. Set environment variables in your hosting environment for secrets — do not commit them.

### 28.8 Try it yourself

1. Run `dotnet publish -c Release -o ./publish`.
2. `cd publish` and `dotnet TaskManager.dll`.
3. Visit `http://localhost:5000` and verify it works.
4. Create a `Dockerfile`, build the image, and run it.
5. (Optional) Deploy to a free Azure App Service or a free Linux VPS.

### 28.9 Common mistakes

- **Deploying a debug build**: much slower and bigger. Always `-c Release`.
- **Hard-coding connection strings**: use environment variables or user secrets.
- **Forgetting to migrate the production database**: include a startup migration step (`await db.Database.MigrateAsync();` in `Program.cs`).

### Summary of Chapter 28

- `dotnet publish -c Release` produces a deployment folder.
- Framework-dependent is smaller; self-contained is portable; single-file is convenient.
- Dockerfile: multi-stage build with SDK image for build, runtime image for serving.
- Production almost always uses a reverse proxy (Nginx or IIS) in front of Kestrel.
- Use environment variables for secrets.

In Chapter 29, we look at architectural patterns for large apps.

---

## Part V · Chapter 29 — Best Practices, Design Patterns, and Clean Architecture

### What you will learn in this chapter
The architectural patterns that pay off as an MVC app grows: layered architecture, Clean Architecture, CQRS, the Unit of Work, the Specification pattern, and domain events. We will not refactor TaskManager to use all of these (over-engineering a small app is its own mistake), but you should know them so you can apply the right ones when the time comes.

### 29.1 Layered architecture

The simplest structure beyond "everything in one project" is to split into projects:

```
TaskManager.sln
├── TaskManager.Domain/        (entities, interfaces, no dependencies)
├── TaskManager.Application/  (services, DTOs, business logic; depends on Domain)
├── TaskManager.Infrastructure/ (EF Core, repositories, external APIs; depends on Application and Domain)
└── TaskManager.Web/           (MVC: controllers, views; depends on Application and Infrastructure)
```

The dependency direction is one-way: Web → Application → Domain. Infrastructure implements interfaces defined in Application, plugged in at the Web layer. This is "ports and adapters" (hexagonal) or "onion architecture" in different terminology.

The benefit: you can change the database (Infrastructure) without touching the domain or the application logic. The web layer is thin — it just receives requests, calls application services, and returns views.

### 29.2 Clean Architecture

Robert C. Martin's "Clean Architecture" is the same idea with stricter rules:

- The **domain** (entities) knows nothing.
- The **use cases** (application services) know the domain, nothing else.
- The **interface adapters** (controllers, presenters, gateways) translate between use cases and the outside world.
- The **infrastructure** (web framework, database, UI) is the outermost layer.

The dependency rule: **dependencies point inward**. Outer layers can know about inner layers; inner layers never know about outer layers.

For a small app like TaskManager, this is overkill. For an app with complex business rules and a long lifetime, it pays off.

### 29.3 CQRS (Command Query Responsibility Segregation)

CQRS splits your operations into:
- **Commands** — write operations (create, update, delete). They change state, return minimal data.
- **Queries** — read operations. They return data, change nothing.

You can implement CQRS without event sourcing or two databases — just split your services into `Commands` and `Queries` namespaces. The benefit: read models can be optimized for reads (denormalized, projected); write models can enforce invariants cleanly. The cost: more files, more mental overhead.

A popular library: **MediatR**. Instead of injecting services into controllers, you send a `IRequest<T>` and MediatR routes it to a handler. Decouples caller from callee.

```csharp
public record CreateTodoCommand(string Title, string? Description, int Priority, int? CategoryId)
    : IRequest<int>;

public class CreateTodoHandler : IRequestHandler<CreateTodoCommand, int>
{
    private readonly AppDbContext _db;
    public CreateTodoHandler(AppDbContext db) => _db = db;

    public async Task<int> Handle(CreateTodoCommand cmd, CancellationToken ct)
    {
        var item = new TodoItem
        {
            Title = cmd.Title,
            Description = cmd.Description,
            Priority = cmd.Priority,
            CategoryId = cmd.CategoryId,
            CreatedAt = DateTime.UtcNow
        };
        _db.TodoItems.Add(item);
        await _db.SaveChangesAsync(ct);
        return item.Id;
    }
}

// Controller:
public async Task<IActionResult> Create(CreateTodoCommand cmd)
{
    var id = await _mediator.Send(cmd);
    return RedirectToAction(nameof(Details), new { id });
}
```

### 29.4 Unit of Work

The `DbContext` is itself a Unit of Work: it tracks changes across multiple entities and commits them in one `SaveChanges` call. If you wrap repositories around it, you typically do not need a separate Unit of Work abstraction — but if you have multiple repositories in one controller action and want them to share a transaction, you can:

```csharp
public interface IUnitOfWork
{
    ITodoItemRepository Todos { get; }
    IRepository<Category> Categories { get; }
    Task<int> SaveChangesAsync();
}
```

In EF Core, `SaveChangesAsync` on the `DbContext` is the transaction. Multiple repository calls in one controller action share the same `DbContext` (scoped lifetime) and commit together.

### 29.5 The Specification pattern

For complex query criteria that you want to reuse:

```csharp
public interface ISpecification<T>
{
    Expression<Func<T, bool>> Criteria { get; }
    List<Expression<Func<T, object>>> Includes { get; }
}

public class OverdueTodoSpec : ISpecification<TodoItem>
{
    public Expression<Func<TodoItem, bool>> Criteria =>
        t => t.DueAt.HasValue && t.DueAt.Value < DateTime.UtcNow && !t.IsCompleted;
    public List<Expression<Func<TodoItem, object>>> Includes => new();
}
```

Repos can accept specifications:

```csharp
Task<IEnumerable<T>> FindAsync(ISpecification<T> spec);
```

This is over-engineered for simple cases but valuable when you have many complex query variations.

### 29.6 Domain events

When a `TodoItem` is completed, you want to:
- Send a notification email.
- Update a dashboard cache.
- Log an audit entry.

Putting these directly in the controller or service couples them. Instead, raise a domain event:

```csharp
public class TodoCompletedEvent
{
    public int TodoId { get; set; }
    public string UserId { get; set; }
    public DateTime CompletedAt { get; set; }
}
```

Handlers subscribe:

```csharp
public class SendNotificationOnTodoCompletedHandler : INotificationHandler<TodoCompletedEvent>
{
    public Task Handle(TodoCompletedEvent e, CancellationToken ct)
    {
        // send email, update cache, log, etc.
        return Task.CompletedTask;
    }
}
```

MediatR publishes events; handlers are resolved from DI. Your domain logic stays clean.

### 29.7 Pragmatic recommendations for TaskManager

For a learning app, do not refactor into Clean Architecture. Use:
- **MVC**: controllers and views (Part II).
- **EF Core with repositories** (Part III) — the abstraction is small and teaches DI.
- **Services** for business logic — when an operation is more than "fetch one entity, save it", put it in a service.
- **View models** for views — always.
- **DTOs** for API responses — when the entity has fields the API should not expose.

When the app grows to dozens of controllers and complex rules, consider introducing MediatR (CQRS), separating the Domain into its own project, and applying Clean Architecture. Add complexity only when you feel the pain of not having it.

### 29.8 Try it yourself

1. Identify one place in TaskManager where a service class would help (e.g. "CompleteTaskAsync" — sets `IsCompleted`, raises an event, sends a notification). Extract it.
2. Install MediatR and refactor that operation into a command + handler.
3. Observe how the controller becomes thinner.

### 29.9 Summary of Chapter 29

- Layered architecture: Web → Application → Domain; Infrastructure implements interfaces.
- Clean Architecture: dependencies point inward; UI and DB are details.
- CQRS: split commands and queries; MediatR is the popular library.
- Unit of Work is built into EF Core's `DbContext`.
- Specification pattern for reusable complex queries.
- Domain events decouple side effects.
- Apply complexity only when you feel the pain.

In Chapter 30, we look at the mistakes people make in real MVC projects.

---

## Part V · Chapter 30 — Common Mistakes and How to Avoid Them

### What you will learn in this chapter
A list of the most common mistakes developers make in ASP.NET Core MVC projects, with the diagnosis for each and the fix. Read this chapter once you have worked through the rest of the guide; it will help you spot bad patterns in your own code and in code you inherit from others.

### 30.1 Fat controllers

**Symptom**: a controller action method is 50+ lines, with business logic mixed with database calls and view rendering.

**Diagnosis**: the controller is doing too much. Controllers should be thin — receive a request, call a service, return a result.

**Fix**: extract the body into a service. Inject the service into the controller. The action becomes:

```csharp
[HttpPost]
public async Task<IActionResult> Create(TodoCreateViewModel vm)
{
    if (!ModelState.IsValid) return View(vm);
    await _todoService.CreateAsync(vm);
    return RedirectToAction(nameof(Index));
}
```

### 30.2 Business logic in views

**Symptom**: `.cshtml` files contain `@if` blocks with many branches, calls to services, complex calculations.

**Diagnosis**: the view is doing too much. Views should render data, not compute it.

**Fix**: compute everything in the controller, pass a view model that already has the answer. Use view components for fragments with their own data.

### 30.3 Sync over async (`Task.Result`, `Task.Wait`)

**Symptom**: production deadlocks under load, or much higher CPU than expected.

**Diagnosis**: somewhere `.Result` or `.Wait()` is blocking a thread waiting for a task.

**Fix**: convert to `async`/`await` throughout. Search the codebase for `.Result` and `.Wait()` and replace each.

### 30.4 Not using ViewModels (over-posting vulnerability)

**Symptom**: the controller binds to the entity directly. A malicious POST adds extra fields.

**Fix**: always use view models for forms. Map explicitly to the entity.

### 30.5 Forgetting `Include` (N+1)

**Symptom**: pages load slowly; the SQL log shows many small queries.

**Diagnosis**: navigation properties accessed without eager loading.

**Fix**: add `.Include(t => t.Related)` to the query. Or disable lazy loading entirely.

### 30.6 Calling `.ToList()` before `Where()`

**Symptom**: a query that should filter on the database loads everything into memory first.

**Diagnosis**: the LINQ has a `.ToList()` or `.AsEnumerable()` before a `.Where(...)`, which forces the rest of the query to run in memory.

**Fix**: order the LINQ so the database does the filtering first. The pattern:

```csharp
// WRONG
var items = _db.TodoItems.ToList().Where(t => t.IsCompleted);

// RIGHT
var items = _db.TodoItems.Where(t => t.IsCompleted).ToList();
```

### 30.7 Putting secrets in `appsettings.json`

**Symptom**: a connection string or API key is committed to source control.

**Fix**: use User Secrets in dev, environment variables in production, Azure Key Vault for sensitive values.

### 30.8 Trusting client-side validation

**Symptom**: a malicious POST bypasses the form and submits invalid data.

**Fix**: server-side validation is the source of truth. Client-side is just UX. Always check `ModelState.IsValid`.

### 30.9 Storing `DbContext` in a static or singleton

**Symptom**: weird "DbContext is disposed" errors, or stale data across requests.

**Diagnosis**: `DbContext` is not thread-safe. It must be scoped to a single request.

**Fix**: register as scoped (default with `AddDbContext`). Never inject it into a singleton.

### 30.10 Catching and swallowing exceptions

**Symptom**: errors disappear, but the system behaves wrong.

**Fix**: log the exception, then either rethrow or convert to a friendly response. Never silently swallow.

### 30.11 Mixing concerns in the entity

**Symptom**: `TodoItem` has `[Display(Name=...)]` attributes — UI concerns in the domain entity.

**Fix**: put UI concerns on view models. Keep entities pure.

### 30.12 No logging

**Symptom**: production has a bug; you have no idea what happened.

**Fix**: add `ILogger<T>` to controllers and services. Log every significant operation.

### 30.13 No tests

**Symptom**: every change breaks something else.

**Fix**: at minimum, write integration tests for the critical paths (login, create, edit, delete).

### 30.14 Over-engineering

**Symptom**: a tiny app has repositories, specifications, CQRS handlers, domain events — and the team can't add a field without touching 10 files.

**Fix**: add complexity when the cost of not having it exceeds the cost of having it. Start simple, refactor when needed.

### 30.15 Under-engineering

**Symptom**: a large app has all logic in the controller; every change risks breaking something else.

**Fix**: extract services, write tests, introduce layered architecture.

### 30.16 Forgetting to commit migrations

**Symptom**: the production database has a different schema than the team's dev databases.

**Fix**: always commit migration files to source control. Always run `dotnet ef database update` as part of deployment.

### 30.17 Not using HTTPS

**Symptom**: the site loads over HTTP in production. Login cookies are sent in the clear.

**Fix**: enable `UseHttpsRedirection` and `UseHsts`. Configure a TLS certificate (Let's Encrypt, Azure App Service Managed Certificates).

### 30.18 Not setting the environment

**Symptom**: the production app shows stack traces because `ASPNETCORE_ENVIRONMENT` is unset (defaulting to Production but not configured).

**Fix**: set `ASPNETCORE_ENVIRONMENT=Production` explicitly on the production server.

### 30.19 Summary of Chapter 30

Read through this list once a month. You will recognize mistakes you have made. That recognition is the skill of senior development.

---

## Appendix A — Quick Reference Cheatsheet

### Routing

```
Conventional:        {controller=Home}/{action=Index}/{id?}
Attribute (class):   [Route("api/[controller]")]
Attribute (method):  [HttpGet("{id}"), HttpPost, HttpPut, HttpDelete]
Tokens:              [controller], [action], [area]
Constraints:         :int, :long, :bool, :guid, :datetime, :alpha,
                     :min(n), :max(n), :range(a,b),
                     :length(n), :minlength(n), :maxlength(n),
                     :regex(pattern)
Generate URLs:       @Html.ActionLink, <a asp-controller asp-action asp-route-id>,
                     Url.Action, Url.RouteUrl
```

### Tag Helpers

```
<form asp-controller asp-action>
<input asp-for="Property" />
<label asp-for="Property"></label>
<select asp-for="Property" asp-items="List"></select>
<textarea asp-for="Property"></textarea>
<validation-span asp-validation-for="Property"></validation-span>
<partial name="ViewName" model="..." />
<vc:view-component-name param1="..." />
```

### Data Annotations

```
[Required] [StringLength(n)] [Range(a,b)] [EmailAddress]
[Url] [Phone] [CreditCard] [Compare(nameof(Other))]
[RegularExpression(pattern)]
[DataType(DataType.Date|Time|DateTime|Password|MultilineText|...)]
[Display(Name="...")] [DisplayFormat(...)]
[Key] [Column] [Table] [NotMapped]
```

### ActionResult Types

```
View()                  → renders view
Content("text")        → text/plain
Json(obj)              → application/json
Redirect(url)          → 302
RedirectToAction(...)  → 302 to action
File(bytes, type)      → file download
NotFound()             → 404
BadRequest()           → 400
Unauthorized()         → 401
Forbid()               → 403
StatusCode(418)        → custom
PartialView()         → partial view
```

### EF Core Async Methods

```
ToListAsync, ToArrayAsync
FirstAsync, FirstOrDefaultAsync
SingleAsync, SingleOrDefaultAsync
CountAsync, LongCountAsync
AnyAsync, AllAsync
MaxAsync, MinAsync, SumAsync, AverageAsync
FindAsync, SaveChangesAsync
```

### Filter Types (in execution order)

```
1. Authorization filters    IAuthorizationFilter, [Authorize]
2. Resource filters          IResourceFilter, [ResponseCache]
3. Action filters           IActionFilter, IAsyncActionFilter
4. Exception filters        IExceptionFilter
5. Result filters          IResultFilter
```

### Common CLI Commands

```
dotnet new mvc -o MyProject
dotnet add package <name> --version 8.0.*
dotnet build
dotnet run
dotnet watch run                # hot reload on save
dotnet ef migrations add <Name>
dotnet ef migrations remove    # undo last migration (if not applied)
dotnet ef database update
dotnet ef database drop
dotnet publish -c Release -r linux-x64 --self-contained
dotnet test
dotnet user-secrets init
dotnet user-secrets set "Key" "Value"
dotnet aspnet-codegenerator identity
dotnet aspnet-codegenerator area <Name>
dotnet tool install --global dotnet-ef
dotnet tool install --global dotnet-aspnet-codegenerator
```

### Service Lifetimes

```
AddSingleton<T>     one instance, whole app
AddScoped<T>        one instance per request
AddTransient<T>     new instance every time
```

---

## Appendix B — Additional Resources and Next Steps

### Official documentation

- **Microsoft Learn — ASP.NET Core MVC**: https://learn.microsoft.com/aspnet/core/mvc/overview
- **Entity Framework Core docs**: https://learn.microsoft.com/ef/core/
- **ASP.NET Core API reference**: https://learn.microsoft.com/dotnet/api/
- **C# programming guide**: https://learn.microsoft.com/dotnet/csharp/

### Free learning paths

- **Microsoft Learn — Create web apps with ASP.NET Core**: a free, guided set of modules with sandboxes.
- **.NET YouTube channel**: official videos from the .NET team.
- ** dotnet channel**: live streams, talks at conferences.
- **The .NET Foundation blog**: https://dotnetfoundation.org/

### Books worth reading

- **"Pro ASP.NET Core MVC"** by Adam Freeman — long, thorough, slightly dated but excellent.
- **"Entity Framework Core in Action"** by Jon Smith — the EF Core book.
- **"C# in Depth"** by Jon Skeet — the deep dive on the C# language.
- **"Clean Architecture"** by Robert C. Martin — the architectural ideas in Chapter 29.
- **"Domain-Driven Design"** by Eric Evans — for when your business logic is the actual product.

### Blogs and newsletters

- **Andrew Lock's `asp.netcore` blog**: https://andrewlock.net/ — deep dives into specific features.
- **Khalid Abuhakmeh**: https://khalidabuhakmeh.com/ — practical tips.
- **.NET Weekly**: a weekly newsletter of the best new posts.

### Open-source ASP.NET Core MVC apps to read

- **Orchard Core**: https://github.com/OrchardCMS/OrchardCore — a CMS built on ASP.NET Core MVC + Razor Pages.
- **nopCommerce**: https://github.com/nopSolutions/nopCommerce — an e-commerce platform.
- **Umbraco CMS**: https://github.com/umbraco/Umbraco-CMS — a popular CMS.
- **Orchard Project's reference apps**: various small examples.
- **The ASP.NET Core samples repo**: https://github.com/dotnet/aspnetcore/tree/main/src — the framework itself.

Reading other people's real code is one of the most underrated learning methods. Find a project similar to what you want to build, clone it, run it, and read the code.

### Community

- **Stack Overflow** with the `asp.net-core-mvc` tag.
- **Reddit** `/r/dotnet`.
- **Discord** `DotEvolution`.
- **The .NET Foundation** Discord.

### What to learn next

After this guide, you have a strong foundation in MVC. From here:

1. **Razor Pages** — the page-centric alternative to MVC; smaller learning curve for some apps.
2. **Blazor** — write interactive UI in C# instead of JavaScript. Blazor Server and Blazor WebAssembly.
3. **Minimal APIs** — for small APIs, controllers are overkill. Minimal APIs use a fluent API to declare endpoints.
4. **gRPC** — high-performance RPC for service-to-service communication.
5. **SignalR** — real-time bidirectional communication; great for chat, dashboards, multiplayer.
6. **EF Core advanced topics** — concurrency tokens, raw SQL, complex value types, owned entities, soft delete.
7. **Identity advanced topics** — external logins, two-factor auth, OAuth/OIDC integration.
8. **Cloud native** — Azure App Service, Azure Functions, Azure Container Apps, Kubernetes.
9. **Observability** — OpenTelemetry, distributed tracing, structured logging at scale.
10. **Performance** — benchmarking with BenchmarkDotNet, profiling with dotnet-trace, AOT compilation.

Pick the one that aligns with the next project you want to build. Do not learn all of these at once; learn one, build something with it, then learn the next.

### Final words

ASP.NET Core MVC is a 17-year-old pattern that has been refined into one of the most productive, performant, and well-supported web frameworks in the world. The skills you learned in this guide will be valuable for many years. The patterns transfer to other frameworks: the separation of concerns, the testability, the dependency injection, the explicit request pipeline — every modern web framework has some version of these ideas.

What you build next is up to you. Build something useful, ship it, and find out what you wish you had known. Then come back to this guide and read the relevant chapter again — you will see things in it you did not see the first time.

Good luck.

---

*This guide was written as a comprehensive rewrite of the README for `AzizNader1/Learning_ASP.NET_MVC_From_Zero_To_Hero`. It is designed to be read from start to finish, in order. Every chapter assumes you have read the previous chapters. Every code block is explained line by line. The sample project, TaskManager, is built up across chapters 12–28 and is the practical application of every concept in this guide.*
