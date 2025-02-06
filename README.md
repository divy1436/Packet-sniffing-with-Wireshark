# Wireshark Installation Guide for Linux

Wireshark allows you to capture and analyze network traffic in real-time. Follow the steps below to install it on your Linux distribution.

## Installation Steps

| **Step**   | **Command (Debian/Ubuntu)**             | **Command (Fedora)**        | **Command (Arch Linux)**      |
|------------|--------------------------------------|----------------------------|------------------------------|
| **Update System** | `sudo apt update && sudo apt upgrade -y` | `sudo dnf update -y` | `sudo pacman -Syu` |
| **Install Wireshark** | `sudo apt install wireshark -y` | `sudo dnf install wireshark -y` | `sudo pacman -S wireshark-gtk` |
| **Allow Non-Root Users** | `sudo usermod -aG wireshark $USER` | `sudo usermod -aG wireshark $USER` | `sudo usermod -aG wireshark $USER` |
| **Verify Installation** | `wireshark --version` | `wireshark --version` | `wireshark --version` |

## Running Wireshark
To start Wireshark, use:
```bash
wireshark
