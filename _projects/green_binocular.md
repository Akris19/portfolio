---
title: The Virtual Binoculars
summary: A Virtual Reality installation concept for Økolariet, where visitors can explore how agriculture and nitrate levels affect rivers, water quality, and surrounding nature.
year: 2023
technologies: Virtual Reality, Unity, C#, Arduino, C/C++, Google Cardboard, 3D Modelling
order: 6
cover: /assets/resources/virtual-binoculars.png
---

A VR installation concept that lets visitors look into a changing water landscape. By interacting with the setup, users can see how farming, nutrients, and nitrate levels affect rivers and local ecosystems.

![Prototype setup]({{ '/assets/resources/virtual-binoculars.png' | relative_url }})

## The idea

The Virtual Binoculars was designed as an interactive VR exhibit for Økolariet. The idea came from an existing installation where visitors could look through binoculars and see a simple 2D animal image. I wanted to expand that concept into an immersive viewpoint over a water landscape.

The goal was to show how a river area can change depending on the amount of nutrients entering the water from agriculture. Through VR, the user could experience a visual transition from a damaged environment with too much nitrate to a healthier, more natural landscape with clearer water and more life.

![Original binocular inspiration]({{ '/assets/resources/okolariet-binoculars.png' | relative_url }})

## Target

The project was aimed at visitors at Økolariet, especially people who learn better through visual and interactive experiences than through text alone.

The experience was designed to make environmental information easier to understand by letting users see the consequences of pollution and nutrient overload directly in a virtual scene.

![User testing setup]({{ '/assets/resources/virtual-binoculars-test.png' | relative_url }})

## The process

The project began with the idea of using a Raspberry Pi, a small screen, Unity WebGL, and a potentiometer. During development, the setup changed to an Arduino Uno, a smartphone, Unity, Google Cardboard, and a potentiometer for user input.

The team worked with both low-fidelity and high-fidelity prototypes. A paper prototype was used to plan what the user should see, followed by digital prototypes that tested whether the hardware could control the transition between two environmental states.

The water landscape was generated in real time to strengthen the feeling that the user’s input had an effect on the environment. This helped create a stronger sense of immersion and made the environmental changes easier to understand.

The prototype was tested mostly through self-tests, but three external users aged 20–30 also tested the experience. The test showed that users quickly understood that agriculture affected the natural environment, and all three felt that they were looking at a real water area.

However, the users only fully understood the purpose after receiving context, and they found the hardware setup too bulky. The slider was also confusing because it filled up as nitrate levels went down.

The main learning was that VR can support environmental education by creating immersion, but the experience still needs supporting text or other media to communicate deeper knowledge clearly.

![Hardware prototype]({{ '/assets/resources/virtual-binoculars-hardware.png' | relative_url }})