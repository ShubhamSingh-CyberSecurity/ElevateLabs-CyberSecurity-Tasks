Elevate Labs - Cyber Security Internship – Task 1

Task Title: Scan Your Local Network for Open Ports

Objective:  
-Discover open ports on devices in your local network using Nmap and analyze network traffic with Wireshark
 to understand service exposure and potential security risks.
Tools Used:
- Nmap – For scanning the local network and identifying open ports.  
- Wireshark– For capturing and analyzing packet-level details during the port scan.
---------------------------------------------------------------------------------------------
Steps Performed:

1. Identified Local IP Range
Command used to find local IP: ipconfig  
Command used to TCP SYN Scan using nmap: nmap -sS 192.168.119.149 -oN scan_result.txt (to save the output record in .txt file)  
2. While executing nmap command i started wireshark Start Capture & after nmap result saved it as wireshark_scan_capture.
3. To analyze Wireshark Packet i used the command tcp.flags.syn == 1 && tcp.flags.ack == 0
 What Was Observed:
 - Nmap sends TCP SYN packets to each IP and port.
 - If the port is open, the target responds with SYN-ACK.
 - If the port is closed, the target responds with RST.
 - These patterns were clearly visible in Wireshark.
 - This file also contain the output screenshot after performing this command.
