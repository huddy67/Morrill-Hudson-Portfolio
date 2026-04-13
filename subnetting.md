## Design and Planning

### Subnet and IP Challenges

(image)

The first number in the IP address has to match. For example, 192.50.40.111 and 192.35.36.120 would follow this idea.

(image)

In this case, the first two numbers must match. For example, 192.50.40.111 and 192.50.36.120.

(image)

Here, the first three numbers need to be the same, and the last number can be anything from 0 to 255. For example, 192.50.40.111 and 192.50.40.120.

(image)

Subnet masks always start with a continuous string of 1s in binary.

(image)

In binary form, subnet masks have all their 1s grouped at the beginning with no breaks. For example: 255.255.192.0.

---

## Technical Development

### Assignment 1

#### Part 1: Build the Network
(image)

#### Part 2: Investigate Communication
- ping 192.168.1.25 (succeeded)

(image)

- ping 192.168.2.10 (failed)

(image)

A ping only works when both devices are on the same network. If they are on different networks and there is no router connecting them, the ping will fail.

#### Part 3: Modify and Test Again
- ping 192.168.2.10 (failed)

(image)

At first, nothing changed because the devices were still on different networks. Since the subnet mask wasn’t adjusted and no router was added, communication still failed.

---

### Scenario A
Change all subnet masks to **255.0.0.0** and test again.

- ping 192.168.2.10 (succeeded)

(image)

---

### Scenario B
Set:
- PC0 → 172.16.1.10 / 255.255.0.0  
- PC1 → 172.16.2.20 / 255.255.0.0  

- ping 192.168.2.10 (failed)

(image)

These devices are not on the same network.

---

### Scenario C

Two PCs that look similar but are **not** on the same network:

(image)

Two PCs that look different but **are** on the same network:

(image)

---

### Assignment 2

#### Scenario C: Small Business Workspace

##### Part 1: Device Exploration
(image)

The network includes several PCs, a switch, and a wireless device. Everything is clearly labeled and laid out in a way that makes the connections easy to follow and understand.

---

##### Part 2: Design Decisions & Part 3: Final Network Layout
(image)

The final design focuses on being clean and efficient. All devices are labeled and connected through switches to keep communication organized. Wired connections are used for devices that need consistent speed and reliability, like desktop computers, while wireless connections allow for flexibility when needed.

---

## Testing and Evaluation

### Assignment 3

#### Part 1: Add the Router & Part 2: Configure Router Interfaces
Fully configured setup with a working router

(image)

(image)

---

#### Part 3: Configure Default Gateway on PCs
Default gateways and IP addresses set on a PC in each LAN

(image)

(image)

---

#### Part 4: Test Communication
Communication from LAN 1 to LAN 2

(image)

The router connects separate networks (LANs) and allows devices on different networks to communicate with each other.

---

### Assignment 4

#### Part 1: Troubleshooting Investigation

1. **Ping (Command Prompt)**  
   - ping 192.168.2.10 (failed)  
   (image)

2. **IP Configuration**  
   PC2 IP Configuration  
   (image)

3. **Visual Inspection**  
   Physical layout  
   (image)

4. **Router CLI**  
   Router IOS command line interface  
   (image)

---

#### Step 2: Identify the Problem
The second terminal had not been configured yet.

(image)

---

#### Step 3: Apply a Fix
Working layout

(image)

---

#### Step 4: Test Again
- ping 192.168.2.10 (working)

(image)

---

## Reflection and Analysis

### Assignment 1 Reflection
A device figures out if another device is on the same network by comparing its IP address and subnet mask. The subnet mask shows which part of the IP address represents the network. If those parts match, the devices are on the same network.

For example, 192.168.1.10 and 192.168.2.10 may look similar, but with a subnet mask of 255.255.255.0, they are actually on different networks. On the other hand, 172.16.1.10 and 172.16.2.20 may look different, but with a subnet mask of 255.255.0.0, they are on the same network.

---

### Assignment 2 Reflection
In my network design, I used a router, switch, server, multiple PCs, and a laptop to create a realistic small business setup. The router connects the network to outside systems, while the switch allows all internal devices to communicate efficiently.

I included a server to represent centralized storage and services, which supports a client-server model instead of peer-to-peer. This makes the network more organized and scalable for a business.

Most devices are wired to ensure stable and fast connections, especially the PCs and server. The laptop represents a more flexible device that could connect wirelessly. Overall, the layout is clean and easy to manage, which would help reduce issues and allow for future expansion.

---

### Assignment 3 Reflection
The router made it possible for devices on different LANs to communicate by acting as a bridge between networks. Each interface on the router connects to a different network and has its own IP address, which helps route traffic correctly.

The default gateway is the router’s IP address that devices use when sending data to other networks. At first, the ping between networks failed, but after configuring the router and setting the default gateways correctly, the ping worked. This confirmed that the router was successfully forwarding data between networks.

---

### Assignment 4 Reflection
One issue I ran into was that a device couldn’t communicate with another network because it wasn’t set up correctly. I found this by using the ping command, which failed, and then checking the IP configuration.

I also used the router’s command line interface to help diagnose the issue. The fix was to properly configure the device with the correct IP address and settings. After making the change, I tested again with ping, and it worked. This confirmed that everything was functioning as it should.

---

