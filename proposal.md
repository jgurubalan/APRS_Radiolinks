# Project Proposal

## Title  
**Experimental Study of Packet Loss and Reliability of Telemetry Transmission over the AMPR (44-net) Network Using Raspberry Pi**

---

## 1. Introduction and Background

The AMPR network (also known as the 44-net) is a ham radio IP network intended for experimentation with IP-based communication over amateur radio and mixed infrastructures. Unlike the commercial internet, ham radio networks may involve unreliable links, variable latency, multi-hop routing, and radio-frequency (RF) segments. These characteristics make them an excellent platform for studying real-world network behavior.

Telemetry and weather data transmission is an important application area for amateur radio, especially in emergency communications, remote monitoring, and experimental networking. Understanding how such data behaves over AMPRnet—in terms of packet loss, delay, and reliability—is valuable for designing robust ham radio digital systems.

---

## 2. Objectives

The objectives of this project are:

- Measure and analyze:
  - Packet loss  
  - Latency (delay)  
  - Jitter (delay variation)  
  - Throughput  

- Compare the behavior of:
  - UDP-based transmission (loss-tolerant, real-time style)
  - TCP-based transmission (reliable but potentially slower)

- Evaluate the suitability of the AMPR network for:
  - Telemetry data
  - Weather station data
  - Similar sensor-based applications

- Build a small experimental IP-based ham network platform that can later be extended to RF links.

---

## 3. Experimental Setup

### 3.1 Hardware

- Two Raspberry Pi 5 systems:
  - **Node A (Sender):** Telemetry / weather data generator
  - **Node B (Receiver):** Data logger and web-based dashboard server

### 3.2 Network

- Both nodes will:
  - Be assigned **44.x.x.x (AMPR) IP addresses**
  - Initially connect to the AMPR network using **internet tunnels**
- In later phases, part of the path will be replaced with **real RF IP links** to study IP-over-radio behavior.

### 3.3 Services

- Node B will host:
  - A simple web interface (inside AMPRnet) to display:
    - Received telemetry
    - Packet statistics
    - Loss and delay measurements

---

## 4. Methodology

1. Node A will transmit telemetry packets containing:
   - Sequence number
   - Timestamp
   - Sensor or simulated sensor value

2. Node B will:
   - Log all received packets
   - Detect missing sequence numbers
   - Calculate:
     - Packet loss percentage
     - End-to-end delay
     - Jitter

3. Tests will be conducted using:
   - UDP (to observe raw packet loss)
   - TCP (to observe retransmissions, throughput, and delay behavior)

4. Experiments will be repeated under varying conditions:
   - Different packet sizes
   - Different sending rates
   - Different times of day
   - Later: with and without RF links

5. Results will be:
   - Logged
   - Plotted as graphs
   - Analyzed and compared

---

## 5. Measurements and Metrics

- Packet loss rate (%)
- One-way delay / round-trip delay
- Jitter
- Throughput
- Stability over time
- Effect of transport protocol (UDP vs TCP)

---

## 6. Expected Outcomes

- Quantitative data on:
  - Reliability of AMPRnet paths
  - Suitability for telemetry and sensor data
- A working:
  - Ham-network telemetry server and dashboard
- Clear comparison of:
  - Reliable vs unreliable transport methods
- A reusable experimental platform for future IP-over-radio tests

---

## 7. Significance

This project:

- Demonstrates practical and experimental use of the AMPR (44-net) network
- Studies real-world network behavior over non-ideal links
- Is directly relevant to:
  - Emergency communications
  - Disaster-resilient networks
  - Remote sensing via ham radio
  - Ham radio digital networking research

---

## 8. Future Extensions

- Replace tunnel links with **real RF IP links**
- Add more nodes to study **multi-hop routing**
- Study:
  - Performance under weak-signal conditions
  - Performance at low data rates
- Integrate:
  - Real weather station sensors
  - Mobile or portable nodes

---

## 9. Summary

This project proposes a structured experimental study of telemetry transmission over the AMPR (44-net) network using Raspberry Pi systems, focusing on packet loss, latency, and reliability. It serves as a foundation for future IP-over-radio experimentation and contributes to understanding how IP-based services perform over ham radio style networks.
