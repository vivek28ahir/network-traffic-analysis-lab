# Network Traffic Analysis Lab (Kali Linux)

## Overview
This project demonstrates hands-on network traffic analysis using Wireshark in a Kali Linux environment. The goal was to capture live network traffic, analyze different protocols, and identify both normal and potentially suspicious behavior.

---

## Tools Used
- Kali Linux
- Wireshark
- Nmap
- curl
- ping

---

## Lab Activities
- Captured live traffic using Wireshark
- Generated ICMP traffic using ping
- Generated HTTP traffic using curl
- Performed port scanning using Nmap
- Applied filters to analyze protocols

---

## Screenshots

### 1. Interface Selection
![Interface Selection](screenshots/1-opening-wireshark.png)

### 2. Starting Packet Capture
![Start Capture](screenshots/2-start-capturing.png)

### 3. ICMP Traffic (Ping)
![ICMP Traffic](screenshots/3-ping-google.png)

### 4. Generating ICMP Traffic (Ping Test)
![PING](screenshots/4-curl-examplecom.png)

### 5. Generating HTTP Traffic (Web Request using curl)
![HTTP Traffic](screenshots/5-nmap-localhost.png)

### 6. Captured Network Traffic Overview
![Captured Traffic](screenshots/6-traffic-captured.png)

### 7. ICMP Traffic Analysis Using Filter
![ICMP Filter](screenshots/7-icmp-traffic.png)

### 8. HTTP Traffic Analysis Using Filter
![HTTP Traffic](screenshots/8-http-traffic.png)

### 9. TCP Traffic Analysis Using Filter
![TCP Traffic](screenshots/9-tcp-traffic.png)

### 10. Detection of Suspicious Traffic (SYN Scan Behavior)
![SYN Scan](screenshots/10-suspicious-traffic.png)

---

## Key Findings
- Identified ICMP request/reply behavior
- Observed DNS resolution before web communication
- Analyzed TCP three-way handshake
- Captured HTTP requests and responses (200 OK, 301 Redirect)
- Detected SYN scan behavior using packet filtering

---

## Security Insight
SYN packets without ACK responses were detected using:
tcp.flags.syn == 1 and tcp.flags.ack == 0
This pattern is commonly associated with port scanning activity.

---

## Report
Full detailed report available in the `/report` folder.

---

## Skills Demonstrated
- Network traffic analysis
- Packet inspection using Wireshark
- Protocol analysis (ICMP, TCP, HTTP, DNS)
- Detection of reconnaissance activity
- Hands-on cybersecurity lab experience

## Project Structure

```
network-traffic-analysis-lab/
├── README.md
├── report/
│   └── network_analysis_report.pdf
├── screenshots/
│   ├── 1-opening-wireshark.png
│   ├── 2-start-capturing.png
│   ├── 3-ping-google.png
│   ├── 4-curl-examplecom.png
│   ├── 5-nmap-localhost.png
│   ├── 6-traffic-captured.png
│   ├── 7-icmp-traffic.png
│   ├── 8-http-traffic.png
│   ├── 9-tcp-traffic.png
│   └── 10-suspicious-traffic.png
```