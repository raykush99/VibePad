---
title: Vibe Pad
author: Kush Ray
description: It will be an electronic vibraphone/marimba that functions just like the real instrument, and can switch between instrument voices
created_at: 2026-09-12
---

# May 29th - Researched parts
Researched which sensors to use to detect notes played. Initally though about pressure sensors, but those would be too expensive. Looked into how electronic drum sets work and decided to use piezoelectric sensors.
For the microcontroller, decided to use the esp32 due to its sd card holder (which can be used to store audio files) and vast number of analog pins for the sensors.
To plan the pin layout for the esp32, I did prelimanry research on how to connect each compent to the esp32, and how many and what type of pins (ADC vs GPIO) each componet needed. However, I came across a problem since I need 37 analog sensors for this project, but the esp32 does not have enough  pins. After doing research, I leanred multiplexers can be used to connect multiple sensors to one pin. I initially decided on the ADS1256 chip, but it only held 8 sensors and was very expensive. Doing more research, I found the cd74hc4067, smaller, cheaper, and able to hold 16 sensors. I decided to use two cd74hc4067 chips and connect five sensors directly to the esp32 for a total of 37 sensors. At the end, I made a diagram showing which pin each component will be connected to (since some pins can't be used and others need to be in a certian state at boot). This allowed me to organize the components and make sure there where enough pins for everything.
![image](https://github.com/user-attachments/assets/435ab749-472a-4602-bd13-b0907ed9f8a7)
**3 hours**
