# Project Introduction
This was our second project of the year. In this project, we worked primarily in the linux terminal on UTM which is a virtual machine ran on mac. We learned the following commands, which were needed as prior knowledge during the activities.

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

/
└── Hudson
    ├── Documents
    │   └── essay.docx
    ├── Music
    └── Photos
        └── Huddy.png

#### pseudocode

Start at home directory (cd ~).
Create new folder “Practice” (mkdir Practice).
Inside “Practice”, create subfolders: Docs, Photos, Music.
Create a text file “notes.txt” inside Docs (touch notes.txt).
Move “notes.txt” into Music folder (mv notes.txt Music/).
Verify structure with ls and tree.
Record the full path of Music folder (pwd).

#### Map The Maze Part 1 Reflection


## Map The Maze 2

Map the maze 2 built off of the firt map the maze. 

#### Tools Used

#### Commands and Outputs

#### Map The Maze Part 2 Reflection

## House Activity in Virtual Machine

This was the third and final activity of the command line interface project. This activity involved trying to navigate a house that we were looking after while a friedn was away. We needed to know the commands previously listed to move in in out of rooms, eat (delete) items, delete multiple items in one command, and create a message for the friend. 


