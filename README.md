
Submitted By:- Nyasha Das
Roll Number:- 2301730085
Program:- BTech CSE (AI/ML) Section:- B
Course:- Computer Networks Lab

---
# Assignment-1-Computer-Networks
# Basic Network Topologies Using Switches and Hubs

## 📌 Objective

This experiment focuses on designing and analyzing different network topologies using Cisco Packet Tracer. The goal is to understand how topology affects connectivity, performance, and fault tolerance.

---

## 🧠 Concepts Used

* Star Topology (Switch-based network)
* Bus Topology (Hub-based network)
* Ring-like Topology (Loop connection using switches)
* IPv4 Addressing
* ICMP Ping (Connectivity Testing)
* Packet Tracer Simulation Mode

---

## 🖧 Network Design

Three different LAN topologies were created:

### 1. Star Topology

* 1 Switch connected to 4 PCs
* Each PC connected directly to the switch
* IP Range: 192.168.10.1 – 192.168.10.4 /24

### 2. Bus Topology (Hub-based)

* Switch replaced with Hub
* All PCs connected to Hub
* Same IP configuration used

### 3. Ring-like Topology

* 3 switches connected in loop
* Each switch connected to 1–2 PCs
* Enables multiple path routing

---

## ⚙️ Configuration

* IP addresses assigned manually to each PC
* Subnet mask: 255.255.255.0
* No routing required (single LAN per topology)

---

## 🧪 Testing & Observations

### ✔ Connectivity Test

* Successful ping between all PCs in each topology

### 🔍 Performance Observations

| Topology  | Behavior                        |
| --------- | ------------------------------- |
| Star      | Fast and reliable communication |
| Bus       | Packet collisions may occur     |
| Ring-like | Redundant paths available       |

### ❌ Failure Test (Ring Topology)

* When one link was disconnected:

  * Network still worked due to alternate path
  * Demonstrates fault tolerance

---

## 📊 Results

* Star topology provided best performance
* Bus topology showed inefficiency due to collisions
* Ring topology showed better fault tolerance

---

## 💡 Conclusion

This experiment demonstrated how different network topologies impact performance and reliability. Star topology is best for small networks, while ring-like topology provides better fault tolerance.

---



# Assignment-2-Computer-Networks
# Packet Flow Visualization Using Simulation Mode

## 📌 Objective

This experiment aims to visualize how packets travel across a network using Cisco Packet Tracer Simulation Mode. It helps in understanding ARP, ICMP, and switch MAC learning behavior.

---

## 🧠 Concepts Used

* Simulation Mode in Packet Tracer
* ARP (Address Resolution Protocol)
* ICMP (Ping)
* MAC Address Table Learning
* Packet Flow Analysis

---

## 🖧 Network Design

* 1 Switch connected to 3 PCs
* IP Address Range: 192.168.20.1 – 192.168.20.3 /24

---

## ⚙️ Configuration

* Manual IP assignment to all PCs
* Subnet mask: 255.255.255.0
* Devices connected using straight-through cables

---

## 🧪 Experiment Steps

### 🔹 Task 1: Build LAN

* Connected 3 PCs to a switch
* Assigned IP addresses

### 🔹 Task 2: First Ping Observation

* Enabled Simulation Mode
* Ping PC1 → PC2
* Observed:

  * ARP Request (broadcast)
  * ARP Reply
  * ICMP Echo Request & Reply

### 🔹 Task 3: Second Ping Observation

* Ping repeated
* Observed:

  * No ARP request (cached)
  * Faster communication

### 🔹 Task 4: MAC Table Learning

* Switch learned MAC addresses
* Reduced unnecessary broadcasting

---

## 🔍 Observations

| Scenario        | Behavior                         |
| --------------- | -------------------------------- |
| First Ping      | Slow due to ARP process          |
| Second Ping     | Faster due to ARP cache          |
| Switch Behavior | Learns MAC and optimizes traffic |

---

## 📊 Results

* ARP is required before ICMP communication
* First ping is always slower
* Switch improves efficiency by learning MAC addresses

---

## 💡 Conclusion

This experiment clearly showed how packet flow works in a LAN. It highlighted the importance of ARP and demonstrated how switches optimize communication using MAC address learning.

---


# Assignment-3-Computer-Networks

# Routing Tables

## 1. Routing Information Protocol

### Copper Straight-Through Connections

| From | To  | Port/Interface        |
|------|-----|-----------------------|
| PC0  | S1  | fa0/1                 |
| PC1  | S1  | fa0/2                 |
| S1   | R0  | fa0/24 → fa2/0        |
| PC2  | S2  | fa0/1                 |
| PC3  | S2  | fa0/2                 |
| S2   | R1  | fa0/24 → fa2/0        |
| PC4  | S3  | fa0/1                 |
| PC5  | S3  | fa0/2                 |
| S3   | R2  | fa0/24 → fa2/0        |

### Serial DTE Connections

| From | To  | Port/Interface        |
|------|-----|-----------------------|
| R0   | R1  | se0/0 ↔ se1/0         |
| R1   | R2  | se0/0 ↔ se1/0         |

## Network Design

The network topology was designed using Cisco Packet Tracer consisting of three routers (R0, R1, R2), three switches (S1, S2, S3), and multiple end devices (PCs).

Each router is connected to a switch, and each switch connects to multiple PCs, forming three different local area networks (LANs). The routers are interconnected using serial DTE links to enable communication between different networks.

IP addresses were assigned to all devices, and routing protocols (RIP and OSPF) were configured to enable communication across networks.

The design ensures:
- Proper segmentation of networks
- Efficient communication between LANs
- Scalability for adding more devices

## Comparison of RIP and OSPF (Based on Simulation)

From the simulations performed using Cisco Packet Tracer, the following conclusions were observed:

### 1. Convergence Time
RIP showed slower convergence as routing updates were exchanged periodically. OSPF converged faster due to immediate exchange of link-state information.
**Conclusion:** OSPF converges faster than RIP.

### 2. Routing Metric
RIP used hop count as the metric, which sometimes resulted in non-optimal path selection. OSPF used cost based on bandwidth, leading to better routing decisions.
**Conclusion:** OSPF provides more optimal path selection.

### 3. Efficiency
RIP periodically sent full routing tables, increasing network traffic. OSPF sent updates only when changes occurred, making it more efficient.
**Conclusion:** OSPF is more efficient than RIP.

### 4. Scalability
RIP is suitable for small networks due to its limitations. OSPF handled larger and more complex networks effectively.
**Conclusion:** OSPF is more scalable than RIP.








# Assignment-4-Computer-Networks

## 🔹 Overview
This assignment demonstrates the setup of a **DNS Server** using Cisco Packet Tracer and analyzes how domain names are resolved into IP addresses within a local network.

---

## 🔹 Network Design

Devices Used:
- 1 Server (DNS)
- 2–3 PCs
- 1 Switch

Topology:
PCs → Switch → Server

---

## 🔹 IP Configuration

Server:
- IP: 192.168.1.2
- Subnet: 255.255.255.0

PCs:
- IP: 192.168.1.3 / 192.168.1.4 / 192.168.1.5
- Subnet: 255.255.255.0
- DNS: 192.168.1.2

---

## 🔹 DNS Configuration

Records added:

- www.example.com → 192.168.1.2  
- www.google.com → 192.168.1.2  

---

## 🔹 Testing

Ping:
ping www.example.com  
ping www.google.com  

NSLOOKUP:
nslookup www.example.com  
nslookup www.google.com  

Traceroute:
tracert www.example.com  

---

## 🔹 Analysis

Query Time:
- ~1–2 ms (low latency due to same network)

Response Accuracy:
- Domain names resolved correctly

Name Resolution Process:
- User enters domain name  
- Request sent to DNS server  
- Server returns mapped IP  
- Communication established  

---

## 🔹 Key Observations

- DNS converts domain names into IP addresses  
- Proper IP configuration is essential  
- DNS and network connectivity are separate  
- Packet Tracer does not support real internet  

---

## 🔹 Conclusion

DNS server was successfully configured and tested.  
The system accurately resolved domain names with minimal delay, demonstrating effective DNS operation in a local network.

---

## 🔹 Tools Used
- Cisco Packet Tracer
- Command Prompt
