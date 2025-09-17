# Project Introduction (Command Line Interface)
This was our second project of the year. In this project, we worked primarily in the linux terminal on UTM which is a virtual machine ran on mac. Common Line Interface is something that is important if you are in the filed of netowrking because it allows you to know the text needed so that the computer can interpret and display for the user. We learned the following commands, which were needed as prior knowledge during the activities.

### Commands

| Command | What It Does / Example |
|---------|-------------------------|
| **pwd** | **Stands for:** print working directory <br> **Does:** shows the full path of the folder you are currently “inside” in terminal <br> **Angle:** helps you always know “where you are” in your file system |
| **ls**  | **Stands for:** list <br> **Does:** lists the files and subfolders in the current directory <br> **Extra options:** <br> • `ls -l` → long listing (permissions, size, dates) <br> • `ls -a` → shows hidden files |
| **cd**  | **Stands for:** change directory <br> **Does:** moves you from your current folder into another folder <br> **Special cases:** <br> • `cd ..` → go up one level (to parent folder) <br> • `cd ~` → go to your home directory <br> **Angle:** like double clicking a folder in Finder <br> **Example:** `cd documents` |
| **mkdir** | **Stands for:** make directory <br> **Does:** creates new folder <br> **Angle:** equivalent to right click → new folder in Finder <br> **Example:** `mkdir projects` |
| **touch** | **Stands for:** no acronym, but it “touches” a file <br> **Does:** creates a new empty file or updates an existing one <br> **Angle:** often used to quickly create a blank file |
| **cp** | **Stands for:** copy <br> **Does:** makes a duplicate of a file <br> **Syntax:** `cp [source] [destination]` <br> **Angle:** difference between copying (duplicate stays in both places) and moving <br> **Example:** `cp notes.txt backup.txt` |
| **mv** | **Stands for:** move <br> **Does:** moves a file from one location to another or renames a file <br> **Examples:** <br> • `mv notes.txt documents/` <br> • `mv notes.txt notes_old.txt` |
| **open** | **Stands for:** open <br> **Does:** opens a file or folder using the default macOS app (like double clicking in Finder) <br> **Options:** <br> • `open .` → opens the current folder in Finder <br> • `open -a "AppName" file` → opens with specific app <br> **Angle:** CLI connects back to GUI apps |
| **rm** | **Stands for:** remove <br> **Does:** deletes a file permanently (does not go to trash) <br> **Extra options:** <br> • `rm -r foldername` → removes a folder and everything inside it <br> **Angle:** BIG caution here – danger. There's no “undo” or trash safety net <br> **Example:** `rm notes.txt` |

### Activities
The following are the activities we did for this project

- Map the Maze
- Map the Maze 2
- House Activity in Virtual Machine

## Map The Maze 

This was the first part of the command line interface project. In this, our main objective was to learn the basics of the file system on our computer, as well as how to navigate it.

#### Key Terms

| Term | Definition / Example |
|------|--------------------|
| Root Directory (`/` or `C:\`) | Top of the file system tree, contains all the file system |
| Folder (Directory) | A container used to organize files and other folders. Folders help group related files so the computer and the user can find them more easily |
| File | Stores data (text documents, images, videos) |
| Path | The address of a file or folder, showing its location inside the file system. Paths are written as a sequence of folder names separated by slashes |
| Absolute Path | Shows the full location of a file or directory |
| Relative Path | A relative path shows the location of a file or folder starting from your current working directory (where you are right now) |

#### diagram of file system tree

This was our first objective of this part of the project. We needed to make a file system tree that would show us the order in which we need to access certain files and folders. This helped us understand in a more linear way the organization of how files can be in folders that are subfolders of a larger folder.

/
└── Hudson
    ├── Documents
    │   └── essay.docx
    ├── Music
    └── Photos
        └── Huddy.png

#### Image of written file system tree

This file system was different since it was formated slightly differently than the digital typed one that I created.

![image](unnamed-4.png)

#### pseudocode

Start at home directory (cd ~).
Create new folder “Practice” (mkdir Practice).
Inside “Practice”, create subfolders: Docs, Photos, Music.
Create a text file “notes.txt” inside Docs (touch notes.txt).
Move “notes.txt” into Music folder (mv notes.txt Music/).
Verify structure with ls and tree.
Record the full path of Music folder (pwd).

#### MTMP1 Lesson 2

In lesson 2, our goal was to have learned how to navigate a file system using CLI commands. The commands we used are listed at the top of the page since they were needed for the house activity as well. We were walked through how to make a folder, subfolders in that folder, files in the sub folder, as well as move the files to a differernt folder. We also compared terminal paths to finder paths. 

Finder Path: /Users/hudsonmorrill/Practice/Music

Terminal Path: /Users/hudsonmorrill/Practice/Music


#### Map The Maze Part 1 Reflection

This section of the proejct was not too complicated, but it allowed us to learn how to do the basics. We mainly learned about how to access folders using the command line interface. Creating the file system tree helped me visualize how files and folders are organized. We learned how the root directory is the starting point of the file system with the other folders branching under as subfolders. We also learend about relative and absolute paths. Because we were guided through most of the project I found it realitivly easy to complete.

Absolute paths: Give the full location of a file

Relative Paths: Based off the current working directory


## Map The Maze 2

Map the maze 2 built off of the first map the maze. We used ubuntu and created files and directories as well as transfered them between mac and our VM (ubuntu)

#### Instructions

| Step | Task | Command / Action |
|------|------|-----------------|
| 1 | Getting Started | Open the terminal in your Ubuntu VM (`Ctrl + Alt + T`) |
| 2 | Navigation Practice | `pwd` → show current directory<br>`cd Documents` → enter Documents folder |
| 3 | Make the MazeGame Folder | `mkdir MazeGame`<br>`cd MazeGame` |
| 4 | Create Three Clue Files | `touch clue1.txt clue2.txt clue3.txt`<br>`ls` → verify files created |
| 5 | Edit Clue #1 | `nano clue1.txt`<br>Type: "Congratulations! You found the first clue."<br>Save with `Ctrl + O`, exit with `Ctrl + X` |
| 6 | Share Files with Your Host | Copy to hostshare: `cp clue1.txt ~/hostshare/`<br>Copy from Mac back to VM: `cp ~/hostshare/filename.txt ~/Documents/MazeGame/` |
| 7 | Reveal the Hidden Message | List hidden files: `ls -a`<br>Open secret file: `cat .secret.txt` |

#### Tools Used
- UTM
- Ubuntu
- Terminal
- HostShare

#### Commands

The commands used for this section of the project are listed above, at the very top of this page since they were also used in the other sections. The most common commands were as follows

- ls
- pwd
- cd
- sudo
- ls -a
- touch

#### Map The Maze Part 2 Reflection

This part of the project was an expansion of Map The Maze Part 1 where now we were focusing more on shared files. I found this to be pretty straighforward since we were given instructions that guided us step by step. I did struggle with a part of this because I could not get the hostshare to work for some reason. I made a folder, put it as a shared directory, but for some reason it did not show up on my computer. I also had this issue with the House Activity. I did feel like there were some commands that I was not entirely familiar with so it was a slight learning curve for me. Overall though I thought i learned a lot of info that will be necessary for other parts of the course as the year goes on. 

## House Activity in Virtual Machine

This was the third and final activity of the command line interface project. This activity involved trying to navigate a house that we were looking after while a friedn was away. We needed to know the commands previously listed to move in in out of rooms, eat (delete) items, delete multiple items in one command, and create a message for the friend. 

### Steps

1.	Download the map to your friend’s house
 To do this, I initally tried to share a directory between the mac and UTM, however I had issues and could not get this to work, so I used the wgit command and pasted the link and unzipped it to download the files.
2.	Go inside your friend’s house:
Command: cd House
3.	See where you can go:
Command: ls
Output: bedroom1  bedroom2  garage  kitchen  main_entrance
4.	Enter the Main Entrance:
Command: cd "main_entrance"
5.	Look around in Main Entrance:
Command: ls
Output: instructions.txt  unopened_mail1.txt  unopenedmail3.txt  shoerack  unopenedmail2.txt
6.	Open instructions.txt:
Command: cat instructions.txt
Message: thank you for watching my house, I have given you a list of tools to help out
7.	Go back to House level:
Command: cd ..
8.	Enter the kitchen:
Command: cd kitchen
9.	Look inside kitchen:
Command: ls
Output: Apple banana cereal crackers donut milk orange
10.	Eat some food (apple, banana):
Command: rm apple (or rm apple banana to remove both)
11.	Find hidden sweets:
Command: ls -a
Output: donut milk orange .rotten.bananan
12.	Remove rotten bananas:
Command: rm .rotten.bananas
13.	Enter Bedroom 1:
Command: cd .. then cd bedroom1
14.	Look around Bedroom 1:
Command: ls -a
Output: .secret_diary.txt
15.	Move to Bedroom 2:
Command: cd .. then cd bedroom2
16.	Look around Bedroom 2:
Command: ls -a
Output: Chair, desk, messy_bed
17.	Check current location:
Command: pwd
Output: /home/ubuntu/house/bedroom2
18.	Navigate to garage:
Command: cd .. then cd garage
19.	See garage contents:
Command: ls
Output: cardboard_box  cardboard_box2  cardboard_box3  garbage1  garbage2  garbage3  hose
20.	Clean boxes and garbage:
Remove garbage: rm garbage
Enter boxes: cd cardboard_box
Remove trash boxes: rm trash (box with trash: cardboard_box2)
21.	Return to Main Entrance:
Command: cd .. then cd main_entrance
22.	Leave a note:
Command: touch note.txt then nano note.txt
23.	Leave the house.

Bonus:
Found hidden room .hidden_basement and hidden_stash inside.
Command: ls -a → cat .hidden_stash
Message: "Congratulations! Put 'I won the game!' in the chat to confirm how much of a winner you are"

### House Sitting Activity Reflection

This was by far the most difficult part of the project for me. I spent the most time with trying to get the files downloaded. Initially, what I did was download the zip file from github into a folder on my mac. I then added that folder as a shared directory inside of the VM. I thought this would work but when I ran ls, I did not see the folder. I then had to find a different solution by using the wget command along with the link to the github. Once I did this, I unzipped the file and was able to access it from there. This is what I spent most of my time on for this project since I thought the commands were pretty simple and we had already had some expereince with it. Overall though I learned a lot but still want to figure out what went wrong with the shared directory and how to fix it.

# General Command Line Interface Reflection

I felt like this project really help me get used to the commands that we will need to know in this class. While we did not go super deep into many commands, I thought it was really helpful that I was able to learn not only what the commands mean, but also how the files and folders are organized (which we learned in Map The Maze Part 1) because I did not really know how important it was to know how they are realted. For example, if I did ls but i was in a specific section of a folder, I would only see that info and not all of the info in the main folder. I struggled particularly with the House Activity because I also was not able to get everything done in class and had to work on it at home without the help of who I was sitting next to. The main area of struggle was downloading the files. I could not figure out how to get the shared directory to work, so I needed to use a command that I was unfamiliar with. Compared to a Gui I thought this was much more difficult. I still am unsure of what went wrong so I will need to make sure to figure out what went wrong, but in the process I learned the wget command that could help me in future projects. On the document we worked on, it did not specifiy say how to downlaod the file which helped me problem solve more. I missed class one day during this, so I may have missed some things that could of been helpful, but I am glad I was able to learn more than I otherwise would have. Overall I found this project, specificly the house exploration very fun once I knew what to do, and I found the other two sections, Map the maze 1 and 2 more informative and something that was necessary to be able to do the final part of the project. In real world networking, although I am not too familiar, I think that what we learned is something that is definitely necessary to be succesful in this field.

