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
