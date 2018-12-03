---
title: StateLens
description: A Reverse Engineering Solution to Making Existing Dynamic Touchscreens Accessible
note: In this research project, I implemented the computer vision back end including reference image matching, dynamic state diagram construction, fingertip detection and feedback instructions, etc. I also prototyped the 3D printed assistive fingercap, ran technical evaluations and user studies, and participated in paper writing.
---

\#Accessibility \#ComputerVision \#Crowdsourcing

### Description

When you walk into a museum, it's may be very hard to understand the art works, especially if you don't have much of an art background. The short descriptions by the art works are sometimes too small to read from far away, but you don't want to block other people. What to do then?

Scene is a project that helps users understand art works with simple and straightforward augmented reality assistance. It helps you understand art works by storing a big number of art work descriptions in the database. Whenever you point your phone camera to an art work, it matches with the art works in our database, and displays the descriptions as text floating above the art work on your screen. In this way, you can have a full view of the art work without having to walk very close to look at the descriptions on the wall.

![Image]({{ site.baseurl }}/images/projects/scene-demo.jpg)

### Implementation

This project was developed using the Vuforia AR SDK. The on-screen interactions were created in Unity and C#. We used the Vuforia built-in image recognition feature to match with the pictures of art works we store in the database, and then display relevant text we grabbed from Wikipedia to the users.

### Tools & Technologies

Google Cloud Platform, Unity, Vuforia SDK, C#

### Team Members

[Oshadha Gunasekara](https://www.linkedin.com/in/oshadhagunasekara), [Peter (Wenze) Shi](https://www.linkedin.com/in/wenze-shi-15920b15b/), [Ziyang Wang](https://www.linkedin.com/in/ziyang-wang-cmu/)

<!-- [Scene](https://github.com/judykong97/scene) -->
