# 🌐 Networking Basics

## 🖥️ Host
A **host** is any device (computer, smartphone, etc.) that **sends or receives network traffic**.

## 🚦 Traffic
Network **traffic** is the flow of data over the internet. Congestion (like **traffic jams**) can lead to issues such as:
- **504 Gateway Timeout** – server didn’t get a timely response from another server.

## 📡 Internet of Things (IoT)
Devices connected to the internet, not traditionally computers:
- Examples: **Smart TVs**, **speakers**, **thermostats**, **refrigerators**, **smartwatches**

## 🧑‍💻 Client & Server Model

| Role     | Description                           |
|----------|---------------------------------------|
| Client   | Initiates requests (e.g., a web browser) |
| Server   | Responds to requests with data or services |

## 🌍 IP Address (Internet Protocol Address)

A unique **identifier** for a device on a network.

### ➤ Properties
- **Unique & Universal**
- Can **change dynamically**
- **Public IP**: Used over internet (assigned by ISP)
- **Private IP**: Used within a local network (home/school)

### ➤ Versions

#### ✅ IPv4
- 32 bits
- Written in 4 octets (e.g., `192.168.1.1`)
- ~4.3 billion addresses (`2^32`)
- Exhausted due to internet growth

#### ✅ IPv6
- 128 bits
- Written in 8 groups of hexadecimal (e.g., `2001:0db8::7334`)
- ~2^128 addresses (virtually unlimited)
- Supports newer internet demands

### ➤ Notations
- **Binary**: 11000000.10101000.00000001.00000001
- **Decimal**: 192.168.1.1

## 🔌 Network
A **network** connects multiple hosts and enables **data transport**.

- Logical grouping of hosts
- Can be divided into **subnets**
- Multiple networks can be connected (e.g., Internet)

## 🏷️ MAC Address (Media Access Control)
- A **unique physical identifier** assigned to network interfaces
- Fixed and burned into the device

## 🌐 DNS (Domain Name System)
Converts **domain names** (like `www.google.com`) into **IP addresses**.

## 🛣️ Default Gateway
A **router** that connects a local network to the internet or another network.

## 🧠 Classful Addressing

Divides the IPv4 address space into **5 classes** based on the **first octet**.

| Class | 1st Octet Range | Network ID Bits | Host ID Bits | Subnet Mask       | Usage              |
|-------|------------------|------------------|---------------|-------------------|---------------------|
| A     | 1 - 126           | 8                | 24            | 255.0.0.0         | Very large networks |
| B     | 128 - 191         | 16               | 16            | 255.255.0.0       | Medium networks     |
| C     | 192 - 223         | 24               | 8             | 255.255.255.0     | Small networks      |
| D     | 224 - 239         | -                | -             | -                 | Multicasting        |
| E     | 240 - 255         | -                | -             | -                 | Reserved            |

### Reserved Addresses
- **0.0.0.0** – Used for broadcasting
- **127.0.0.1** – Loopback (used to test software on same machine)

## 🔁 Addressing Types

| Type       | Description                                |
|------------|--------------------------------------------|
| Unicast    | One-to-one communication                   |
| Broadcast  | One-to-all communication within subnet     |
| Multicast  | One-to-many (specific group of hosts)      |

## 🧩 Subnetting

**Dividing a network** into smaller **sub-networks** for better management and bandwidth utilization.

### Subnet Mask
Defines which portion of an IP is **network** and which is **host**.

| Example       | Subnet Mask       | CIDR Notation |
|---------------|-------------------|----------------|
| Class A       | 255.0.0.0         | /8             |
| Class B       | 255.255.0.0       | /16            |
| Class C       | 255.255.255.0     | /24            |

### CIDR (Classless Inter-Domain Routing)
- Replaces rigid class-based system
- Example: `192.168.1.0/24` means 24 bits are for the network

## 🌐 Broadcast Address
- The **last IP address** in a subnet range (used to communicate with all hosts in subnet)
- IP range: `0.0.0.0` to `255.255.255.255`

## 📏 Bandwidth & Latency

| Term       | Definition                                 |
|------------|--------------------------------------------|
| Bandwidth  | Data transfer capacity (e.g., Mbps, Gbps)  |
| Latency    | Time delay during data transmission        |

## 🗂️ Domain
The **name** used in a browser (e.g., `.com`, `.org`) that maps to an IP via DNS.

### 📊 IP Class Identification

| Class | 1st Octet Range | 1st Bits   |
|-------|------------------|------------|
| A     | 0 - 127          | 0xxxxxxx   |
| B     | 128 - 191        | 10xxxxxx   |
| C     | 192 - 223        | 110xxxxx   |
| D     | 224 - 239        | 1110xxxx   |
| E     | 240 - 255        | 1111xxxx   |

# 🔍 Question
Find the **subnet mask**, number of **networks**, number of **hosts**, number of **subnets**, and **broadcast IP**  
Given IP: `205.150.65.0/25`  
**Create 10 subnets**

---

## ❌ Problem

- `/25` gives only **2 subnets**
- But we need **10 subnets**
- So we need to **subnet further**

---

## ✅ Solution

- Use **/28** instead of `/25`
- `/28` means:
  - **Subnet Mask**: `255.255.255.240`
  - **Total Subnets**: `16`
  - **Usable Hosts per Subnet**: `14`
  - ✅ Enough for 10 subnets

---

## 📋 First 2 Subnets (out of 10)

| Subnet | Network Address     | First IP         | Last IP          | Broadcast IP       |
|--------|---------------------|------------------|------------------|--------------------|
| 1      | `205.150.65.0/28`   | `205.150.65.1`   | `205.150.65.14`  | `205.150.65.15`    |
| 2      | `205.150.65.16/28`  | `205.150.65.17`  | `205.150.65.30`  | `205.150.65.31`    |

> 📌 Each subnet increases by **16**

---

## 📝 Final Answer Summary

| Item                     | Value                  |
|--------------------------|------------------------|
| **New Subnet Mask**      | `255.255.255.240`      |
| **CIDR**                 | `/28`                  |
| **Total Subnets**        | `16`                   |
| **Usable Hosts/Subnet**  | `14`                   |
| **Broadcast IP (1st)**   | `205.150.65.15`        |

---

