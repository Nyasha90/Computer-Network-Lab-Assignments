# Computer-Network-Lab-Assignments
Here will be all the files of lab experiments of computer networks

Assignment 1: Basic Network Topologies Using Switches and Hubs
Experiment Objectives:
In this experiment, students will create three small LAN designs in Cisco Packet Tracer to 
understand how network topology influences connectivity, fault tolerance, and performance. 
Students will configure end devices with IPv4 addressing and verify communication using ICMP.
Learning Outcomes
• Create small networks in Packet Tracer using different topologies
• Assign IP addresses correctly and test connectivity
• Identify failure points in different physical layouts
• Compare topology behavior using simulation results
Concepts Used
• Star / Hub-based / Loop (ring-like) layouts
• IPv4 addressing and subnetting
• ICMP ping
• Packet Tracer Simulation Mode
Detailed Instructions
Task 1: Star Topology (Switch)
• Place 1 switch + 4 PCs
• Connect all PCs to the switch
• Assign IPs (example): 192.168.10.1–4 /24
• Ping PC1 → PC2, PC3, PC4
Task 2: Bus-like Topology (Hub)
• Replace switch with hub
• Keep same IP scheme
• Send pings simultaneously and observe packet flow
Task 3: Ring-like Topology (Loop)
• Place 3 switches and connect them in a loop
• Attach 1–2 PCs to each switch
• Ping across switches and observe path
Task 4: Failure Test
• Disconnect one link in ring-like design
• Test if communication still works and note observations
Expected Output
• Successful ping results in each topology
• Screenshot of each topology
• Observation notes on failure behavior and performance
Practical Applications
• LAN design for offices and labs
• Selecting topology based on cost and fault tolerance
• Understanding basic physical network planning






Assignment 2: Packet Flow Visualization Using Simulation Mode
Experiment Objectives
Students will use Packet Tracer Simulation Mode to observe how packets move between devices, 
how switches learn MAC addresses, and how ICMP echo request/reply travels through a small 
network.
Learning Outcomes
• Use Simulation Mode effectively
• Observe ARP + ICMP behavior
• Understand switch MAC learning behavior
• Interpret packet event list timeline
Concepts Used
• Simulation Mode
• ICMP ping
• ARP resolution
• Switch MAC address table learning
Detailed Instructions
Task 1: Build a Simple LAN
• 1 switch + 3 PCs
• IP example: 192.168.20.1–3 /24
Task 2: First Ping Observation
• Enable Simulation Mode
• Ping PC1 → PC2
• Observe ARP request and ARP reply before ICMP
Task 3: Second Ping Observation
• Ping PC1 → PC2 again
• Observe fewer packets (ARP cached)
Task 4: MAC Table Check
• View switch MAC table (if available) / observe switch learning through events
Expected Output
• Event list showing ARP then ICMP
• Screenshots of packet journey steps
• Short notes: first ping vs second ping differences
Practical Applications
• Troubleshooting LAN issues
• Understanding why “first ping is slow”
• Switch learning and broadcast behaviour







 


