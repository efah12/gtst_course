# Some Advanced User Commands
- To change Password of user 
       - sudo passwd username 
- To change user id 
       - sudo usermod  -u new_id username 
- To Delete User 
     - sudo userdel -r username
- To change users on terminal 
## 🦸‍♂️Sudoers File 
- The sudoers file is a file Linux and Unix administrator use to allocate system rights to system users 
- The user you created doesn't have to use sudo as the original one 
- This is Because it is not Added in the sudoers file 
- To access this file                
      - sudo visudo 
-> The 1st appearance when you open the sudoers file 
-> You can add the user you need to have access to the sudeors file, so he can use the sudo command.
-> Then after the user can use sudo command  
## Linux File permission 
- Every file on linux have their own 
     - Owner 
     - Permission 
- There is 5 main parts on the listing 
      - Permission 
      - Owners
      - Date
      - Size
      - Filename
## Ownership
- Ownership is the owner of the file 
- This have 2 kinds 
    - User 
    - Group
- This change yhe owner of file you can use the command 
     - chown user:group filename 
## Permission 
- There are 3 types of permissions
      - Read (r)         
      - Write (w)
      - Execute (x)
- The folders and files differ with the 'd' and '-' on the beginning of the permission .
-  There still the permission have 3 parts.
    - user-group-other
- user(u) => power of user defind on the ownership 
- Group(g) => power of group defined on the ownership     
- Other(o) => power of other users.
- ALL(a) => power of all which can be found in the 3 above owners .
- Command to change permission of file 
     -  chmod <option> filename
## CHMOD Command
- This command helps to change file permission 
- Those file permissions are read,write,execute.
- Each of the permission have a number representations.
      - Read -> 4 -r
      - Write -> 2 -w
      - Execute -> 1 -x     
- SYNTAX 
    - chmod <parameter>filename      
- The parameter can be in numbers and symbols 
I. Parameters in Symbol
>  Note :- +  for adding,- for removing
   - chmod a+x filename = chmod +x filename
   - chmod u+x filename
   - chmod g+x filename
   - chmod o+x filename
   - chmod -x filename   
   - chmod a+rwx,u-rw,g-x,o-xw filename
II. Parameters in Number   
 - chmod 621 filename -> 6 for user,2 for group, 1for other (6=4+2),6 = rw
 - chmod 777 filename -> 7 for user,7 for group,7 for others (7 = 4+2+1),7 = rwx
 ## Package Installation On Linux 
- ON Linux to install softwares you use package managers .
       -  E.g:apt,pacman,pkg  
- We will use debian package manager .
- On debian the package manager i called 'APT' also ther is called 'dpkg'
- Package manager are a free-software user interface that work with an online server to handle the installation and removal of software on Debian,and Debian-based Linux distributions .
## ! The Repository 
-> This is the site/server kali use to upload the packages 
# !! Advanced package tool / apt /
- Apt is a free-software user interface that work with an online server to handle the installation and removal of softwares on Debian-based Linux distribution used for online and offline purpose.
- The old 'apt used as 'apt-get'
- Syntax  

           - sudo apt update 
           - sudo apt search <softname>
           - sudo apt install <softname>
           - sudo apt remove <softname>
           - sudo apt upgrade 
           - sudo apt purge <softname>
## Package dependencies 
- A software can built based on another program called 'modules'
- SO, a program to work properly,they dependencies have to be installed successfully.   
- Those package managers install the software+dependencies.   
## DPKG / Debian package manager /
- Dpkg is an offline packages managing program .
Packages on debian have an extension ".deb"
- SYNTAX

         - sudo dpkg -i <packagename>
         - sudo dpkg -r <packagename>
         - sudo dpkg -P <packagename>

             