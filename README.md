# 5G-wireless-network
# The 5G System
- ### Global Standardization Effort:
  it's a global standard developed through an international effort. The International Telecommunication Union (ITU) led this initiative with a vision to "connect all the world's people".
  
  <img width="1381" height="848" alt="Screenshot (303)" src="https://github.com/user-attachments/assets/9b5b6bdb-c62b-4dd1-8fdd-63d5a063eadc" />

- #### Key Requirements:
  The 5G standard, known as IMT-2020, has much higher performance requirements than its predecessor, IMT-Advanced (4G). This includes significant improvements in
  Peak Data Rate, Latency, and Connection Density.

  <img width="1384" height="734" alt="Screenshot (304)" src="https://github.com/user-attachments/assets/f89de145-096f-436c-927b-7e41558500a6" />


- ### The Role of 3GPP:
  -  The primary organization responsible for developing the specifications for 5G is the 3rd Generation Partnership Project (3GPP).

   -  It is a global initiative with organizational partners from countries like Japan, China, Korea, the USA, and Europe.
 
- ### Organizational Structure:
  
  <img width="1395" height="738" alt="Screenshot (306)" src="https://github.com/user-attachments/assets/5a1e3825-40d3-4450-a71d-23a0c00a8b56" />

  
  3GPP is divided into several working groups that focus on specific areas of the mobile system.

  -  <h6>TSG RAN (Radio Access Network)</h6> handles specifications for the radio interface, including layer 1, 2, and 3 protocols.

  -  <h6>TSG SA (Service & Systems Aspects)</h6> manages the Core Network and end-to-end aspects like security, architecture, and multimedia codecs.

  -  <h6>TSG CT (Core Network & Terminals)</h6> focuses on protocols within the Core Network and its interoperability with external networks.


- ### Timeline and Releases:
  
  <img width="1396" height="833" alt="Screenshot (308)" src="https://github.com/user-attachments/assets/195cfa5e-12f6-42f5-90b0-ca2e7b3d76f0" />


  3GPP releases specifications in phases over time.Release 15 was the first major release to define the 5G standard.

# The Three Main 5G Use Cases
5G technology enables three main types of services, each with its own set of requirements.

<img width="1392" height="706" alt="Screenshot (309)" src="https://github.com/user-attachments/assets/d9eef7f4-ae0e-4d44-884f-9aabc935eabb" />


### 1. Enhanced Mobile Broadband (eMBB)
eMBB focuses on high data rates and is the most common use case people think of for 5G. It's designed to handle a large amount of data quickly and efficiently.

<img width="1046" height="226" alt="Screenshot (310)" src="https://github.com/user-attachments/assets/90469d6e-3c9f-4b58-8553-43a205fd66eb" />


- #### Key Features:

  -  <h6>Peak Data Rate:</h6> Up to 20 Gbps (downlink) and 10 Gbps (uplink).
  -  <h6>User Experience:</h6> A typical user can expect data rates of 100 Mbps (downlink) and 50 Mbps (uplink)
  - <h6>High Mobility:</h6> Supports speeds up to 500 km/h.
- ### Examples:
  Streaming 4K/8K video, virtual and augmented reality, and working or playing in the cloud.

### 2. Massive Machine-Type Communications (mMTC)
mMTC is designed for a huge number of devices that need to communicate without a lot of human involvement, like in the Internet of Things (IoT). These devices typically send and receive small amounts of data.

<img width="1128" height="216" alt="Screenshot (311)" src="https://github.com/user-attachments/assets/41ac463a-e9f8-4a10-af6f-dc8621fd69f0" />


- #### Key Features:

  -  <h6>Connection Density:</h6> Can support up to 1,000,000 devices per square kilometer.
  -  <h6>Low Power:</h6> Devices can have a battery life of 10-15 years.
  -  <h6>Low Data Rate:</h6> Data rates are generally low, from 1-100 kbps.

- ### Examples:
  Smart meters, smart agriculture, and tracking in logistics.

### 3. Ultra-Reliable and Low-Latency Communications (URLLC)
URLLC is for applications where every millisecond and every connection counts. It's about providing extremely reliable and immediate communication for mission-critical tasks.

<img width="1039" height="232" alt="Screenshot (312)" src="https://github.com/user-attachments/assets/f73f708d-b145-4b43-8a5d-acf00377c027" />


- #### Key Features:
  -  <h6>Low Latency:</h6> User plane latency is as low as 1 ms, and the control plane latency is 10 ms.
  -  <h6>High Reliability:</h6> It has a 99.999% success rate for connections.
  -  <h6>Mobility:</h6> It's designed for high mobility without service interruption.

- ### Examples:
   Traffic safety and control, remote surgery and manufacturing, and industrial automation.

# The 5G System: 
Core Concepts The 5G system is fundamentally divided into two main parts: 

<img width="1348" height="665" alt="Screenshot (314)" src="https://github.com/user-attachments/assets/27ad9e88-a7d6-4aea-a7d8-38db769fbd5a" />


- the Radio Access Network (RAN) and the 5G Core. These two parts are connected by various interfaces, like N1, N2, and N3.

- A key design principle of 5G is the separation of the Control Plane and the User Plane.

- This separation allows for more independent scaling and flexible deployment. This means the network can be optimized to meet the very different needs of various use cases, such as Massive Machine-Type    Communications (mMTC) and Mobile Broadband.
  
  <img width="1391" height="665" alt="Screenshot (316)" src="https://github.com/user-attachments/assets/8cf8d98c-cf28-49bd-8a6a-0ba48cb7fcbd" />


#### Key Network Functions
The 5G system is made up of several important network functions, each with a specific role:

- <h6>gNodeB:</h6> This is the base station in the 5G RAN. Its job is to provide wireless connectivity and connect directly to the user equipment (UE).

<img width="1141" height="522" alt="Screenshot (317)" src="https://github.com/user-attachments/assets/fee68a4d-b529-4b07-92bd-c6ba6ef3de0c" />

- <h6>UPF (User Plane Function):</h6> A part of the 5G Core, the UPF is responsible for handling user data. It acts as a mobility anchor, enforces policies, and handles lawful interception.

<img width="605" height="587" alt="Screenshot (318)" src="https://github.com/user-attachments/assets/e8df0a58-225d-44c0-825d-d989bfc15a64" />

- <h6>SMF (Session Management Function):</h6> The SMF manages all data sessions. It controls how the UPF handles data flow and ensures sessions are properly set up and managed.

- <h6>AMF (Access and Mobility Function):</h6> This function is in charge of managing mobility and user registration. The AMF is like a control hub that oversees a user's connection to the network and how they move between different areas.

- <h6>AUSF (Authentication Server Function):</h6> The AUSF handles all security-related tasks by authenticating users before they can access the network.

- <h6>UDM (Unified Data Management):</h6> The UDM stores all the user's subscription data and information.

- <h6>PCF (Policy Control Function):</h6> The PCF sets and enforces policies within the network, which can include rules for session management and charging.

# 5G System Deployment Options
The path from 4G to 5G isn't a single step; it involves various deployment options that allow for different levels of integration with existing networks. These options are primarily categorized as 

### Non-Standalone (NSA) Options
NSA options use the existing 4G core network (EPC) to provide basic connectivity and services while adding 5G NR for enhanced speeds.

- <h6>Option 3 (EN-DC):</h6> This is a very common NSA deployment where the 4G network provides the control plane, and both 4G and 5G radio access networks are used for the user plane. This option is often used when 5G coverage is spotty because it relies on the more widespread 4G network for core functions. There are also variants like Option 3a and Option 3x. 

<img width="1374" height="805" alt="Screenshot (327)" src="https://github.com/user-attachments/assets/ced3fc70-d008-4db1-b361-c842f64105e5" />


### Standalone (SA) Options
SA options use a new 5G Core network, which is fully independent of the 4G EPC. This allows for the full capabilities of 5G, such as low latency and massive device connectivity.

- <h6>Option 2:</h6> This is the first SA option where a 5G RAN and a 5G Core are deployed from scratch, without relying on any legacy 4G systems. It's a true 5G system.

<img width="1403" height="677" alt="Screenshot (325)" src="https://github.com/user-attachments/assets/5b8753d4-6ea3-4919-87c6-d7844eb6457c" />


- <h6>Option 4 (NE-DC):</h6> This option uses a 5G Core and a 5G NR base station for the primary control and user plane. It can also use an LTE eNodeB to provide additional user plane capacity. This is often used when 5G provides the primary coverage

<img width="1361" height="673" alt="Screenshot (329)" src="https://github.com/user-attachments/assets/409dc2d1-261c-4353-8f44-26954c41d078" />


- <h6>Option 5:</h6> This is another SA option that uses a 5G Core with an eLTE eNodeB. It's essentially using a 4G radio with a 5G Core

<img width="1367" height="638" alt="Screenshot (330)" src="https://github.com/user-attachments/assets/78854fda-5bc3-4d20-9f8b-1721a80f5229" />

# RAN Protocol Stack
The RAN Protocol Stack is divided into two main parts: 

the User Plane and the Control Plane. Each plane has a specific set of layers that handle different tasks, from transmitting data to managing the connection.

### 1. User Plane Protocol Stack
This stack is responsible for carrying user data from the device (UE) to the core network. The main layers from top to bottom are:

- <h6>SDAP (Service Data Adaptation Protocol):</h6> This layer is at the top and handles the mapping of QoS (Quality of Service) flows to radio bearers.

- <h6>PDCP (Packet Data Convergence Protocol):</h6> This layer is in charge of header compression and encryption to ensure data security.

- <h6>RLC (Radio Link Control):</h6> The RLC layer manages segmentation and re-segmentation of data, ensuring the efficient transmission of data over the radio interface.

- <h6>MAC (Medium Access Control):</h6> This layer handles multiplexing, scheduling, and retransmissions. It ensures that multiple devices can share the same radio channel efficiently.

- <h6>PHY (Physical Layer):</h6> The physical layer is the lowest layer and is responsible for the actual radio transmission and reception of bits over the air.

### 2. Control Plane Protocol Stack
This stack is used for signaling and managing the connection between the user device (UE), the gNodeB, and the Access and Mobility Function (AMF) in the 5G Core Network. The key layers are:

- <h6>NAS (Non-Access Stratum):</h6> This layer, at the top of the stack, handles functions like authentication, security, and idle mode procedures. It communicates directly between the UE and the AMF.

- <h6>RRC (Radio Resource Control):</h6> The RRC layer manages the radio bearers and the control plane itself. It handles signaling between the UE and the gNodeB.

- <h6>The layers below RRC are the same as in the User Plane:</h6> PDCP, RLC, MAC, and PHY. They are used for the reliable transmission of RRC and NAS messages.

# Service Data Adaptation Protocol (SDAP)
The SDAP layer is a crucial part of the 5G User Plane Protocol Stack. Its main purpose is to manage diverse traffic types and ensure that each one receives the correct Quality of Service (QoS).

It acts like a traffic manager, directing data flows to the appropriate paths.

#### Key Functions
- <h6>QoS Flow Mapping:</h6> SDAP's primary function is to map incoming data flows to specific radio bearers.This ensures that different types of data, like a voice call versus a background download, are handled correctly according to their unique performance needs.

- <h6>QoS Flow Identifier (QFI):</h6> Each data flow is identified by a QoS Flow Identifier (QFI). This allows the network to distinguish between different types of traffic and apply the correct QoS policies to each one.

### Types of QoS Flows
The PDF outlines different types of QoS flows, each defined by a 5QI (5G QoS Identifier).

- <h6>GBR (Guaranteed Bit Rate):</h6> This is for services that need a guaranteed data rate, like voice calls or real-time video streaming. These services are more sensitive to delays and require consistent performance.

- <h6>Non-GBR (Non-Guaranteed Bit Rate):</h6> This is for services that don't need a guaranteed data rate, such as browsing the web, downloading files, or social media. These services are more flexible and can tolerate some delay or variation in speed.

- <h6>Delay Critical GBR:</h6> This is a specific type of GBR for applications that are extremely sensitive to delay, such as remote control and vehicle-to-everything (V2X) communications.

# Packet Data Convergence Protocol (PDCP)
The PDCP layer sits in the middle of the RAN protocol stack. Its primary role is to ensure the secure and reliable delivery of data packets.

#### Key Functions

- <h6>Header Compression:</h6> PDCP uses a technique called Robust Header Compression (ROHC) to reduce the size of the IP header in data packets. 

  This is especially useful for applications like Voice over IP (VoIP), where the header can be much larger than the actual voice payload. By compressing the header, the network becomes more efficient.

- <h6>Ciphering and Integrity Protection:</h6> This is a core security function of the PDCP layer. It uses encryption to prevent eavesdropping and integrity protection to ensure that the data hasn't been tampered with. 

  The PDCP layer applies these security measures to both user data and control signaling.

- <h6>In-sequence Delivery:</h6> PDCP ensures that data packets are delivered to the higher layers in the correct order. If packets arrive out of order from the lower layers, PDCP reorders them before passing them up.

- <h6>Routing and Duplication:</h6> PDCP can intelligently route data. For example, in a "split bearer" scenario, the PDCP layer can duplicate packets and send them over multiple radio links to ensure higher reliability.

# Radio Link Control (RLC)
The RLC layer is a key part of the 5G RAN protocol stack, sitting between the PDCP and MAC layers. Its main responsibility is to ensure the efficient and reliable delivery of data packets.

It does this by using different operational modes, each suited for a specific type of data traffic.

### RLC Modes
The RLC layer operates in three different modes, each with unique capabilities:

- <h6>Transparent Mode (TM):</h6> This is the simplest mode. It does not perform any segmentation, reassembly, or retransmissions.

  It simply passes data through without any changes. This is used for very specific signaling messages where the higher layers are responsible for any reliability.

 - <h6>Unacknowledged Mode (UM):</h6> This mode performs segmentation and reassembly. It breaks down large data packets into smaller segments for transmission and then puts them back together at the receiving end. However, it does not perform retransmissions. This is suitable for services that can tolerate some data loss, like streaming video.

 - <h6>Acknowledged Mode (AM):</h6> This is the most robust mode. It performs all the functions of Unacknowledged Mode, plus it handles retransmissions (ARQ - Automatic Repeat Request). 

   If a data segment is lost or received with an error, the receiver will request the sender to retransmit it. This mode is used for services that require a high level of reliability, like web browsing or file downloads.

# Medium Access Control (MAC)
The MAC layer sits just below the RLC layer and is responsible for managing the radio channel efficiently. Its main job is to coordinate the flow of data from various sources and ensure everything is scheduled correctly.

#### Key Functions
- <h6>Multiplexing and De-multiplexing:</h6> This is a core function of the MAC layer. It takes data from different Logical Channels (like those for voice, video, or signaling) and combines them into a single data block for the lower layers. At the receiving end, it does the reverse, separating the data and sending it to the correct RLC layer.

- <h6>Scheduling:</h6> The MAC layer is responsible for scheduling all data transmissions. It decides which devices get to transmit and receive data, when they can do it, and how much data they can send. This is a crucial function for optimizing network performance and ensuring a fair distribution of resources.

- <h6>Hybrid ARQ (HARQ):</h6> This is a mechanism for retransmissions. Unlike the RLC layer's retransmissions, HARQ works very quickly at the physical layer. It combines a retransmitted data packet with the original packet to increase the chances of a successful decode. This makes the system more robust and reliable. In 5G, asynchronous HARQ is used, which means it can handle retransmissions for multiple data streams at the same time, without waiting for one to finish.

- <h6>Logical vs. Transport Channels:</h6> The PDF also shows how the MAC layer connects Logical Channels (which define the type of information, e.g., traffic or control) to Transport Channels (which define how the data is sent over the radio link, e.g., a broadcast or shared channel). The MAC layer handles this mapping.

# The MAC Scheduler
The MAC scheduler is like the traffic cop of the 5G network. Its job is to efficiently manage and distribute the limited radio resources (like frequency and time slots) among many users. It works by taking in various inputs and making smart decisions to ensure the network runs smoothly.

#### Key Functions
-  <h6>Resource Allocation:</h6> The scheduler decides which user gets to transmit or receive data, where on the frequency band this happens, and for how long. It's constantly making decisions to assign resources based on the current network conditions and what each user needs.

- <h6>Balancing Inputs:</h6> The scheduler makes its decisions by considering a few key inputs:

  -  Channel Conditions: It looks at the quality of the radio channel for each user. If a user has a good connection, the scheduler might give them more resources to maximize data speeds.

  -  Buffer Status: It checks how much data each user has waiting to be sent (in their RLC buffer). If a user has a lot of data to send, the scheduler will prioritize them to prevent delays.

  -  Quality of Service (QoS): It considers the QoS requirements of each service. For example, a voice call needs a low delay, so the scheduler will prioritize it over a file download, which is less sensitive to delay.

- <h6>Downlink and Uplink Scheduling:</h6> The scheduler handles both downlink (from the network to the device) and uplink (from the device to the network) traffic. It uses different signals and mechanisms for each direction to make its decisions. For example, for uplink scheduling, it considers the user's buffer status and a Scheduling Request (SR) sent by the device.

# Physical Layer (PHY)
The Physical (PHY) layer is the most fundamental layer of the 5G protocol stack. It is responsible for the actual radio communication, taking the data from the MAC layer and converting it into a signal that can be transmitted wirelessly. The PHY layer is the core of how the network connects a device to the gNodeB.

#### Key Functions
- <h6>Transport Channels to Physical Channels:</h6> The PHY layer is the bridge between the Transport Channels (which define how data is delivered) and the Physical Channels (which are the actual radio resources used for transmission). For example, the Downlink Shared Channel (DL-SCH) is mapped to the Physical Downlink Shared Channel (PDSCH).

- <h6>Error Correction:</h6> The PHY layer adds redundancy to the data using Low-Density Parity-Check (LDPC) coding. This allows the receiver to detect and correct errors that occur during wireless transmission, making the communication more reliable.

- <h6>Modulation:</h6> This process converts digital data into an analog radio signal. The PDF mentions various modulation schemes like QPSK, 16QAM, 64QAM, and 256QAM. Higher-order schemes can carry more data but are more susceptible to noise.

- <h6>Resource Mapping:</h6> This function assigns the data to specific time-frequency resources. In 5G, the network uses an Orthogonal Frequency Division Multiplexing (OFDM)-based waveform to transmit data efficiently by dividing it into many sub-carriers.

- <h6>MIMO (Multiple Input Multiple Output):</h6> Although not explicitly detailed in the PDF, the physical layer uses multiple antennas to send and receive data, which significantly increases the network's capacity and data speeds. This is managed through functions like Layer Mapping and Antenna Mapping.

# Physical Layer Structure
The Physical Layer is where the actual radio communication happens. This explains some of the key technologies that make 5G's high performance possible, particularly how it handles data transmission in the time and frequency domains.

### 1. Orthogonal Frequency Division Multiplexing (OFDM)
OFDM is the core modulation scheme used in 5G. It's a method for transmitting a wideband signal by breaking it down into many smaller, overlapping, narrow-band signals called subcarriers.

- <h6>Why it's used:</h6> A major challenge in wireless communication is Intersymbol Interference (ISI), which happens when a signal's reflections from obstacles arrive at different times, corrupting the main signal. OFDM helps combat this by using a Cyclic Prefix.

- <h6>Cyclic Prefix:</h6> This is a copy of the end of an OFDM symbol that is pasted at the beginning. It acts as a guard interval, helping the receiver to handle reflections and avoid ISI.

### 2. Downlink (DL) vs. Uplink (UL) Waveforms
- <h6>Downlink:</h6> The network uses OFDMA (Orthogonal Frequency Division Multiple Access).

- <h6>Uplink:</h6> The user device uses a variation called DFT-precoded OFDM or SC-FDMA (Single-Carrier Frequency Division Multiple Access).

  The reason for this difference is PAPR (Peak-to-Average Power Ratio). SC-FDMA has a lower PAPR, which means it requires less power from the device's amplifier, leading to better battery efficiency for the user equipment (UE).

### 3. Flexible Numerology and Time Domain Structure
5G uses a concept called Flexible Numerology, which means it can adjust parameters like Subcarrier Spacing (SCS).

- A larger SCS makes the system more robust against frequency errors  and is used for services requiring very low latency.

- The time domain structure in 5G is also flexible. It is organized into a 10ms radio frame, which is divided into subframes. Each subframe is made up of slots, and the duration of a slot changes depending on the subcarrier spacing. This allows the network to adapt to different traffic needs.

### 4. Resource Elements and Resource Blocks
The fundamental unit of radio resource in 5G is the Resource Element.

- A Resource Element is a single subcarrier over one OFDM symbol.

- Resource Blocks are groups of resource elements, which are assigned to users for their data transmission.

# RRC and NAS
These two layers are at the top of the control plane protocol stack. They work together to manage a user device's connection to the 5G network.

- <h6>NAS (Non-Access Stratum):</h6> This layer acts as the bridge between the device (UE) and the core network's AMF (Access and Mobility Function). It handles high-level functions that aren't specific to the radio connection, such as:

  -  Authentication and security.

  -  Registration and idle-mode procedures. 

  -  Assigning IP addresses

- <h6>RRC (Radio Resource Control):</h6> This layer sits between the user device (UE) and the gNodeB. Its main job is to configure and manage the radio connection. Its functions include:

  -  Managing the connection state and mobility functions.

  -  Broadcasting system information.

  -  Configuring and reporting measurements to assist with handovers.

  -  Handling device capabilities.

# RRC States and Mobility
The RRC layer defines the three main states a device can be in, which determine how the network manages its connection and mobility.

- <h6>RRC Idle State:</h6> When a device is powered on but not actively connected to the network, it is in this state. It is Deregistered with the network and has no RRC connection context stored at the gNodeB. Mobility in this state is controlled by the device itself , which tracks Tracking Areas (TAs) defined in the core network.

- <h6>RRC Connected State:</h6> When a device needs to send or receive data, it establishes a connection and moves to this state. Both the device and the network store information about the connection, and the device is Registered. In this state, the network controls mobility, managing handovers between cells.

- <h6>RRC Inactive State:</h6> This is a new state in 5G that provides a middle ground between Idle and Connected. The device and the RAN store a "radio configuration and security" context , allowing for a very fast return to the Connected state when needed. The device's mobility in this state is controlled by the device, similar to the Idle state.

























 


























  
  
 



    














