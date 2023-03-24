u---
layout: default
is_contact: true
---

![Banner Immage for Course](cs4222_banner.png)  

# Wireless Networking aka "Wireless for IoT Class"
## Course code: CS4222/CS5222  
### Instructor: Professor Ambuj Varshney
### Contact: [ambujv@nus.edu.sg](mailto:ambujv@nus.edu.sg), COM3: #02-25     

----
****

# PROMPTS FOR CHATGPT

## OVERVIEW
Large language models (LLMs) like [ChatGPT](https://chat.openai.com/chat) are trained on vast amounts of data, making them proficient in conversation and providing feedback. Despite a somewhat unsuccessful history, chatbots are finally reaching a point where they can be highly beneficial for learning. ChatGPT, for example, can be used to gain knowledge about wireless technology. We encourage the use of this tool for educational purposes in our course.

Below are answers obtained from ChatGPT based on GPT4. We have vetted these responses, but please not they may still have in-accuracies. 

## Lecture 8:

### Why is local discovery useful for wireless networks?
**Answer:** Local discovery is essential for wireless networks because it enables devices to find and communicate with each other within a given area. This process is critical for establishing connections, sharing resources, and exchanging information between devices. Specifically, local discovery:

Facilitates efficient resource allocation: Local discovery allows devices to identify nearby network nodes, enabling the most efficient use of available resources such as bandwidth and power.

* Enables ad-hoc networks: Local discovery allows devices to dynamically form ad-hoc networks, which can be useful in situations where a central infrastructure is unavailable or impractical.
* Enhances network security: By discovering local devices, network administrators can monitor network activity and identify potentially malicious nodes or security threats.
* Simplifies network setup and maintenance: Local discovery can help automate the process of setting up and maintaining network configurations, which can be especially useful for large, complex wireless networks.

### What is synchronous and asynchronous neighbour discovery? What is the difference between the two?
**Answer:** Synchronous and asynchronous neighbour discovery are two methods used by wireless devices to detect and establish connections with nearby devices in a network. The main difference between the two lies in their timing and coordination mechanisms.

* Synchronous neighbour discovery: In this method, devices follow a predefined schedule to send and listen for discovery messages. This requires accurate time synchronization among all devices in the network. The advantage of synchronous discovery is that it can be more energy-efficient, as devices know exactly when to listen for messages and can power down their radios during other periods.

* Asynchronous neighbour discovery: In this method, devices do not rely on a common schedule or time synchronization. Instead, they send and listen for discovery messages independently and at random intervals. Asynchronous discovery is more robust and can work in networks with unreliable or no time synchronization, but it can be less energy-efficient due to the increased likelihood of devices listening for messages when none are being sent.

### What is power save mode in wireless communication in mobile devices?
**Answer:** Power save mode is a feature in wireless communication systems, particularly in mobile devices, designed to conserve energy by minimizing the device's radio usage. This is achieved by:

* Reducing transmission power: The device may lower its transmission power when communicating with nearby devices, as less energy is needed to maintain a strong signal.

* Periodic listening: The device may periodically switch its radio on and off to listen for incoming messages, rather than continuously listening. This allows the device to conserve energy during periods when no communication is taking place.

* Sleep intervals: The device may enter a low-power sleep mode during periods of inactivity, during which its radio and other components are powered down to conserve energy.

These measures help extend the battery life of mobile devices, making them more suitable for use in situations where access to a power source is limited or unavailable.

### What is the birthday paradox? How can it be used to design efficient neighbour discovery protocols?
**Answer:**  The birthday paradox, also known as the birthday problem, is a probability theory concept that states that in a group of 23 people, there is a 50% chance that at least two of them share the same birthday. This counterintuitive result is due to the fact that the probability of a shared birthday increases with the number of possible pairings between people, rather than the number of people themselves.

In the context of neighbour discovery protocols, the birthday paradox can be applied to design efficient algorithms. By leveraging the concept of collisions (when two devices transmit at the same time) in asynchronous neighbour discovery, designers can create protocols that minimize energy consumption and discovery latency. Using the birthday paradox principles, devices can be programmed to transmit discovery messages at random intervals, such that the likelihood of collisions (and thus, successful discovery) increases.

### What is routing in computer networking?
**Answer:** Routing in computer networking is the process of selecting paths in a network along which data packets are sent from a source device to a destination device. Routers, which are specialized network devices, use routing algorithms and protocols to determine the best path for data packets based on various factors such as network topology, link capacity, and network conditions. The primary goal of routing is to deliver data packets efficiently and reliably while optimizing network performance.

### What makes routing challenging in wireless networks when compared to wired networks?
**Answer:** Routing in wireless networks can be more challenging than in wired networks due to several factors:

* Dynamic topology: Wireless network nodes may frequently join, leave, or move within the network, causing frequent changes in network topology. This requires routing protocols to quickly adapt to changes and find new routes.

* Limited resources: Wireless devices, especially battery-powered ones, have limited resources like power and bandwidth. Routing protocols must consider these constraints when determining routes.

* Interference and signal fading: Wireless signals can be affected by interference, multipath propagation, and signal fading, which can lead to unreliable and fluctuating link qualities. This adds complexity to route selection and maintenance.

* Scalability: Wireless networks can have a large number of nodes, and routing protocols need to scale efficiently to support such networks.

* Security: Wireless networks are more susceptible to security threats due to the open nature of the medium, making secure routing a significant concern.

### What are the advantages of sending information over multiple wireless hops compared to a single hop? What are the disadvantages?
**Answer:** 

Advantages of multi-hop communication:

* Increased range: Multi-hop communication allows data packets to travel longer distances by forwarding them through intermediate nodes.
* Improved connectivity: Multi-hop communication can provide alternate paths to bypass areas with poor signal quality or network congestion.
* Reduced transmission power: By forwarding packets over shorter distances between intermediate nodes, devices can use lower transmission power, potentially conserving energy.


Disadvantages of multi-hop communication:

* Increased latency: Transmitting data over multiple hops introduces delays due to processing, queuing, and transmission time at each intermediate node.
* Higher energy consumption: The total energy consumption may increase due to the combined energy usage of all the intermediate nodes involved in the communication.
* Increased complexity: Multi-hop communication requires more complex routing algorithms and protocols to manage and maintain routes.

### From an energy consumption and reliability perspective, is it better to send data over one hop or multiple hops?
**Answer:** The choice between one-hop and multi-hop communication depends on the specific scenario and network conditions. In some cases, one-hop communication can be more energy-efficient and reliable, as it avoids the additional energy consumption and potential failure points introduced by intermediate nodes. However, in other scenarios, multi-hop communication can provide better energy efficiency and reliability by reducing transmission power and providing alternate paths through the network. Ultimately, the best approach will depend on factors such as network topology, node density, and communication requirements.

### What are some simple routing solutions?
**Answer:** Some simple routing solutions include:

* Static routing: Predefined routes are manually configured by a network administrator. This is suitable for small networks with a stable topology but is not scalable or adaptable to dynamic networks.
* Flooding: Data packets are broadcast to all neighboring nodes, which in turn forward the packets to their neighbors until the destination is reached. This guarantees delivery but can cause high network overhead and congestion.
* Random walk: Data packets are forwarded to a randomly chosen neighbor at each hop until the destination is reached. This is a simple and decentralized approach but can result in long and inefficient routes.

### What is reactive routing?
**Answer:** Reactive routing, also known as on-demand routing, is a type of routing protocol used in wireless networks, particularly in mobile ad hoc networks (MANETs) and wireless sensor networks (WSNs). In reactive routing, routes are discovered and established only when needed, as opposed to proactive routing, where routes are maintained continuously regardless of actual communication demands. The primary components of reactive routing include:

* Route discovery: When a source node needs to send data to a destination node, it initiates a route discovery process to find a suitable route. This usually involves broadcasting route request packets throughout the network until the destination node or an intermediate node with a valid route is reached.
* Route maintenance: Once a route is established, it is maintained as long as it is needed for communication. If a link within the route fails, the route is either repaired or a new route discovery process is initiated.
* Route expiration: Unused routes may be discarded after a certain period of inactivity to save resources and maintain up-to-date routing information.

Reactive routing protocols can be more efficient in terms of bandwidth and energy consumption compared to proactive protocols, especially in dynamic networks with changing topologies and sporadic communication patterns. However, they may introduce higher latency due to the route discovery process. Some examples of reactive routing protocols include Ad hoc On-Demand Distance Vector (AODV) and Dynamic Source Routing (DSR).

### What is AODV protocol? Where is it commonly used?
**Answer:** The Ad hoc On-Demand Distance Vector (AODV) protocol is a reactive routing protocol used in mobile ad hoc networks (MANETs) and wireless sensor networks (WSNs). AODV discovers routes only when needed, minimizing overhead and conserving resources in dynamic networks where nodes frequently join, leave, or move within the network. AODV is commonly used in situations where establishing a fixed network infrastructure is impractical or unnecessary, such as military communications, emergency response, or temporary event setups.

### What are various messages sent in AODV protocol?
**Answer:** There are three main types of messages used in the AODV protocol:

* Route Request (RREQ): When a source node needs to send data to a destination node and does not have a valid route, it broadcasts an RREQ message to its neighbors. The RREQ contains the source and destination addresses, as well as sequence numbers to ensure fresh routing information.

* Route Reply (RREP): When the RREQ reaches the destination node or an intermediate node with a valid route to the destination, an RREP message is sent back to the source node, either unicast or piggybacked on the data packet. The RREP contains the route information, such as hop count and sequence numbers.

* Route Error (RERR): When a link in an active route breaks, the node detecting the failure sends an RERR message to its upstream neighbors, informing them of the broken link. Upon receiving the RERR, nodes remove the invalid route from their routing tables and may initiate a new route discovery if necessary.

### What is dynamic source routing protocol?
**Answer:** Dynamic Source Routing (DSR) is a reactive routing protocol designed for use in mobile ad hoc networks (MANETs) and wireless sensor networks (WSNs). It discovers routes on-demand and utilizes source routing, which means that the entire route is included in the data packet's header. The main components of DSR include:

* Route discovery: When a source node needs to send data to a destination node and lacks a valid route, it initiates a route discovery process by broadcasting a route request. The request contains the source and destination addresses and a route record, which accumulates the traversed nodes.

* Route reply: When the destination node or an intermediate node with a valid route receives the request, it sends a route reply back to the source node. The reply contains the complete route, which is then used for data transmission.

* Route maintenance: If a link in the active route fails, route maintenance is performed by sending a route error message to the source node, which can then initiate a new route discovery if needed.

DSR is well-suited for networks with low to moderate mobility and traffic, but its reliance on source routing can lead to large packet headers and increased overhead in larger or more dynamic networks.

### What is reactive and proactive routing? What is the tradeoff between these two schemes?
**Answer:** Reactive and proactive routing are two distinct approaches to routing in wireless networks, particularly in mobile ad hoc networks (MANETs) and wireless sensor networks (WSNs):

* Reactive routing: Reactive routing protocols, also known as on-demand routing protocols, discover and establish routes only when needed. This reduces routing overhead and conserves resources in networks with dynamic topologies and sporadic communication patterns. However, reactive routing can introduce higher latency due to the route discovery process. Examples include AODV and DSR.

* Proactive routing: Proactive routing protocols continuously maintain up-to-date routing information, even when no communication is taking place. This ensures lower latency when initiating data transmission but can lead to higher overhead and resource consumption due to constant route updates. Examples include Optimized Link State Routing (OLSR) and Destination-Sequenced Distance Vector (DSDV) routing.

The tradeoff between reactive and proactive routing lies in balancing overhead, latency, and resource consumption. Reactive routing is generally more suitable for dynamic networks with infrequent communication, while proactive routing is better suited for more stable networks with consistent communication patterns.

### What are some possible routing metrics in a mesh IoT network?
**Answer:** Various routing metrics can be used to determine the best route in a mesh IoT network:

* Hop count: The number of intermediate nodes between the source and destination. Lower hop count routes are generally preferred.
* Link quality: The quality of individual links in the route, which can be influenced by factors like signal strength, interference, and packet loss.
* Latency: The time it takes for a data packet to travel from the source to the destination.
* Bandwidth: The available capacity on the links in the route, which can impact the overall throughput.
* Energy consumption: The amount of energy required to transmit data along the route, which is particularly important in battery-powered IoT networks.
* Reliability: The probability of successful data delivery along the route, considering factors like link quality, interference, and node failures.


### What is ETX as a routing metric? How do you estimate it?
**Answer:** Expected Transmission Count (ETX) is a routing metric that estimates the number of transmissions required to successfully send a data packet over a wireless link. The lower the ETX value, the better the link quality. ETX considers factors such as packet loss rates and retransmissions, making it a more accurate representation of link quality than just considering hop count or signal strength.

ETX is typically estimated by exchanging probe packets between neighboring nodes. Nodes periodically send probe packets to their neighbors, which in turn, acknowledge the successful reception of these packets. By measuring the packet loss rates in both directions, nodes can calculate the ETX value for each link. The formula for ETX is:

ETX = 1 / (delivery rate in forward direction * delivery rate in reverse direction)

### Can you add ETX together?
**Answer:** Yes, ETX values can be added together to compute the cumulative ETX for a multi-hop route. By summing the ETX values of all individual links in the route, you can obtain an overall estimate of the route's quality. Lower cumulative ETX values indicate better routes with fewer expected transmissions and higher reliability. This approach allows routing algorithms to choose more efficient and reliable paths in wireless networks, especially in mesh IoT networks where link quality can vary significantly.

### Is a wireless link with the lowest hop count always the one with lower ETX? Give an example.

**Answer:** No, a wireless link with the lowest hop count does not always have a lower ETX value. ETX considers factors like packet loss rates and retransmissions, while hop count only considers the number of intermediate nodes. A route with fewer hops may have worse link quality or higher packet loss, leading to a higher ETX value.

Example: Consider two routes between a source and destination node:

Route A: 2 hops, with link qualities of 90% and 80% (ETX = 1 / (0.9 * 0.8) = 1.389)
Route B: 3 hops, with link qualities of 95%, 95%, and 95% (ETX = 1 / (0.95 * 0.95 * 0.95) = 1.106)
In this example, Route B has a higher hop count but a lower ETX value, indicating better overall link quality and fewer expected transmissions.

### What is a mobile ad hoc network?
**Answer:** A mobile ad hoc network (MANET) is a self-configuring, decentralized network of mobile devices connected wirelessly without the need for fixed infrastructure or centralized administration. Nodes in a MANET can communicate directly with each other or through intermediate nodes, using multi-hop communication when necessary. MANETs are highly dynamic, as nodes can join, leave, or move within the network, causing frequent topology changes. They are typically used in scenarios where establishing a fixed network infrastructure is impractical, such as military communications, disaster relief, and temporary event setups.

### What is a delay-tolerant network?
**Answer:** A delay-tolerant network (DTN) is a network designed to operate under challenging conditions, where connectivity may be intermittent, and end-to-end paths may not always exist. DTNs use a "store-and-forward" approach, in which data is stored at intermediate nodes and forwarded when a suitable next-hop becomes available. This allows DTNs to tolerate long delays, high packet loss rates, and frequent network partitions. DTNs are used in scenarios where traditional networking protocols may fail, such as deep-space communication, remote sensing, and disaster response.

### How is routing in sensor (IoT) networks different from other wireless networks?
**Answer:** Routing in sensor or IoT networks differs from other wireless networks due to several factors:

* Resource constraints: IoT devices often have limited processing power, memory, and battery life, necessitating energy-efficient and lightweight routing protocols.
* Scalability: IoT networks can have a large number of nodes, requiring scalable routing solutions that can handle high node density.
* Data-centric communication: In IoT networks, communication is often data-centric rather than node-centric, with data aggregation and in-network processing playing crucial roles.
* Network topology: IoT networks may have a hierarchical or flat topology, affecting the choice of routing protocols and algorithms.

As a result, routing in IoT networks often focuses on minimizing energy consumption, maximizing network lifetime, and supporting data aggregation and in-network processing.

## POLICY REGARDING USING AI TOOLS


**IMPORTANT:** It is important to note that Large Language Models (LLMs) are still in the early stages of development and may not always produce accurate results. Therefore, these tools should only be used as a supplement, not as the primary source of information, and one should use them with caution.
