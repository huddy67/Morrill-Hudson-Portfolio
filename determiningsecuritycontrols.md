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

Confidentiality
- encryption agreements
- The only thing that can decode data is an encryption key (ssh).
- Keeps information secret from people who shouldn't see it
- Websites could have security breaches

Integrity
- Keeping information/data uncorrupted, accurate, and trustworthy
- data has not been tampered with on purpose or by accident

Availability
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
 
phishing Attacks

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

## Cyber Security Basics for Devices

