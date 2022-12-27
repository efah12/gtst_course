# 🔚FINISHING FOR LINUX🔚
 ## Script Insatallation
- Some hacking tools are developed by some peoples and those peoples make it open-sourse,that means we can get those scripts/programs from github.
- git has a feature called 'clone'
- Syntax 


      -  git clone <link_of_the_script_from_github> 
## Script modules 
- Scripts are made with scripting languages (programming) like {python,bash,go,ruby . . .}
- So when we use these programming languages to do tasks thir is something called modules/libraries these are needed to run the script as the dependencies.
- Exmaple:
1) python : to install python modules we use -> pip install <module name>
    i.  For requirments file -> pip install -r requirments.txt
2) Go:to install go modules -> go install <modulename>    
3) Ruby: to install ruby modules -> gem install <modulename> 
## If you need help on linux about command 
###  You can use  
- man(manual)
     - This will give you thewhole manual and instraction of a tool or command. 
          - man (your command)    
          >KEYS: arrow keys for navigation | q for quit
- Help 
     - Some Commands have help option.
         - <your command>   -h
         - <your command>   -help
         - <your command>   - -help 
## Linux Processes & Services
- As we interact with linux,we create numbered instaces of running progmas called "processes"
- To get the processes 
     - ps -> for process running on my shell
     - ps -A -> view all running process 
     - ps-u username -> view users process 
-   PID - process ID
- To stop the process 
     - kill -19 PID -> to stop the process
     - kill -18 PID -> to resume the process we stopped 
     - kill -9 PID -> to stop a process immediately
     - . . . there are 31 options.
## Foreground / background     
- Thus far,we have run commands at the prompt and waited for them to complete.We call this running in the "foreground".
- Use the '&' operator,to run programs in the 'background' or press ^Z
- To get background to process back to foreground 
   - Fg
- To stop a process going inside your shell just press ^C  
## Null Device 
- /dev/null - Redirects output to nowhere.
- If you want to ignore output,you can send it to the null device , /dev/null.The null device is a special file that throws away whatever is fed to it.
- On shell output there are 2 things.
      - STDERR = 2
      - STDOUT = 1
- To redirect the errors from a command and result we do 
      - command 1> filename
- To redirect the error-FREE ouput
      - command 2> filename
- So if we redirect our commands output to /dev/null we will get error free result 
       - command 2> /dev/null
## alias
- Used to give a name to some bunch of commands.
- E.g : if i wanted to name ls-la 'rex' so anytime i want to get output of ls-la i just type rex 
       -   alias rex='ls-la'  
## Tmux - Terminal Multiplexer
- Tmux is used to classify our terminal work.
- You can install it using apt.On kali it is built-in
- Then to start it just type 'tmux'\
- To create config file type 
  - nano .tmux.conf
     - Type this  
      - unbind C-b
     - unbind l
     - set -g prefix C-a
     - unbind %
     - bind e split-window -h
     - bind o split-window -v
     - set -g base-index 1
     -  setw -g pane-base-index 1
- To spilt horizontal 
      - ^A then o
- To spilt vertically
      - ^A then e
- To exit 
      - ^A then x or just type exit
- To create tab
      - ^A then c
- To rename the tab 
      - ^A then ,
- To switch tabs
      - ^A then <numbers>
      - To switch partitions 
             - ^A then <arrow>
## wget 
 -  Is a tool used to download files from websites/servers 
 - Syntax 
      - wget[options][link]
## find 
- On terminal if you want to search for files/folders/musics/videos, we can find command.
- It is very essential tool
- Syntax
      - find[search path][option][search word]
      - find /-name"linux"
      - find/home-perm777
      - find-type f | find-type d
