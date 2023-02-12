---
layout: default
is_contact: true
---

![Banner Immage for Course](cs4222_banner.png)  

# Wireless Networking aka "Wireless for IoT Class"
## Course code: CS4222/CS5422  
### Semester 2, 2022/2023
### Instructor: Professor Ambuj Varshney
### Contact: [ambujv@nus.edu.sg](mailto:ambujv@nus.edu.sg), COM3: #02-25     

----
****

# TUTORIAL 4 for WEEK 6 (Starting 13th of February 2023)


[1] **Question 1:** What is the typical battery capacity of common devices that you use in your daily life such as wearables (Apple Watch/Fitbit), earphones, laptops, and mobile phones?

[2] **Question 2:**
* In the figure represnting state transition diagram, which chipset is more suitable for used in Internet of Things applications? Explain your reasoning.

* For the chipset chosen in the question above, assume that the devices are designed to operate at a very low duty-cycle (<0.01%) and you are allowed to reduce the current drawn from only one of the states (idle, receive (RX) or transmit (TX)). Which state would you reduce the current from?    

![Question2, Tutorial](tutorial4_question2.png)  

[3] **Question 3:**  Please find specification of following technologies:

| Specification | Bluetooth| ZigBee | WiFi | [LoRa](https://cdn-shop.adafruit.com/product-files/3179/sx1276_77_78_79.pdf) | [LoRea (Backscatter)](https://www.diva-portal.org/smash/get/diva2:1163386/FULLTEXT01.pdf) | [Judo (Backscatter)](https://www.diva-portal.org/smash/get/diva2:1713259/FULLTEXT02) | 
|-------|--------|---------|---------|---------|
| VDD(V) | 1.8 | 3.0 | 3.3 | 3.3 | 2| 0.12|
| Transmit (mA)| 60 | 30 |220| 28 | 0.035| 0.7 |
| Receive (mA)| 50 | 25 | 210| 13.8 | N.A | N.A|
| Bitrate (Mb/s)| 1.2| 0.25 | 54 | 0.027 | 0.003| 0.1|

* Calculate the energy (in Joule) require to transmit 1 bit for different technologies listed above.  
* For low power IoT devices, should you always select the network technology with the lower transmission energy per bit? Explain your answer
* In addition to energy needed to transmit/receive a bit, what other criteria(s) should you take into account when selecting a network technology for use in a low power Internet of Things? 
* What kind of applications would choose to use Bluetooth technology? 
* What kind of application would choose to use LoRa technology?
* What kind of application would choose to use Backscatter technology?

Q4: TBA

























