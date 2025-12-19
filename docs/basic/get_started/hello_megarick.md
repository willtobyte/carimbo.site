---
sidebar_position: 1
title: Hello, Megarick
---

# Introduction 

This game serves as a "Hello World" example for Carimbo. It runs directly on the browser through [carimbo.games](https://carimbo.games/), you can check the code directly through the [GitHub Repo](https://github.com/willtobyte/megarick). But the explanation is quite simple: 

The engine reads `scripts/main.lua`, wich then starts the Engine in with the defails from Engine Factory, starting the game on the platform you want. 

It then reads from this file, initializes the Engine and reads the `scenes`, from scenemmanager, wich builds the game you see on screen. This scenes reads from `objects` with assets and visual items for what you see on screen.

You can read further documentation on the scene part of this site with deatils on how to write the metddata with `json`, together with a lua script to handle logic and specific situations.