# 🌐 Networking Devices & Infrastructure Fundamentals — SOC Engineer Notes

A comprehensive reference guide covering core networking hardware, their OSI layer placements, functionalities, and security significance for SOC Analysts and Security Engineers.

---

## 📌 Table of Contents

1. [Network Interface Card (NIC)](#1-network-interface-card-nic)
2. [Hub](#2-hub)
3. [Switch](#3-switch)
4. [Router](#4-router)
5. [Modem](#5-modem)
6. [Access Point (AP) & Wireless Router](#6-access-point-ap--wireless-router)
7. [Repeater & Extender](#7-repeater--extender)
8. [Bridge](#8-bridge)
9. [Firewall](#9-firewall)
10. [Gateway](#10-gateway)
11. [Quick Comparison Summary Table](#11-quick-comparison-summary-table)

---

## 1. Network Interface Card (NIC)

* **Operating Layer:** Layer 1 (Physical) & Layer 2 (Data Link)
* **What is it?** Hardware component (built-in chip or expansion card) that allows a machine to connect to a network.
* **Key Function:** Contains a permanent **MAC Address** (Media Access Control) assigned by the manufacturer. Converts digital data into electrical, optical, or radio signals.

---

## 2. Hub

* **Operating Layer:** Layer 1 (Physical)
* **What is it?** A legacy connecting device for multiple LAN endpoints.
* **Key Characteristic:** **Non-intelligent device.** It uses **broadcasting**. When data arrives at one port, the hub transmits it to *all* other ports regardless of the intended destination.
* **Security & Performance Concerns:**
  * High collision domain (frequent packet collisions).
  * Vulnerable to **eavesdropping/packet sniffing** because every host receives all traffic.

---

## 3. Switch

* **Operating Layer:** Layer 2 (Data Link) *(Layer 3 for Managed/MLS Switches)*
* **What is it?** An intelligent LAN connecting device.
* **Key Function:** 
  * Builds and maintains a **MAC Address Table** (CAM Table).
  * Uses **Unicasting** — forwards incoming data packets *only* to the specific device port based on destination MAC address.
* **SOC Significance:**
  * Switches isolate collision domains.
  * Attackers target switches using **MAC Flooding** attacks to turn them into hub-like behavior, or perform **ARP Spoofing / Poisoning**.

---

## 4. Router

* **Operating Layer:** Layer 3 (Network)
* **What is it?** A device that connects two or more different networks (e.g., LAN to WAN / Internet).
* **Key Function:**
  * Evaluates **IP Addresses** to determine the best path for data packet transmission using **Routing Tables**.
  * Performs **NAT (Network Address Translation)** to map private internal IPs to a public IP.
* **SOC Significance:**
  * Acts as the primary gateway for inbound/outbound corporate traffic.
  * Configured with **ACLs (Access Control Lists)** to filter unauthorized IP ranges.

---

## 5. Modem (Modulator-Demodulator)

* **Operating Layer:** Layer 1 (Physical) & Layer 2 (Data Link)
* **What is it?** A hardware device that converts signals for transmission over telephone lines, fiber optics, or coaxial cables.
* **Key Function:**
  * **Modulation:** Converts digital data from a computer into analog signals.
  * **Demodulation:** Converts incoming analog signals back into digital data.

---

## 6. Access Point (AP) & Wireless Router

* **Operating Layer:** Layer 2 (Data Link)
* **What is it?** A device that allows wireless Wi-Fi devices to connect to a wired network using IEEE 802.11 standards.
* **Security Best Practices:**
  * Use **WPA3 / WPA2-Enterprise** encryption instead of weak WEP/WPA.
  * Disable WPS (Wi-Fi Protected Setup) to prevent PIN brute-force attacks.

---

## 7. Repeater & Extender

* **Operating Layer:** Layer 1 (Physical)
* **What is it?** A signal regeneration device.
* **Key Function:** Receives weak network signals, cleans noise, amplifies them, and retransmits them to extend coverage distance without altering packet payload data.

---

## 8. Bridge

* **Operating Layer:** Layer 2 (Data Link)
* **What is it?** A device used to connect two separate LAN segments into a single aggregated network.
* **Key Function:** Filters traffic based on MAC addresses to prevent unnecessary packet transmission across network segments.

---

## 9. Firewall

* **Operating Layer:** Layer 3 (Network), Layer 4 (Transport), & Layer 7 (Application)
* **What is it?** A primary security appliance designed to monitor and filter incoming/outgoing network traffic based on security policies.
* **Types:**
  * **Packet-Filtering Firewall:** Checks basic source/destination IPs and ports.
  * **Stateful Inspection Firewall:** Tracks active connection states.
  * **Next-Generation Firewall (NGFW) / WAF:** Inspects deep packet payloads (Layer 7) to block malware, exploits, and unauthorized web requests.

---

## 10. Gateway

* **Operating Layer:** Layers 4 through 7 (Upper Layers)
* **What is it?** A protocol converter that enables communication between networks running on different protocol architectures (e.g., connecting an enterprise network to a legacy system).

---

## 11. Quick Comparison Summary Table

| Device | Primary OSI Layer | Traffic Type | Address Used | Intelligence Level |
| --- | --- | --- | --- | --- |
| **Hub** | Layer 1 | Broadcast | None | Low (Dummy) |
| **Switch** | Layer 2 | Unicast | MAC Address | Medium |
| **Router** | Layer 3 | Unicast / Routing | IP Address | High |
| **Firewall** | Layer 3, 4, 7 | Filtered / Inspected | IP, Port, Payload | Very High |
| **Repeater** | Layer 1 | Signal Amplification | None | None |

---

### 📝 Author Note

*Documented as part of foundational cybersecurity and SOC home lab study notes.*