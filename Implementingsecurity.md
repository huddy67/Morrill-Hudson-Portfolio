# Implementing Security Controls For Devices

### Objectives

Password algorithm - Create a unique algorithm that makes a secure password

  ##### Principles for Secure Password

     - length
     - unpredictability
     - entropy
     - making sure it is memorable
     - special characters
     
MFA installation - Install MFA (pam_google_authenticator) and serify it via SSH

Patching Sequence - Keep ubuntu secure by patching and updating software. Understand the benefits of updating and the risks of not updating

NIST/OWASP guidlines

### Notes on Password Entropy

Link: https://docs.google.com/document/d/1TeFBieNnrw9kggYTQZFMGe3J8r8IhxLfDrKi_XJu3Ow/edit?tab=t.0

### Screenshots of Design Steps

## Password Algorithm Design

My Password Algorithm

	•	Go to the online dictionary
	•	Scroll until you want to stop
	•	Pick a random word
	•	Repeat 4 times
	•	Put the words together and make every other letter upper case
	•	In between each word put a number 1–10
	•	Put a special character at the end

## Changing Password Ubuntu

Original: ubuntu

New: Book1Story2Page3Word4!!

This new password followed my algorithm that I had created before excpet for instrad of randomly scrolling in the dictionary I picked 4 words that I could think of, and made sure they were similar to eachother. I did this to save more time, as well as make the password more memorable.

   #### Steps to changing password

   1. Log in
      - Username: ubuntu
      - Password: ubuntu

   2. Open terminal

   3. Change password
      ```passwd```
      (current password: ubuntu)
      (new password: your strong password)

   4. Test with sudo
      ```sudo ls /root```

   5. Create new user
      ```sudo adduser yourname```
      ```sudo usermod -aG sudo yourname```

   6. Lock default user
      ```sudo passwd -l ubuntu```

      the result is that my password was changed from ubuntu to the one I had created using my algorithm (Book1Story2Page3Word4!!)

   #### Changing Passwords in Ubuntu Screenshots

   



## MFA Installation in Ubuntu

#### Steps and Commands

1. Log in as the admin account
    Username: ubuntu
    Password: ubuntu

2. Test sudo
```sudo ls /```

3. Add your student account to sudoers
```sudo usermod -aG sudo yourusername```
```sudo reboot```

# Log in as your own account and test
sudo ls /

#### MFA (pam_google_authenticator) installed and verified via SSH

4. Install Google Authenticator
```sudo apt update```
```sudo apt install libpam-google-authenticator -y```

google-authenticator answer prompts:
 Time-based tokens: y
 Update .google_authenticator file: y
 Disallow multiple uses: y
 Enable rate-limiting: y

5. Enable MFA for SSH login
sudo nano /etc/ssh/sshd_config
 Change/add:
 KbdInteractiveAuthentication yes
 UsePAM yes
 PasswordAuthentication yes  (if needed)
 ```sudo systemctl restart ssh```

sudo nano /etc/pam.d/sshd
 Add at top:
 auth required pam_google_authenticator.so
```sudo systemctl restart ssh```

6. Test SSH login with MFA
```ssh yourusername@localhost```
 Enter your Ubuntu password
 Enter 6-digit verification code from authenticator

#### Common Issues Fix

7. Fix common issues
 If nano is missing
```sudo apt update```
```sudo apt install nano -y```

 If verification code rejected, check system clock
```timedatectl status```

## Patches in Ubuntu

- Check for available updates
```sudo apt update```
```sudo apt list --upgradable```

- Apply updates
```sudo apt upgrade```

- View update history
```cat /var/log/apt/history.log```

- Search update logs by date
```grep "YYYY-MM" /var/log/apt/history.log```

- See installed or updated packages
```grep "Install:" /var/log/apt/history.log```

- Count installation events
```grep "Install:" /var/log/apt/history.log | wc -l```

- View most recent install
```grep -A 2 "Start-Date" /var/log/apt/history.log | tail -n 10```

- Search for a specific program/package
```grep "nano" /var/log/apt/history.log```
```grep "firefox" /var/log/apt/history.log```
```grep "google-authenticator" /var/log/apt/history.log```

- Check the most recent log entries
```tail -n 20 /var/log/apt/history.log```

- Check automatic update schedule
```ls -l /var/lib/apt/periodic/```

### Patches in Ubuntu Screenshots 

![](photo1.png)
![](photo2.png)
![](photo3.png)
![](photo4.png)
![](photo5.png)
![](photo6.png)
![](photo7.png)


# Reflection
