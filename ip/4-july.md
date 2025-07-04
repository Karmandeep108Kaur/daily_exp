Here's your content fully converted to **Markdown format**:

---

# 📡 Basic Networking Commands & Concepts

---

## 1. `ping` – Check Connectivity

**Purpose**: Tests if another device/server is reachable.

```bash
ping www.google.com
```

**Use**: Sends packets and waits for replies – if it replies, it's "alive".

### ➤ Shortcut

Check your own system:

```bash
ping 127.0.0.1
```

---

## 🖥️ 2. localhost & Loopback

* **Localhost** refers to your own computer.

**Loopback address:**

* **IP**: `127.0.0.1`
* **Domain**: `localhost`

### 🔁 Uses:

* Testing local apps/services
* No need for internet
* Run your project (e.g., on XAMPP/Flask)

---

## 🛰️ 3. `tracert` (Windows) – Trace Route

**Command:**

```bash
tracert gendec.com
```

**Use**: Tracks each step (router) your data takes to reach a destination.

### 🔹 Important Notes:

* `*` → Means the router didn't respond
* Helps identify where data is blocked
* Combine with `ping` to troubleshoot

---

## 🧮 4. `ipconfig` (Windows)

**Use**: Shows current network configuration.

**Command:**

```cmd
ipconfig
```

### 🔍 Output Includes:

* **IPv4 Address** – e.g., `192.168.1.5`
* **Subnet Mask** – e.g., `255.255.255.0`
* **Default Gateway** – Router’s IP
* **Ethernet/Wi-Fi status**
* **Loopback interface** (`lo0` on Linux)

---

## 🔌 5. Ethernet / Wi-Fi / LAN / WAN / DHCP

### 🔷 Ethernet

* Wired connection using a cable
* More secure, faster, and stable

**How it works**:

* One end in PC, other in router
* Internet via physical cable
* Check using `ipconfig`

### 🔷 Wi-Fi

* Wireless via radio signals
* Easier to connect
* Less secure/stable
* May suffer from interference

### ⚖️ Ethernet vs Wi-Fi

| Feature    | Ethernet    | Wi-Fi           |
| ---------- | ----------- | --------------- |
| Connection | Wired       | Wireless        |
| Speed      | Faster      | Slower (varies) |
| Security   | More secure | Less secure     |
| Stability  | Very stable | Can disconnect  |
| Setup      | Needs cable | Easier setup    |

---

## 🌐 LAN vs WAN

| Term | Full Form          | Description                                      |
| ---- | ------------------ | ------------------------------------------------ |
| LAN  | Local Area Network | Small network in a room/building                 |
| WAN  | Wide Area Network  | Network across cities/countries (e.g., Internet) |

---

## 🎯 6. Use Your Own IP Address

You can host or test your app using your **local IP**:

```bash
ping <your_IP_address>
```

**Check your IP using:**

```bash
ipconfig     # Windows
ifconfig     # Linux/macOS
```

---

## 🧠 7. DHCP – Dynamic Host Configuration Protocol

* Automatically assigns IP address to each device
* No manual IP configuration needed
* Used in almost all routers
* Devices get IP like `192.168.1.x` from the router

---
