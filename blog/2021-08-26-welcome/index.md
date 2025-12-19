---
slug: welcome
title: Carimbo now have a better stack trace and Sentry integration
authors: [skhaz]
tags: [carimbo, stack]
---

[Docusaurus blogging features](https://docusaurus.io/docs/blog) are powered by the [blog plugin](https://docusaurus.io/docs/api/plugins/@docusaurus/plugin-content-blog).

As I’ve already said countless times, I’m working on my first game for Steam, which you can check out online at [reprobate.site](https://reprobate.site/).

Since it’s a paid game, I need to provide proper bug support. With that in mind, and based on both professional and personal experience, I decided to use [Sentry](https://sentry.io/welcome/).

At first, integrating C++ and Lua should have been straightforward, but I ran into some issues when using the Conan package manager.

Initially, the package wasn’t being included in the compiler’s include flags, which led me to open an issue both on [Conan Center](https://conan.io/center) and on [Sentry Native](https://conan.io/center/recipes/sentry-native).

After spending a whole day on this, I eventually found out that the fix was actually pretty simple. Now Carimbo has native support for Sentry, both on the web (WebAssembly) and natively (Android, iOS, Linux, Windows, and macOS).

Here’s how I managed to get it working.


<!-- truncate -->

## CMake & Conan 

