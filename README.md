# Metasploitable2 Network Scanning Using Nmap

## Introduction
Nmap (Network Mapper) is an open-source network scanning and security auditing tool.
It is used to discover active hosts, identify open ports, and detect running services.
It helps security professionals understand network configurations and identify potential security risks.

## Tools Used
- Kali Linux
- Nmap
- Metasploitable 2

## Target Information
- Target Machine: Metasploitable 2
- Target IP Address: `192.168.204.135`

## Scanning Techniques and Commands

### 1. Host Discovery
**Command:** `nmap -sn 192.168.204.135`

This command checks whether the target host is active on the network.
It performs host discovery without conducting a port scan.

### 2. Scan Techniques – SYN Scan
**Command:** `sudo nmap -sS 192.168.204.135`

This command performs a TCP SYN scan to identify open ports.
It is commonly known as a half-open scan.

### 3. Port Specification – Fast Scan
**Command:** `nmap -F 192.168.204.135`

This command scans the 100 most common TCP ports.
It provides a quick overview of commonly used open ports.

### 4. Service and Version Detection
**Command:** `nmap -sV 192.168.204.135`

This command identifies services running on open ports.
It also attempts to determine the software versions of those services.

### 5. Script Scanning
**Command:** `nmap --script=http-title -p 80 192.168.204.135`

This command uses Nmap's HTTP title script to retrieve the webpage title.
It helps identify basic information about the HTTP service running on port 80.

### 6. OS Detection
**Command:** `nmap -O 192.168.204.135`

This command attempts to identify the operating system running on the target machine.
It uses network responses to estimate the OS and kernel version.

### 7. Timing and Performance
**Command:** `nmap -T4 192.168.204.135`

This command uses Nmap's T4 timing template for faster scanning.
It increases scan speed compared with the default timing template.

## Results
- Successfully discovered the target host.
- Identified open TCP ports and running services.
- Detected the target operating system as Linux 2.6.X.
- Explored different Nmap scanning and timing options.

## Disclaimer
This project was performed in an isolated virtual lab environment for educational purposes.
All scans were conducted against the Metasploitable 2 virtual machine.
