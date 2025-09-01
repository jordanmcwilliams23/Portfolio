---
title: "PlayStation"
permalink: /PlayStation/
layout: single
author_profile: true
---
## Overview

My time working at Sony Interactive Entertainment (referred to as PlayStation throughout) has been nothing short of phenomenal. I am so proud to have contributed to such an incredible team full of talented, caring, and helpful people. My team's name is **Game Validation & Integration Platform (GVIP)**, responsible for integrating and testing developmental features of the PlayStation for PC (PSPC) SDK within our propietary flagship game.
{% include figure image_path="/assets/images/CardboardPS5.jpg" alt="Cardboard PS5" %}
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
{% include figure image_path="/assets/images/Astro-books.jpg" alt="Astro-books" %}
### Upgrading Unreal Engine Version

I was placed in charge of upgrading our Unreal Engine version used for development from UE5.4 to UE5.5. Our previous upgrade presented a significant challenge to us and took over 5 months to complete. Similarly, this upgrade also took a significant amount of time but due to the server upgrade also required rather than the engine itself. I completed the engine upgrade itself within a planning cycle by merging our custom engine modifications in to support the PSPC SDK functionality, then fixed any errors that came up while trying to build, and finally successfully packaged for Windows, PS5, and Linux servers.

Uploading the new UE5.5 servers, we realized there was a major incompatibility issue: our current Amazon Linux 2 (AL2) servers didn't meet the requirements needed for UE5.5 Linux servers. There was a major upgrade needed here, both for the GameLiftServerSDK plguin used in our project and the Amazon Linux version by our GameLift Fleets. This was especially hard to debug because Linux crash logs don't provide debugging symbols by default, making the root cause difficult to track down. Through collaboration with the team's Principal Engineer and a plethora of research done on my end, we finally managed to solve all of these crash issues and get the server working on our non-prod (development) environment. However, our production environments faced a timeout issue where a client would always be disconncted from the server after 30 seconds. This stumped us for a while and took a lot of learning about VPC Peering, knowledge about our AWS backend infrastructure, and communications with external partners and support teams to locate the issue. One of the security groups used for our fleet's VPC Peering was at capacity and couldn't accept any new rules. Clearing out old, unused fleets as well as requesting a higher limit for rules cleared up this issue and we were able to fully deploy servers across all environments successfully.

Now that we were unblocked came extensive testing to ensure all game functionality was intact and no new regressions were found. The entire team joined together to prioritize this and we divided & conquered to get all testing done in an efficient manner. We were able to merge in the massive PR after approvals and I helped team members upgrade their local build environments to the latest engine without issue. This was a fantastic learning experience in every way, from learning technical skills like working with AWS to cross-team collaboration skills, I can say with confidence I'm much more prepared for any and all future challenges!