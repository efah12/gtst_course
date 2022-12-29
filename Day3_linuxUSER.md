# Linux For User 

## Overview of kali-linux
- Specifically,i will going to show you with "kali linux " with gnome but you can have any kinda,BUT  Debian is recommended,
- Previouslynknown as Backtrack

---
 ## 1)  INFORMATION GATHERING 
- Tools for information gathering,in system ,network,host 
     - dmitry
     - ike-scan 
     - legion
     - maltego
     - netdiscover
     - nmap
     - p0f
     - recon-ng
     - spiderfoot
 ## 2) Vulnerability Analysis
  - Tools for Finding Vulnerabilities 
       - legion
       - lynis
       - nikito 
       - nmap 
       - unix-prives. . .
## 3) Web Application Analysis
- Tools for Finding Vulnerabilities and exploits on websites.
     - burpsuite
     - commix
     - httrack 
     - paros
     - skipfish
     - sqlmap
     - webscarab
     - wpscan
     - ZAP
## 4) Database Assessment
- Tools for finding vulnerabilities and exploits on Databases.
   - jSQL Injection
   - mdb-sql
   - oscanner
   - sidguesser
   - sqldict 
   - SQLite data. . . 
   - sqlmap
   - sqlninja
   - sqlsus
   - tnscmd10g
## 5) Password Attacks 
- Tools for exploiting Passwords for login, websites, application, windows . . 
   - cewl
   - crunch
   - hashcat
   - hashcat
   - john
   - johnny
   - medusa
   - ncrack
   - ophcrack
   - rainbowcrack
   - rcracki_mt
   - wordlists
## 6) Wireless Attacks
- Tools for exploiting Wireless systems like wifi,bluetooth . .
     - aircrack-ng
     - chirp
     - cowpatty
     - fern wifi cra . . .
     - kismet
     - mdk3
     - mfoc
     - mfterm
     - pixiewps
     - reaver
     - wifite
## 7) Reverse  Engineering
- Tools for exploiting Softwares ,Mobile Applications and any binary files
   - apktool
   - bytecode-vi. . .
   - clang
   - clang++
   - dex2jar
   - edp-debug. . .
   - ghidra
   - jadx-gui
   - javasnoop
   - NASM shell 
   - ollydpg
   - radare2
## 8) Exploitation Tools
- Tools for exploiting Softwares, Mobile, Computers, websites and anythings
    - armitage
    - beef xss fra . . . 
    - metasploit Fram. . .
    - msf payloa. . .
    - searchsploit
    - social engin. . . 
    - sqlmap
    - termineter
## 9) Sniffing & spoofing
- Tools for listening or hijacking networks
     - driftnet
     - ettercap-gr. . . 
     - hamster
     - macchanger
     - mitmproxy
     - netsniff-ng
     - responder
     - wireshark
## 10) POST exploitation
- Tools for maintaining our access. Used after exploiting a system
     - backdoor-f. . . 
     - exe2hex
     - mimikatz
     - nishang
     - powersploit
     - proxychains4
     - weevely
## 11) Forensics
- Tools for Doing researches and investigate cyber Attacks. 
    - autopsy
    - binwalk
    - bulk_extrac. .  . 
    - chkrootkit
    - foremost
    - galleta
    - hashdeep
## 12) Reporting Tools
- Tools for report preparation.After some forensic you will get data and you will write report and these tools will help you.
     - cutycapt
     - dradis fram . . .
     - faraday IDE. .  .
     - maltego
     - pipal 
     - recordmyd. . . 
## 13) Social Engineering Tools
- Tools used for social engineering attacks 
   - backdoor-f . . .
   - beef xss fra . . .
   - maltego
   - msf paylo . . .
   -  social Engin. . . 
## 14) System Services
- Buttons used to start some services.
     - beef start 
     - beef stop
     - dradis start
     - dradis stop
## 15) Usually Used Applications 
- Softwares  for   some basic purposes
---
### *FOLDER MANAGERS
A) Dolphin

B) Thunar

C) Nautilus

---

## !Linux Commands
- Linux System uses shell. The shell help us to communicate with the kernel and helps to execute codes.
- Shell also colled "terminal"  
- The terminal have 5 parts.
  - Username = anony
   - Hostname = Kali
   - Current Diroctory = PATH
    - Priviledge=$-(user),#-(root)
    - Command Place = _
- Home directory is ~
- Local directory with .
- All directory     
## Linux Commands Basics
- On Linux there are over 100 commands.But we will see the main and the useful only. 
- Also those commands have their own options and arguments .
---
### WHAT IS COMMAND???
## "Small programs that do one task well "
---
### ls/ list directory
- SYNOPSIS
   - ls [option] . . .[File] . . .
- DESCRIPTION
   - list information about the FILEs (the current directory by default).
- ls -l
- ls -a
- ls filename
- ls -R=> Recursive
- You can combine them => ls -Rla "linux hidden files start with dot".
---
### cd / Change directory
- SYNOPSIS
  - cd[directory]
- DESCRIPTION
   - It is used to change current working directory 
 - cd /  =>root
- cd    =>home
- cd.. =>1x back
- cd../..=>2x back
- cd foldername 

> if  folder name have space you have to add the name inside"foldername"
cd"foldername"
  ----
## Pwd / print working directory
- SYNOPSIS
    - Pwd[-option]
- DESCRIPTION
   - It prints the path of the working directory,starting from the root .
   - E.g after typing pwd:/home/omar/desktop/OSlab
   ---
## echo 
- SYNOPSIS 
   - echo[option] [string]
- DESCRIPTION 
    - echo command in linux is used to display  line of text/string that are passed as an argument. This is a built in command that is mostly used in shell scripts and batch files to output status text to the screen or a file .
- you can write texts into files.
     - echo text >file.txt
- you can add texts(append) 
    -echo text >>file.txt   
    ---      
## cat / head / tail / less
- SYNOPSIS
   - cat[FILE]
- DESCRIBTION
   - Used to show the content of a file
   ---
   ## touch
 -   synopsis
       - touch[FIIE1][FILE2][FILE3]
  - DESCRIBTION
     -  Creates any kind of files with the name you gave it. With empty inside
     ---

     ## Mkdir / Make Directory
- SYNOPSIS       
   - mkdir[FOLDER-NAME 1][FOLDER-NAME 2][FOLDER-NAME 3]
- DESCRIPTION
   
   Creates Folder with the name u gave it.

         - DON'T forget to add the "" when you are using folders with space between them.
---
## clear 
- SYNOPSIS 
    - clear
- DESCRIPTION
    - clears your screen.
    ---
 ## rm / remove
 - SYNOPSIS 
    - rm [File 1][File 2][File 3]
 - DESCRIPTION
      - Remove file
 - rm -r => recursive(for folders)
 - rm -i => for prompt(ask)
 - rm -f => force delete
 > you can use them in combination too like, rm -rf'filename'
 ---
 ##  cp| mv /copy,move
 - SYNOPSIS
    - cp[oldFILEPLACE][newFileplace]
    - mv[oldFileplace][newFileplace]
 - DESCRIPTION
     - Copy/move files & Folders
 ---
 #  grep
 - grep[options]pattern[files]
 - The grep filter searches a file for a particular pattern of characters and displays all lines that contain that pattern. The pattern that is searched in the file is referred to as the regular expression (grep stands for global search for regular expression and print out).
- grep -i"search"file
     -  -case insensetive 
- grep -c"search"file 
    - -count numbers
- grep -l"search"file
    - -displays filename
- grep -R"search"foldername   
    - -search text in folders
 ## Wc - Word count 
- SYNOPSIS
  - wc [option]...[file]...
- DESCRIPTION
  - It is used to find out number of lines word count, byte and characters count in the files specified in the file arguments.

LINE(-l)    WORD(-w)      BYTE(-c)
## Multiple Command Executions
- You can run / execute multiple commands in one line.
- using 3 methods
    - And (&&)
    - Or (||)
    - Pipeing (|)
## AND (&&)
- On AND operation all commands you entered will be executed .
- If both are working without error 
## OR (||)
- On OR operation the command will executed.If it have error or not
## Pipeing(|)
- On pipe,will help you run commands by using the output of the first command as the input for the next one.