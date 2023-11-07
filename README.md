<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, HTTP/S, DNS, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (22H2)
- Ubuntu Server 20.04

<h2>What we will be obseving inside of Wireshark</h2>

- Source
- Destination
- Protocol
- Length info

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/ZJao03s.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

 <p>
<img src="https://i.imgur.com/6xJBrvx.png="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p> 
  
  So if you look at the screenshot above, you can see all of the different things that we can look at when observing network traffic using Wireshark. To do this all you have do is once Wireshark is open, if you look at the top of the screen you should see a filter bar in which you can type whichever protocol you would like to observe and analyze.
</p>
<br />

<h2>ICMP Command lines</h2>

- Ping (Private IP Address) of the other Computer
- Ping (Domain names like www.google.com ) into a readable IP Address
- Ping (example: 10.0.0.5 -t)
- Press CTRL+C on your keyboard to stop the perpetual ping



<h2>Connecting to a SSH Command Line</h2>
 
 - ssh (Username)(@)(Private IP Address)
- Enter the password: Password1 (example)
- Type ‘exit’ to leave

<p>
<img src="https://i.imgur.com/lPvFep0.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<h2>DHCP Command line</h2>

 - ipconfig /renew (will attempt to create a fresh IP address on the computer)

<p>
<img src="https://i.imgur.com/0ZPUicr.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<h2>DNS Command line</h2>

- nslookup www.google.com

<p>
<img src="https://i.imgur.com/1y86tBc.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<h2>Allow/Deny one of the protocols inside of the Network Security Group within Azure</h2>

*Steps*
Network Security Group > Inbound Rules > + Rule > Type; DENY_ICMP_PING_FROM_ANYWHERE

<p>
<img src="https://i.imgur.com/FeAKaNG.jpg height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
