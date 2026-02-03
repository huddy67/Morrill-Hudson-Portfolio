# Common Security Controls in a LAN

---

## 1. Planning & Conceptual Understanding

### Clear Evidence of Planning and Conceptual Understanding  
*(Understanding of flat LAN risk, internal trust, and physical vs technical security)*

In a local area network, the easiest device for an attacker to compromise is usually a standard user workstation or other lightly managed endpoint. These devices are built for convenience and productivity, not for verifying every piece of network information they receive. Because of this, they automatically trust services like ARP and DHCP to provide correct addresses and routing details. If an attacker connects to the same LAN, they can take advantage of this trust to impersonate network infrastructure or quietly observe traffic without needing to break into the device directly. Physical proximity does not mean safety inside a LAN. Once a device is connected, it can receive broadcast traffic and participate in discovery processes that reveal nearby hosts, gateways, and general network structure. In a flat LAN, this visibility becomes even greater because there are no boundaries separating devices. This demonstrates a major flat LAN risk: internal trust is assumed by default. Technical security controls help manage traffic and access logically, while physical security controls prevent unauthorized devices from joining the network in the first place. Both are necessary to reduce internal exposure.

---

### Distinguishing Threats, Vulnerabilities, and Controls — LAN Threat Scenario Rotation

| Scenario | Symptoms (Summary) | Hypothesis | Justification |
|--------|-------------------|------------|---------------|
| A | Default gateway suddenly incorrect | ARP manipulation | Gateway changes suggest traffic redirection rather than random error |
| B | Switch CPU spikes; many MACs learned on one port | MAC flooding attack | Overloading the MAC table forces broadcast behavior |
| C | Clients receive IP settings from unknown source | Rogue DHCP server | DHCP clients trust the first valid response |
| D | New device communicates broadly | Unauthorized plug-in device | Weak access control allows wide visibility |
| E | Host accesses restricted systems | Lateral movement | Internal trust enables access beyond permissions |

---

### Group Reflection — Patterns of Internal LAN Risk

The strongest conclusions were made for Scenarios B and C because their symptoms closely matched how switches and DHCP behave when they are abused. Scenario D was the hardest to interpret, since similar behavior could also happen because of poor configuration rather than an attack. Talking with another group helped highlight that many LAN threats do not look suspicious at first and often blend into normal traffic. A major pattern across all scenarios is that most threats start inside the network, not outside it. This reinforces how dangerous internal trust can be when proper controls are missing.

---

## 2. Technical & Security Development

### Execution of LAN Security Investigation and Security Reasoning

### Task A — LAN Observation (VM-Based Evidence)

**Evidence**

![](ipshowd1s1.png)

**Reflection — Vulnerabilities Exposed Through Observation**

The ARP and routing outputs show active devices, IP-to-MAC mappings, and the default gateway. This information can be misused by an attacker to identify important systems and plan impersonation or interception attempts. Seeing how devices learn about each other reveals a vulnerability in how much information is shared by default. Without protections, this visibility gives attackers a strong advantage once inside the LAN.

---

### Task B — Vulnerability-to-Control Mapping

| Evidence from VM | Possible Threat | Explanation |
|------------------|----------------|-------------|
| Default gateway in routing table | ARP spoofing | Gateway identity can be impersonated |
| IP-to-MAC mappings | ARP spoofing | ARP updates are trusted automatically |
| Visible neighboring hosts | Lateral movement | Reveals potential internal targets |
| Multiple MACs on one port | MAC flooding | Forces switch into broadcast mode |

This mapping shows how normal LAN behavior can turn into a vulnerability when attackers exploit trust assumptions. Security controls are designed to limit or verify these behaviors rather than remove them completely.

---

### Task C — Threat Analysis and Abuse of Normal LAN Behavior

ARP spoofing works because ARP is designed for speed and simplicity, not verification. Devices accept ARP messages and update their tables without checking whether the information is legitimate. An attacker can send forged ARP replies that associate their MAC address with the gateway’s IP address. Once this happens, traffic is redirected through the attacker’s system. Because this traffic looks normal, the attack is difficult to notice without additional security controls.

---

## 3. Testing, Observation & Risk Evaluation

### Interpretation of Evidence and Risk-Based Reasoning

### VM Evidence

**Workstation Perspective**

![](ipshowd1s1.png)

**Infrastructure Perspective**

![](22.png)

---

### Observation of ARP Behavior and Broadcast Scope

ARP traffic reveals how devices resolve IP addresses to MAC addresses and how much trust exists within the LAN. The protocol assumes that all responses are truthful, which creates a major vulnerability. Bridged networking was required so both virtual machines existed in the same broadcast domain, allowing ARP traffic to be observed and analyzed. This setup reflects how real internal networks behave.

---

### Risk Evaluation — Likelihood and Impact

ARP spoofing is one of the hardest internal LAN threats to detect because it blends into everyday network behavior. ARP tables change frequently during normal operation, which makes malicious updates difficult to identify. The evidence collected shows how easily these mappings can be altered without triggering warnings. Because attackers can intercept or modify traffic silently, the potential impact on confidentiality and integrity is high. This makes ARP spoofing a serious internal risk.

---

## 4. Professional Integration & Portfolio Quality

### Internal LAN Threat Catalog — Clear and Professional Documentation

- **ARP Spoofing** — Impersonates trusted devices using forged ARP replies.
- **MAC Flooding** — Overloads switch MAC tables to force broadcast traffic.
- **Rogue DHCP** — Issues unauthorized IP configurations to clients.
- **Unauthorized Plug-In Device** — Gains access through open network ports.
- **Lateral Movement** — Exploits internal trust to reach additional systems.

---

### LAN Attack Path Diagram — Professional Artifact

![](diagram.png)

**Explanation**

The diagram shows how an attacker can impersonate the default gateway using ARP spoofing. Devices trust ARP traffic without validating its source, allowing traffic to be redirected through the attacker. Dynamic ARP Inspection would stop this attack by validating ARP messages against trusted bindings. VLAN segmentation would further reduce the impact by limiting broadcast visibility.

---

### Physical Security Integration — Physical vs Technical Security

#### Identified Physical Vulnerabilities
- Unauthorized access to laboratories
- Weak separation between public and restricted areas
- Poor protection of server and network rooms
- Inconsistent visitor monitoring
- Limited surveillance coverage
- Exposed storage areas

---

### Physical Security Plan — Layered Defense

**Environmental Controls**  
Protect equipment from failure and downtime.

**Access Control**  
Limit entry based on roles and permissions.

**Surveillance**  
Detect and deter unauthorized activity.

**Hardware Security**  
Prevent tampering and rogue device connections.

**Personnel Procedures**  
Reduce human error and enforce security policies.

---

### Digital Physical Security Diagram

![](111.png)

---

### Risk Justification and Priority Controls

Access control, surveillance, and hardware security are the most important physical controls because they directly prevent unauthorized access to network infrastructure. Strong physical security supports technical controls like VLANs, ACLs, and monitoring systems. When physical protections are weak, attackers can bypass technical defenses by simply plugging into the network. A layered approach ensures that both physical and technical security work together.

---

## Conclusion

This portfolio provides clear evidence of planning, investigation, and risk analysis related to internal LAN security. Through observation, testing, and threat analysis, it demonstrates how internal trust and flat network design increase risk. The inclusion of both technical and physical security controls shows an understanding of how layered defenses reduce attack paths. Overall, this assessment highlights why strong internal controls are essential for secure and reliable network operations.
