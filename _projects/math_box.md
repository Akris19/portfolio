---
title: Math Box 
summary: A two-person Virtual Reality Game aimed at High School students, where the users can enhance and improve their mathematical skills by communication together. The two players must use math to solve a bomb.
year: 2023
technologies: Virtual Reality, Unity, C#, Raspberry Pi Pico W, C/C++, BNO055, Adobe Illustrator, Socket.IO, Google Cloud Platform, PCB Design, Eagle, KiCad, Laser Cutting
order: 5
cover: /assets/resources/math.png
---

A cooperative VR learning game that turns math practice into a shared puzzle experience. One player explores a virtual classroom, while the other uses a formula sheet and keypad to solve math challenges through communication.

![Prototype setup]({{ '/assets/resources/math.png' | relative_url }})

## The idea

Mathbox was developed as a learning-based game for first-year high school students studying mathematics at C-level. The project explored whether Google Cardboard, custom hardware, and cooperative gameplay could make skill-based math practice more engaging and social.

The core idea was inspired by games like Keep Talking and Nobody Explodes and We Were Here, where players have different information and must communicate clearly to solve problems together. In Mathbox, the goal was to make students talk about math instead of solving tasks silently on their own.

![Prototype setup]({{ '/assets/resources/board.png' | relative_url }})

## Target

The project was aimed at first-year high school students who need to practise basic math skills, such as fractions, powers, right-angled triangles, linear functions, vectors, and combinatorics.

The experience was designed for classroom use, where two students work together: one student is inside the VR environment, while the other supports with formulas, calculations, and input. This creates a learning situation where communication becomes part of the math practice.

![Prototype setup]({{ '/assets/resources/Screenshot from 2026-04-27 19-51-22.png' | relative_url }})

## The process

The project was developed through several iterations. The first low-fidelity prototype was a cardboard box with post-it notes containing math questions. This was used to test whether the concept could create dialogue around mathematics. Early testing showed that the communication was not strong enough, and one player often became a passive messenger while the other did most of the work.

The next iteration added symbols and more game-like elements to encourage communication, but testing showed that the dialogue became more about decoding symbols than discussing the math itself. The project then moved into a high-fidelity prototype built in Unity for Google Cardboard. A virtual classroom was created, and a keypad controller was developed so answers could be entered and displayed in the game.

Later in the process, the physical box returned as an important interaction element. A custom controller was built using a Raspberry Pi Pico W and a BNO055 sensor to track the box’s rotation. A separate Android keypad app was also created when the physical keypad became too difficult to finish within the project timeline.

The final prototype was tested with first-year students from Esbjerg Gymnasium. The test showed that the game was confusing at first, but once the students understood the system, all three test groups enjoyed the experience. The feedback also showed that the difficulty level did not fit all students equally, and that the game needed a clearer manual and stronger onboarding before students could play independently.

![Prototype setup]({{ '/assets/resources/Screenshot from 2026-04-25 13-48-31.png' | relative_url }})

![Prototype setup]({{ '/assets/resources/Screenshot from 2026-04-25 13-49-20.png' | relative_url }})

![Prototype setup]({{ '/assets/resources/Screenshot from 2026-04-27 19-53-47.png' | relative_url }})