# 🌐 Computer Networks

## 1. Introduction to Computer Networks

A **computer network** is a system of interconnected devices (computers, servers, routers, switches, mobile devices, IoT sensors, etc.) that can exchange data and share resources with each other.  
In today’s IT world, networks form the backbone of almost everything we do — from browsing websites, deploying applications in the cloud, video conferencing, to managing distributed systems in DevOps.

---

### 🔑 Why Networks Matter in IT?
- **Collaboration:** Teams across the globe can work together in real-time (e.g., Google Docs, Slack).  
- **Cloud Computing:** AWS, Azure, and GCP rely entirely on networking to connect data centers and customers.  
- **Microservices & DevOps:** Modern applications are broken into multiple services (APIs, databases, caching layers) that communicate over the network.  
- **Remote Work:** VPNs, SSH, and secure protocols allow engineers to manage servers from anywhere.  

Without networks, there would be no **Internet**, no **email**, no **websites**, no **DevOps pipelines**, and no **distributed systems**.

---

### ⚙️ Real-World Example: Opening `https://github.com`
When you type `https://github.com` in your browser:
1. **DNS Resolution:** The domain name `github.com` is translated into an IP address.  
2. **TCP Connection:** Your browser establishes a **TCP connection** with GitHub’s server over port `443` (HTTPS).  
3. **TLS Handshake:** A secure encrypted channel is set up using TLS.  
4. **HTTP Request:** Your browser sends an HTTP `GET` request asking for the GitHub homepage.  
5. **Server Response:** GitHub’s servers respond with HTML, CSS, and JavaScript files.  
6. **Rendering:** Your browser renders the page and shows the GitHub homepage.  

All of this happens in **milliseconds**, powered by computer networks.

---

### 🧩 Key Takeaways
- A network connects devices so they can **communicate** and **share resources**.  
- Networking is essential for **software engineers, DevOps engineers, and cloud architects**.  
- Even simple actions like opening a website involve **multiple networking steps and protocols**.  

---

## 2. History & Evolution of Networks

Computer networking has evolved rapidly over the past few decades. Let’s focus on the **key changes that shaped today’s Internet**:

---

### 📡 Early Days
- **1960s–70s:** ARPANET connected a few universities — the first step towards the Internet.  
- Networks were limited, used mainly for research and text-based communication.  

---

### 💻 Client-Server Era
- **1980s–90s:** Rise of **client-server model** — PCs connected to central servers for email, file sharing, and applications.  
- Protocols like **SMTP (email), FTP (file transfer), HTTP (web)** became popular.  
- Businesses began deploying **LANs (Local Area Networks)** in offices.  

---

### 🌍 Birth of the Internet
- **1990s:** Networks worldwide connected, forming the **Internet**.  
- Websites, web browsers, and ISPs became mainstream.  
- **Optical fiber cables** and undersea cables started forming the global backbone.  

---

### ☁️ Modern Networking
- **2000s–Present:**  
  - **Cloud Computing (AWS, Azure, GCP):** On-demand servers and services accessible via the Internet.  
  - **Mobile & Wireless:** WiFi, 4G/5G networks enable always-on connectivity.  
  - **DevOps & Microservices:** Applications are distributed across multiple services communicating over APIs.  
  - **Virtual Networks:** VPNs, SDN (Software Defined Networking), and container networking (Kubernetes CNIs).  

---

### 🧩 Key Takeaways
- Networking moved from **research → business → Internet → cloud-native world**.  
- Today, almost all modern IT infrastructure — from Kubernetes clusters to CI/CD pipelines — relies on computer networks.  

---

## 3. Networking Architectures

The way devices communicate in a network can be organized into different **architectures**. The two most common are **Client-Server** and **Peer-to-Peer (P2P)**.

---

### 🖥️ Client-Server Architecture
In this model, one system acts as the **server** (provides services or resources), and the other systems act as **clients** (request services).

- **How it works:**
  1. The client sends a request (e.g., “give me the homepage”).
  2. The server processes the request.
  3. The server sends a response back to the client.

- **Real-world IT examples:**
  - **Web Applications:** Your browser (client) requests data from a web server (GitHub, Gmail, Netflix).  
  - **Databases:** An application connects to a database server (MySQL, PostgreSQL) to fetch records.   

- **Advantages:**
  - Centralized control and management.
  - Easier to secure and monitor.
- **Disadvantages:**
  - Server can become a bottleneck.
  - If server fails → service downtime.

---

### 🤝 Peer-to-Peer (P2P) Architecture
In this model, **each device (peer)** can act as both **client and server**. There’s no single point of control.

- **How it works:**
  - Devices connect directly and share resources with each other.

- **Real-world IT examples:**
  - **BitTorrent:** Peers share pieces of a file with each other.  
  - **Blockchain & Cryptocurrencies:** Every node maintains a copy of the ledger and validates transactions.  
  - **Collaboration Tools:** Some messaging apps (early Skype versions) used P2P for direct communication.  

- **Advantages:**
  - Highly scalable (no central server dependency).
  - Resource sharing is distributed.  
- **Disadvantages:**
  - Harder to secure and manage.
  - Performance depends on peers’ availability.  

---

### 🧩 Key Takeaways
- **Client-Server**: Centralized, reliable, but server can be a bottleneck.  
- **P2P**: Decentralized, scalable, but harder to control.  
- Modern systems often use a **hybrid approach** (e.g., P2P for file distribution + central servers for authentication).  

---

## 4. Protocols & Standards

A **protocol** is a set of rules that define how data is transmitted and received over a network.  
Without protocols, devices from different vendors would not be able to communicate reliably.

---

### 📜 Why Standards Matter
- Networking involves millions of devices across the globe — from laptops and smartphones to routers and cloud servers.  
- **Standards** ensure that all these devices can talk to each other, regardless of manufacturer.  
- Example: A Windows laptop can connect to a Linux server using SSH because both follow the **SSH protocol standard**.  

---

### 🔑 Common Networking Protocols
Here are the most widely used protocols in modern IT environments:

| Layer (TCP/IP) | Protocol | Purpose | Real-World Example |
|----------------|----------|---------|--------------------|
| Application | **HTTP/HTTPS** | Web communication | Browsing `https://github.com` |
| Application | **DNS** | Converts domain names → IP addresses | Resolving `github.com` to `140.82.xx.xx` |
| Application | **SMTP, IMAP, POP3** | Email transmission & retrieval | Sending email via Gmail/Outlook |
| Application | **FTP/SFTP** | File transfer | Uploading files to a server |
| Application | **SSH** | Secure remote login | Connecting to a Linux VM in AWS |
| Transport | **TCP** | Reliable communication | Git clone over HTTPS |
| Transport | **UDP** | Low-latency communication | Online gaming, video streaming |
| Internet | **IP (IPv4/IPv6)** | Logical addressing & routing | Sending packets across the Internet |
| Internet | **ICMP** | Error reporting, diagnostics | `ping google.com` |
| Network Access | **Ethernet, WiFi** | Physical + Data Link transmission | Office LAN, home WiFi |

---

### 🌍 Real-World Example
When you run:

```bash
curl https://example.com
````

This is what happens under the hood:

1. **DNS**: Your system resolves `example.com` into an IP address.
2. **TCP**: A TCP connection is established on port `443`.
3. **TLS (HTTPS)**: Encryption is negotiated for secure transfer.
4. **HTTP**: A GET request is sent for the `/` resource.
5. **Server Response**: The server replies with an HTML page.

This single command uses **multiple protocols** working together in layers.

---

### 🧩 Key Takeaways

* Protocols = **rules for communication**.
* Standards allow **interoperability** across devices, OSes, and vendors.
* Every time you open a website, check email, or SSH into a server, multiple protocols are working behind the scenes.

---

## 5. Data Transmission Basics

At the core of networking is the process of **sending and receiving data**.  
But computers do not send entire files or web pages in one go — instead, data is broken into **small packets**, which are then transmitted across the network.

---

### 📦 What is a Packet?
- A **packet** is the basic unit of data transmitted over a network.  
- Each packet contains:
  - **Header** → Control information (source/destination IP, port, protocol type, sequence numbers).  
  - **Payload** → The actual data being carried (HTML content, JSON response, etc.).  
  - **Trailer** → Error-checking information (in some layers).  

---

### 🔄 Encapsulation & Decapsulation
When data is sent from one computer to another, it passes through multiple layers of the networking stack.  
Each layer **adds its own header** (encapsulation).  
At the receiving end, each layer **removes its header** (decapsulation).

#### Flow Example: Sending an HTTP request
1. **Application Layer (HTTP):**  
   - Data = `GET / HTTP/1.1` request.  
2. **Transport Layer (TCP):**  
   - Adds TCP header (source port, destination port, sequence number).  
3. **Internet Layer (IP):**  
   - Adds IP header (source IP, destination IP).  
4. **Data Link Layer (Ethernet/WiFi):**  
   - Adds MAC addresses of source and destination devices.  
5. **Physical Layer:**  
   - Converts the data into electrical signals, light pulses, or radio waves.  

On the receiving side (the server), the reverse process happens (decapsulation).  

---

### 🌍 Real-World Example: Accessing `https://example.com`
1. You type `https://example.com` in your browser.  
2. The browser generates an **HTTP request**.  
3. The request is encapsulated with TCP, IP, and Ethernet headers.  
4. The data travels from:
   - **Your laptop → WiFi router → ISP → Internet backbone → Server**.  
5. At each hop, devices like **routers** examine the IP header to decide the next path.  
6. At the destination, the server decapsulates the packet, processes the HTTP request, and sends back a response.  

---

### 📊 Packet Fragmentation
- Networks have size limits called **MTU (Maximum Transmission Unit)**.  
- If a packet is too large, it is **fragmented** into smaller packets.  
- Example: Uploading a 10 MB file → broken into thousands of smaller packets.  

---

### 🧩 Key Takeaways
- Data is always transmitted in **packets**, not as a whole file at once.  
- **Encapsulation** wraps data with headers at each layer, and **decapsulation** unwraps them.  
- Tools like **Wireshark** let engineers capture and analyze packets in real-time.  

---

## 6. IP Addressing

Every device in a network needs a unique identifier to communicate.  
That identifier is the **IP address (Internet Protocol address)**.

---

### 📍 What is an IP Address?
- An **IP address** is a logical numeric address assigned to each device on a network.  
- It identifies both:
  - **Source** (where the packet came from).  
  - **Destination** (where the packet is going).  

Example:
- When you call your friend, from contacts you will be calling to his name but in back ground its dailing to his unique mobile number.  
- When you ping Google (`ping google.com`), your packet might be routed to an IP like `142.250.77.78` (Google has many servers in your case it might be differ).

---

### 🌐 IPv4
- **32-bit address** (4 octets, written in decimal).  
- Example: `192.168.1.10`  
- Total: ~4.3 billion possible addresses.  
- Problem: With billions of devices (IoT, cloud, mobile), IPv4 is not enough.  

---

### 🌍 IPv6
- **128-bit address** (written in hexadecimal).  
- Example: `2001:0db8:85a3:0000:0000:8a2e:0370:7334`  
- Virtually unlimited addresses (~340 undecillion).  
- Designed to replace IPv4, but both are used today (dual stack).  

---

### 🏠 Public vs Private IPs
- **Public IP:** Globally routable on the Internet (e.g., a cloud VM’s IP).  
- **Private IP:** Used within local networks, not accessible directly from Internet.   

**Real-world example:**  
- In AWS, a **VPC subnet** may use private IPs (`10.x.x.x`).  
- To access the Internet, instances go through a **NAT Gateway** with a public IP.  

---

### 🖧 Static vs Dynamic IPs
- **Static IP:** Manually assigned, does not change. (e.g., database server).  
- **Dynamic IP:** Assigned automatically by **DHCP**. (e.g., laptops on office WiFi).  

---

### ✂️ Subnetting & CIDR
- Networks can be split into **subnets** for efficiency and security.  
- **CIDR (Classless Inter-Domain Routing)** notation defines how many bits are used for network vs host.  
  - Example: `192.168.1.0/24` → 256 IPs (from `.0` to `.255`).  

**Real-world example:**  
- A Kubernetes cluster might use `10.244.0.0/16` CIDR for pod networking.  
- Each node/pod gets an IP from that range.  

---

### 🧪 Practical Commands
- **Check your IP:**  
  ```bash
  ip addr show   # Linux
  ipconfig       # Windows
  ```

- **Test connectivity (ping):**
```bash
ping 8.8.8.8
```

- **Trace packet path:**
```bash
traceroute google.com   # Linux
tracert google.com      # Windows
```
### 🧩 Key Takeaways

- IP address = unique logical identifier of a device.
- IPv4 is running out → IPv6 is the future.
- Public IP = Internet-facing, Private IP = internal use.
- Subnetting & CIDR are crucial for cloud and DevOps networking.

## 7. Ports & Sockets

An IP address identifies a **device** on a network, but a device can run many services at the same time (web server, SSH, database, etc.).  
To distinguish between them, we use **ports**.

---

### 🔢 What is a Port?
- A **port** is a 16-bit number (0–65535) that identifies a specific process or service running on a device.  
- **Well-known ports** (0–1023) are reserved for common services.  
- Examples:
  - **22** → SSH  
  - **53** → DNS  
  - **80** → HTTP  
  - **443** → HTTPS  
  - **3306** → MySQL  

---

### 🔌 What is a Socket?
- A **socket** = **IP Address + Port Number**.  
- This uniquely identifies a connection.  
- Example:  
  - Client (your laptop): `192.168.1.5:50512`  
  - Server (GitHub): `140.82.xx.xx:443`  
  - Together, they form a socket pair that enables communication.  

---

### 🌍 Real-World Examples
#### 1. SSH into a Server

```bash
ssh ubuntu@34.120.xx.xx -p 22
```

* Your laptop uses a random port (e.g., `50512`) to connect to the server’s port `22`.

#### 2. Web Browsing

* Browser connects to `github.com:443` (HTTPS).
* Multiple tabs can open different sockets to the same server IP.

#### 3. Databases in DevOps

* Application connects to `db.internal.company:3306` (MySQL).
* Only the DB server listens on that port; firewall rules restrict access.

#### 4. Kubernetes Services

* A pod running NGINX might listen on port `80`.
* A Kubernetes Service maps it to a NodePort (e.g., `30080`) or LoadBalancer port.

### 🔐 Ephemeral Ports

* When your system initiates a connection, it picks a random high-numbered port (usually `49152–65535`).
* This is called an **ephemeral port**.
* That’s why you can open multiple browser tabs to the same website — each uses a different ephemeral port.

### 🧩 Key Takeaways

- **IP** = device address
- **Port** = service address
- **Socket** = IP + Port uniquely identifies a connection
- Well-known ports are standardized for common protocols
- DevOps engineers must know ports when configuring firewalls, load balancers, and Kubernetes services

## 8. Networking Infrastructure

Networking infrastructure defines how devices are physically and logically connected. Depending on scale, we classify networks into different types.

---

### 🖥️ Local Area Network (LAN)
- Covers a **small geographic area** (office, home, campus).  
- High speed (up to 1–10 Gbps commonly).  
- Usually built with **Ethernet (wired)** or **WiFi (wireless)**.  
- Example:  
  - Your office floor where all employee laptops, IP phones, and printers are connected to a central switch.  
  - Internal systems like Jenkins, GitLab runners, or a local database cluster may be accessible only via LAN.  

---

### 🏙️ Metropolitan Area Network (MAN)
- Covers a **city or large campus**.  
- Connects multiple LANs together using fiber optics.  
- Example:  
  - A university with several departments connected via MAN.  
  - An ISP (Internet Service Provider) using MAN to connect data centers within a city.  

---

### 🌍 Wide Area Network (WAN)
- Covers a **large geographic area** (country or continent).  
- The **Internet itself is the largest WAN**.  
- Example:  
  - A company’s branch office in Bengaluru accessing databases hosted in AWS Mumbai region.  
  - VPN tunnels connecting corporate offices across the globe.  

---

### 📱 Personal Area Network (PAN)
- Very small network (a few meters).  
- Example:  
  - Developer using Bluetooth tethering to connect laptop ↔ mobile hotspot.  
  - Wireless keyboard/mouse connected to a workstation.  

---

### 🌐 Submarine Cables (Optical Fiber Backbone)
- The Internet heavily depends on **undersea optical fiber cables**.  
- These cables transmit data between continents at **Tbps speed**.  
- Example in IT:  
  - When you open `github.com` in India, your request might travel through submarine cables to GitHub’s data centers in the US or Europe.  
- Without submarine cables, cloud services, SaaS products, and global communication would be impossible.  

---

### 🧩 Key Takeaways
- **LAN** = office/home networks.  
- **MAN** = city-wide networks.  
- **WAN** = country/continent-wide, the Internet itself.  
- **PAN** = personal small-scale connections.  
- **Submarine cables** are the backbone of global connectivity.  
- DevOps engineers rely on this layered infrastructure to connect CI/CD systems, cloud environments, and global services.  

---

## 9. Networking Devices

Networking devices are the physical and virtual components that make communication possible in IT environments. These devices forward, filter, and secure traffic between systems.

---

### 🖧 Switch
- Operates at **Layer 2 (Data Link Layer)**.  
- Forwards traffic based on **MAC addresses**.  
- Connects multiple devices inside a **LAN**.  
- Example: An office floor where all laptops connect to a switch, which builds a MAC address table to forward frames efficiently.  

---

### 🌐 Router
- Operates at **Layer 3 (Network Layer)**.  
- Forwards packets between different networks using **IP addresses**.  
- Example: Your office LAN is connected to the Internet via a router. The router ensures traffic from `192.168.1.x` (private IP) can reach the public Internet.  

---

### 📡 Modem
- Converts **digital signals** (computer) ↔ **analog signals** (telephone/cable lines).  
- Example: Your ISP gives a modem that translates signals on coaxial/fiber lines into Ethernet that your router/switch can use.  

---

### 🔥 Firewall
- Monitors and controls **incoming/outgoing traffic** based on rules.  
- Can be hardware or software (e.g., iptables, AWS Security Groups).  
- Example: Blocking all traffic except ports 22 (SSH) and 443 (HTTPS) on a production server.  

---

### ⚖️ Load Balancer
- Distributes network traffic across multiple servers to ensure **high availability** and **scalability**.  
- Example:  
  - AWS Elastic Load Balancer distributing traffic across multiple EC2 instances running a web app.  
  - NGINX or HAProxy used in Kubernetes ingress to balance traffic between pods.  

---

### 📶 Access Point (AP)
- Extends a wired LAN into a **wireless network (WiFi)**.  
- Example: Office WiFi AP allows laptops and mobile devices to join the LAN without Ethernet cables.  

---

### 🧰 Other Devices
- **Hub** – A basic, outdated device that broadcasts packets to all connected devices (inefficient compared to a switch).  
- **Gateway** – A device that translates between two different network protocols.  
- **Proxy Server** – Acts as an intermediary between client and server for caching, filtering, or anonymity.  

---

### 🧩 Key Takeaways
- **Switch** = connects devices inside a LAN using MAC addresses.  
- **Router** = connects different networks using IP addresses.  
- **Modem** = converts analog ↔ digital signals for ISP connections.  
- **Firewall** = enforces security rules for network traffic.  
- **Load Balancer** = distributes requests across multiple servers.  
- **Access Point** = extends LAN to WiFi.  

---

## 10. Network Topologies

A **network topology** defines how devices (nodes) are arranged and interconnected in a network. The physical layout affects performance, fault tolerance, and scalability.

---

### 🔗 1. Bus Topology
- All devices share a single backbone cable.  
- Cheap but inefficient; if the backbone fails, the whole network goes down.  
- Rarely used in modern IT.  
- Example: Early Ethernet (10Base-2, coaxial cable) networks.  

---

### 🔗 2. Ring Topology
- Each device connects to exactly two neighbors, forming a closed loop.  
- Data passes through each node until it reaches its destination.  
- If one node fails, the entire ring can break (unless dual-ring).  
- Example: Some legacy telecom networks.  

---

### ⭐ 3. Star Topology
- All devices connect to a central device (usually a **switch**).  
- If one device fails, others remain unaffected.  
- Central node failure = entire network failure.  
- Example: Most **office LANs** today (devices connected to a switch).  
- Cloud/DevOps analogy: A **Load Balancer** acts like the central hub, distributing requests to backend servers.  

---

### 🌳 4. Tree (Hierarchical) Topology
- A combination of multiple star topologies arranged hierarchically.  
- Used in large organizations to structure departments.  
- Example:  
  - Core router → Distribution switches → Access switches → End devices.  
- Common in enterprise LANs.  

---

### 🕸️ 5. Mesh Topology
- Every device is connected to every other device.  
- Provides high redundancy and reliability.  
- Expensive due to many connections.  
- Example:  
  - In cloud-native setups, **Service Mesh (Istio, Linkerd)** works similarly by enabling all microservices to communicate reliably.  

---

### 📶 6. Hybrid Topology
- Combination of two or more topologies.   

---

### 🧩 Key Takeaways
- **Bus/Ring** = old, rarely used today.  
- **Star** = most common in modern LANs.  
- **Tree** = scalable, hierarchical enterprise setup.  
- **Mesh** = highly reliable, used in data centers and service meshes.  
- **Hybrid** = real-world networks often combine topologies.  

## 11. OSI Model (7 Layers) – Client to Server Flow

The **OSI model** defines seven layers of networking abstraction.  
We will explain **how a user entering a URL in a browser travels through the layers at the client side** and how it is processed **at the server side**.

---

### 🌐 Scenario: User types `https://example.com` in a browser

---

## Client Side: Layer 7 → Layer 1 (Top-Down)

1. **Layer 7 – Application Layer**
   - The browser takes the URL and prepares an **HTTP GET request**:  
     ```
     GET / HTTP/1.1
     Host: example.com
     ```
   - Adds application-specific metadata (cookies, headers).  
   - Data at this layer: **HTTP request (application data)**

2. **Layer 6 – Presentation Layer**
   - Converts the data into a **network-compatible format**.  
   - Handles encryption (TLS/SSL), compression, and encoding.  
   - Example: HTTP request is encrypted into **HTTPS (TLS record)**.  
   - Data at this layer: **Encrypted HTTP payload**

3. **Layer 5 – Session Layer**
   - Manages the session between client and server.  
   - Establishes/maintains/terminates sessions.  
   - Example: Session is maintained so user is not required to login again and again.
   - Like Gmail we logged in long back but still we can directly access our inbox without password every now and then

4. **Layer 4 – Transport Layer**
   - TCP splits the data into **segments**.  
   - Adds **source and destination port numbers** (e.g., client ephemeral port 50512 → server port 443).  
   - Ensures reliability: sequence numbers, checksums, acknowledgments.  
   - Data at this layer: **TCP segments containing encrypted HTTP payload**

5. **Layer 3 – Network Layer**
   - Encapsulates TCP segments into **IP packets**.  
   - Adds **source and destination IP addresses**.  
   - Routing decisions are made here (how packet moves from client → server across networks).  
   - Data at this layer: **IP packets with TCP segments inside**

6. **Layer 2 – Data Link Layer**
   - Encapsulates IP packets into **frames**.  
   - Adds **MAC addresses** for local delivery (client NIC → switch → router).  
   - Error detection via CRC.  
   - Data at this layer: **Ethernet/WiFi frame**

7. **Layer 1 – Physical Layer**
   - Converts frames into **electrical signals, light pulses, or radio waves**.  
   - Data is transmitted over **cables, fiber, or wireless medium**.  
   - Data at this layer: **bits traveling through the medium**

---

## Server Side: Layer 1 → Layer 7 (Bottom-Up)

1. **Layer 1 – Physical Layer**
   - Server’s NIC receives **bits** from the physical medium.  
   - Signals are converted back to frames.  

2. **Layer 2 – Data Link Layer**
   - Checks MAC addresses, error detection, and extracts **Ethernet frame** payload.  
   - Passes IP packet to Layer 3.

3. **Layer 3 – Network Layer**
   - Reads **destination IP**, verifies it belongs to server.  
   - Extracts TCP segment from IP packet.  

4. **Layer 4 – Transport Layer**
   - Uses **destination port** to deliver segment to the correct application.  
   - Reassembles multiple TCP segments into complete **encrypted HTTP message**.  

5. **Layer 5 – Session Layer**
   - Associates incoming data with the correct **TLS session**.  

6. **Layer 6 – Presentation Layer**
   - Decrypts TLS payload.  
   - Converts network bytes into **application-readable data (HTTP request)**.  

7. **Layer 7 – Application Layer**
   - Web server processes HTTP request.  
   - Fetches homepage, generates HTTP response.  
   - Response now travels **top-down Layer 7 → Layer 1** back to client.  

---

### 🔄 Summary of Data Transformation

| Layer | Client Side Data Transformation | Server Side Data Transformation |
|-------|-------------------------------|-------------------------------|
| 7 App | HTTP GET Request | HTTP GET Request received |
| 6 Presentation | TLS Encrypted | TLS Decrypted |
| 5 Session | Session data | Session association |
| 4 Transport | TCP segments with ports | TCP segments reassembled |
| 3 Network | IP packets with source/dest IP | IP packets extracted |
| 2 Data Link | Ethernet/WiFi frames | Frames decoded |
| 1 Physical | Bits over medium | Bits received from medium |

---

### 🧩 Key Takeaways
- **Client**: Data flows **top-down (7 → 1)**, converted from user input → packets → bits.  
- **Server**: Data flows **bottom-up (1 → 7)**, converted from bits → frames → packets → application data.  
- OSI model layers map real-world processes like **HTTP request, TCP segmentation, IP routing, Ethernet switching, and physical transmission**.  

## 12. TCP/IP Model

The **TCP/IP model** is a simplified networking model used in real-world Internet communication. It has **4 layers** (sometimes described as 5) that correspond to OSI layers.

---

### TCP/IP Layers and Their OSI Mapping

| TCP/IP Layer          | OSI Layer(s)        | Function | Real-World Example |
|----------------------|-------------------|---------|------------------|
| Application          | OSI 7,6,5          | Provides network services to applications. | HTTP request from a browser, SSH connection, DNS query |
| Transport            | OSI 4              | Reliable/unreliable transport; manages ports and sessions. | TCP segment for `git clone https://github.com` or UDP for video streaming |
| Internet / Network   | OSI 3              | Logical addressing, routing packets across networks. | IP packet carrying HTTP request from client IP to server IP |
| Network Access / Link| OSI 2,1            | Physical and data link transmission over the medium. | Ethernet/WiFi frame sent over cables, fiber, or radio waves |

---

### 🌍 How a TCP/IP Request Works: Browser Example

1. **Application Layer**  
   - Browser generates an **HTTP GET request** to `https://example.com`.  
   - Data includes headers, cookies, and encrypted TLS payload.  

2. **Transport Layer**  
   - TCP adds **source/destination ports**, sequence numbers, and checksums.  
   - Data is now a **TCP segment**.  

3. **Internet Layer**  
   - TCP segment is encapsulated into an **IP packet** with source/destination IP addresses.  
   - Routers use IP to forward the packet across networks.  

4. **Network Access / Link Layer**  
   - IP packet is encapsulated into an **Ethernet/WiFi frame** with MAC addresses.  
   - Physical layer converts frames into **bits** for transmission.  

---

### ✅ Key Takeaways
- TCP/IP is the **practical model used in real-world networking**.  
- Maps closely to OSI model but is simpler and widely adopted.  
- TCP/IP layers show **how data moves from application → transport → network → link → physical medium**.  
---

## 13. IP Packets, Segments, Frames, and Checksum

Understanding how data is structured and validated in transit is crucial for reliable networking. This section explains **how data is encapsulated and checked for errors**.

---

### 📦 1. TCP Segment
- **Transport layer (Layer 4)** divides application data into **segments**.  
- Each segment contains:
  - Source & destination ports
  - Sequence number
  - Acknowledgment number
  - Flags (SYN, ACK, FIN)
  - Payload (application data)
  - **Checksum** for error detection at transport layer  
- Example: Browser sends an HTTP GET request as a TCP segment to port 443 on a web server.

---

### 🌐 2. IP Packet
- **Network layer (Layer 3)** encapsulates TCP segments into **IP packets**.  
- Each packet contains:
  - Source & destination IP addresses
  - TTL (Time to Live)
  - Protocol (TCP/UDP)
  - Header checksum (for header integrity)
  - Encapsulated TCP segment as payload
- Example: TCP segment from client port 50512 → server port 443 is wrapped inside an IP packet destined for the server’s public IP.

---

### 🖧 3. Ethernet / WiFi Frame
- **Data Link layer (Layer 2)** encapsulates IP packets into **frames**.  
- Each frame contains:
  - Source & destination MAC addresses
  - EtherType (protocol type)
  - Payload (IP packet)
  - Frame Check Sequence (FCS) / CRC for error detection
- Example: NIC sends Ethernet frame over switch port or WiFi access point.

---

### ⚡ 4. Physical Layer – Bits
- **Layer 1** converts frames into **electrical signals, light pulses, or radio waves**.  
- The data is transmitted as a **stream of bits** over the physical medium.

---

### ✅ Checksum – Ensuring Data Integrity
- Both **Transport (TCP)** and **Network (IP)** layers include **checksum fields**.  
- Purpose: Detect errors during transmission.  
- Mechanism:
  1. Sender calculates a checksum from header/data.  
  2. Receiver recalculates checksum and compares.  
  3. Mismatch → packet is discarded or retransmitted (TCP).  
- Example: TCP segment with corrupted data triggers **retransmission**.

---

### 🧩 Summary of Encapsulation
| Layer | Encapsulation Unit | Error Detection |
|-------|-----------------|----------------|
| Transport | TCP Segment | Checksum |
| Network | IP Packet | Header Checksum |
| Data Link | Ethernet/WiFi Frame | FCS / CRC |
| Physical | Bits | Not applicable |

---

### 🌍 Real-World IT Example
- When you `curl https://github.com`:
  1. HTTP request → TCP segment → IP packet → Ethernet frame → bits sent over cable/fiber/WiFi.  
  2. Switches forward frames based on MAC, routers forward packets based on IP.  
  3. Server NIC receives bits → frame → packet → segment → HTTP request.  
  4. Checksums at TCP/IP layers ensure **data was not corrupted** during transit.

---

## 14. TCP and UDP – Transport Layer Protocols

The **Transport Layer** ensures end-to-end communication between applications on different devices. TCP and UDP are the most widely used transport protocols.

---

### 🟢 TCP (Transmission Control Protocol)

#### 1. 3-Way Handshake (Connection Establishment)
TCP is **connection-oriented**, meaning a reliable connection must be established before data transfer.

**Steps:**
1. **SYN**: Client sends a synchronize (SYN) packet to the server to initiate connection.  
2. **SYN-ACK**: Server acknowledges (ACK) and sends its own SYN to the client.  
3. **ACK**: Client acknowledges the server’s SYN.  
- Connection established; data transfer begins.

**Example:**  
- `ssh ubuntu@server` → TCP handshake on port 22 ensures reliable connection before login.

---

#### 2. Data Transfer & Flow Control
- TCP breaks data into **segments** and assigns **sequence numbers**.  
- Receiver sends **ACKs** to confirm successful receipt.  
- **Flow control** ensures sender does not overwhelm the receiver.  
- **Retransmission** occurs if ACK is not received within a timeout.

**Example:**  
- `git clone https://github.com` → large data transferred reliably with sequencing and acknowledgments.

---

#### 3. Connection Termination
- TCP uses a **4-step FIN-ACK process** to gracefully close a connection.  

---

### 🔵 UDP (User Datagram Protocol)
- **Connectionless**: No handshake, no acknowledgment.  
- Lightweight and faster than TCP.  
- Data is sent as **datagrams**, which may arrive out of order or get lost.  
- Use cases:
  - DNS queries (`port 53`)  
  - Video/voice streaming (VoIP)  
  - Online gaming  

**Example:**  
- Streaming a live webinar uses UDP to minimize latency; occasional packet loss is acceptable.

---

### ⚡ Comparison: TCP vs UDP

| Feature | TCP | UDP |
|---------|-----|-----|
| Connection | Connection-oriented | Connectionless |
| Reliability | Reliable (ACKs, retransmission) | Unreliable |
| Speed | Slower | Faster |
| Use Case | Web, SSH, Git, Email | Video streaming, DNS, VoIP |
| Flow Control | Yes | No |
| Error Checking | Checksum, ACK | Checksum only |

---

### 🌍 Real-World Example
1. **Web browsing (HTTPS)**: TCP ensures that all HTML, CSS, JS files arrive in order and intact.  
2. **Live video call**: UDP is used because real-time delivery is more important than perfect reliability. 

---

### 🧩 Key Takeaways
- **TCP** = reliable, ordered, connection-oriented (critical for DevOps tools, Git, SSH, HTTP).  
- **UDP** = fast, connectionless, suitable for real-time apps.  
- **3-way handshake, flow control, and retransmission** make TCP robust for IT workloads.  


---

## 15. DNS (Domain Name System) and How Email Works

DNS and email are fundamental services on the Internet. DNS translates human-readable domain names into IP addresses, while email systems handle sending, routing, and receiving messages.

---

### 🌐 DNS (Domain Name System)

1. **Purpose:** Convert domain names (e.g., `example.com`) into IP addresses (`93.184.216.34`) that computers use to route packets.

2. **How DNS Works (Simplified Flow)**
   - User types `https://example.com` in browser.
   - Browser checks **local DNS cache**.
   - If not found, query goes to **recursive DNS server** (usually provided by ISP or corporate network).
   - Recursive server queries **root DNS server** → **TLD server** (`.com`) → **authoritative DNS server** for `example.com`.
   - Authoritative server returns **IP address** to recursive server, which forwards it to the client.
   - Browser now knows which server to contact via TCP/IP.

**Real-World DNS Example:**  
- AWS Route53, Cloudflare DNS, or Google DNS provide scalable DNS resolution for global traffic.

---

### 📧 How Email Works

Email delivery uses **SMTP (Simple Mail Transfer Protocol)**, **IMAP**, and **POP3** protocols.

1. **Sending an Email (Client → Server)**
   - User composes email in Gmail or Outlook.
   - Email client connects to **SMTP server** (port 25, 587).
   - SMTP server validates sender and forwards email to recipient’s mail server.

2. **Routing via MX Records**
   - Sender’s server looks up recipient domain’s **MX record** via DNS.
   - Routes email to recipient’s SMTP server.

3. **Receiving Email (Server → Client)**
   - Recipient fetches email using **IMAP (port 143/993)** or **POP3 (port 110/995)**.
   - IMAP keeps messages on server for multi-device access.
   - POP3 downloads emails and optionally deletes from server.
---

### 🧩 Key Takeaways
- **DNS** is the Internet’s phonebook, translating domains into IPs.
- **Email** relies on SMTP, IMAP, POP3, and DNS MX records for reliable delivery.

## 16. Sessions and Cookies

Sessions and cookies are mechanisms used to **maintain state and user identity** across multiple requests in web applications. They are essential for authentication, personalization, and secure communication.

---

### 🔹 Cookies

1. **Definition:** Small pieces of data stored on the **client-side (browser)**.  
2. **Purpose:**  
   - Maintain user preferences  
   - Track user activity  
   - Store session identifiers  
3. **Types of Cookies:**  
   - **Session Cookies:** Temporary, deleted when browser closes  
   - **Persistent Cookies:** Stored for a defined period  
   - **Secure Cookies:** Only sent over HTTPS  
   - **HttpOnly Cookies:** Cannot be accessed via JavaScript (prevent XSS attacks)  

**Example:**  
- After logging into GitHub, a cookie stores your session token.  
- Browser sends this cookie with each HTTP request to authenticate you automatically.

---

### 🔹 Sessions

1. **Definition:** Server-side storage of **user state**.  
2. **How it works:**  
   - Server creates a **unique session ID** when a user logs in.  
   - Session ID is sent to the client as a **cookie**.  
   - Client sends session cookie with each request; server uses it to fetch stored session data.  

**Example Flow:**  
1. User logs into Gmail → server generates session ID `xyz123`.  
2. Browser stores cookie: `Set-Cookie: session_id=xyz123`.  
3. Subsequent requests include this cookie → server retrieves session info → user stays logged in.  

---

### 🔹 Client-Server Interaction with Cookies

| Step | Action |
|------|--------|
| 1 | Client sends login request |
| 2 | Server authenticates and creates session |
| 3 | Server responds with **Set-Cookie** header |
| 4 | Browser stores cookie and sends it in future requests |
| 5 | Server reads cookie → fetches session data → maintains state |

---

### 🧩 Key Takeaways

- **Cookies:** Client-side storage; lightweight; used to store session IDs and preferences.  
- **Sessions:** Server-side storage; more secure; used to maintain user state across requests.  

