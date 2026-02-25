---
layout: post
title: Float Away
date: 2024-03-13
categories: Projects
tags: wfc rts 3D unity
image:
  path: /assets/img/postBg/FA_full.png
---

Working on my thesis gave me the chance to deepen my knowledge on a topic that I find very interesting: 
the creation of content procedurally generated through algorithms. 
At the same time this allowed me to develop the demo of a RTS video game: Float Away.
The goal of the game is to extract resources from a floating island and then move on to the next one; 
in the meanwhile enemy invasions require the player to defend the base by building defences and recruiting new units.

>
-- **Role**: jack of all trades  
-- **Team**: me +  
[Enzo Di Stefano](https://enzodistefano.wordpress.com/) - Music  
-- **Engine**: Unity  
-- **Duration**: 3 months  
-- **Platform**: PC  
>

<!-- markdownlint-capture -->
<!-- markdownlint-disable -->
> [Float Away](https://maydave.itch.io/float-away) itch.io page
{: .prompt-info }
<!-- markdownlint-restore -->

![faGif](/assets/img/gif/faGif.gif)

### Features and stuff that I learned

- Base building
- Grid system
- RTS army controls
- Unit's formation behaviour
- Modular wave generator
- Finite State Machine
- Pathfinding
- Camera and scene management
- Visual and audio settings
- Basic save & load system
- Responsive UI using code
- Vfx: shaders, particles and post effects
- Dynamic music  

### Procedural Level Generation

The [WFC](https://github.com/mxgmn/WaveFunctionCollapse/) algorithm's origins and evolution are discussed in my thesis as well as how I implemented it to generate maps in a deterministic way. 
I utilized the *Tessera* tool which allowed me to use the (open-source) DeBroglie and Sylves C# libraries simultaneously, translating the typical WFC features into Unity.
- *Debroglie* allowed me to define modules with proximity and frequency constraints, both local and global, as well as to perform backtracking in case of failed generation.
- *Sylves* facilitates the creation, customization, and management of grids and graphs of any shape and size.

The generation can go on virtually for ever, provided that we subdivide it into chunks and we carefully design the modules and the constraint that we will be used.

![modules](/assets/img/content/FA_modules.png)
![generator](/assets/img/content/FA_generator.png)

### Progression

I added a rogue-like game mode and progression: after you have gathered all the resources on the current island you can go to the next one, spend your points to unlock and upgrade units, structures and abilities. The map should be graph-shaped and randomly generated (just like in *Slay the Spire* or *Bad North*). This part is far from being completed cause it needs a lot of balancing and playtesting. 

![graphMap](/assets/img/content/FA_graphMap.png){:  .w-75}  
