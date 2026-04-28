---
title: Murder Mysteries
summary: A location-based Augmented Reality detective game where users explore the real world, find murder cases through GPS, and investigate digital crime scenes through their smartphone.
year: 2023
technologies: Augmented Reality, Unity, C#, GPS, Location-Based Interaction
order: 12
status: Vertical Slice
cover: /assets/resources/murder-mysteries.png
---

An augmented reality murder mystery game where players explore the real world to find cases, then use their phone as a window into a digital crime scene. By moving around the scene and controlling time, users investigate character movements and solve the mystery.

![AR world overview]({{ '/assets/resources/murder-mysteries.png' | relative_url }})

## The idea

Murder Mysteries explored how augmented reality and GPS could turn detective stories into physical exploration. The concept was inspired by virtual murder mystery games, geocaching, and location-based treasure hunts.

The goal was to create an app where users could walk through the real world, find murder mystery locations on a map, and then spawn a miniature AR crime scene through their smartphone.

Inside the scene, users could move around, rewind or fast-forward time, and follow character movements to figure out what happened.

![World sketch]({{ '/assets/resources/murder-mysteries-sketch.png' | relative_url }})

## Target

The project was aimed at people who enjoy mysteries, investigation games, geocaching, and interactive storytelling.

The experience was designed for users who like solving puzzles by exploring, observing, and piecing together information rather than simply reading clues. It also encouraged movement by placing mysteries in real-world locations.

![Location-based testing]({{ '/assets/resources/murder-mysteries-test.png' | relative_url }})

## The process

The process started with a low-fidelity sketch of the crime scene, followed by a written overview of how each character should move through the fictional world. This helped plan the timeline before building the AR version in Unity.

The high-fidelity prototype was divided into two scenes. One scene handled the GPS map, where the user could follow their location and walk toward red map pins. When the user came close to a pin, a text box appeared and allowed them to investigate the mystery.

The second scene handled the AR crime scene, where users could spawn the world, view a clock, and use a slider to move through time.

The characters’ movements were created with a Path Tool in Unity, using routes and time codes so the user could compare where each character was at different moments.

The prototype was tested with three external users. The test showed that spawning the AR world was easy to understand, and users liked the overall idea. However, they needed clearer feedback about their position on the map, the time display was not understood, and the story needed more focus and polish to make the mystery more engaging.

The main learning was that the technology worked as a proof of concept, but the experience needed stronger narrative design, clearer feedback, and more polish to become a complete AR mystery game.

![Character movement plan]({{ '/assets/resources/murder-mysteries-timeline.png' | relative_url }})