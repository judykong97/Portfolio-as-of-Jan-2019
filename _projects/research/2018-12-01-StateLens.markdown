---
title: StateLens
description: A Reverse Engineering Solution to Making Existing Dynamic Touchscreens Accessible
note: In this research project, I implemented the computer vision back end including reference image matching, dynamic state diagram construction, fingertip detection and feedback instructions, etc. I also prototyped the 3D printed assistive fingercap, ran technical evaluations and user studies, and participated in paper writing.
date: 2018-12-01 19:55:16
---

\#Accessibility \#ComputerVision \#Crowdsourcing

Collaborated work with Anhong Guo and Michael Riva, advised by Prof. Jeffery Bigham. This work is in submission to UIST 2019.

### Motivation

Blind people frequently encounter inaccessible dynamic touchscreens
in their everyday lives that are difficult, frustrating, and
often impossible to use independently. Touchscreens are often
the only way to control everything from coffee machines and
payment terminals, to subway ticket machines and in-flight
entertainment systems. In this project, we aim to make currently inaccessible touchscreen interfaces accessible to visually-impaired users.

### Description

![Image]({{ site.baseurl }}/images/projects/statelens-interfacelist.jpg)

StateLens is a system that uses a hybrid crowd-computer vision
pipeline to provide interactive feedback to help blind
users access touchscreen devices. It works by dynamically
reverse engineering state diagrams of existing interfaces
from point-of-view usage videos. Even if an interface
state has not been seen before, StateLens can interactively
gather information about the state on-the-fly, enabling access
in a short amount of time. We also introduce a 3D-printed
finger cap that enables capacitive touchscreens to be used
non-visually by preventing accidental touches on the interface.
The design and architecture of StateLens was informed by a
formative study with blind users, and our evaluation shows
that StateLens can accurately reconstruct interface structures
from crowdsourced stationary and point-of-view usage videos.
We believe StateLens represents an important step for solving
this long-standing accessibility problem, and its technical
approach may find application broadly for augmenting how
people interact with the touchscreens they encounter.

### Fingercap

We iterated on the designed of a fingercap that keeps the user's finger from touching the screen while exploring the interface. When they wish to click on a button, then can tilt the finger to tap on the screen. We are currently iterating on the fingercap and trying out different possibile designs.

![Image]({{ site.baseurl }}/images/projects/statelens-fingercap.jpg)

### Reverse-Engineering Crowdsourcing Pipeline

We represent the state transitions with a state diagram. We used computer vision to match captured image with reference images of the interface. Once a new screen is detected, we add it to the statesend it through the crowdsourcing pipeline to gather information about the description, button layout and information.

![Image]({{ site.baseurl }}/images/projects/statelens-cv.jpg)

This is an on-going project and more details will be updated.




