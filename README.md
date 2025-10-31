# Intrusion Detection System (IDS) – Networking Project

## 📘 Overview

This project implements a **Network-based Intrusion Detection System (NIDS)** using **Cisco Packet Tracer**. The IDS monitors and detects suspicious activities, unauthorized access, or any policy-violating network behavior. It demonstrates how a secure and structured IDS-enabled network can protect an organization’s digital infrastructure from internal and external threats.

The system captures and analyzes packets across multiple connected LANs, alerts the administrator when malicious activity is detected, and logs these alerts through a centralized **SYSLOG Server**.

## 🔐 Abstract

An **Intrusion Detection System (IDS)** is software or hardware designed to monitor network traffic for malicious activities or policy violations. Once detected, it alerts the system administrator or logs the information in a central system called **SIEM (Security Information and Event Management)**.

There are two main types of IDS:

* **NIDS (Network-based Intrusion Detection System):** Monitors network traffic across devices.
* **HIDS (Host-based Intrusion Detection System):** Monitors key system files and local logs.

This project focuses on implementing a **NIDS** in a simulated multi-network environment to detect suspicious activity, using **Cisco Packet Tracer** and CLI-based router configurations.

## 🧩 Table of Contents

1. [Overview](#-overview)
2. [Project Objectives](#-project-objectives)
3. [System Design](#-system-design)
4. [Software & Hardware Requirements](#-software--hardware-requirements)
5. [Implementation Steps](#-implementation-steps)
6. [Testing & Results](#-testing--results)
7. [Challenges & Future Work](#-challenges--future-work)
8. [Conclusion](#-conclusion)

---

## 🎯 Project Objectives

* To design and implement a **Network Intrusion Detection System**.
* To ensure **real-time monitoring** and **logging** of suspicious network activities.
* To configure **SYSLOG** for centralized event recording.
* To understand **packet routing**, **traffic control**, and **network layer communication**.
* To simulate and demonstrate a **secure, IDS-enabled network environment**.

## 🖥️ System Design

The network is divided into **three LANs**, connected through routers:

* **Network 1 (192.168.1.0/24)** – Hosts SYSLOG Server, PCs, and Printer
* **Network 2 (192.168.10.0/24)** – Hosts FTP Server, Laptop, and Printer
* **Network 3 (192.168.30.0/24)** – Hosts PC and Laptop

Each LAN is connected using Cisco 2960 Switches, and routers (Cisco 1941) are used for inter-network communication.

### Network Devices Used

* Cisco 1941 Routers
* Cisco 2960 Switches
* SYSLOG Server
* HTTP and FTP Servers
* PCs and Laptops
* PT Printer

### Cables Used

* **Straight-through cable**: for PC ↔ Switch ↔ Router connections
* **Serial DCE cable**: for Router ↔ Router connections

---

## ⚙️ Software & Hardware Requirements

### Software

* **Cisco Packet Tracer (latest version)**
* Operating System: Windows / macOS / Linux

### Minimum Hardware

* Intel Pentium 4 (2.5 GHz or higher)
* 2 GB RAM
* 1 GB free storage
* 1024x768 display resolution

## 🧠 Implementation Steps

1. **Design the Network Layout**

   * Create three LANs and connect them using routers.
   * Assign IP addresses (Class A and Class C).

2. **Configure Devices via CLI**

   * Assign IPs to all interfaces.
   * Enable routing between routers.
   * Test intra-network and inter-network connectivity using `ping`.

3. **Enable SYSLOG Server**

   * Configure routers to send log messages to the SYSLOG server.

4. **Implement IDS Configuration**

   * Set up **NIDS** to monitor network packets.
   * Define detection signatures for known malicious traffic.
   * Log detected intrusions to the SYSLOG server.

5. **Testing the IDS**

   * Simulate attacks or suspicious packets.
   * Observe logs and alerts on the SYSLOG server.

## 🧪 Testing & Results

* **Ping Test** between PCs verifies successful routing.
* **ICMP Packet Test** demonstrates detection of unauthorized traffic.
* **SYSLOG Logging** confirms IDS alerts and network event recording.

The IDS successfully detects and logs unauthorized traffic across the networks, alerting the admin for corrective action.

## ⚠️ Challenges & Future Work

### Challenges

* Limited IDS functionality in Packet Tracer (no live packet capture).
* Need for advanced signatures and real-time response mechanisms.
* Difficulty in simulating high-traffic attack environments.

### Future Enhancements

* Integrate **IPS (Intrusion Prevention System)** to automatically block attacks.
* Implement **Machine Learning models** for anomaly-based detection.
* Extend simulation using **GNS3** or real Cisco hardware.

## 🏁 Conclusion

This project successfully demonstrates how a **Network-based Intrusion Detection System (NIDS)** can monitor, log, and alert network administrators about suspicious activities. Using Cisco Packet Tracer and CLI commands, the network was built, configured, and tested to ensure connectivity and security.

The IDS strengthens network defense and helps understand practical cybersecurity principles in network architecture.

## 👥 Contributors

* **Suleman Sarwar**
* **Team Members (if any)**
* Department of Software Engineering, SZABIST University, Islamabad

## 📚 References

* Cisco Networking Academy
* NIST SP 800-94, *Guide to Intrusion Detection and Prevention Systems*
* CNSSI 4009-2015, *National Information Assurance Glossary*
* James P. Anderson, *Computer Security Threat Monitoring and Surveillance* (1980)
