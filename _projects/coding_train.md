---
title: The Reading Train
summary: A programmable train prototype designed for children and young people, where users build and program a physical robot train that reads markers on wooden tracks and communicates with a digital twin.
year: 2025
technologies: Raspberry Pi Pico W, MicroPython, Unity, C#, UDP, WiFi, Multithreading, Fusion 360, 3D Printing, Bambu Lab A1-series, Servo Motors, DC Motors, Color Sensor, IR Line Sensor, Digital Twin
order: 3
status: High-fidelity Prototype
cover: /assets/resources/reading-train-cover.png
---

A programmable train prototype created for Teknologiskolen, designed to help children succeed in their first meeting with robotics. The project combines physical building, programming, sensors, motors, wireless communication, and a digital twin into a hands-on learning experience.

![The Reading Train prototype on wooden tracks]({{ '/assets/resources/reading-train-cover.png' | relative_url }})

## The idea

The Reading Train was developed as a bachelor project in collaboration with Teknologiskolen, an organisation that introduces children and young people to technology through camps and weekly courses.

The idea was to create a robotics project that could be built and programmed by children aged 10 to 16. The train should drive on wooden tracks, read markers on the track, react to them, and later communicate wirelessly with a digital twin in Unity.

The project was also designed around the idea of gamifying the learning process. Instead of presenting the full robot at once, the building and programming process could be divided into smaller “levels”, where each step introduces a new component or concept.

![Early train prototype]({{ '/assets/resources/reading-train-early-prototype.png' | relative_url }})

![Early train prototype with wagon]({{ '/assets/resources/reading-train-early-prototype_1.png' | relative_url }})


## Target

The project was aimed at children and young people aged 10 to 16 who participate in Teknologiskolen’s courses and camps.

The challenge was to design something simple enough for younger beginners to complete, while still being interesting and technically challenging for older or more experienced participants.

The project therefore needed to support different skill levels. Beginners should be able to build and understand the core train, while more advanced participants could explore sensors, wireless communication, multithreading, and the digital twin.

![Children experimenting with different track layouts]({{ '/assets/resources/reading-train-track-testing.png' | relative_url }})

## The process

The process began with concept development around several possible robotics projects, including a line-following robot, a drawing robot, a robot arm, and a programmable train. After discussing the ideas with Teknologiskolen, the train was chosen because the track system gave users more room to experiment and build their own layouts.

Early iterations explored both the train and a robot arm. The robot arm was prototyped with LEGO, 3D printed parts, servo motors, and different mechanical systems such as a Geneva mechanism and worm drive. However, testing showed that combining the train and robot arm made the project too complex, so the focus shifted fully to the train.

![LEGO robot arm prototype used during early exploration]({{ '/assets/resources/reading-train-robot-arm-lego.png' | relative_url }})

The first train prototypes focused on basic movement, steering, and track compatibility. IKEA wooden tracks were used as the foundation, and several 3D printed train bodies were created in Fusion 360. Different steering and drivetrain solutions were tested, including fixed axles, LEGO O-ring wheels, bevel gears, differential gears, and Ackermann steering.

A major part of the process was finding a reliable way for the train to read information from the track. The project first explored a colour sensor, but the readings changed too much between tests. Later, the system was simplified by using an IR line sensor to count black markers on the track. Instead of reading many different instructions, the train could understand how far it had travelled based on the number of markers.

![Testing black markers on wooden tracks]({{ '/assets/resources/reading-train-marker-test.png' | relative_url }})

The train body was eventually redesigned as a modular system inspired by LEGO-style pegs. This made the prototype easier to print, assemble, and understand. The final modular version consisted of separate parts for the motor, front wheels, steering, reading sensor, and controller unit.

![Modular train body with peg system]({{ '/assets/resources/reading-train-modular-body.png' | relative_url }})
![Differential Gear printed with a 2mm nozzle]({{ '/assets/resources/reading-train-differential-gear.png' | relative_url }})
![Ackermann steering]({{ '/assets/resources/reading-train-ackermann-steering.png' | relative_url }})

Testing was done in two stages. First, former helpers and instructors from Teknologiskolen tested the project using a SWOT approach. They highlighted hands-on learning, broad appeal, and the fun of building tracks as strengths, but also noted that the project might be difficult for younger beginners without a strong guide.

The second test was conducted with children aged 10 to 12. The test showed that the physical assembly was still complex, especially the wiring and mounting of the robotics board and battery box. Some participants needed a lot of help, while others managed more independently.

Later in the process, a digital twin was added in Unity. The idea was to create a meaningful reason for the train to drive around the track by connecting the physical train to a digital world. The real train and the digital twin were synchronised using wireless communication, so the digital version could reflect the physical train’s movement.

The main learning from the project was that the technical prototype had strong potential, but the learning framework needed to be designed more clearly. The train worked as a robotics platform, but the full course should be structured more carefully into levels, guides, and meaningful challenges for the target group.

![Assembly guide for the train prototype]({{ '/assets/resources/reading-train-assembly-guide.png' | relative_url }})

![Final train prototype with digital twin]({{ '/assets/resources/reading-train-demo.gif' | relative_url }})