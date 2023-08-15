---
layout: post
title: FurPy Redux
date: 2023-08-15 14:22 -0700
---

The previous design was based off the Google AIY kit that I had been tinkering with at the time. I've learned a few new tricks and am taking a new approach to this project.

First, I defined the objective:

as my companion, furPy should:
1. be easily reproducable
2. detect light, touch (belly, back, tongue) and infrared
3. be conversational (chatgpt api, long term memory (pinecone))
4. scream when it's been flipped? (IMU)

Second, I defined the scope:
1. what original components can be used?
2. what are the overall power requirements?
3. what new components provide the desired functionality? and do they work together?
4. Do they all fit within the confines of the original pcb dimensions?
5. where do i put the raspberry pi?

Next, I took a few photos for scale. This was really helpful later on when trying to place components.
![image](https://github.com/gsswrk/gsswrk.github.io/assets/26857790/2f986fac-5135-4674-a26d-de74caa97df6)
![image](https://github.com/gsswrk/gsswrk.github.io/assets/26857790/aa636356-b0c4-405b-972c-13ce619b14b1)

Using the measurements of the main pcb of the original 1998 Furby, I came up with something that should fit all the same. Here is a rough idea of what the final product might look like.
![image](https://github.com/gsswrk/gsswrk.github.io/assets/26857790/d0a5f071-0161-4759-8b81-1c87a13205c7)


Then started sourcing components. Making sure to pick surface mount where possible. I decided to just go with the through hole add-on for the IMU because it added a lot of complexity. KISS 

When the dust finally settled, I came up with this schematic that included just about everything... everything except battery management. Which I think can be addressed in revision 3.1.6 after we have some success with the initial prototypes. 
![image](https://github.com/gsswrk/gsswrk.github.io/assets/26857790/43bcccb0-f38f-4794-a13a-bfb98adac2d6)

Next step is to design the pcb using the recently updated schematic and send it off to get made. 
