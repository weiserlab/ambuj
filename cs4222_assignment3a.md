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

# ASSIGNMENT 3(a) (Due, 2nd April 2023)
 
This is a **GROUP** assignment.

You can conduct this experiment in a group of 2-4 group. It should be completed with each project group.

Assignment weightage towards final grade: 13% of Course Grade   

**Important: We will check for code similarity and potential cases of plagiarism**  
**Important: Please do not use ChatGPT to write code for this assignment. We will particularly check for ChatGPT plagiarism.**


### Overview

In this assignment, you will learn about the concept of RSSI (Received Signal Strength Indicator) and how it relates to wireless communication. You will conduct experiments to observe:

1. How RSSI varies with the distance between the sender and the receiver
1. How RSSI is affected by obstacles that block the line-of-sight between the sender and the receiver
1. How accurate RSSI is as a measure of the distance between the sender and the receiver.


### Programs

You can download [makefile and unicast_communication.c from here](https://ambuj.se/unicast.zip)

### Setting up Contiki

1. Create a folder named unicast in the contiki-ng/examples directory
1. Copy unicast_communication.c and Makefile in the above created folder
1. The same file unicast_communication.c is responsible for both conducting transmissions and receptions. It has been modified appropriately with comments to explain its functioning


### Hardware

You would need two nodes for this assignment. Please pick one as a transmitter and another as a receiver.

### Address Configuration

Please make and compile the unicast_communication program. Next, flash the compiled code using uniflash onto sensortag (receiver).

Once, the node starts, it would print the receiver's link-layer address among other device cofiguration information. Please refer to the screenshot below.

![Link Measurement](assign3a_img4.jpg)  

Next, replace the variable called static linkaddr_t dest_addr, given in unicast_communication.c with the link-layer address you have found above. Also, modify the program to send 4 packets every second for at least 10 seconds.

Finally, compile and flash unicast_communication to the transmitter sensor tag.

Now, the transmitter will start transmitting packets desitned to receiver (with link-layer address found above), and the receiver will print the received data with the RSSI value.


### TASKS:  RSSI vs Distance

![Link Measurement](assign3a_img2.jpg)  

Put the receiver and the sender at line-of-sight (no obstacle) and observe how RSSI and packet reception ratio changes (# of packet received in 10 sec. / # of transmitted in 10 sec.) when you change the distance between them from 1m to 30m. Report your results using two graphs similar to the graphs shown below (RSSI vs distance and loss ratio vs distance).

Repeat the experiments in other environments and different placement of receiver but keeping line-of-sight and no obstacle between transmitter and receiver. Discuss your measurements in your report.

![Link Measurement](assign3a_img1.jpg)  

### TASKS: RSSI with Obstacles

Let’s see how different obstacles between the sender and the receiver affect RSSI & packet loss ratio. Let’s measure RSSI at the same distance (use a distance of between 1m to 5m). You should keep the distance the same but you need to specify the distance used in the measurements.
Try out different type of obstacles between sender and receiver (at least 5 types). Discuss your measurements in your report.

| Obstacles (some examples)|  RSSI | 
|-------|--------|
| Door|  | 
| Wall | | 
| Thick Wall | | 


### TASKS: Discussion

1. Are there any other factors that can affect RSSI other than distance and obstacles? Design new experiments and analyse the test results as needed.
1. How good is RSSI as proxy for distance? Justify your answer based on experimental results.


### Evaluation

**Submission instructions:** Submit a single zip file (“Assignment3a - YourGroupNumber.zip”) to folder “Assignment3 Submission” on Canvas by the due date. If you submit multiple times, only the latest submission will be evaluated. Your submission should include the following:

1. Code used in your measurements.
1. A report in PDF format that contains the answers to above task questions

Late penalty is 10% per day after 31st March 2023.

### Special Thanks

Very grateful to the teaching assistant Malaika who helped port this to Contiki-NG platform.






