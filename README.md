# 5G-wireless-network: Architecture, Functions & Call Flows
This repository offers a comprehensive and organized study of the complex world of 5G wireless networks. The project's goal is to simplify the core principles of the 5G System Architecture, its key Network Functions, and the essential data exchanges (call flows) that occur between them.

Here you will find detailed notes on the relationship and operational procedures between the Radio Access Network (RAN) and the Core Network. This includes an in-depth analysis of the roles of major functions like AMF, SMF, UDM, UPF, PCF, and an explanation of their respective protocol stacks.

This project is a valuable resource for anyone who wants to gain a deeper understanding of the technical aspects of 5G, whether you are a student, an engineer, or simply curious about this transformative technology.

## Table of Contents
- [The 5G System](#the-5g-system)
- [The Three Main 5G Use Cases](#the-three-main-5g-use-cases)
- [The 5G System: Core Concepts](#the-5g-system-core-concepts)
- [5G System Deployment Options](#5g-system-deployment-options)
- [RAN Protocol Stack](#ran-protocol-stack)
- [Service Data Adaptation Protocol (SDAP)](#service-data-adaptation-protocol-sdap)
- [Packet Data Convergence Protocol (PDCP)](#packet-data-convergence-protocol-pdcp)
- [Radio Link Control (RLC)](#radio-link-control-rlc)
- [Medium Access Control (MAC)](#medium-access-control-mac)
- [The MAC Scheduler](#the-mac-scheduler)
- [Physical Layer (PHY)](#physical-layer-phy)
- [ Physical Layer Structure](physical-layer-structure)
- [RRC and NAS](#rrc-and-nas)
- [RRC States and Mobility](#rrc-states-and-mobility)
- [Initial Access](#initial-access)
- [Random Access Procedure](#random-access-procedure)
- [5G Core Network Identifiers](#5g-core-network-identifiers)
- [Service-Based Architecture (SBA)](#service-based-architecture-sba)
- [Access and Mobility Management Function (AMF)](#access-and-mobility-management-function-amf)
- [Session Management Function (SMF)](#session-management-function-smf)
- [Unified Data Repository (UDR)](#unified-data-repository-udr)
- [Unified Data Management (UDM)](#unified-data-management-udm)
- [User Plane Function (UPF)](#user-plane-function-upf)
- [Policy Control Function (PCF)](#policy-control-function-pcf)

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

# The 5G System: Core Concepts
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

<img width="1351" height="627" alt="Screenshot (343)" src="https://github.com/user-attachments/assets/b91b1a6f-d958-47f0-9b88-1aabb9368cef" />


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

<img width="1105" height="458" alt="Screenshot (353)" src="https://github.com/user-attachments/assets/38224519-b683-4ac1-8cdf-071c08c4cc2e" />


It acts like a traffic manager, directing data flows to the appropriate paths.

#### Key Functions
- <h6>QoS Flow Mapping:</h6> SDAP's primary function is to map incoming data flows to specific radio bearers.This ensures that different types of data, like a voice call versus a background download, are handled correctly according to their unique performance needs.

<img width="1139" height="593" alt="Screenshot (354)" src="https://github.com/user-attachments/assets/f5780dfe-f380-4df9-9175-8d34dabca170" />


- <h6>QoS Flow Identifier (QFI):</h6> Each data flow is identified by a QoS Flow Identifier (QFI). This allows the network to distinguish between different types of traffic and apply the correct QoS policies to each one.

### Types of QoS Flows
The outlines different types of QoS flows, each defined by a 5QI (5G QoS Identifier).

<img width="976" height="553" alt="Screenshot (357)" src="https://github.com/user-attachments/assets/df22a241-8ec2-4dfb-a7cb-721a4f901f83" />


- <h6>GBR (Guaranteed Bit Rate):</h6> This is for services that need a guaranteed data rate, like voice calls or real-time video streaming. These services are more sensitive to delays and require consistent performance.

- <h6>Non-GBR (Non-Guaranteed Bit Rate):</h6> This is for services that don't need a guaranteed data rate, such as browsing the web, downloading files, or social media. These services are more flexible and can tolerate some delay or variation in speed.

- <h6>Delay Critical GBR:</h6> This is a specific type of GBR for applications that are extremely sensitive to delay, such as remote control and vehicle-to-everything (V2X) communications.

# Packet Data Convergence Protocol (PDCP)
The PDCP layer sits in the middle of the RAN protocol stack. Its primary role is to ensure the secure and reliable delivery of data packets.

#### Key Functions

- <h6>Header Compression:</h6> PDCP uses a technique called Robust Header Compression (ROHC) to reduce the size of the IP header in data packets. 

  This is especially useful for applications like Voice over IP (VoIP), where the header can be much larger than the actual voice payload. By compressing the header, the network becomes more efficient.

  <img width="1400" height="809" alt="Screenshot (361)" src="https://github.com/user-attachments/assets/200eee80-4acb-476e-bf12-6946868dc74f" />


- <h6>Ciphering and Integrity Protection:</h6> This is a core security function of the PDCP layer. It uses encryption to prevent eavesdropping and integrity protection to ensure that the data hasn't been tampered with. 

  The PDCP layer applies these security measures to both user data and control signaling.

  <img width="1382" height="581" alt="Screenshot (362)" src="https://github.com/user-attachments/assets/de6dbbfd-370e-42f5-9416-f74565ca5c34" />


- <h6>In-sequence Delivery:</h6> PDCP ensures that data packets are delivered to the higher layers in the correct order. If packets arrive out of order from the lower layers, PDCP reorders them before passing them up.

<img width="1237" height="626" alt="Screenshot (364)" src="https://github.com/user-attachments/assets/c4b212b3-aa40-4c4e-8f66-282d6490b437" />

- <h6>Routing and Duplication:</h6> PDCP can intelligently route data. For example, in a "split bearer" scenario, the PDCP layer can duplicate packets and send them over multiple radio links to ensure higher reliability.

<img width="1379" height="663" alt="Screenshot (363)" src="https://github.com/user-attachments/assets/836b3804-5fee-41a1-871e-eef346df428d" />


# Radio Link Control (RLC)
The RLC layer is a key part of the 5G RAN protocol stack, sitting between the PDCP and MAC layers. Its main responsibility is to ensure the efficient and reliable delivery of data packets.

It does this by using different operational modes, each suited for a specific type of data traffic.

<img width="1358" height="680" alt="Screenshot (365)" src="https://github.com/user-attachments/assets/c3d26da1-9d27-4e1b-879f-1b0847fe5920" />


### RLC Modes
The RLC layer operates in three different modes, each with unique capabilities:

- <h6>Transparent Mode (TM):</h6> This is the simplest mode. It does not perform any segmentation, reassembly, or retransmissions.

  It simply passes data through without any changes. This is used for very specific signaling messages where the higher layers are responsible for any reliability.

 - <h6>Unacknowledged Mode (UM):</h6> This mode performs segmentation and reassembly. It breaks down large data packets into smaller segments for transmission and then puts them back together at the receiving end. However, it does not perform retransmissions. This is suitable for services that can tolerate some data loss, like streaming video.

 - <h6>Acknowledged Mode (AM):</h6> This is the most robust mode. It performs all the functions of Unacknowledged Mode, plus it handles retransmissions (ARQ - Automatic Repeat Request). 

   If a data segment is lost or received with an error, the receiver will request the sender to retransmit it. This mode is used for services that require a high level of reliability, like web browsing or file downloads.

# Medium Access Control (MAC)
The MAC layer sits just below the RLC layer and is responsible for managing the radio channel efficiently. Its main job is to coordinate the flow of data from various sources and ensure everything is scheduled correctly.

<img width="1326" height="646" alt="Screenshot (376)" src="https://github.com/user-attachments/assets/87919fb5-b162-44b6-a781-6cca72b23381" />


#### Key Functions
- <h6>Multiplexing and De-multiplexing:</h6> This is a core function of the MAC layer. It takes data from different Logical Channels (like those for voice, video, or signaling) and combines them into a single data block for the lower layers. At the receiving end, it does the reverse, separating the data and sending it to the correct RLC layer.

<img width="865" height="429" alt="Screenshot (378)" src="https://github.com/user-attachments/assets/508fdbfd-418a-485f-a01b-9103d5f9157b" />


- <h6>Scheduling:</h6> The MAC layer is responsible for scheduling all data transmissions. It decides which devices get to transmit and receive data, when they can do it, and how much data they can send. This is a crucial function for optimizing network performance and ensuring a fair distribution of resources.

- <h6>Hybrid ARQ (HARQ):</h6> This is a mechanism for retransmissions. Unlike the RLC layer's retransmissions, HARQ works very quickly at the physical layer. It combines a retransmitted data packet with the original packet to increase the chances of a successful decode. This makes the system more robust and reliable. In 5G, asynchronous HARQ is used, which means it can handle retransmissions for multiple data streams at the same time, without waiting for one to finish.

<img width="1295" height="534" alt="Screenshot (380)" src="https://github.com/user-attachments/assets/ed6d1d2a-6199-454f-bb32-a34b15594ec1" />


- <h6>Logical vs. Transport Channels:</h6> This shows how the MAC layer connects Logical Channels (which define the type of information, e.g., traffic or control) to Transport Channels (which define how the data is sent over the radio link, e.g., a broadcast or shared channel). The MAC layer handles this mapping.

# The MAC Scheduler
The MAC scheduler is like the traffic cop of the 5G network. Its job is to efficiently manage and distribute the limited radio resources (like frequency and time slots) among many users. It works by taking in various inputs and making smart decisions to ensure the network runs smoothly.

<img width="1183" height="595" alt="Screenshot (383)" src="https://github.com/user-attachments/assets/8fdd106b-ac6f-4f9e-bb51-a91f2d38a122" />


#### Key Functions
-  <h6>Resource Allocation:</h6> The scheduler decides which user gets to transmit or receive data, where on the frequency band this happens, and for how long. It's constantly making decisions to assign resources based on the current network conditions and what each user needs.

- <h6>Balancing Inputs:</h6> The scheduler makes its decisions by considering a few key inputs:

  -  Channel Conditions: It looks at the quality of the radio channel for each user. If a user has a good connection, the scheduler might give them more resources to maximize data speeds.

  -  Buffer Status: It checks how much data each user has waiting to be sent (in their RLC buffer). If a user has a lot of data to send, the scheduler will prioritize them to prevent delays.

  -  Quality of Service (QoS): It considers the QoS requirements of each service. For example, a voice call needs a low delay, so the scheduler will prioritize it over a file download, which is less sensitive to delay.

- <h6>Downlink and Uplink Scheduling:</h6> The scheduler handles both downlink (from the network to the device) and uplink (from the device to the network) traffic. It uses different signals and mechanisms for each direction to make its decisions. For example, for uplink scheduling, it considers the user's buffer status and a Scheduling Request (SR) sent by the device.

# Physical Layer (PHY)
The Physical (PHY) layer is the most fundamental layer of the 5G protocol stack. It is responsible for the actual radio communication, taking the data from the MAC layer and converting it into a signal that can be transmitted wirelessly. The PHY layer is the core of how the network connects a device to the gNodeB.

<img width="1203" height="533" alt="Screenshot (393)" src="https://github.com/user-attachments/assets/7d6feac4-679d-4929-a369-47ef3aa5b08c" />


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

<img width="1267" height="535" alt="Screenshot (408)" src="https://github.com/user-attachments/assets/f230fd2a-4ffa-496a-a341-d7d5736158f6" />


- <h6>Why it's used:</h6> A major challenge in wireless communication is Intersymbol Interference (ISI), which happens when a signal's reflections from obstacles arrive at different times, corrupting the main signal. OFDM helps combat this by using a Cyclic Prefix.

- <h6>Cyclic Prefix:</h6> This is a copy of the end of an OFDM symbol that is pasted at the beginning. It acts as a guard interval, helping the receiver to handle reflections and avoid ISI.

### 2. Downlink (DL) vs. Uplink (UL) Waveforms
- <h6>Downlink:</h6> The network uses OFDMA (Orthogonal Frequency Division Multiple Access).

- <h6>Uplink:</h6> The user device uses a variation called DFT-precoded OFDM or SC-FDMA (Single-Carrier Frequency Division Multiple Access).

  The reason for this difference is PAPR (Peak-to-Average Power Ratio). SC-FDMA has a lower PAPR, which means it requires less power from the device's amplifier, leading to better battery efficiency for the user equipment (UE).

### 3. Flexible Numerology and Time Domain Structure
5G uses a concept called Flexible Numerology, which means it can adjust parameters like Subcarrier Spacing (SCS).

<img width="1257" height="601" alt="Screenshot (411)" src="https://github.com/user-attachments/assets/9ceab89f-32f8-4cf6-97b7-b3fca4b17961" />

- A larger SCS makes the system more robust against frequency errors  and is used for services requiring very low latency.

- The time domain structure in 5G is also flexible. It is organized into a 10ms radio frame, which is divided into subframes. Each subframe is made up of slots, and the duration of a slot changes depending on the subcarrier spacing. This allows the network to adapt to different traffic needs.

### 4. Resource Elements and Resource Blocks
The fundamental unit of radio resource in 5G is the Resource Element.

- A Resource Element is a single subcarrier over one OFDM symbol.

- Resource Blocks are groups of resource elements, which are assigned to users for their data transmission.

# RRC and NAS
These two layers are at the top of the control plane protocol stack. They work together to manage a user device's connection to the 5G network.

<img width="1339" height="638" alt="Screenshot (416)" src="https://github.com/user-attachments/assets/3f798318-8f1a-4ed0-9440-c39b6e1de935" />

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

<img width="1342" height="594" alt="Screenshot (418)" src="https://github.com/user-attachments/assets/2b050e96-3535-40f1-a7f1-21efb53e4e6e" />


- <h6>RRC Idle State:</h6> When a device is powered on but not actively connected to the network, it is in this state. It is Deregistered with the network and has no RRC connection context stored at the gNodeB. Mobility in this state is controlled by the device itself , which tracks Tracking Areas (TAs) defined in the core network.

- <h6>RRC Connected State:</h6> When a device needs to send or receive data, it establishes a connection and moves to this state. Both the device and the network store information about the connection, and the device is Registered. In this state, the network controls mobility, managing handovers between cells.

- <h6>RRC Inactive State:</h6> This is a new state in 5G that provides a middle ground between Idle and Connected. The device and the RAN store a "radio configuration and security" context , allowing for a very fast return to the Connected state when needed. The device's mobility in this state is controlled by the device, similar to the Idle state.


# Initial Access
Initial access is the procedure by which a user device (UE) finds a 5G cell, synchronizes with it, and gets the essential information needed to connect to the network. This process is a crucial prerequisite for any data or signaling exchange.

#### Key Steps
### 1.Cell Search:

<img width="1303" height="631" alt="Screenshot (503)" src="https://github.com/user-attachments/assets/05f13668-0461-456d-8f4c-90a18aa10c21" />

The UE first scans for Synchronization Signal Blocks (SSBs) from nearby cells. The SSB is a combination of two signals and one channel:

- <h6>PSS (Primary Synchronization Signal):</h6> Helps the device get coarse time and frequency synchronization and determines the cell's Physical Cell ID (PCI) Group.

- <h6>SSS (Secondary Synchronization Signal):</h6> Provides fine-tuned synchronization and helps determine the PCI within the group.

- <h6>PBCH (Physical Broadcast Channel):</h6> Carries the Master Information Block (MIB), which contains critical system information needed to decode other network broadcasts.

### 2.Decode System Information:
After synchronizing, the device decodes the broadcasted information. The MIB points to the location of the SIB1 (System Information Block 1).

- <h6>SIB1:</h6> This block contains information about cell selection and access, including a list of neighboring cells, and schedules for other SIBs.

- <h6>Other SIBs:</h6> The network can also broadcast other SIBs (like SIB2-9) that provide additional information, such as cell re-selection parameters or public warnings. These can be transmitted periodically or on-demand.

### 3.Random Access Procedure:
Once the device has the necessary system information, it begins the Random Access procedure to establish a connection. There are two main types of random access:

- <h6>Contention-Based Random Access (CBRA):</h6> This is a four-step process where multiple devices may try to access the network at the same time, which can lead to collisions. The procedure includes the device sending a Random Access Preamble, receiving a Random Access Response (RAR) from the gNodeB, and then a Contention Resolution step to resolve any conflicts.

- <h6>Contention-Free Random Access (CFRA):</h6> This is a two-step process used when a dedicated preamble is assigned to a single device (e.g., during a handover), eliminating the risk of a collision.


# Random Access Procedure
The Random Access procedure is the method a device uses to establish a connection with the network. It is triggered by several events, such as when a device has uplink data to send, when it needs to re-sync with the network, or during a handover. The procedure can be either contention-based or contention-free.

<img width="1261" height="585" alt="Screenshot (502)" src="https://github.com/user-attachments/assets/4f581999-7b4b-4b71-b795-0e8c80d8a0d4" />

## Contention-Based Random Access (CBRA)
This is the standard, four-step process used when a device does not have a dedicated preamble from the network. There's a chance that two or more devices might try to access the network at the same time, which can cause a "contention" or collision.

<h6>Step 1: Random Access Preamble (PRACH):</h6> The device sends a random preamble to the gNodeB. This is like a "Hello, I want to connect" message. The gNodeB uses this to estimate the timing and power of the device.

<h6>Step 2: Random Access Response (RAR):</h6> The gNodeB hears the preamble and sends back a response. This response includes:

- A Timing Advance Command to correct the device's timing.

- A Temporary Cell-Radio Network Temporary Identifier (TC-RNTI), which is a temporary ID for the device.

- An Uplink Scheduling Grant that tells the device where and when it can send its next message.

<h6>Step 3: Scheduled Transmission (Msg3):</h6> Using the uplink grant from the previous step, the device sends its RRC Connection Setup Request message. This message also contains a unique identifier (UE Contention Resolution Identity) to resolve any potential collisions.

<h6>Step 4: Contention Resolution (Msg4):</h6> The gNodeB broadcasts a message that includes the unique identifier from Step 3. All devices that participated in the random access listen. The device whose ID matches is now officially connected, and its TC-RNTI is promoted to a permanent C-RNTI. Other devices that were in a collision receive no response and must restart the process.

## Contention-Free Random Access (CFRA)
This is a simpler, two-step process used to avoid collisions. The network explicitly assigns a dedicated random access preamble to a device, which guarantees that only that device will use it. This is typically used during handovers or for specific services.

# 5G Core Network Identifiers
In a 5G network, there are various types of identifiers, which can be divided into two main categories: Device Identity and Subscription Identity.

## 1. Permanent Equipment Identifier (PEI)

<img width="1275" height="689" alt="Screenshot (463)" src="https://github.com/user-attachments/assets/8232267d-eb1c-4a23-9297-a931997539b8" />

- This is a permanent ID for each User Equipment (UE) or device.

- It can be sent in the network as the International Mobile station Equipment Identity (IMEI) or International Mobile station Equipment Identity and Software Version Number (IMEISV).

- The IMEISV is a 16-digit number that includes the Type Allocation Code (TAC), Serial Number (SNR), and Software Version Number (SVN).

## 2. Subscription Permanent Identity (SUPI)
This is a permanent ID for a user's subscription.An example of this is the International Mobile Subscriber Identity (IMSI).

<img width="1384" height="739" alt="Screenshot (464)" src="https://github.com/user-attachments/assets/201b1cb7-1aa2-4ca8-937a-62e06013bf06" />

The IMSI can be 15 or 16 digits long and has three parts:

- Mobile Country Code (MCC): 3 digits.

- Mobile Network Code (MNC): 2 or 3 digits.

- Mobile Subscriber Identification Number (MSIN): Up to 10 digits.

The SUPI can also be represented as a Network Access Identifier (NAI), which is in the username@realm format.

## 3. Subscription Concealed Identity (SUCI)
The SUCI is a temporary ID used to protect the SUPI when it's being sent in the network.

<img width="1315" height="652" alt="Screenshot (465)" src="https://github.com/user-attachments/assets/7ca4c63f-8bbd-4c79-a979-1325f5076374" />

- Its main purpose is to prevent security issues like IMSI Catching.

- When the SUPI is transmitted in the network, the SUCI is used to conceal its original form.

## 4. Globally Unique Temporary Identifier (GUTI)
The GUTI is a temporary ID that the network assigns to the user's device.Its purpose is to enhance security and prevent permanent IDs like the SUPI or SUCI from being sent over the network unnecessarily.

<img width="1303" height="700" alt="Screenshot (466)" src="https://github.com/user-attachments/assets/b8f1e88f-8ef0-4a75-8e20-d582b98f3a36" />

The GUTI is divided into two parts:

- Globally Unique AMF ID (GUAMI): This includes the MCC, MNC, and AMF Region, AMF Set, and AMF Pointer.

- 5G Temporary Mobile Subscriber Identity (5G-TMSI): This is a temporary ID given to the user.

# Service-Based Architecture (SBA)
Unlike the traditional "Reference Point" architecture of 4G, which used fixed interfaces between network elements, the 5G Core uses a Service-Based Architecture. In this model, each Network Function (NF) (like AMF, SMF, etc.) is a self-contained microservice that exposes its services to other NFs. This makes the network more flexible and scalable.

#### Key Concepts
- <h6>Network Functions (NFs):</h6> These are the individual components of the 5G Core. Instead of being physical boxes, they are software functions that can be deployed on a cloud platform.

- <h6>Service Producers and Consumers:</h6> In SBA, one NF (Service Producer) offers a service that another NF (Service Consumer) can use. For example, the PCF (Policy Control Function) produces a service that the AMF (Access and Mobility Management Function) consumes.

- <h6>Web-Based Interfaces:</h6> Communication between NFs happens over open, web-based APIs, primarily using HTTP/2. This is a major shift from the dedicated, complex protocols of 4G. The common HTTP methods like POST (to send information), PUT (to send/replace information), and DELETE (to remove information) are used.

### How Service Discovery Works
For this architecture to work, a Network Function needs to be able to find and communicate with the specific services it needs. This is handled by a central Network Function called the Network Repository Function (NRF).

- <h6>1.Service Registration:</h6> When a Network Function (e.g., the AMF) comes online, it first registers itself with the NRF. It sends a message (HTTP PUT) to the NRF, providing details about its services. The NRF stores this information.

- <h6>2.Service Discovery:</h6> When another Network Function (e.g., the SMF) needs a service, it doesn't need to know the address of the specific NF providing that service. Instead, it sends a query (HTTP GET) to the NRF.

- <h6>3.Service Request:</h6> The NRF responds with a list of the NFs that can provide the requested service. The consuming NF can then send its request (HTTP POST) to one of those NFs to get the information it needs.

# Access and Mobility Management Function (AMF)
The Access and Mobility Management Function (AMF) is a critical Network Function within the 5G Core Network, responsible for the Control Plane. It handles the control signaling between your user equipment (UE), which is your phone, and the network.

Its main functions are:
### 1. Registration Management</h6>
When a device connects to the 5G network for the first time, it has to complete a Registration Procedure.The AMF manages this procedure, which involves authenticating (identifying) and authorizing (granting access to) the device with the network. This process creates the user's context within the network.

<img width="1351" height="761" alt="Screenshot (480)" src="https://github.com/user-attachments/assets/a4ed72fd-7667-49a5-9eb4-205bd4f40a49" />

### 2. Connection Management
The AMF establishes and releases the control plane signaling connections between the device and the core network. This connection is created through Radio Resource Control (RRC) and Non-Access Stratum (NAS) signaling.

<img width="1374" height="592" alt="Screenshot (481)" src="https://github.com/user-attachments/assets/6e212483-ac92-432c-a01c-656b9d0a7cfc" />

### 3. Mobility Management
The AMF manages the location tracking and handover (moving from one cell to another) of connected devices. If a device moves from one cell to another, the AMF handles its mobility to ensure its data connection remains active.

<img width="1392" height="600" alt="Screenshot (484)" src="https://github.com/user-attachments/assets/4cde9a31-8364-4ed6-bae9-6f62e3fbfd0c" />

# Session Management Function (SMF)
The Session Management Function (SMF) is a core network function in the 5G system. It is responsible for all aspects of PDU Session Management. The SMF controls the user plane function (UPF) and handles the signalling related to data sessions.

#### Key Responsibilities of the SMF
- <h6>PDU Session Establishment, Modification, and Release:</h6> The SMF sets up, changes, and tears down PDU Sessions. A PDU Session is a logical connection that provides data services (like internet access) between the user equipment (UE) and a Data Network (DN).

<img width="1367" height="684" alt="Screenshot (487)" src="https://github.com/user-attachments/assets/23330364-65e0-4a7f-8fcd-a9c2b758413f" />

- <h6>IP Address Allocation:</h6> The SMF is in charge of assigning an IP Address to the device (UE) for each PDU Session. It can allocate IPv4, IPv6, or dual-stack (both) addresses.

- <h6>UPF Selection and Control:</h6> The SMF selects the appropriate User Plane Function (UPF) for the session and controls its data path.

- <h6>Session Continuity Management:</h6> The SMF manages how a session remains active when a device moves. The document mentions Session Continuity Modes (SSC Modes):

<img width="1351" height="749" alt="Screenshot (493)" src="https://github.com/user-attachments/assets/49435afb-d0fd-4b5e-b64e-7a014f70e226" />

  -  SSC Mode 1: This is a "break-before-make" approach. When the device moves to a new location that requires a different anchor point, the old PDU Session is released, and a new one is set up with a new IP address.

  -  SSC Mode 2: This is a "make-before-break" approach. A new PDU Session is established first with a new anchor point and a new IP address, and only then is the old session released. This minimizes service interruption.

The SMF works closely with the AMF (Access and Mobility Management Function) to provide a complete service to the user. While the AMF handles connection and mobility on the control plane, the SMF manages the actual data sessions.

# Unified Data Repository (UDR)
The UDR is a database where various types of data are stored. It serves as a central repository for different types of information, including:

<img width="1359" height="635" alt="Screenshot (495)" src="https://github.com/user-attachments/assets/f9db937c-9734-461d-b818-924e62327b0e" />


- <h6>Subscription Data:</h6> Information about the user's subscription.

- <h6>Policy Data:</h6> Data related to network policies.

- <h6>Structured Data for Exposure:</h6> Data that is made available to external applications.

- <h6>Application Data:</h6> Information related to specific applications.

The design is described as cloud-native and stateless.

# Unified Data Management (UDM)
The UDM functions as the front-end for the user subscription data that is stored in the UDR. Its main responsibilities include:

<img width="1259" height="710" alt="Screenshot (496)" src="https://github.com/user-attachments/assets/96969c6b-d684-4b49-9d70-1e3e74dd6cc7" />


- Supporting application logic.

- Managing access and registration.

- Handling authentication.

In essence, the UDR stores the data, while the UDM provides the logic and services that access and manage that data.

# User Plane Function (UPF)
The User Plane Function (UPF) is a core component of the 5G Core network. Its primary role is to handle all user data traffic, acting as a crucial bridge between your device (known as the UE, or User Equipment) and external networks like the internet.

<img width="1367" height="730" alt="Screenshot (498)" src="https://github.com/user-attachments/assets/838ef98a-290b-428f-9e08-e9f5b471943c" />

A key function of the UPF is to conceal your device's movement from these external networks. This ensures that even as you move and hand off between different cell towers, your connection remains stable and seamless

#### Key Functions of the UPF
- <h6>Connects to External Networks:</h6> The UPF connects the 5G network to external IP networks, such as the public internet.

- <h6>Serves as an Anchor Point:</h6> It acts as the anchor for all of your device’s data sessions. This ensures continuous connectivity and a smooth user experience, even when you are mobile.

- <h6>Handles Charging and Reporting:</h6> The UPF is responsible for generating data records and traffic usage reports, which are essential for billing purposes.

- <h6>Manages Traffic Flow:</h6> It handles data buffering and applies Quality of Service (QoS) markings to manage and prioritize traffic, ensuring that different types of data (like voice calls versus a web page) are handled appropriately.

The UPF uses the Packet Forwarding Control Protocol (PFCP) for session management. When a data packet arrives, the UPF performs a lookup using a Packet Detection Rule (PDR) to find the correct PFCP session. It then applies a set of instructions from several different rules:

- Forwarding Action Rules (FAR) to determine where to send the packet.

- Buffering Action Rules (BAR) if the packet needs to be temporarily held.

- QoS Enforcement Rules (QER) to apply quality of service.

- Usage Reporting Rules (URR) to track data usage.

# Policy Control Function (PCF)
The Policy Control Function (PCF) is a core component of the 5G network that sets and enforces rules for user behavior, data sessions, and network traffic. It acts as the central brain for policy decisions.

<img width="1356" height="546" alt="Screenshot (499)" src="https://github.com/user-attachments/assets/72869517-3ab6-4e05-9610-a962970d756c" />

#### Key Policy Types
The PCF manages two main types of policies:

- Non-session-related policies: These control a user's overall access and mobility. Examples include:

  -  Service Area Restrictions: Limiting where a user can access the network.

  -  UE Route Selection Policy (URSP): Guiding a device on which network slice or access technology (like Wi-Fi) to use.

- Session-related policies: These are specific to a data session and include:

  -  Gating Control: Allowing or blocking specific data packets.

  -  QoS Control: Ensuring each data flow receives the right Quality of Service (QoS), like providing low latency for a video call.





























 


























  
  
 



    














