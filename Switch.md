# Switch Security Portfolio

---

## 1. Planning & Conceptual Understanding
### Initial Network Security Thinking

A Local Area Network is often treated as secure simply because it exists inside an organization, but this assumption creates risk. One of the most vulnerable points in a switched LAN is a standard workstation, such as a classroom desktop or staff computer. These systems are trusted by default once connected to a switch port and are rarely monitored closely unless a problem is obvious.

Even without special permissions, a normal device on the LAN can learn useful information about the network. Basic tools reveal the default gateway, nearby devices, and address relationships. Because internal traffic is generally assumed to be safe, this information is exposed with little resistance. This shows that switched LANs are vulnerable before any security controls are applied, mainly due to implicit trust and limited internal monitoring.

---

## 2. Threat Scenario Analysis & Reasoning

| Scenario | Symptoms | Hypothesis | Justification |
|--------|----------|------------|---------------|
| **Scenario A** | Devices stay connected but internet behavior is inconsistent | Internal traffic redirection is occurring | Connectivity remains intact while routing behavior changes, suggesting manipulation rather than an outage |
| **Scenario B** | Switch performance slows significantly | One device is exhausting switch resources | Abnormal MAC learning patterns traced to a single port correlate with performance degradation |
| **Scenario C** | Devices work but resolve websites incorrectly | Incorrect DNS settings are being provided | IP connectivity remains functional while name resolution fails, indicating configuration interference |
| **Scenario D** | New device appears and communicates broadly | Unauthorized network access through a physical port | The device is undocumented and originates from an unsecured connection point |
| **Scenario E** | Internal systems accept traffic without restrictions | Lack of internal access controls | Flat network design allows unrestricted lateral communication |

---

## 3. VM Evidence Collection & Interpretation
### Collected VM Evidence

A Linux virtual machine was used to observe internal network information. Commands such as `arp` and `ip neigh` revealed the default gateway’s address, neighboring devices, and router presence without requiring administrative access.

### Evidence Explanation

This information would be valuable to an attacker because it allows internal network mapping and identification of key infrastructure. Knowing gateway addresses and nearby hosts makes it easier to influence trusted communication paths. The lack of alerts during this process shows how easily reconnaissance can occur within a switched LAN.

### Evidence, Risk, and Controls

| Evidence | Risk | Control | Explanation |
|--------|------|--------|-------------|
| Gateway visible in ARP table | Gateway spoofing | DHCP Snooping | Restricts which devices can issue network configuration |
| Neighbor discovery enabled | Internal mapping | VLANs | Limits visibility between groups of devices |
| Excessive MAC learning | Switch overload | Port Security | Limits MAC addresses per port |

---

## 4. Reflection, Synthesis & Professional Quality
### Observing Switch Security Controls

#### No Security Controls

A flat switched network allows all devices to communicate freely. This model assumes every device is trustworthy, increasing the impact of a single compromised system.

#### VLANs

VLANs reduce broadcast traffic and limit unnecessary communication. However, they do not verify traffic authenticity on their own.

#### Port Security

Port security limits which devices can connect to a switch port, helping control physical access. It does not prevent misuse by already authorized systems.

#### DHCP Snooping and Related Controls

DHCP Snooping, Dynamic ARP Inspection, and ACLs work together to enforce trust boundaries and prevent unauthorized configuration or communication.

---

## Example Secure Network Design

### VLAN Layout
- VLAN 10 — Students
- VLAN 20 — Teachers
- VLAN 30 — Administration
- VLAN 40 — Servers

### Access Rules
- Students → Servers: Denied
- Students → Teachers: Limited
- Teachers → Servers: Allowed
- Administration → Servers: Allowed

Student devices are the least trusted, while servers require the strongest protection. Controls should be enforced at access ports and between VLANs.

### Why Multiple Controls Are Needed

VLANs separate traffic but do not verify identity. DHCP Snooping ensures trusted configuration sources, Dynamic ARP Inspection validates address mappings, and ACLs restrict communication paths. Together, these controls reduce reliance on implicit trust.

---

### Final Reflection

Scenario C is the most realistic because devices appear normal while operating with incorrect configuration, making detection difficult. This portfolio shows that switched LANs expose more internal information than expected and rely heavily on trust. The most difficult threats to detect are trusted devices quietly observing or influencing traffic without causing disruption.
