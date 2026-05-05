---
title: Coding Train V2
summary: A continuation of the Coding Train, using an IKEA train and 3D-printed T-track switches.
year: 2026
technologies: BIPES, MicroPython, Raspberry Pi Pico W, Fusion 360, 3D Printing, Electronics, Bluetooth
order: 2
status: Early development
cover: /assets/resources/coding-train-v2-cover.jpeg
---

I was not satisfied with my first attempt. It became rather messy and clumsy. The problem was that I was constrained by the hardware that Teknologiskolen already had and used. Because of that, I could not make the electronics as compact and neat as I wanted to.

<!-- Place this image in /assets/resources/coding-train-v2-cover.jpeg -->
<figure class="media media--medium">
  <img src="{{ '/assets/resources/coding-train-v2-cover.jpeg' | relative_url }}" alt="The Coding Train V2">
  <figcaption>The first prototype of the Coding Train V2</figcaption>
</figure>

## The idea

For my second try, I wanted to approach the project differently by using a premade train. However, one problem quickly became clear: *how does the train manoeuvre the track system?* This quickly led me towards my 3D printer.

## The process

Before tackling how the train should turn, I opened up the premade train. I wanted to know how it was assembled and whether there was room for integrating additional hardware. The premade train was able to toggle between moving forward, moving backward, and being at rest. This was controlled by a small toggle switch on top of the train.

The electronics were rather simple. The toggle switch could either close or open the circuit, meaning current could either flow or not. The toggle switch also controlled the direction of the current, which determined which way the small DC motor would spin.

<figure class="media media--medium media--center">
  <img src="{{ '/assets/resources/coding-train-v2-demo1.gif' | relative_url }}" alt="The train detecting different track markers">
  <figcaption>The train distinguishes between different markers and displays a colour according to the marker it reads.</figcaption>
</figure>

I concluded that it was possible to add a small MOSFET transistor and a Raspberry Pi Pico W. I also saw an opportunity to replace the existing yellow LED with an RGB LED. This allowed me to control the train wirelessly. However, I gave up the ability to move in both directions. Furthermore, I added an IR sensor so the train could once again detect markers on the tracks, making it able to sense its environment and become more autonomous.

<figure class="media media--medium media--center">
  <img src="{{ '/assets/resources/coding-train-v2-switch-demo.gif' | relative_url }}" alt="The 3D-printed T-track switch toggling between states">
  <figcaption>A closer look at the T-track switch and how it toggles between the three valid states.</figcaption>
</figure>

I did some research into how others had made switch tracks before. I wanted to be economical and only use one servo motor. I came up with two ideas: a standard two-track switch and a T-track switch. I went to my favourite CAD program and started designing a track that would allow the train to switch route.

The standard two-track switch was easy. However, the T-track switch came with a fun challenge. The track connects three different points, and each point can be directed in two ways. This gives eight possible states. The challenge was that out of the eight states, only three are valid. So how could I toggle between the valid states using only one servo motor?

I could easily do it with two servos, where the first servo controlled the top point and toggled between its two states, while the second servo controlled the two points on the same linear path. These two points simply needed to be reversed. But how could I do it with only one servo motor? I started by looking into gears before finally settling on a system using a cam disc and rubber bands.

<figure class="media media--medium">
  <img src="{{ '/assets/resources/coding-train-v2-switch-back.jpeg' | relative_url }}" alt="T-track switch mechanism with a cam disc and rubber bands">
  <figcaption>T-track switch using a cam disc and rubber bands.</figcaption>
</figure>

Then came the challenge of making the train autonomous by enabling it to know where it was on the track system. In version 1, I used black markers to count how many track pieces the train had passed. However, I wanted a smarter solution where I could use fewer markers while giving the train more knowledge about its current location.

I came up with a binary system where the IR sensor detects rises and falls. Each marker detection is triggered by detecting a black marker. The train then samples over a given time period based on its velocity. The sampling reads the number of highs, which are black markers, and lows, which are white markers. Based on the number of highs and lows, as well as the sequence, the train can distinguish between the different markers.

<figure class="media media--medium media--center">
  <img src="{{ '/assets/resources/coding-train-v2-demo2.gif' | relative_url }}" alt="Demonstration of the 3D-printed T-track switch">
  <figcaption>Demonstration of the 3D-printed T-track switch.</figcaption>
</figure>