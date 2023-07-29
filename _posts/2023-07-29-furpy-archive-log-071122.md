---
layout: post
title: FurPy - Archive Log 071122
date: 2023-07-29 11:17 -0700
---

7/11/22 - 
managed to get voice recog working again
lights are flickering and more testing needs to be done

combined the cloudspeech script and the main_test script into "speech_led_test.py"
current issue is that the neopixels want sudo and the mic does not

about logic level shifters and getting a 3.3v data signal up to 5v for neopixels:
<https://learn.adafruit.com/neopixel-levelshifter>

neopixel - shift level diagram:
<https://cdn-learn.adafruit.com/assets/assets/000/064/121/medium640/led_strips_raspi_NeoPixel_Level_Shifted_bb.jpg?1540314807>

neopixel:
<https://github.com/jgarff/rpi_ws281x/issues/326>

mic:
<https://github.com/synesthesiam/rhasspy/issues/90>
<https://www.adafruit.com/product/1312>

motor driver pin out
<https://core-electronics.com.au/guides/how-to-control-a-motor-with-the-raspberry-pi/>
<https://www.sparkfun.com/products/14451>

pi zero pinout
<https://www.etechnophiles.com/wp-content/uploads/2020/12/pinout-.jpg>

audio amp 
<https://www.lucadentella.it/en/2017/04/26/raspberry-pi-zero-audio-output-via-i2s/>

mic pinout
<https://www.mdpi.com/informatics/informatics-07-00048/article_deploy/html/images/informatics-07-00048-g001.png>


<https://cdn.hackaday.io/images/679611454410143033.png>

