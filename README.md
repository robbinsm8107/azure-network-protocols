<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 22.04

<h2>High-Level Steps</h2>

- We created a Resource Group with two Azure Virtual Machines. One of these Virtual Machines has a Windows 10 operating system and the other is utilizing Ubuntu 22.04
- We then installed Wireshark on the Windows 10 Virtual Machine. This is a packet analyzer that will allow you to see the actual packet transmission between the two virtual machines
- We then analyzed the packets within Wireshark for some of the most common protocols (SSH, RDH, DNS, HTTP/S, ICMP)

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/J2zAB58.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The first thing we did was utilize the Azure Subscription to create a "Resource Group". If you think of your Azure Subscription as its own "Computer", then a Resource Group can be thought of as a "Subdirectory" within this large "Computer". This is a way for you to create a grouping for a project and keep the various aspects and resources alienated. This makes it easier to keep track of the various projects that you are working on within the Azure Cloud Space. 
</p>
<br />

<p>
<img src="https://i.imgur.com/iwpq53g.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We then searched for the Wireshark application download within the Windows 10 Virtual Machine. Wireshark is a network protocol analyzer that has a multitude of uses through various aspects of Information Technology. For instance, when I was studying for the Cisco CCNA exam, we utilized Wireshark for various packet capture and analysis to gain a better understanding of the various packets and what is actually being sent within the packets. The Wireshark application has a vast amount of uses and we are just scratching the surface in this project to see the difference between some of the most commonly used packets in your day-to-day life as an Information Technology Professional. 
</p>
<br />

<p>
<img src="https://i.imgur.com/eGHyzX1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The final step was to actually utilize protocols and capture sackets to see the information presented. The screenshot I chose to use for this project was the most interesting in my opinion because I was able to utilize the SSH protocol over TCP Port 22 to securely log into my Ubuntu Virtual Machine. You can see the Key Exchange, the protocol used, and the actual logging into the second server via the Windows Command Prompt within this Windows Virtual Machine. A few examples of hod other protocols include running a permanent ping between the Virtual Machines "ping ip address -t" while enabling and disabling ICMP. While disabled, the Windows Virtual Machine kept sending Echo Requests but there were no Echo Replies sent back from the Ubuntu virtual machine.

I was able to see RDP TCP Port 3389 as soon as I turned on Wireshark because I was utilizing Remote Desktop Protocol from my personal computer. I was able to utilize "nslookup example.com" to see Domain Name System utilization of TCP/UDP Port 53 also. I was able to see the difference between HTTP TCP Port 80 and HTTPS TCP Port 443 by browsing different websites. If the website is not currently utilizing an SSL certificate, then you would only be browsing through TCP Port 80 which would not secure the web traffic over the internet. SSL Certificates are a very interesting concept, and I hope to dive into this in more detail in a later project.
</p>
<br />
