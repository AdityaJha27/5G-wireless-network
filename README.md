# 5G-wireless-network
# The 5G System
- ### Global Standardization Effort:
  it's a global standard developed through an international effort. The International Telecommunication Union (ITU) led this initiative with a vision to "connect all the world's people".
  
  <img width="1381" height="848" alt="Screenshot (303)" src="https://github.com/user-attachments/assets/9b5b6bdb-c62b-4dd1-8fdd-63d5a063eadc" />

- ### Key Requirements:
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


- ### Key Features:
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


### Key Network Functions
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

















  
  
 



    














