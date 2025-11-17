

# Planning and Design

## 1. Project Overview

### Purpose
This project focuses on learning how networks connect, communicate, and function. The work includes exploring lower OSI layers, making Ethernet cables, comparing network modes, drawing topology layouts, and creating a small SOHO network setup.

### Objectives
- Use Ubuntu tools to explore OSI Layer 1 and Layer 2
- Create Ethernet cables and confirm successful connectivity
- Compare shared networking mode and bridged networking mode
- Draw and label multiple network topology layouts
- Build a functional SOHO network using correct addressing and basic security settings

### Requirements for Completion
| Task | Evidence Needed |
|------|-----------------|
| OSI Layer 1 and 2 exploration | Screenshots with notes |
| Ethernet cable construction | Video showing successful test |
| Shared vs bridged mode comparison | Completed IP comparison table |
| Network topologies | Labeled diagram images |
| SOHO network simulation | Successful connection tests |

---

## 2. OSI Layer Background

The OSI model separates networking into seven different layers. For this project, the focus is on Layer 1 and Layer 2, since they deal with physical transmission and device-to-device communication inside the same network.

### Layer 1: Physical Layer
Layer 1 focuses on the physical medium used to carry data. Examples include:

- Ethernet, coaxial, and fiber optic cables
- Wall jacks, ports, and connectors
- Wireless transmission (Wi-Fi, Bluetooth)
- Network interface cards (physical or virtual)

Data exists as bits (0s and 1s) here, and the job of this layer is to transmit signals without handling accuracy or addressing.

### Layer 2: Data Link Layer
Layer 2 is responsible for reliable data transfer across a local network. Data is organized into frames that contain:

- The actual data being sent
- Source MAC address
- Destination MAC address
- Error checking information

This layer ensures that information reaches the correct device and detects possible corruption.

### Relationship Between Layer 1 and Layer 2
Layer 1 provides the path and signal used to move data.  
Layer 2 controls how that path is used by organizing frames, handling addressing, and confirming delivery.  
Layer 1 transports the data, while Layer 2 manages how devices share and verify it.

---

## 3. Network Topology Planning

A network topology shows how devices are arranged and connected. The design affects performance, expansion, cost, and overall reliability.

### Common Topologies
| Topology | Description | Typical Use |
|----------|-------------|-------------|
| Star | All devices connect to a central switch or hub | Home networks and small offices |
| Bus | Devices share a single line connection | Older Ethernet networks |
| Ring | Devices connect in a loop and data travels around the circle | Specialized and legacy systems |
| Mesh | Multiple paths between devices for redundancy | Data centers and wireless mesh |
| Hybrid | Mixture of two or more topology styles | Large organizations or multi-building networks |

---

## 4. SOHO Network Overview

A SOHO (Small Office or Home Office) network supports internet access, device communication, and shared resources for smaller environments.

### Core Components
| Device | Purpose |
|--------|---------|
| Modem | Connects the internal network to an ISP |
| Router | Assigns IP addresses and forwards traffic |
| Switch | Provides additional wired network ports |
| Access Point | Offers wireless connectivity |
| End Devices | Computers, TVs, printers, phones, etc. |

---


## OSI Layer 

screenshots

![](iplinkshow.png)
![](arpn.png)
![](ipslink.png)
![](tcpdump.png)

## SOHO Network Activity

screenshots
![](IPComputerA.png)
![](compbip.png)
![](pingb.png)
![](ufw.png)
![](traceroute.png)
![](results.png)
![](arp.png)
![](pingb.png)
![](netstat.png)

## Exploring ip in shared and bridged mode

![](ipa.png)
![](whatismyip.png)
![](ipa2.png)
![](whatismyip2.png)

## Wires Activity

![](alignedwires.png)
![](strippedcable.png)
![](pairs.png)
