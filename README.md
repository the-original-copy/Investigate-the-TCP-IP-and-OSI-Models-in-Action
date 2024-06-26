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

<div align="center">
  
![ScreenShot](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/771f46dc-1138-464c-b2c8-dfd0cc7a07bf)
<br/>Image 1: Simulation mode selected 

</div> 

b)
Selected HTTP from the event filter list by unchecking all the check boxes and then selected HTTP from the Misc tab as shown below:

<div align="center">
  
![ScreenShot](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/c7ed5d8e-74bf-4054-b778-5861e972afd1)
<br/>Image 2 : HTTP is the selected option in the event filters

</div>

The IPv4 and IPv6 options remain unchecked as shown below:

<div align="center">

![ScreenShot](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/3a056f5e-3a68-4aed-a986-530ed228457b)
<br/>Image 3 : IPv6 Event filter list

</div>

<div align="center">

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/7ccbabf1-f080-44ad-b180-ded9a6286980)
<br/>Image 4 : IPv4 Event Filter list

</div>

### Step 2: Generate web (HTTP) traffic

a)

Opened the web browser of the web client, inputed www.osi.local in the search field and run the search. The picture below shows the web client browser being used to perform the search operation:

<div align="center">
  
![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/6c61c86f-bce9-48c6-81ab-938bad4c31d1)

</div>

b) 

Run the search in the browser. Clicked the capture/forward button for times and four event showed up in the event list as shown below:

<div align="center">
  
![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/81b47dac-6076-4f38-8df6-990bf17a57b3)
<br/>Image 5: The events that popped up after running the search

</div>

The web client browser page changed to:

<div align="center">
  
![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/b763ad64-0b3c-4ceb-987c-6f9e53eb1b05)

</div>

### Step 3: Explore the contents of the HTTP packet
a)
Clicked the first colored box under the Event List > Type column and below was the output:

<div align="center">
  
![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/fa5fb8b9-579d-49a0-abe5-61ccd16135aa)
<br/>Image 6 : Details after clicking the first colored box

</div>
b)

I ensured the OSI Model tab and clicked layer 7. 
The information displayed directly below the layers and out layers boxes for layer 7 is: 1. The HTTP client sends a HTTP request to the server
* This can be confirmed by going to image 6.
The Dst Port value for Layer 4 under the Out Layers column is: 80
* This can be confirmed by going to image 6.
The Dest. IP value for Layer 3 under the Out Layers column is : 192.168.1.254
* This can be confirmed by going to image 6

The information displayed at Layer 2 under the Out Layers column is as follows:

1.The next-hop IP address is a unicast. The ARP process looks it up in the ARP table
2.The next-hop IP address is in the ARP table. The ARP process sets the frame’s destination
3.The device encapsulates the PDU into an Ethernet frame

This can be confirmed using the picture below:
<div align="center">
  
![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/1de835f2-7ae8-42e5-91f5-be780e07c054)
</br> Image 7: Information displayed at Layer 2

</div>
c)

Opened the Outbound PDU details tab as shown below:

<div align="center">

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/3e3a2c18-87e5-469e-915f-850b67c1a77d)
<br/>Image 8 : Outbound PDU details tab

</div>

The common information listed under the IP section as compared to the information listed in the OSI Model tab is:
The source IP which is: 192.168.1.1 and the Dest IP which is: 192.168.1.254. It is associated with Layer 3 in the OSI model as shown in the pictures below:

<div align="center">

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/bb8952b9-b1c7-4f6c-a325-5ddb680cdc62)
<br/>Image 9: OSI Model

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/a2867213-1e72-4036-a174-68a2b62e9a1e)
<br/>Image 10: Outbound PDU the IP section

</div>

The common information listed under the TCP section of the outbound PDU details compared to the OSI Model is: The source port which is 1025 and the destination port which is 80. The OSI layer that is associated with this information is layer 4 as shown in the pictures below:

<div align="center">

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/277c45e9-edb8-4543-bdaf-e8069aa1a4e1)

</div>

The host listed under the HTTP section in the Outbound PDU Details is:

The host can not be identified from the given information in the PDU since its not listed. This information would be typically liked with layer 7 since the HTTP request header contains info such as accepted languages.

<div align="center">

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/b2c13a28-8b27-4a5e-bcbb-07204fb368a5)
<br/>Image 11: Not enough information in the request header to know the host

</div>

d) 
Clicked the next colored square and only layer one was active as shown below:

<div align="center">

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/d3d01182-d5d0-4539-b61a-009db355fb19)

</div>

e)

Clicked the next colored square and it contained both In layers and Out Layers as shown in the picture below:

<div align="center">

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/1c4fb93e-b4cb-40ce-932f-664e9f52c517)

</div>


The major differences between the 2 layers are:

1. In layer 4 , the in layer has a TCP src port of 1025 and a Dst port of 80 while the out layer has a TCP Src port of 80 <br/> and a Dst port of 1025
2. In layer 3, the IP Header Src. IP of the in layer is 192.168.1.1 and a Dest IP of 192.168.1.254 while the IP Src    <br/>header of the out layer is 192.168.1.254 while the Dest Header is 192.168.1.1
3. In layer 2, the in layer Ethernet 2 header is 0060.47CA.4DEE(Sender’s MAC Address) >> 0001.96A9.401D(Receiver MAC address) while the out layer has the Ethernet 2 header as 0001.96A9.401D(Sender’s MAC Address) >>  0060.47CA.4DEE(Receiver MAC address)

f) 
Clicked the inbound and outbound packet details as shown below:

<div align="center">
  
![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/2c83a211-4792-4c0c-8c69-d3b67fd70bcc)
<br/>Image 12: Inbound PDU details

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/48638c94-bc64-4a35-a99f-8d7fe547738d)
<br/>Image 13: Outbound PDU details
</div>

## Part 2: Display Elements of the TCP/IP Protocol Suite

### Step 1: View Additional Events

a)
Additional events that shows all the protocols used in the TCP/IP Protocol suite are as shown below:


<div align="center">

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/1ec0a15f-6e8b-4aae-9f32-26c9d29503ba)
</div>

b) 
Clicked the first DNS event in the **Type** column and explored the **OSI Model** and **PDU Details** tabs in order to note the encapsulation processes as shown below:

<div align="center">

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/a96c3211-6649-4726-8175-f6cd85466d0a)

Image 14: DNS OSI Model<br/>

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/9f1c279a-d8f2-42b8-8f09-7b81491f0be9)

Image 15: DNA PDU Details<br/>
</div>

c) 
In the DNS Query tab what is listed in the **NAME** field in the DNS QUERY section is www.osi.local as shown in the picture below:

<div align="center">

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/d065a810-8fb0-444c-9847-d9f6fa3faf36)

</div>

d) 
In order to see at which device the PDU was captured I clicked in the last DNS **info** colored square box in the event list. This information would be listed in the value with the field called **ADDRESS** as shown in the series of pictures below:

<div align="center">

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/cb45d603-5590-431e-81c0-c5abe8ab4742)

Image 16: OSI Model PDU Information

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/edfa96f3-ec51-4b7a-95f0-5fe384b7edae)

Image 17: Inbound PDU Information

</div>

The value listed next to address is non-existent since there is no field listed as **ADDRESS**  as shown below:

<div align="center">

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/77f19332-264c-4199-b7f8-dfbd5a3af011)

Image 18: DNS Answer Section

</div>

e)
Found the first HTTP event and then clicked the next TCP following the HTTP event and the OSI model Produced was as follows:

<div align="center">

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/cec67a3f-161c-4ae9-8e9e-ebf3d95a611b)

</div>

The information listed under items 4 and 5 are:
**4 -> The TCP connection is successful**
**5 -> The device set the connection state to be ESTABLISHED**

f)
I clicked the last TCP event and received and OSI model that looks as shown below:

<div align="center">

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/a318da86-f5f6-403b-acb2-a3ed1b2a9ddd)

Image 19: The OSI Model<br/>

</div>


This event is meant to close the connection between the communicating devices since the necessary information has been transmitted to the required parties.


##Challenge Questions

To know what port number the web server is listening for the web request I went to the web server’s first HTTP instance and clicked the colored square. Based on the information recieved the port number is : **1025**

<div align="center">

![image](https://github.com/the-original-copy/Investigate-the-TCP-IP-and-OSI-Models-in-Action/assets/77143082/a3e2cdc6-99aa-49a2-ba1e-d4cfa520c03e)
<br/>Image 20: OSI Model For the first HTTP instance of the web server

</div>

# Conclusion

In conclusion, this lab provided a comprehensive introduction to the TCP/IP protocol suite and its correlation with the OSI model. Through Packet Tracer's simulation mode, we gained valuable insights into the encapsulation process of data as it traverses through the network layers. By dissecting the data into smaller pieces known as protocol data units (PDUs) and associating them with specific layers, I deepened my understanding of how information flows across the network. Lastly this lab served as a foundational exploration of Packet Tracer's functionality and the visualization of encapsulation processes.










