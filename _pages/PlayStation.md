---
title: "PlayStation"
permalink: /PlayStation/
layout: single
author_profile: true
---
## Overview

My time working at Sony Interactive Entertainment (referred to as PlayStation throughout) has been nothing short of phenomenal. I am so proud to have contributed to such an incredible team full of talented, caring, and helpful people. My team's name is **Game Validation & Integration Platform (GVIP)**, responsible for integrating and testing developmental features of the PlayStation for PC (PSPC) SDK within our propietary flagship game.
<img src="/assets/images/CardboardPS5.jpg" alt="Cardboard PS5" style="border-radius: 16px; width: 300px;">

## My Work

My work as a Software Engineer primarily focuses on:
- Feature Integration
- Upgrading Unreal Engine Version
- Debugging Faulty Features
- Code Maintainance

### Feature Integration

I was responsible for integrating a new PSPC feature API into our game's frontend and backend to display retrieved information in the UI. 
- The first challenge of this involved creating new **C++** utility classes and functions for the purpose of compatibility with Unreal Engine's reflection system and therefore accessible in Blueprints and UI widgets.
- I created UI using Unreal Motion Graphics (UMG) ie. Widgets, according to the Figma designs we received from the Design Team. I hooked up the UI buttons to the C++ backend functionality and manually overrode UI navigation to handle both keyboard and gamepad input.
- Once the database was setup with information and images to retrieve, I wrote C++ functionality to convert the received image URLs into Textures to display in the UI. This was tricky because it involved two levels of multi-threading: one to get each set of data, and another to get all images from each set of data, requiring thread locks, *std::atomic*, and edge-case handling to work properly.
- The end result worked like a charm on both PC and PS5, was set up modularly to handle any number of data sets with any (or no) images, and met all stakeholder expectations.

### Upgrading Unreal Engine Version

