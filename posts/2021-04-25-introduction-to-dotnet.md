---
title: "Introduction to .NET"
tags: [dotnet, csharp]
---

.NET is a open-source cross-platform for building web, mobile, desktop , and cloud applications. Currently, it is at version 5 which released in November 2020.

.NET provides a runtime environment (CLR), with programming languages like C#, a base class library, a couple of application frameworks, such as ASP.NET Core. 

The platform supports multiple operating systems (Windows, macOS, and Linux), and on various CPU architectures (x86 and ARM)

First released in 2002, the platform has kept evolving during its 20 years.

And the ecosystem is being developed in the open on GitHub. In fact, the .NET ecosystem was the first that Microsoft really started open-sourcing. Since then it has just increased in scope, and Microsoft has become a leading open-source company.

## The "Old" .NET Framework

The versions up to .NET Framework 4.8 ran exclusively on Windows and is closed-source, but .NET 5 is fully open-source, and run on Windows, macOS, and Linux. 

Not all the frameworks from older Windows-exclusive versions are available in 5 or later. Although, they did port WPF and Windows Forms for Windows in order to let developers migrate their existing apps to the new version of .NET. This has improved performance, and it is supported by component vendors.

## The CLR

.NET consists of a Common Language Runtime(CLR) that consists of an execution engine and a base class library. It supports various operating systems and CPU architectures. 

Code, written in for instance C#, is compiled into portable bytecode (CIL) that, when executed, is being verified, and compiled by the runtime into the type of machine code that is compatible with the CPU that it is currently running on. The process is called Just-in-Time (JIT) compilation.

The other option, Ahead-of-Time compilation lets you compile and bundle everything ahead of time for a specific platform. Event single-file compilations are available.

.NET lets also you bundle all your app with a specific version of the runtime. This allows you to run apps using different runtime versions without having to install the runtimes separately. It also removes the risk of a runtime install affecting another. This is ideal for cloud apps that are being hosted on servers.

## C# programming language

C# (C Sharp) is the preferred programming language. It is  a multiparadigm programming language which is imperative and object-oriented at its core. It is a member of the C language family, and draws a lot of influences from Java in both syntax and semantics. The language also borrows from C++.

Over the years, the language has evolved to integrate elements from other paradigms, like functional programming, with features such as pattern matching.

## Tools

Development starts with the .NET. Command-Line Interface (CLI). The CLI lets you create a new project from a project template, then building your project, and finally publish it. It integrates with the MSBuild engine.

There are many Integrated Development Environments (IDE) to choose from: Visual Studio, Visual Studio for Mac, Visual Studio Code, and JetBrains Rider.

## App Models

.NET stack supports these main scenarios: Web, Mobile Desktop, and Cloud.

You write your code using a language like C#, VB.NET, or F#. These languages are all evolving in the open.

Using those languages you can develop apps for a number of app models that come out-of-box with .NET 5 and later:

Web apps with the ASP.NET Core web framework (including MVC and WeB API). You can build Mobile apps for Windows UWP, iOS, and Android. Cloud apps that integrate with Microsoft Azure services. You can also write Desktop apps for Windows in WinForm or WPF.

The preferred way of defining UIs in UWP and WPF is to do it declaratively using an XML language called XAML - which is to apps what HTML is to the Web. All of the dialects have an evolved templating system and a styling system.

You can also write modern web apps for client-side app using the Blazor framework, running in the browser, targeting WebAssembly. You build UIs in a templating language called Razor, that mixes HTML with C#.

You can write apps that run in Azure, and you can even write apps that run on a Raspberry Pi.

Uno is an open-source project that aims att bringing Microsoft UWP app model to platforms other than Windows, like Android, iOS and macOS. They even support targeting the Web via WebAssembly. Allowing you to write C# and XAML for the Web.

.NET has an ecosystem of libraries and frameworks developed by third-parties, the majority of them are also open-source. They are distributed as NuGet packages through a package manager.

## .NET “Core”

There were some versions of the cross-platform .NET runtime branded “.NET Core “, but they have now been superseded by .NET 5. Using the .NET branding instead.

The initial goal for .NET Core was to build a runtime that was optimized for hosted cloud-scenarios. That later expanded to support more scenarios and app models.

This might be a simplification, but for all intents of purposes pre-Core versions are considered exclusive to Windows.

## So what's up next?

The upcoming release, .NET 6, will integrate support for developing apps for Android, iOS, and macOS - and bring a new framework for building cross-platform apps: .NET Maui (Multi-platform App UI). This is the successor to Xamarin.Forms mobile app framework.

A theme that was planned for .NET 5 was the unification of .NET, which was  delayed because of COVID. The .NET 6 release will finally make the tooling uniform across the stacks and existing app model.

The Mobile (previously Xamarin), and WebAssembly stacks, that use the Mono runtime, will be fully integrated by .NET, when it is released in November 2021.

Microsoft is committed to release a new major version of .NET every year. Every other release will be an LTS release. (Long-Term Support) The next LTS release is .NET 6 that will be released in November 2021.

## Conclusion

As you see, the ecosystem is huge, and evolving. And it is open-source, meaning that you as a developer can contribute to the projects that make up the framework.
