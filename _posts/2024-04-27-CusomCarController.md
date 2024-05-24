---
layout: post
title: "Custom Car Controller"
date: 2024-04-27
categories: Prototypes
tags: vehicle 3D
image:
  path: /assets/img/postBg/Car1.png
---

While I was studying the elastic behavior applied in various contexts to improve the game feel, 
I came across a video that explained the making of a custom raycast-based car physics controller used in a party game named [Very Very Valet](https://www.youtube.com/watch?v=CdPYlj5uZeI). 
Understanding the basics of how such a system works has led me to create two types of car controller cause I wanted to explore the main differences between simulation and arcade driving controls: 
“A simulation is a game with physics that only focuses on, and lets me do things, I could do in reality (within the margin of possibility). 
An arcade racer is the opposite. It focuses and lets me do things I could never do in the real world.”

### Arcade
For the arcade feeling I implemented a **Custom Physics Controller** that simulate a car using a single rigidbody and a raycast-based approach. 
We apply a force to the position of each tire, the vector representing this force has three components (one for each axis): 
suspension, accelleration and steering.

![arcadeCar](/assets/img/gif/CarProto_Custom.gif)

### Simulation
Unity has a **Wheel Collider** that is a collider for grounded vehicles. 
It has buit-in collision detection, wheel physics, and a slip-based tire friction model. 
It can be used for objects other than wheels, but it is specifically designed for vehicles with wheels. 
The steps to make a simulator as close as possible to reality are endless, I just implemented some modular component such as: 
tyres, engine, brakes, transmission, suspension, steering and basic aero dynamics.

![simCar](/assets/img/gif/CarProto_Sim.gif)

### Other stuff that I learned

- AI Steering Behaviour
- Checkpoint System
