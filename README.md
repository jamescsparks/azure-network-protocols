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
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1 Deploy Two Virtual Machines
- Step 2 Install and Configure Wireshark
- Step 3 Test Common Protocols
- Step 4 Modify NSG Rules

<h2>Actions and Observations</h2>


![86C346CB-58B7-4521-82D2-99E77D0A7C04](https://github.com/user-attachments/assets/a00a5eb8-04ed-4462-87a1-cea92f223e74)

</p>
<p>
Step 1: Deploy Two Virtual Machines
Set up one Windows 10 VM and one Ubuntu Server VM within the same virtual network and subnet.
Ensure both VMs are accessible via public IP or RDP/SSH as needed.
<p>
Step 2: Install and Configure Wireshark
On the Windows 10 VM, install Wireshark to monitor and capture network traffic.
Set the correct network interface for packet capture.
</p>
<br />

![935CF83F-9985-48C1-8307-3722B358F493](https://github.com/user-attachments/assets/f2fe9946-7281-43f4-a492-78aa1a29e227)

</p>
<p>
Step 3: Test Common Protocols
From the Ubuntu VM, initiate traffic such as:
ping (ICMP)
curl to HTTP/HTTPS sites
nslookup or dig for DNS
SSH sessions
Observe corresponding packets in Wireshark on the Windows VM.
<p>
Step 4: Modify NSG Rules
Navigate to Azure NSG settings for the subnet or NIC.
Create or adjust inbound and outbound rules (e.g., block ICMP, allow only HTTP).
Re-run traffic tests and observe the effect in Wireshark.
Record whether traffic is allowed or denied based on NSG rule
</p>
<br />

![13D3E25F-C108-48D1-895F-3F7E7C9BDB7C_4_5005_c](https://github.com/user-attachments/assets/708afe31-26c5-476a-bc33-abd3122298f8)

</p>
<p>
</p>
<br />
