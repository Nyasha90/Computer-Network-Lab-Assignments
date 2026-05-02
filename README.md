# Assignment-3-Computer-Networks

Submitted By:- Udit Anand

Roll Number:- 2301730091

Program:- BTechCSE(AI/ML) section:- B

Course:- Computer Networks Lab

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

