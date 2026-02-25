---
layout: post
title: "Adaptive and Spatial Sound"
date: 2025-02-12
categories: Prototypes
tags: simulation 3D
image:
  path: /assets/img/postBg/Hut1.png
---

An interactive first-person scene developed for the course "Sound in Interaction," designed to maximize player immersion within a mountain shelter environment. The prototype simulates a tranquil forest setting where the audio reacts dynamically to player actions and in-game parameters. Key interactive sound effects include: variable footsteps on different surfaces, opening/closing a door, radio music inside the hut and chopping wood (minigame). The ambient soundscape adapts to a real-time day-night cycle and changing weather conditions (wind & rain), creating a calm, slow-paced, and deeply atmospheric experience.

![hut](/assets/img/postBg/Hut2.png)

The project was built in **Unity** to handle game logic and player interaction, while the complex, adaptive audio was designed and implemented using the **FMOD** middleware. This separation allowed for powerful, data-driven sound design. To achieve a high level of spatial realism and immersion. **Steam Audio** was later integrated, providing physics-based sound propagation, including real-time occlusion, reverb, and HRTF-based binaural audio.
