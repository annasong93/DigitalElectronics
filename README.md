# DigitalElectronics
3 Sensor

Temperature Sensor:
Temperature Sensor is not like the thermometers we use in home. It can sense temperature by voltage. It is all done by the chip inside. The sensor is small and precise. Temperature Sensor can be use to control on off by detection surrounding temperature.

FSR Force Sensitive Resistor:
It is a pressure sensor that can detect squeezing and weight change. The mechanism is change in resistance by the weight it received. It is most used for detecting if one thing received physical squeeze by how much. But it can also be used for determine weight.

Photocells:
It is a light detect sensor. This sensor is very small and easy to carry out but it does have downside that each sensor varies a lot. The difference is up to 50%. So it is not very good to use for a precise measure in light change.

Interesting Arduino Project

Awake
https://www.hackster.io/sofia-aronov/awake-f2cedc

Awake is an interactive arduino project. It makes a painting alive by using conductive ink. I find it interesting that make a painting live and people can interactive with it. Unlike many interactive advertisement in public space which use screen base interactive, this project alows people touch and feel the thing interact with them. It gives people physical feedback which I find is important in interaction. The screen based interaction use kinect sensor but doesn't give audiance the actual touch or feeling of the action. Combine arduino and processing is also the part I feel interested in. It is not only give a feedback to physical touch but use the animation and light project to give audiance different sence in the experience.


# Week 3
## Project 1: Led Bracelet
### IDEA

My idea is to make led light respond to music. It will detect the beat and blink with the beat and change color with it. I want to make it a bracelet as a decoration when people going to music festival. The light will blink with music in order to visualize the music.

*Idealy it can form different shape or motion with the led lightbulbs.

Here is the sketch:

![8b779585-ebce-4ef2-85e7-1d95111a8be0](https://user-images.githubusercontent.com/35709830/35965250-20e8a4b0-0c6f-11e8-8880-0cfb33363a65.jpg)

Components and sensor:

1. LED strip or lightbulbs.
2. Sensor: Parallax sound impact sensor

### some other addon ideas
1. Light control LED: Put a light sensor in to detect light. The led on the bracelet only light up when surrounding light is below certain darkness. Otherwise, it won't light up even it hear sounds. 

2. Color: Led color is controlled by the vibration sensor. When the sensor detects more vibration the color will vary.

Reference:
https://www.youtube.com/watch?v=nvPOUdz5PL4


## Midterm Project: Led braclet
### Concept: create a led braclet react to music

### Step 1
First I need a sound sensor and led to test when the sensor sence sound led can light up.

Search online for resources. I find this video using Sound Sensor Detection Module LM393 Chip
https://www.youtube.com/watch?v=setjiVH0_IY

<img width="768" alt="screen shot 2018-03-08 at 10 49 18 am" src="https://user-images.githubusercontent.com/35709830/37170019-8962def6-22be-11e8-817a-eb05e085ff63.png">

First step successed. The light react the sound but it is not exactly what I want. The sensor is adjustable by hand so it is not excurate.

### Step 2
So I start look for different sensor which has analog so it can sense different sound in music.
I find another link it is helpful.
http://www.instructables.com/id/Arduino-Vu-Meter-Using-a-Sound-Sensor/

Sound Sensor
![sound sensor](https://user-images.githubusercontent.com/35709830/37172313-479ee166-22c5-11e8-8b11-0015278d0eb2.jpg)

I want to use:
 * 9 leds with different set of color. 
 * Sparkfun Sound Detector
 * 100Ω Resistor

Here is the schematic

![diagram](https://user-images.githubusercontent.com/35709830/37174263-daa3d6b0-22ca-11e8-8743-2acf3cc14cab.jpg)


This is how it look like.

![enlight88](https://user-images.githubusercontent.com/35709830/37172528-e3a51008-22c5-11e8-8ee7-a03c68305331.JPG)


Video:
https://youtu.be/ctge5t-EC08




### Future steps
The next project I want to develop deeper based on current one. The concept not only a wearble device shows lights react to music, but also have color change with surronding like Chameleons. So I will build a glove with color sensor in front and lights around arms. When I touch an object, the color of my arm will change to that and reflect to the sound change.

* change to rgb led.
* Add color sensor it change the color of the led when it sense color nearby.
* build it in cloth make it wearble. 

----------------------------------------------------------------------------------------

# Futher development
### Concept
The idea is from Chameleon. Based on music visualization function of the bracelet, I futher develop it with a color change. When user touch someone, the bracelet will turn to the color that person wear. When I close to you, I will become same color as you.

### Parts for changing
- neopixel ring instead of led. First I tought about using rgb led, but each rgb led has four legs, it is difficult to control each of it in a large number. So I use neopixel ring which can allow me use code to control each of it, and only with one input pin.
(picture)
- color sensor: I use TCS34725 flora color sensor. The size of this sensor is small enough to make it fit into wearable device.
(picture)

### Step 1 sound
Now I need to connect neopixel to sound sensor. Make it react to sound.
First I found a project doing similar thing as I want. Here is the link: https://learn.adafruit.com/sound-reactive-neopixel-peace-pendant/overview
But i find the code is too difficult to hack. So I start to try out myself using similar structure as the code I use for non rgb leds in the previous project. 

Schematic
![fritzing](https://user-images.githubusercontent.com/35709830/39659145-c47fcaf4-4fd6-11e8-9d68-8de37acadc3b.png)
(video)
(code)

### Step 2 color
Now my device can react to music using the neopixel ring. The second step is to add color sensor to control the color.
Use library of TCS34725, I find out the number of color sensor senses is different from rgb 255,255,255. So I am looking for a way to convert it to 255. Finally I find in the example there is a gamma table doing this job for you. I take this part to my code and finally make it work. 
(schemetic)
(video)
(code)

### Prototype looking
(picture)
(video)

### Step 3 Design looking
Final step is how to tranfer prototype to a bracelet. I designed a hexagon shape bracelet to best fit all these components into it. Use laser cut and buil up layer by layer.
(laser cut picture)
(build up pictures)
(final shape inside details)
(final looking outside)
(video)
