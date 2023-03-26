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

# Project (Due, 21st April 2023)

This is a **GROUP** assignment.

You can conduct this experiment in a group of 2-4 group. It should be completed with each project group.

Assignment weightage towards final grade: 13% of Course Grade   

**Important: We will check for code similarity and potential cases of plagiarism**  
**Important: Please do not use ChatGPT to write code for this assignment. We will particularly check for ChatGPT plagiarism.**

### Overview

In this project, you will integrate and apply various concepts acquired throughout the course, such as sensor interfacing, proximity detection using received signal strength, neighbor discovery, programming contiki operating system and delay-tolerant networking. You will develop a comprehensive project encompassing all these elements.

The project is structured into two  parts. In the first part, you will implement a neighbor discovery mechanism based on the "birthday protocol." Subsequently, in the second part of the project, you will enhance this neighbor discovery mechanism to establish a delay-tolerant sensing application. The following sections provide a detailed description of these components.

### Neighbour Discovery

You have been given a program that implements a fundamental "birthday protocol." In this protocol, each node wakes up at random intervals to transmit data and listen for transmissions from nearby devices. The following illustration demonstrates the steps involved in the protocol's operations.

![Neighbour discovery course](nbrimg.png)  

The identical code is executed on all nodes. Each node wakes up for a duration of Twake, during which it sends two packets: one at the beginning of the wake-up period and another at the end, just before returning to sleep. Following the initial transmission, the node keeps its radio on to listen for potential incoming messages.

In the illustration above, Node 1 and Node 2 operate based on their individual timers. The intervals between two consecutive wake-up slots (Tsleep1 and Tsleep2 in the figure) are randomly selected from a uniform distribution, sharing the same mean Tsleep value.

Adjusting Twake and Tsleep will influence the latency experienced by nodes when discovering neighboring devices and the radio energy consumption. The radio's duty cycle can be calculated using the formula: Twake / (Twake + Tsleep).

You are provided with a C program, "nbr_discovery.c," which implements the fundamental logic outlined above. The modifiable parameters in the program are as follows:

WAKE_TIME (Twake): The default value is set to (RTIMER_SECOND / 10) or 100ms.

The maximum duration of a single sleep interval is constrained by the RTIMER count wraparound. Therefore, the total sleep interval between two wake-up periods is calculated as the product of the duration of a single sleep (SLEEP_SLOT) and the number of sleep cycles (SLEEP_CYCLE).

* SLEEP_SLOT: The default value is the same as WAKE_TIME.
* SLEEP_CYCLE: This represents the average number of sleep cycles, with a default value of 9.
The duty cycle is calculated using the formula: WAKE_TIME / (WAKE_TIME + SLEEP_CYCLE * SLEEP_SLOT).

### Setting up Contiki

1. Create a folder named "nbr_discovery" in the contiki-ng/examples directory
1. Copy nbr_discovery.c and Makefile in the above created folder
1. Compile the nbr_discovery program using command “make TARGET=srf06-cc26xx BOARD=sensortag/cc2650 CPU_FAMILY=cc26xx” in the directory “contiki-ng/examples/nbr_discovery”.
1. Use uniflash program to burn the binary file to the SensorTag.
1. Observe the output of the program through the USB serial port.

You need to run the program on at least 2 devices to perform the experiment. Consider two devices A and B.


### TASK 1

1. Using the default settings, observe and record how long the devices take to discover each other. Pick one of the devices as A and plot the cumulative distribution of the intervals between packet receptions on device A hearing from device B.
1. Reset device B and observe how long it takes for device A to hear from device B after device B reboots. You may need to modify the given code to observe this duration. Perform the experiments at least 10 times and plot the cumulative distribution.
1. Try out different settings and discuss your observations.

### Delay-tolerant Sensing and Communication




### PROGRAM

You can download [makefile and unicast_communication.c from here](https://ambuj.se/unicast.zip)

**IMPORTANT:** When sending at fast rates, you might encounter errors. The solution is to replace log_info with printf. Please make these changes in the program before doing the following tasks.



### Hardware

You would need two nodes for this assignment. Please pick one as a transmitter and another as a receiver.

### Address Configuration


### Evaluation

**Submission instructions:** Submit a single zip file (“Assignment3a - YourGroupNumber.zip”) to folder “Assignment3 Submission” on Canvas by the due date. If you submit multiple times, only the latest submission will be evaluated. Your submission should include the following:

1. Code used in your measurements.
1. A report in PDF format that contains the answers to above task questions

Late penalty is 10% of marks after 21st April 2023 (Submission would not be accepted after 30th April 2023).

### Special Thanks

Very grateful to the teaching assistant Malaika who helped port this to Contiki-NG platform.






