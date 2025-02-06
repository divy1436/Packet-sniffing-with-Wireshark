# 📡 Packet Sniffing with Wireshark on Linux

Wireshark is a powerful tool for capturing and analyzing network traffic. It provides deep insight into network communications and helps diagnose performance issues and security threats.

---

## 🔍 What is Wireshark?
Wireshark is an open-source network protocol analyzer that captures and inspects packet data in real-time. It supports multiple protocols, providing detailed analysis to troubleshoot network-related problems.

### **Key Features:**
- Live packet capture and offline analysis
- Deep inspection of protocols such as TCP, UDP, HTTP, and DNS
- Ability to apply complex filters for targeted analysis
- Export and save packet captures for later review

---

## 🛠️ Installation
If Wireshark is not installed, install it using:

```bash
sudo apt update && sudo apt install wireshark -y
```
For **Fedora**:
```bash
sudo dnf install wireshark
```

---

## 🚀 Running Wireshark
If installed, launch it with:

```bash
sudo wireshark
```

To run Wireshark **without root privileges**, add your user to the `wireshark` group:

```bash
sudo usermod -aG wireshark $USER
newgrp wireshark
```

---

## 📊 Command Guide

| 🎯 **Action**                | 💻 **Command**                                  | 🔍 **Description** |
|-----------------------------|----------------------------------------------|----------------|
| Run Wireshark as root       | `sudo wireshark`                            | Starts Wireshark with full privileges |
| Run Wireshark without root  | `sudo usermod -aG wireshark $USER`          | Adds the user to the Wireshark group |
| Start capture from terminal | `sudo tshark -i wlan0`                     | Captures packets from interface `wlan0` |
| Capture only HTTP packets   | `sudo tshark -i wlan0 -f "tcp port 80"`     | Filters traffic for TCP port 80 |
| Save captured packets       | `sudo tshark -i wlan0 -w capture.pcap`      | Saves packets to a file for later analysis |
| Open saved packets          | `wireshark capture.pcap`                    | Opens a `.pcap` file in the GUI |

---

## 🎯 Filtering in Wireshark

| 🔍 **Filter**               | 📌 **Usage** |
|----------------------------|-----------|
| `http`                     | Show only HTTP traffic |
| `tcp`                      | Show only TCP packets |
| `ip.addr == 192.168.1.1`   | Show packets from/to a specific IP |
| `udp.port == 53`           | Show only DNS traffic |

---

## 🔧 Other Network Analysis Tools
Apart from Wireshark, here are some other powerful tools for network monitoring and packet analysis:

| 🛠️ **Tool**            | 🔍 **Description** |
|----------------------|------------------|
| **tcpdump**         | Command-line packet analyzer for capturing network traffic |
| **Nmap**            | Network scanner for discovering hosts and services |
| **Netcat (nc)**     | Utility for reading and writing data across network connections |
| **iftop**           | Real-time bandwidth usage monitoring |
| **ngrep**           | Network packet matcher, similar to `grep` for network traffic |

---

## 💾 Saving the Capture
To save captured traffic:
```bash
sudo tshark -i wlan0 -w my_capture.pcap
```
Then, open the file in Wireshark:
```bash
wireshark my_capture.pcap
```

---

### ✅ Now you can use Wireshark and other tools to analyze network traffic efficiently! 🚀
