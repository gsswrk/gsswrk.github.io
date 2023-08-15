---
layout: post
title: FurPy Redux
date: 2023-08-15 14:22 -0700
---

The previous design was based off the Google AIY kit that I had been tinkering with at the time. I've learned a few tricks and am taking a new approach to this project. 

My biggest hurdles previously were the size of the components I was trying to cram inside the furby, and, stupid audio drivers for the mic. 
SO, I decided to ditch the pcb mic in favor of a usb mic and instead of the raspi B+, we are now using the raspi zero 2 w. KISS.

First, I defined the objective. As my companion, furPy should:
1. Be easily reproducable
2. Detect light, motion, sound, infrared, and, touch (belly, tongue) 
3. Be conversational (chatgpt api, long term memory (pinecone))
4. Scream when it's been flipped? (IMU)

Second, I defined the scope:
1. What original components can be used?
2. What are the overall power requirements?
3. What new components provide the desired functionality? and do they work together?
4. Do they all fit within the confines of the original pcb dimensions?
5. Where do i put the raspberry pi?

Components list:
TB6612FNG - motor driver
bno055 - 9axis imu
MAX98357A - I2S audio amp out
sn74ahct125n - Quad Level-Shifter converting 3V logic up to 5V for neopixels


Next, I took a few photos for scale. This was really helpful later on when trying to place components.
![image](https://github.com/gsswrk/gsswrk.github.io/assets/26857790/2f986fac-5135-4674-a26d-de74caa97df6)
![image](https://github.com/gsswrk/gsswrk.github.io/assets/26857790/aa636356-b0c4-405b-972c-13ce619b14b1)

Using the measurements of the main pcb of the original 1998 Furby, I was able to draw an outline of board and place the holes needed for things like screws. 
Then I started sourcing components. Making sure to pick surface mount where possible. I decided to just go with the through hole add-on for the IMU because it added a lot of complexity. KISS 

When the dust finally settled, I came up with this schematic that included just about everything... everything except battery management. Which I think can be addressed in revision 3.1.6 after we have some success with the initial prototypes. 
![image](https://github.com/gsswrk/gsswrk.github.io/assets/26857790/43bcccb0-f38f-4794-a13a-bfb98adac2d6)

Next step is to design the pcb using the recently updated schematic and send it off to get made. 

Here is a rough idea of what the final product might look like.
![image](https://github.com/gsswrk/gsswrk.github.io/assets/26857790/d0a5f071-0161-4759-8b81-1c87a13205c7)
