## Exploring IP Addresses

Answer the following in complete sentences in a well-written paragraph on your digital portfolio:

Are your internal and external IP addresses the same or different?
They’re different. The internal one only works inside your own network, and the external one is what shows up online.

Which IP belongs to your local network?
The internal/private IP is the one that your local network uses.

Which IP belongs to the internet?
The external or public IP is the one that’s used when you’re actually on the internet.

Why might a virtual machine use Network Address Translation (NAT) when connecting to the internet?
A VM uses NAT so it can go online through the host computer’s connection without needing its own public IP.

How does Shared mode make it easier to connect multiple virtual machines on one computer?
Shared mode helps because all the VMs can use the same internet connection without a bunch of extra setup.

IP a in shared:  ![](ipa.png)

ip a in bridged: ![](ipa2.png)

whatismyipaddress results

shared: ![](whatismyip.png)

bridged: ![](whatismyip2.png)

Answer the following in complete sentences in a well-written paragraph on your digital
portfolio:

How did your internal IP address change when you switched to Bridged mode?
The internal IP changed because switching to Bridged mode put the VM on a different part of the network, so it got a new private IP address.

Did your external IP address change or remain the same?
The external IP stayed the same since the VM was still using the same internet connection from the provider.

In Bridged mode, does your virtual machine act more like a separate computer or a computer behind another device?
In Bridged mode, the VM acts more like its own separate computer on the network instead of being hidden behind the host.

Why might an organization choose Bridged mode instead of Shared (NAT) mode?
An organization might choose Bridged mode so the VM can directly communicate with other devices on the network without extra steps.

What security or management challenges could come with using Bridged mode?
Bridged mode can cause issues because each VM is fully visible on the network, which can make security and managing devices more complicated.

Table: | Mode         | Internal (Private) IP | External (Public) IP | Notes                                                                 |
| Mode         | Internal (Private) IP | External (Public) IP | Notes                                                                 |
|--------------|------------------------|------------------------|------------------------------------------------------------------------|
| Shared (NAT) | 192.168.64.3/24        | 173.95.44.210         | The internal and external are different, but the external stays the same. |
| Bridged      | 10.12.25.4/20          | 173.95.44.210         | The internal and external are very different in this mode. |

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



## Wires Activity

![](alignedwires.png)
![](strippedcable.png)
![](pairs.png)
