---
layout: post
title: Float Away
date: 2024-03-13
categories: Projects
tags: wfc rts 3D
image:
  path: /assets/img/postBg/FA_full.png
---

<!-- markdownlint-capture -->
<!-- markdownlint-disable -->
> Wait for the link
{: .prompt-info }
<!-- markdownlint-restore -->

>
-- **Role**: jack of all trades  
-- **Team**: me +  
Enzo Di Stefano - Music  
-- **Engine**: Unity  
-- **Duration**: 3 months  
-- **Platforms**: PC  
>

### Description

Working on my dissertation give me a the opportunity to deepen a topic that interests me a lot: 
the creation of content procedurally generated through algorithms. 
At the same time this allowed me to develop the demo of a video game: Float Away is a (RTS) real time strategy, 
once you are in, the goal will be to extract resources from a floating island and then move on to the next one; 
in the meanwhile you will have to defend the base from enemy invasions by building defences and recruiting new units.  

### Features and stuff that I learned

- Base Building
- Toggle Grid System
- RTS Army Controls
- Units Formation
- Modular Wave Generator
- Finite State Machine
- Pathfinding
- Camera & Scene Management
- Settings
- Basic save & load system
- Animated UI using code
- Vfx: Shaders, Particles and Post Effects
- Dynamic Music  

### Procedural Level Generation

The [WFC](https://github.com/mxgmn/WaveFunctionCollapse/) algorithm's origins and evolution are discussed in my thesis as well as how I implemented it to generate maps in a deterministic way. 
I utilized the **Tessera** tool, developed by BorisTheBrave, which allows us to use the (open-source) DeBroglie and Sylves C# libraries simultaneously, translating the typical WFC features into Unity.
- **Debroglie** allows us to define our modules with proximity and frequency constraints, both local and global, as well as to perform backtracking in case of failed generation.
- **Sylves** facilitates the creation, customization, and management of grids and graphs of any shape and size.

The generation can go on virtually for ever, provided that we subdivide it into chunks and we carefully design the modules and the constraint that we will be used.

![modules](/assets/img/content/FA_modules.png)
![generator](/assets/img/content/FA_generator.png)
