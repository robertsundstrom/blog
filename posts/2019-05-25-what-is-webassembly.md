---
title: What is WebAssembly?
date: 2019-05-25 07:00:00Z
author: Robert Sundström
tags: test
---

![WebAssembly logo](images/wasm_logo.png)

There has been a lot of talk about WebAssembly lately. But what is it really? In this article we will have a look at the technology and the benefits it brings to developers.

## Background

Programming the Web has for long time been limited to using [JavaScript](https://en.wikipedia.org/wiki/JavaScript) - or in the early days using proprietary browser plugins, like [Java](https://en.wikipedia.org/wiki/Java_(programming_language)), [Flash](https://en.wikipedia.org/wiki/Adobe_Flash) or [Silverlight](https://en.wikipedia.org/wiki/Microsoft_Silverlight). Until now, there has been no standard for targeting the web using any other programming language than JavaScript.

Due to its status as the exclusive language of the Web, JavaScript has been widely used as a compilation target for other languages - for CoffeScript and a bunch of other languages. That is why it has been nicknamed the *"Assembly language of the Web"*.

Another early initiative was the [Emscripten](https://emscripten.org/) toolchain project that enabled for C/C++ code to be compiled into JavaScript. Further attempts in trying to improve  performance gave birth to ASM.js, a highly optimized version of JavaScript that layed the foundation for WebAssembly.

## What is WebAssembly?

[WebAssembly](https://en.wikipedia.org/wiki/WebAssembly) (or WASM, for short) is set of open web standards that define a portable binary format for a stack-based execution environment (a Virtual Machine, or VM). It is analogous to the Java Bytecode, or CIL/MSIL of .NET.

The motivation for creating the WASM standard is to enable languages other than JavaScript to target the Web. It therefore serves as a low-level compilation target. Developers would probably not write any WASM directly (it is possible), but rather compile their existing code to this new binary format.

WASM has been designed with JavaScript interop in mind. Currently (at the time of writing), there is no direct way of accessing the browser's Web API:s. So if you want to manipulate the HTML Document Object Model (DOM), or use WebGL, then you have to write some "glue code" in JavaScript.

Also, still being worked on is support for *threading* and *garabage collection* (GC). That is expected to be finalized in the near future.

There is a system interface, called *WASI*, that serves as a interface for the host platform.

All modern web browsers support WebAssembly, but when targeting older browsers, like for example Internet Explorer, then it can be easily polyfilled using ASM.js.

## Targeting WebAssembly

The simplest and most clearest reason for targeting WebAssembly involves some existing C/C++ code that you want to leverage in your web app.

To compile that code you would use Emscripten, which is based upon the LLVM toolchain, using the Clang C/C++ compiler. The project provides a WebAssembly back-end that also will generate some glue code.

There are many other languages and platforms targeting WebAssembly. Rust is one of them that directly targets WebAssembly.

Then there is Mono, the portable .NET runtime, a Virtual Machine, running on top of WebAssembly.

## Use Cases

WebAssembly lets developers leverage existing code on the Web, without having to rewrite any logic in JavaScript and to suffer in performance.

Using WASM as a compilation target, many companies have now been able to port their apps to the web and earned performance gains, compared to when using ASM.js.

Some notable examples are AutoCAD and SketchUp.

You will find an extensive list of use cases [here](https://webassembly.org/docs/use-cases/).


## Will WebAssembly replace JavaScript?

WebAssembly is not a replacement for JavaScript. It enables for other languages to target the Web and expands the capabilities of the Web as a platform.

JavaScript could theoretically target WebAssembly. In fact, there are JavaScript engines running on WebAssembly.

## Not just the Web

In spite of the name, WebAssembly is not tied to the Web, or JavaScript for that matter.

There are a couple of projects in which they are developing standalone WebAssembly runtimes that run outside the browser, similar to how NodeJS run JavaScript outside the browser.

Wasmer, developed by Mozilla, is one of them. There is even a package manager, the Wapm. From there you can download apps like Nginx and JavaScriptCore. (Apple’s JS engine) and immediately run them in Wasmer.

This shows how much investment is going into WebAssembly as a platform.

## What about NodeJS?

Users of NodeJS should not worry. Full Stack JavaScript will not die soon. It will continue to flourish as there is already a lot of investment in the ecosystem.

But we might see a shift in the tooling ecosystem, since NodeJS no longer will be the dominant platform when creating web apps.

WebAssembly will greatly benefit those projects that have a dependency on native addons. Avoidng all the hassle having to target each platform and architecture (Linux, MacOS, Windows etc), the C/C++ code will simply be compiled into WebAssembly instead.

This is already being leveraged by popular NodeJS-based tools, including libsass.

## Conclusion

WebAssembly is a new open and standardized way for other languages to target the Web.

It truly opens up a new world for developers to create new experiences that span across platform, using the technologies that make us truly productive.