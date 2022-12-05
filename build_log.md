---
layout: page
title: Build Notes
permalink: /buildnotes/
---



# [](#header-1) Build Notes
### Updates posted periodically. Build started October 2022.
The documentation for Hangprinter v4 is a bit sparse, but ultimately contains what you need to get the job done. Check out the link in the upper right to the official Hangprinter website, where you'll find links to all the relevant repos and a page with details on the build and calibration process. There's also a link in the upper right to my copy of the BOM, with links to where I bought from and costs as of October 2022.

That being said, this page will simply document things I ran into, peculiarities that may warrant extra documentation, and things that are particular to my build. 

* * *

### Note on configurations

Hangprinter v3 was essentially a proof of concept compared to v4, which is a large step up in complexity and cost. It uses brushless DC motors (BLDC) from ODrive, along with ODrive motor controllers, which are controlled with a Duet3 board, 4 expansion boards, and a rasberry pi with a camera and computer vision system (HP-mark) to aid with calibration. 

Though v4 is relatively new, there are potential configuration changes just around the corner due to some new releases by the electronics manufacturers, which may affect decisions on when and how you decide to build:

- Duet recently released a new board, the 6XD, which is smaller and cheaper and would do away with the 4 1XD expansion boards. 
![Image](/assets/images/6XD.png)
- The recommended ODrive controllers, v3.6, are end-of-life. ODrive just released their S1 board, which is smaller, cheaper, and presumably better. It has onboard encoders which eliminate the need to buy them separately.
![Image](/assets/images/S1.png)

The Duet mainboard and expansion boards, the motor controllers, and the encoders account for somewhere in the neighborhood of 40-50% of the cost of materials, and will come down in a meaningful way once the above changes are incorporated. However, this hardware was just released (October 2022), and the firmware will require some modifications and testing before its stable. Probably a good idea to make contact with Tobben on the Discord channel to check the status of this before making a final call. 

### Order of operations

#### Ordering Parts

A good first step after you decide which way to go on the configuration would be to start ordering the major parts. You can see on my copy of the BOM where I ordered everything from. Lead times were generally not much of an issue, I received most parts within a couple of weeks (a lot of the smaller parts are available on Amazon). Randomly, the ceramic eyelets which go on all the line guides took the longest, around 3 weeks. The lines themselves, which are high-end kitesurfing line made from Dyneema (extremely low stretch), took some effort to source, but I was eventually able to find them through a sailing/kite-surfing supplier named Murray's (see BOM for link).