# Determining Security Controls for Devices

### Project overview

In this project, the main objective was to learn how we can properly secure our data, as well as identify when our data or information my be at risk

### Objectives

- Learn the CIA Triad (Confidentiality, Integrity, Availability)
- Identify vulnerabilites that hackers could take advantage of
- Understand how to defend your device from vulnerabilities
- Check to see if software was updated and installed, and if not then either update or install it to prevent vulnerabilites from being exploited
- know common tactics that hackers may use to access your data and information

### Guided Notes: Cybersecurity Basics for Devices

We took notes on a google doc where we learned about the CIA triad, common device vulnerabilities, common ports, and types of phishing attacks. 

CIA Triad

##### Confidentiality
- encryption agreements
- The only thing that can decode data is an encryption key (ssh).
- Keeps information secret from people who shouldn't see it
- Websites could have security breaches

##### Integrity
- Keeping information/data uncorrupted, accurate, and trustworthy
- data has not been tampered with on purpose or by accident

##### Availability
- Making sure that information and systems are available when we need them
EX. College board making sure servers are up while people are taking exams

Common Device Vulnerabilities:

- Weaknesses that can be exploited
  - Ex. outdated operating systems
    - Companies release updates to fix weaknesses
  - Ex. unencrypted data
  - Ex. weak passwords
  - Ex. open ports
    - Place where software can connect to the internet
    - Like a “window” or “door” that lets services communicate
    -  Some ports are necessary

- Well-known ports
  - `80`   — HTTP  — hypertext transfer protocol (unencrypted web)
  - `443`  — HTTPS — secure web traffic 
  - `22`   — SSH   — secure shell
  - `25`   — SMTP  — simple mail transfer protocol
  - `110`  — POP3  — retrieve mail
  - `143`  — IMAP  — mail on server
  - `3389` — RDP   — remote desktop protocol 
  - `53`   — DNS   — domain name system

- Unpatched software
  - Ex. Windows updates (Patch Tuesday)
  - Ex. Web browsers (Chrome, Firefox, Safari)
  - Ex. Mobile apps
  - Ex. Ubuntu/Linux
 
### Phishing Attacks

Phishing - Attempt to get you to click malicious links via email, text, etc...
Tailgating - unauthorized person gaining access to information from an authorized person
Spear phishing - phishing that targets a specific person
Pretexting - creating a realistic scenario to access someones information
Baiting - baiting someone to give confidential info by deceiving them into a trap



#### Matching Cards Activity

We started off by doing an activity where we were given two sets of cards, one set being orange and the other being green. The green cards would have an example of someone doing something that puts their data at risk, and the orange cards would have a solution to making sure that their data is not at risk. Me and Scarlett were partners for this activity and our pictures of our card matches are below. 

(pictures)

## Outdated Software

In this activity we checked software in the ubuntu VM to see if it was up to date or even installed. If it was not up to date then we updated it and if it was not installed we installed it. We then answered questions about the importance of keeping softwares up to date as well as which softwares were the most important to keep up to date. 

Before checking or installing we ran the following commands which made sure latest versions were installed:
- sudo apt update 
- sudo apt upgrade -y

### Table of my results

| Software / Version     | Status        | Risk                                                                 |
|------------------------|---------------|----------------------------------------------------------------------|
| OpenSSL                | Outdated      | Can leak data if not updated.                                        |
| Firefox                | Up to Date    | Safe, protects against scams and phishing.                           |
| LibreOffice            | Outdated      | Hackers could get into files and steal important info.                |
| Python                 | Outdated      | Older versions have bugs and can make the system less secure.         |
| Apache HTTP Server     | Not Installed | No risk since it’s not on the system.                                |
| GIMP                   | Not Installed | No risk since it’s not on the system.                                |
| Java                   | Not Installed | No risk since it’s not on the system.                                |
| OpenSSH                | Outdated      | Hackers could break in remotely if not updated.                      |

Most of the software was not updated. In terms of the risk it imposes on the school devices, I do not think there is much risk because it is only students at charlotte latin using the computers, but for personal devices these often have more information that needs to be private, or could have work information. Therfore, you should always try to keep these updated to prevent people from stealing your information. Because the software is outdated there are vulnerabilities that hackers know of and can exploit, but if you update it then it is much harder since the exploits likely got patched. 

## Cyber Security Basics for Devices

This was the second big project we worked on. In this we learned how to identify the ports open in our VM and whether they were necessary. We also learned how to place firewalls, which act like locks on unused doors

### Project Walkthrough

The first command I ran was: netstat -tuln

For whatever reason this did not work so i ran: ss -tuln

This command identified ports that I had open

Next I ran: sudo apt update && sudo apt upgrade 
sudo apt install ufw -y 

This ensured that UFW was installed because it normally is not installed by default

I then checked firewall status: sudo ufw status 

My firewall was not enabled so I ran: sudo ufw enable

I then blocked port 23 using: sudo ufw deny 23/tcp (the reason for doing so is because this is outdated and hackers can use this to easily steal info)

Next I checked for LUKS encryption using: lsblk -f (I did not see crypto_LUKS which means there wasn't encryption)

reflection: 

- The firewall was not enabled initially, so I needed to enable it.
- I also blocked telnet because it was not secure.
- disk encryption was not enabled, but should be for encryption

This assignment helped me learn the risks with having unused ports open. We learned the importance of firewalls which act as a lock for unused ports and prevent hackers from gaining access. This was something I was not familliar with at all prior to the project, so I am still learning this, but I feel like I gained a basic understanding of the importance of making sure your data and information is encrypted.

# Overall Reflection:






 
