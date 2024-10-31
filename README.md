# Network Traffic Analysis (TCP Dump)

## Overview

In this lab, we explore network traffic analysis using **TCP Dump** and **Wireshark**. We will demonstrate the installation and usage of these tools on different operating systems, focusing on how they can capture, analyze, and manipulate network packets.

<h2>Table Contents </h2>

- [1.1	Intro to TCP dump and basic commands](https://github.com/Mumo01)
- [1.2	Running TCP dump and sniffing network traffic](https://github.com/Mumo01)
- [1.3	Analyzing Hex and ASCII](https://github.com/Mumo01)
- [1.4	Create a backdoor with Netcat](https://github.com/Mumo01)

### Machines Used

- Kali Linux
- Metasploitable
- Mac (Host)
- Windows

## 1. TCP Dump

### 1.1 Introduction to TCP Dump and Basic Commands

- Check all interfaces on the Kali machine.
- <img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
- The interfaces of interest are Ethernet and Loopback: `eth0` and `lo`.

### 1.2 Running TCP Dump and Sniffing Network Traffic

- **Scenario**: A ping request between two machines.
- **Context**: This scenario is reminiscent of the famous Target Breach, where attackers compromised the HVAC system and began sending ping requests to the cash register.

- <img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  **Key Issues**:
  - Why was the HVAC able to successfully ping the Cash Register?
  - Why did the pinging go unnoticed during the attack?

### 1.3 Analyzing HEX and ASCII Data

- In the analysis, the highlighted area indicates the attackers switched to pinging customer credit card details.
- <img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
- This can be observed through the HEX and ASCII data captured.

### 1.4 Creating a Backdoor with Netcat

<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
- Opened port `4444` and instructed Netcat (`nc`) to listen on this port (`-l -p 4444`).

  ```bash
  nc -l -p 4444
