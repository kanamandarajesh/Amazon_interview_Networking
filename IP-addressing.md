**IP addressing** is the system used to assign a unique address to each device connected to a network. It's like a postal address for devices on the internet or a local network. There are two main types of IP addresses: **IPv4** and **IPv6**.

### 1. **IPv4 (Internet Protocol version 4)**
IPv4 is the most commonly used address format. It uses **32 bits** and is written as four sets of numbers (called octets), each ranging from 0 to 255, separated by dots. For example:

```
192.168.1.1
```

- **Total possible IPv4 addresses**: 4.3 billion (2^32), but due to the growth of the internet, we are running out of IPv4 addresses.

#### **Structure of IPv4 Address:**
   - **Network portion**: Identifies the network where the device is located.
   - **Host portion**: Identifies the device within that network.

   Example:
   - **192.168.1.1** could represent a device (like your computer) on the **192.168.1** network.

### 2. **IPv6 (Internet Protocol version 6)**
IPv6 was introduced to solve the problem of running out of IPv4 addresses. It uses **128 bits** and can support a much larger number of devices. IPv6 addresses are written as eight groups of four hexadecimal digits, separated by colons:

```
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```

- **IPv6 addresses** are much longer than IPv4, and there are a huge number of possible addresses (around 340 undecillion addresses—enough to give every atom on Earth its own address).

### **Types of IP Addresses:**

1. **Public IP Address**:
   - These are unique and assigned to your network by an **ISP (Internet Service Provider)**.
   - Every device on the internet needs a public IP address to communicate with other devices across the world.
   - Example: **8.8.8.8** (Google’s public DNS server).

2. **Private IP Address**:
   - Used within private networks (like home or office networks) and are not routable over the internet.
   - These addresses are reserved for use in local networks.
   - **IPv4 private address ranges**:
     - **10.0.0.0 - 10.255.255.255**
     - **172.16.0.0 - 172.31.255.255**
     - **192.168.0.0 - 192.168.255.255**
   - Example: **192.168.1.1** (common for home routers).

3. **Loopback Address**:
   - Used to test the network interface on your own machine (usually **127.0.0.1** for IPv4).
   - Example: **127.0.0.1** is the **loopback address** for IPv4, which is used to refer to the local machine itself.

### **Subnetting** (Breaking IP into Subnets):
- Subnetting divides a network into smaller segments called **subnets**. It helps improve network performance and security.
- A **subnet mask** (like **255.255.255.0**) tells the network which part of the IP address is the network portion and which part is the host portion.
   - Example: In the IP address **192.168.1.1/24**:
     - **192.168.1** is the network portion.
     - **1** is the host portion.
     - The **/24** means the first 24 bits (of the 32-bit address) are used for the network, leaving 8 bits for the host.

### **DHCP (Dynamic Host Configuration Protocol)**:
   - **DHCP** is a protocol used to automatically assign IP addresses to devices on a network.
   - When you connect a device to a network, **DHCP** assigns it an available IP address, so you don’t have to manually configure it.

### **CIDR Notation (Classless Inter-Domain Routing)**:
   - CIDR notation is a shorthand for describing IP addresses and subnets.
   - Example: **192.168.1.0/24**
     - **192.168.1.0** is the network address.
     - **/24** indicates that the first 24 bits are for the network (this corresponds to the subnet mask **255.255.255.0**).

### **Classes of IPv4 Addresses**:
   - **Class A**: 1.0.0.0 to 127.255.255.255 (large networks).
   - **Class B**: 128.0.0.0 to 191.255.255.255 (medium networks).
   - **Class C**: 192.0.0.0 to 223.255.255.255 (small networks).
   - **Class D**: 224.0.0.0 to 239.255.255.255 (used for multicast).
   - **Class E**: 240.0.0.0 to 255.255.255.255 (reserved for future use).

### **How IP Addressing Works**:
- When a device (e.g., your computer) wants to communicate over the internet, it needs to know the **destination IP address**. This can be achieved via **DNS (Domain Name System)**, which converts human-readable addresses (like `google.com`) into IP addresses.
- Routers use the destination IP address to forward packets of data between devices and networks.
- Devices can either use **private IPs** for internal network communication (e.g., home Wi-Fi) or **public IPs** for communicating over the broader internet.

---

### **Summary**:
- **IPv4** addresses are 32-bit and look like `192.168.1.1`.
- **IPv6** addresses are 128-bit and look like `2001:0db8:85a3::8a2e:0370:7334`.
- **Private IPs** are used in local networks (e.g., **192.168.x.x**).
- **Public IPs** are used for internet communication.
- **Subnetting** helps divide networks into smaller parts.
- **DHCP** assigns IP addresses automatically to devices.

IP addressing is essential for devices to communicate on a network or the internet by uniquely identifying each device.
