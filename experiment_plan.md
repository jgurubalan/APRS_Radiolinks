# Experiment Plan

## Title  
**Measurement of Packet Loss, Latency, and Reliability of Telemetry Transmission over the AMPR (44-net) Network**

---

## 1. Purpose of the Experiment

The purpose of this experiment is to study how IP-based telemetry and weather data behaves when transmitted over the AMPR (44-net) network. In particular, the experiment focuses on measuring:

- Packet loss  
- Latency (delay)  
- Jitter (variation in delay)  
- Throughput and reliability  

The experiment will first be conducted using AMPR tunnels only (baseline measurement). In later phases, radio (RF) links will be introduced to compare performance.

---

## 2. Experiment Topology (Phase 1: Tunnel Only)


- **Pi A (Sender):**
  - Sends telemetry / weather packets
- **Pi B (Receiver):**
  - Receives packets
  - Logs data
  - Computes statistics
  - Hosts a simple web dashboard (optional)

Both Pis:

- Have 44.x.x.x AMPR IP addresses
- Are connected to AMPRnet using tunnels

---

## 3. Hardware and Software

### 3.1 Hardware

- Raspberry Pi 5 × 2
- Internet connection for both

### 3.2 Software

- Linux OS
- Tunnel client for AMPR access
- Python (or similar) for test scripts
- Standard tools:
  - `ping`
  - `traceroute`
  - `iperf` (optional)

---

## 4. Data Format

Each telemetry packet sent by Pi A will contain:

- Sequence number
- Timestamp
- Sensor value (real or simulated)

Example (logical format):


---

## 5. Test Methods

### 5.1 Test 1: Basic Connectivity

- Use:
- Measure:
- Packet loss %
- Round-trip time

- Use:
- Record:
- Number of hops
- Approximate path

---

### 5.2 Test 2: UDP Packet Loss Test

- Pi A sends:
- N numbered UDP packets (e.g., 1000 packets)
- Pi B:
- Logs received sequence numbers
- Detects missing packets

Compute:

- Packets sent
- Packets received
- Packets lost
- Loss percentage
- Delay and jitter

Repeat with:

- Different packet sizes
- Different sending rates

---

### 5.3 Test 3: TCP Reliability Test

- Transfer a file or stream data using TCP
- Measure:
- Transfer time
- Throughput
- Stability
- Observe:
- Effect of retransmissions
- Effect of delay and packet loss on speed

---

## 6. Parameters to Vary

- Packet size (small, medium, large)
- Sending rate (slow, medium, fast)
- Time of day
- Test duration
- Protocol:
- UDP vs TCP

---

## 7. Measurements to Record

- Packet loss rate (%)
- Average delay
- Jitter
- Throughput
- Stability over time
- Number of route hops

---

## 8. Data Logging and Analysis

- All received packets will be logged to files
- Scripts will:
- Count missing packets
- Compute delay and jitter
- Results will be:
- Tabulated
- Plotted as graphs
- Compared across different test conditions

---

## 9. Expected Results

- Baseline measurements of:
- Loss
- Delay
- Jitter
- Clear difference between:
- UDP (loss visible)
- TCP (retransmissions, slower but reliable)
- Understanding of:
- How suitable AMPRnet is for telemetry-style data

---

## 10. Phase 2 (Future Extension)

Replace part of the tunnel path with a real RF IP link:


Repeat the same experiments and compare:

- Tunnel-only vs RF + tunnel
- Effect of RF on loss, delay, and throughput

---

## 11. Summary

This experiment provides a structured and repeatable method to study IP network behavior over the AMPR (44-net) network, starting with tunnel-based connectivity and later extending to real RF links. The results will help understand the suitability of ham IP networks for telemetry, weather data, and other sensor-based applications.
