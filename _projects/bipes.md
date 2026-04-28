---
title: BIPES
summary: BIPES is a browser-based platform where users program devices with blocks or text, connect through serial, WiFi, or Bluetooth, control devices through widgets or MQTT, and integrate computer vision and machine learning into their projects.
year: 2026
technologies: HTML, CSS, Javascript, Blockly, EasyMQTT, Web Serial, Web Bluetooth, WebSocket, OpenCV, Tensorflow.js, Micropython, Python, Flask, Gunicorn, PostgreSQL, SQLite, Flask-MQTT / Paho MQTT integration, Nginx reverse proxy Docker, Docker Compose, HTTPS, Mosquitto, Github, Docker Hub
status: Development
order: 1
cover: /assets/resources/bipes-cover.png
---

BIPES is my browser-based platform for programming microcontrollers and IoT devices with either blocks or text. In my version of the platform, available at [bipes.teknologiskolen.dk](https://bipes.teknologiskolen.dk/), users can connect through serial, WiFi, or Bluetooth, control devices through widgets, and integrate computer vision and machine learning directly into their projects. 

<!-- Place this image in /assets/resources/bipes-cover.png -->
<figure class="media media--medium">
  <img src="{{ '/assets/resources/bipes-cover.png' | relative_url }}" alt="Overview of the BIPES interface">
  <figcaption>BIPES as a browser-based environment for programming and controlling embedded devices</figcaption>
</figure>

## The idea

The original idea behind BIPES was to lower the barrier to embedded programming by making it possible to work with connected devices directly from the browser instead of relying on heavy local toolchains. In that sense, BIPES was created as a teaching and prototyping platform where users could build programs visually, connect to physical devices, and explore embedded systems through a more approachable interface ([original IDE](https://bipes.net.br/ide/), [original paper](https://ieeexplore.ieee.org/document/9246562/)).

My goal has been to extend that idea into a broader learning and interaction platform. I have been especially interested in how BIPES can help users not only make something work, but also understand how programs are structured and how visual logic translates into real code.

## My focus

My main contribution has been to make BIPES easier to program with and easier to learn through. I have treated the platform as a bridge between beginner-friendly block programming and more advanced text-based programming. That has meant designing around gradual progression instead of treating blocks and code as two separate worlds.

A central part of that work has been the transition from blocks to text. In BIPES, users can inspect the generated Python while programming with blocks, copy that code, and continue working in the text editor. In the other direction, the visual editor still works as a useful starting point for exploration and experimentation. This makes BIPES valuable as a learning environment because it helps users see how block structures map to actual Python instead of hiding the text representation away.

<!-- Place this image in /assets/resources/bipes-blocks-to-text.png -->
<figure class="media media--medium">
  <img src="{{ '/assets/resources/bipes-blocks-to-text.png' | relative_url }}" alt="BIPES showing blocks alongside generated Python code">
  <figcaption>The transition from blocks to Python is part of the learning experience, not a separate step</figcaption>
</figure>

## Pipelines and device control

Another major focus has been to make communication pipelines easier to set up and easier to reason about. Users can connect to devices through serial, WiFi, or Bluetooth, and control can happen either through widgets or through MQTT-based communication. I have worked to support a range of practical flows, including device-to-browser, device-to-browser-to-device, device-to-device, and device-to-many through MQTT. Instead of expecting users to assemble these patterns from scratch, the platform aims to make the communication structure visible and manageable.

Widgets and dashboard interactions are an important part of that work. My aim has been to make it easier to control devices, trigger actions, monitor values, and build interactive interfaces around hardware projects. This matters both in teaching and in prototyping, because it reduces the amount of repeated boilerplate work needed to connect user interaction, device communication, and program logic.

<!-- Place this image in /assets/resources/bipes-dashboard-widgets.png -->
<figure class="media media--medium">
  <img src="{{ '/assets/resources/bipes-dashboard-widgets.png' | relative_url }}" alt="BIPES dashboard widgets controlling connected devices">
  <figcaption>Widgets make it easier to build interactive control and monitoring interfaces around physical devices</figcaption>
</figure>

## Vision and machine learning

I have also helped expand BIPES beyond traditional device scripting by integrating browser-based computer vision and machine learning workflows. TensorFlow.js support makes it possible to run machine learning workflows directly in the browser, and I have worked on a node-based system that allows OpenCV-style image processing to become part of the same pipeline-oriented environment.

This means BIPES can be used not only to read sensors and control outputs, but also to build browser-based processing flows where image analysis, computer vision, and machine learning predictions become part of the interaction between devices and software. That extension supports more advanced project work while still keeping the interface visually structured and approachable.

<!-- Place these images in /assets/resources/bipes-vision.png, /assets/resources/bipes-ml_1.png, and /assets/resources/bipes-ml_2.png -->
<figure class="media media--medium">
  <img src="{{ '/assets/resources/bipes-vision.png' | relative_url }}" alt="Computer vision pipeline in BIPES using browser-based image processing nodes">
  <figcaption>BIPES makes it easy to use OpenCV by having a node-based system</figcaption>
</figure>

<div class="media-grid media-grid--2">
  <figure class="media-grid__item">
    <img src="{{ '/assets/resources/bipes-ml_1.png' | relative_url }}" alt="Showcasing how do use machine learning in BIPES with me">
    <figcaption>Showcasing how do use machine learning in BIPES with me</figcaption>
  </figure>
  <figure class="media-grid__item">
    <img src="{{ '/assets/resources/bipes-ml.png' | relative_url }}" alt="Showcasing how do use machine learning in BIPES without me">
    <figcaption>Showcasing how do use machine learning in BIPES without me</figcaption>
  </figure>
</div>

## Platform features

Alongside the programming and pipeline work, BIPES has also grown as a platform. I have focused on adding a login system, expanding the available widgets, and supporting file sharing, which makes the environment more suitable for teaching, collaboration, and continued work across devices and sessions. These additions support the larger goal of making BIPES practical not only as a demo environment, but as a real working platform for classrooms, workshops, and project development.

## Perspective

What interests me most about BIPES is that it can function as a bridge on several levels at once: from blocks to text, from learning to production-like thinking, and from isolated device scripts to complete communication pipelines. My contribution has been to push the platform in that direction by making the progression more gradual, the pipelines easier to assemble, the interaction with devices more immediate, and machine learning and computer vision easier to integrate into real projects.

In that sense, the goal is not only to make it possible to program embedded systems in the browser, but to make the process easier to understand, easier to teach, and easier to continue with as users become more confident.

<!-- Optional: place a short demo video in /assets/resources/bipes-demo.mp4
<figure class="media media--medium">
  <video controls preload="metadata">
    <source src="{{ '/assets/resources/bipes-demo.mp4' | relative_url }}" type="video/mp4">
  </video>
  <figcaption>A short walkthrough can show the flow from blocks to Python, dashboard control, and device pipelines</figcaption>
</figure>
-->
