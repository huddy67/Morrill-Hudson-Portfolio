# Implementing Security Controls For Devices

### Objectives

password algorithm
MFA installation
Patching Sequence
NIST/OWASP guidlines

### Notes on Password Entropy

### Screenshots of Design Steps

## Password Algorithm Design

My Password Algorithm

## Changing Password Ubuntu

original: ubuntu

New: Book1Story2Page3Word4!!

This new password followed my algorithm that I had created before

#### Steps to changing password

1. Log in
   - Username: ubuntu
   - Password: ubuntu

2. Open terminal

3. Change password
   '''passwd'''
   (current password: ubuntu)
   (new password: your strong password)

4. Test with sudo
   '''sudo ls /root'''

5. Create new user
   '''sudo adduser yourname'''
   '''sudo usermod -aG sudo yourname'''

6. Lock default user
   '''sudo passwd -l ubuntu'''
