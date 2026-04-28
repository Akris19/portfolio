---
title: Math Box
summary: A two-person Virtual Reality game aimed at high school students, where users can enhance and improve their mathematical skills by communicating together. The two players must use math to solve challenges in a shared puzzle experience.
year: 2023
technologies: Virtual Reality, Unity, C#, Google Cardboard, Raspberry Pi Pico W, BNO055, Socket.IO, Node.js, Google Cloud Platform, Android App, PCB Design, Eagle, KiCad, Laser Cutting, User Testing
order: 6
status: Finished
cover: /assets/resources/mathbox-cover.png
---

A cooperative VR learning game that turns math practice into a shared puzzle experience. One player explores a virtual classroom, while the other uses a formula sheet and keypad to solve math challenges through communication.

<figure class="media media--medium">
  <img src="{{ '/assets/resources/mathbox-cover.png' | relative_url }}" alt="Math Box prototype showing the VR classroom, keypad app and physical controller">
  <figcaption>Math Box prototype showing the VR classroom, keypad app and physical controller</figcaption>
</figure>

## The idea

Math Box was developed as a learning-based game for first-year high school students studying mathematics at C-level. The project explored whether Google Cardboard, custom hardware, and cooperative gameplay could make skill-based math practice more engaging and social.

The core idea was inspired by games like Keep Talking and Nobody Explodes and We Were Here, where players have different information and must communicate clearly to solve problems together. In Math Box, the goal was to make students talk about math instead of solving tasks silently on their own.

<figure class="media media--medium">
  <img src="{{ '/assets/resources/mathbox-cardboard-prototype.png' | relative_url }}" alt="Early cardboard prototype with math questions placed on the sides of a box">
  <figcaption>Early cardboard prototype with math questions placed on the sides of a box</figcaption>
</figure>

## Target

The project was aimed at first-year high school students who need to practise basic math skills, such as fractions, powers, right-angled triangles, linear functions, vectors, and combinatorics.

The experience was designed for classroom use, where two students work together: one student is inside the VR environment, while the other supports with formulas, calculations, and input. This creates a learning situation where communication becomes part of the math practice.

<figure class="media media--medium">
  <img src="{{ '/assets/resources/mathbox-user-test_1.png' | relative_url }}" alt="Follow students trying the low-fidelity prototype">
  <figcaption>Follow students trying the low-fidelity prototype</figcaption>
</figure>

## The process

The project was developed through several iterations. The first low-fidelity prototype was a cardboard box with post-it notes containing math questions. This was used to test whether the concept could create dialogue around mathematics. Early testing showed that the communication was not strong enough, and one player often became a passive messenger while the other did most of the work.

The next iteration added symbols and more game-like elements to encourage communication, but testing showed that the dialogue became more about decoding symbols than discussing the math itself. The project then moved into a high-fidelity prototype built in Unity for Google Cardboard. A virtual classroom was created, and a keypad controller was developed so answers could be entered and displayed in the game.

<figure class="media">
  <img src="{{ '/assets/resources/mathbox-vr-classroom.png' | relative_url }}" alt="Virtual classroom environment used in the high-fidelity prototype">
  <figcaption>Virtual classroom environment used in the high-fidelity prototype</figcaption>
</figure>

Later in the process, the physical box returned as an important interaction element. A custom controller was built using a Raspberry Pi Pico W and a BNO055 sensor to track the box’s rotation. A separate Android keypad app was also created when the physical keypad became too difficult to finish within the project timeline.

<figure class="media media--medium">
  <img src="{{ '/assets/resources/mathbox-keypad-app.png' | relative_url }}" alt="Android keypad app used to submit answers during gameplay">
  <figcaption>Android keypad app used to submit answers during gameplay</figcaption>
</figure>

<figure class="media media--medium">
  <img src="{{ '/assets/resources/mathbox-hardware-controller.png' | relative_url }}" alt="Physical box controller with electronics used to track rotation">
  <figcaption>Physical box controller with electronics used to track rotation</figcaption>
</figure>

<figure class="media media--medium">
  <img src="{{ '/assets/resources/mathbox-board.png' | relative_url }}" alt="Board inside the virtual class-room ">
  <figcaption>Board inside the virtual class-room </figcaption>
</figure>

The final prototype was tested with first-year students from Esbjerg Gymnasium. The test showed that the game was confusing at first, but once the students understood the system, all three test groups enjoyed the experience. The feedback also showed that the difficulty level did not fit all students equally, and that the game needed a clearer manual and stronger onboarding before students could play independently.

<figure class="media media--medium">
  <img src="{{ '/assets/resources/mathbox-user-test.png' | relative_url }}" alt="First-year high school students testing the Math Box prototype">
  <figcaption>First-year high school students testing the Math Box prototype</figcaption>
</figure>


<div class="media-grid media-grid--2">
    <figure class="media media--medium">
    <img src="{{ '/assets/resources/mathbox-pcb.png' | relative_url }}" alt="Physical Calculator was also created ">
    <figcaption>Physical Calculator was also created </figcaption>
    </figure>
    <figure class="media media--medium">
    <img src="{{ '/assets/resources/mathbox-laser.png' | relative_url }}" alt="Physical Calculator Laser cutted edition">
    <figcaption>Physical Calculator Laser cutted edition</figcaption>
    </figure>
</div>
