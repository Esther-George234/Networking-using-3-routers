1 Introduction 
A network is a Group of components or devices which are connected together to give the user a 
certain service (application). 
Computer networking provides the foundation for communication between devices, enabling data 
exchange, resource sharing, and connectivity across the world. This report introduces the 
fundamentals of networking, including topologies, the OSI and TCP/IP reference models, and 
practical concepts of router configuration with static and dynamic routing. 

2 Fundamentals of Computer Networking 
Networking allows devices to exchange data and share resources. Important concepts include: 
• IP Addressing: Every device gets a unique identifier. 
• Protocols: TCP/IP governs communication across networks. 
• Devices: Switches connect devices within a LAN, while routers link multiple networks. 
2.1 Network Topologies and OSI, TCP/IP Models 
• Topology: How devices are connected together 
✓  Physical Topology: It describes how devices are physically cabled 
✓  Logical Topology: It describes how devices communicate across  
Types of Network Physical Topologies: 
• Bus Topology: A single backbone cable where all devices connect. Simple but prone to 
collisions. 
• Star Topology: All devices connect to a central switch or hub. Easy to manage, widely used in 
LANs. 
• Ring Topology: Devices are connected in a circular fashion; data travels in one direction. 
• Mesh Topology: Every device connects directly to others. Offers high redundancy, common 
in WANs. 
• Hybrid Topology: A mix of two or more topologies, often used in large enterprises. 
2.2 OSI Seven Layers of Networking: 
1. Physical Layer – Transmission of raw bits (cables, switches). 
2. Data Link Layer – Frames, MAC addressing, error detection.        
  
3. Network Layer – Logical addressing and routing (IP). 
4. Transport Layer – Ensures reliable delivery (TCP/UDP). 
5. Session Layer – Manages sessions between applications. 
6. Presentation Layer – Data formatting, encryption, compression. 
7. Application Layer – Interfaces for user applications (HTTP, FTP). 
This model standardizes communication, ensuring compatibility across systems. 
2.3 Difference Between IP Address and MAC Address: 
• IP Address (Logical Address): 
o A numerical label assigned to a device on a network (e.g., 192.168.1.10). 
o Works at the Network Layer (Layer 3) of the OSI model. 
o Dynamic – it can change depending on the network (e.g., when moving between Wi
Fi networks). 
o Used for identifying a device’s location in a network so that data can be routed 
properly. 
o Example: Your laptop may have one IP at home and a different IP at school. 
• MAC Address (Physical/Hardware Address): 
o A unique identifier permanently burned into the network interface card (NIC) by 
the manufacturer (e.g., 00:1A:2B:3C:4D:5E). 
o Works at the Data Link Layer (Layer 2) of the OSI model. 
o Static – does not change (although it can be spoofed). 
o Used for delivering frames within the local network (LAN). 
o Example: Your laptop’s Wi-Fi adapter has a permanent MAC address, no matter 
which IP it uses. 
2.4 TCP/IP model: 
The TCP/IP model (Transmission Control Protocol/Internet Protocol) is the practical framework used 
for communication over the internet. While the OSI model is a theoretical reference model, the 
TCP/IP model was developed by the U.S. Department of Defense (DoD) and is widely used in real
world networking. 
TCP/IP Layers: 
1. Application Layer – Combines the OSI application, presentation, and session layers. Includes 
protocols such as HTTP, FTP, SMTP. 
2. Transport Layer – Similar to OSI transport layer; uses TCP (reliable) and UDP (faster, 
connectionless). 
3. Internet Layer – Equivalent to OSI network layer; handles IP addressing and routing of 
packets. 
4. Network Access Layer (Link Layer) – Combines OSI’s data link and physical layers; manages 
hardware addressing and media access. 
Key Differences Between OSI and TCP/IP Models: 
• Number of Layers: OSI has 7 layers, TCP/IP has 4 layers. 
• Development Purpose: OSI was designed as a universal standard for teaching and protocol 
design; TCP/IP was developed for practical implementation on the internet. 
• Layer Mapping: OSI separates presentation and session functions, while TCP/IP merges them 
into the application layer. 
• Usage: OSI is mainly used as a conceptual framework, while TCP/IP is actually implemented 
in real-world networking. 
    
3 Router Configuration 
Routers are critical devices that direct traffic between networks, ensuring data reaches the correct 
destination. Proper configuration begins with initialization and understanding router modes. 
3.1 Router Initialization 
When a router is powered on, it undergoes the following steps: 
1. POST (Power-On Self-Test): Verifies hardware functionality. 
2. Bootstrap Program: Loads from ROM to initialize hardware and locate the operating system. 
3. Load IOS (Internetwork Operating System): IOS is the router’s OS, loaded from flash 
memory. 
4. Configuration File Loading: The router checks NVRAM for a saved startup configuration. 
o If present, it loads the configuration. 
o If absent, it enters setup mode for initial configuration. 

3.2 Basic Router Modes 
Cisco routers (and many others) use a hierarchical command-line interface (CLI) with different 
modes: 
• User EXEC Mode (>): 
o Basic monitoring commands only (e.g., ping). 
o Limited access for security. 
• Privileged EXEC Mode (#): 
o Access to advanced monitoring and debugging commands. 
o Allows entry into global configuration. 
o Entered with the command: enable. 
• Global Configuration Mode ((config)#): 
o Used to make system-wide changes (e.g., configuring IP addresses, routing protocols). 
• Sub-Configuration Modes ((config-if)#, (config-line)#): 
o Interface configuration mode for setting IPs, enabling interfaces. 
o Line configuration mode for console, SSH, or Telnet access settings. 
3.3 Router Interfaces 
Routers are typically configured using: 
• Console Port – Direct physical setup with a terminal. 
• Telnet/SSH – Remote configuration (SSH provides encryption). 
• Web Interface – GUI setup for small/home networks. 
   
3.4 Static and Dynamic Routing 
• Static Routing: 
o Routes are manually defined by the administrator. 
o Advantages: simple, secure, and predictable. 
o Disadvantages: requires manual updates and is unsuitable for large or changing 
networks. 
• Dynamic Routing (RIP – Routing Information Protocol): 
o Routers automatically share information and update routing tables. 
o RIP uses hop count as its metric (maximum 15 hops). 
o Advantages: adapts to changes, easier to manage large networks. 
o Disadvantages: limited scalability and less efficient in large networks. 
Final project simulation on packet tracer using RIP protocol 
4 Conclusion 
Networking is the backbone of modern communication and industrial systems. By studying 
topologies, learners understand how networks are physically and logically arranged. The OSI and 
TCP/IP models provide structured frameworks for communication, with OSI being theoretical and 
TCP/IP serving as its real-world implementation. 
Understanding router initialization and basic router modes is fundamental for configuration tasks, 
while knowledge of static and dynamic routing prepares learners for managing small to large-scale 
networks. These skills are crucial for careers in IT, automation, and systems engineering. 
