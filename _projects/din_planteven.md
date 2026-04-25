---
title: Din Planteven
summary: Din Planteven is a mobile application design to help the user with keeping their plants alive.
year: 2022
technologies: Unity, C#, Adobe Illustrator, Adobe After Effects
order: 9
cover: /assets/resources/Screenshot%20from%202026-04-25%2014-07-02.png
---

As a part of my master's thesis, I created the BRICKO 2.0 Educational Robotics system. This system shared similarities with LEGO Mindstorms, featuring a controller module that could be expanded with various modules, including sensors and actuators.

The primary aim behind BRICKO 2.0 was to facilitate the seamless integration of Educational Robotics into primary school classes. Additionally, the system was designed to be a sustainable investment by catering to a wider range of users across different age groups.

## Integration into primary school classes

After closely working with local primary schools, teachers, and students, I discovered that despite having LEGO Mindstorms systems provided by the municipality, they were rarely used.

![BRICKO classroom test]({{ '/assets/resources/Screenshot from 2026-04-25 14-04-49.png' | relative_url }})

To overcome these challenges, I created the BRICKO 2.0 system. It is modular with a velcro-based design, requires no additional programs, is OS-independent, and operates directly from any web browser.

<video controls preload="metadata">
  <source src="{{ '/assets/resources/bricko/demo.mp4' | relative_url }}" type="video/mp4">
</video>

## Age-range of users

BRICKO 2.0 catered to a wider age-range of pupils with both tangible and visual block-based programming.

![Programming examples]({{ '/assets/resources/bricko/programming-examples.jpg' | relative_url }})

## LEGO Spike

Two years later, LEGO adopted similar approaches for the Spike system, implementing multi-language support, vertical coding, and introducing new elements for easier construction.

## An overview of the BRICKO 2.0 system

### Modules

The controller supported up to three DC or servomotors and three additional modules, including a buzzer, color, distance, pressure, and rotation sensors.

![Module overview]({{ '/assets/resources/bricko/modules.jpg' | relative_url }})

### GUI

The GUI, accessible via any web browser, featured a drag-and-drop block-based language with support for nested loops, conditionals, and functions.

![GUI screenshot]({{ '/assets/resources/bricko/gui.jpg' | relative_url }})

### Internal Hardware

The controller module's internal hardware was based on an Arduino Yun, extended with custom-made shields stacked on top.

![Hardware stack]({{ '/assets/resources/bricko/hardware.jpg' | relative_url }})

## Usage examples

Alarm systems and train track shifting are simple scenarios demonstrating input-output systems.

<video controls preload="metadata">
  <source src="{{ '/assets/resources/bricko/usage-example.mp4' | relative_url }}" type="video/mp4">
</video>

## User tests

During development, I consistently conducted user tests to assess the response of previous and new users to implemented changes and the system.

![User test]({{ '/assets/resources/bricko/user-test.jpg' | relative_url }})
