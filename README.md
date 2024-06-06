# Investigate-the-TCP-IP-and-OSI-Models-in-Action

## Introduction

The goal of this simulation exercise is to provide me with a basic understanding of the TCP/IP protocol suite and how it relates to the OSI model. I saw the contents of the data being transported over the network at each tier by using the simulation mode.
Data is detected and divided into smaller parts as it travels across the network, allowing the pieces to be assembled at the destination. Every component has a unique name (protocol data unit [PDU]) and is connected to a particular OSI and TCP/IP layer. Viewing every layer and its corresponding PDU is possible when using the Packet Tracer simulation mode. 

## Objectives

1. Provide a base level understanding of the TCP/IP protocol suite and its relationship to the OSI model <br/>
2. View the protocol layers and the associated PDU

## Methodology

### Part 1: Examine HTTP Web Traffic
### Step 1: Switch from realtime to simulation mode

a) Selected the simulation mode as shown in the diagram below:

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/eb826b6b-453c-4998-bc1a-38a8b7a71c32)

Image 1: Simulation mode selected 

b)
Selected HTTP from the event filter list by unchecking all the check boxes and then selected HTTP from the Misc tab as shown below:

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/c7ed5d8e-74bf-4054-b778-5861e972afd1)
Image 2 : HTTP is the selected option in the event filters

The IPv4 and IPv6 options remain unchecked as shown below:

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/3a056f5e-3a68-4aed-a986-530ed228457b)
<br/>Image 3 : IPv6 Event filter list

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/7ccbabf1-f080-44ad-b180-ded9a6286980)
<br/>Image 4 : IPv4 Event Filter list

### Step 2: Generate web (HTTP) traffic

a)

Opened the web browser of the web client, inputed www.osi.local in the search field and run the search. The picture below shows the web client browser being used to perform the search operation:

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/6c61c86f-bce9-48c6-81ab-938bad4c31d1)

b) 

Run the search in the browser. Clicked the capture/forward button for times and four event showed up in the event list as shown below:

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/81b47dac-6076-4f38-8df6-990bf17a57b3)
<br/>Image 5: The events that popped up after running the search

The web client browser page changed to:

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/b763ad64-0b3c-4ceb-987c-6f9e53eb1b05)


### Step 3: Explore the contents of the HTTP packet

