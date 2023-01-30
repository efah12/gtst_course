# System Hacking
## What is System Hacking?
- System hacking is defined as the compromise between computer systems and 
software to access the target computer and steal or misuse their sensitive 
information. 
- The malware and the attacker identify and exploit the vulnerability of the computer 
system to gain unauthorized access.
- Here the malicious hacker exploits the weaknesses in a computer system or network 
to gain unauthorized access to its data or take illegal advantage. 
## Linux System Hacking
- As we all know, Linux is an Operating System (OS) assembled user the model of 
open-source software development and distribution and is based on Unix OS created by 
Linus Torvalds.
- Now to hack a Linux-based computer system and get access to a password protected 
Linux system, we have to know Linux's basic file structure. 
- As we know, Linux is considered to be the most secure OS to be hacked or cracked, but in 
the world of Hacking, nothing is 100% secured.
- Hackers usually use the following techniques to hack the Windows system.
    - Hack Linux using the SHADOW file.
    - Another technique commonly used by hackers is to bypass the user password option in 
Linux.(Privilege Escalation)
    - In another technique, the hacker detects the bug on Linux distribution and tries to take 
advantage of it.  
## Windows Hacking
- The user password of Windows OS, which appears after the Windows 
starts logging in, lets users protect the computer from getting 
unauthorized access.
- Choosing a strong password of more than eight digits is an excellent 
practice.
- Henceforth you can protect your files and folders from the hands of 
malicious users. 
- There are several tricks and techniques to crack a windows password. 
But, from the hacker's point of view, if you can use social engineer your 
victim and find a Windows computer open, you can easily modify the 
existing password and give a new password that will be unaware of the 
victim or the owner of the computer.
- Also There is a simple method to bypass windows login  
## Windows Login Bypass.
- As you see on the login page there is a button 
that can be vulnerable to this.
- A button on the right buttom, beside the 
Ethernet icon is called “Easy to access”
- When you click this button it will open a 
program called Utilman.exe from 
C:\Windows\System32
- So what hacker is going to do is you will rename 
this file to other thing and you will rename your 
terminal to Utilman.exe then BOOM  
- We will Swap their name.
- To do this

    a. Shutdown your windows

    b. Turn it on 

        - and when you see windows logo, press the power button , it will shut 
        - Again turn it on
        - and when you see windows logo, press the power button , it will shut 
        - Repeat this until you get the recovery mode.  
>> Recovery mode
- When This window comes press the power button and repeat until you see this screen 
### Recovery mode
Then go to

1. Advanced option
2. Troubleshoot
3. Advanced Options
4. System Image Recovery  
### System image recovery
Goto:
1. Cancel
2. Next
3. Advanced
4. Install a Driver
5. OK

- Renames 
1. This PC
2. Find the Correct C drive
a. Because Their letter will be different
b. Mine is “Local Disk(E:)”
3. Goto 
a. Your C drive>Windows>System32
4. Find and Rename Utilman.exe
a. Utilman.exe -> Utilman1.exe
5. Find and Rename cmd.exe 
a. Cmd.exe -> Utilman.exe
6. Exit and close them
7. Click Continue or restart your pc 
### The HACK
- Open Windows and Click on 
the easy to access button
- When you get cmd ,type
    - net user - to see users
    - net user “username” *
- Add new password
    - Just Enter to remove the 
password
- Then close cmd and login! 
### Reverse Shells
- As we saw shells are The only way to interact with the kernel.
- A reverse shell, also known as a remote shell or “connect-back shell,” takes advantage of the 
target system's vulnerabilities to initiate a shell session and then access the victim's 
computer.
- Reverse shells allow attackers to open ports to the target machines, forcing communication and 
enabling a complete takeover of the target machine. 
- Therefore it is a severe security threat. 
- This method is also commonly used in penetration tests.  
>> On reverse shells, the attacker will listen for any request on specific port, and the victim will start the 
request on that port, so we will have a shell., the victim may not sending the request intentionally. But if 
the attacker send him a link/malware that can start the reverse request that can leads to reverse shell 
### Netcat
- Netcat is a Command-line Interface (CLI) Based tool that is use to 
read/write data over TCP/UDP. 
- It is a Back-End tool which can smoothly be cross utilized by other 
programs
- It is a tool That helps to create Reverse shells or Bind shells
- It is built in on kali and parrot but for windows you have to download it.
- Lets demonstrate with it… 
- ON the attacker machine we started a listner…
- On the victim i called the attacker IP on that 
    - specific port
    - THis is for Example. 
- As you see on the attacker machine we got reverse shell and we can interact with the victims PC. 
## Web servers
- On the hardware side, a web server is a computer that stores web server 
software and a website's component files (for example, HTML 
documents, images, CSS stylesheets, and JavaScript files). 
- A web server connects to the Internet and supports physical data 
interchange with other devices connected to the web.
- It is A computer software and hardware that uses HTTP and HTTPS to 
provide a website.
- There are a lot of softwares that can be installed on the server to work like 
webserver
- As we talked previously, servers are just computers. So to be specific and 
talk about webserver, we have to install some web things. 
### A. Apache server
- This Server software will help to provide Web contents.
- On linux it comes Built in
- But on windows you can install it with softwares called Xampp and 
wampp and will give you localhost web contents
- To Start this server software
- From now on our computer is acting like a webserver. 
### Web Server - apache
- By going to out IP on any browser we can get a 
websites.
- The default path of apache2 is /var/www/html
- So on any webserver the websites are running on 
This path.
- The website you see on the right side is the default 
web for apache2 the file for this is the “index.html” 
from the /var/www/html file  
### B. Python Server
- We can you python to start web servers
- To start the service
- The python will help you to host website from any path on your computer with any 
port you need.
    - Example: on the above command i started the web server in ~/rex folder with port 9090
    - So to access the website i need to type the port with the ip
        - 192.168.1.7:9090 => will be the site for this 
##### CVE
##### - CVE stands for Common Vulnerabilities and Exposures. 
##### - CVE is a glossary that classifies vulnerabilities. 
##### - The glossary analyzes vulnerabilities and then uses the Common Vulnerability 
Scoring System (CVSS) to evaluate the threat level of a vulnerability.
##### - The CVE glossary is a project dedicated to tracking and cataloging vulnerabilities in consumer software 
and hardware.
##### - It is maintained by the MITRE Corporation with funding from the US Division of Homeland Security. 
##### - Vulnerabilities are collected and cataloged using the Security Content Automation Protocol (SCAP). 
##### - SCAP evaluates vulnerability information and assigns each vulnerability a unique identifier.
## - CVE-2019-0708  
# Metasploit
- The Metasploit framework is a very powerful tool which can be used by cybercriminals 
as well as ethical hackers to probe systematic vulnerabilities on networks and servers. 
- Because it’s an open-source framework, it can be easily customized and used with most 
operating systems.
- It is written with ruby.
- It have a lot of exploits for different kind of vulnerabilities and CVE’s
- It Provides you 
    - Exploits,
    - Payloads: a program that helps to run after exploiting/getting reverse-shells
    - Auxiliarys: Programs That will help to scan further on the system. 
    - Encoders,
    - Listners,
    - Post-exploitation codes: Used to run after we Exploit / privilege Escalation 
    ### Start.
- ON kali/parrot it is already installed,
- To start it just type, “msfconsole”
- We can search any exploit for a system.
    - Example: for apache
    - “search apache”  
## Create a Payload for windows.
- We will use metasploits Feature called msfvenom to create a payload.
- As you see we have created the payload
- Now we will send this to the victim
- This is the malware for our reverse attack. 
### Create a listener 

1. We start Metasploit.

2. We search for an exploit called Multi/handler

3.To use this exploit 
- use exploit/multi/handler
- use 29
4. set LHOST <IP>
5. set LPORT <port>
6. To run it
- exploit
- run 
- Metasploit is a very old tool and even the encoders are 
very old.
- This means almost every users tried them and exploited 
for some time but now a days all the antivirus and 
Microsoft defender will stop them and detect them.
- But it is Still handly tool for other exploitation and 
Scanning, you will see it in the future use.
- If you want to test these encoders on your system(may be 
if it is vulnerable for some of them.)
- Just add -e and the encoder name from the list and create 
the payload.(msfvenom) 
### So…we cant HACK???
- At this time, there are some Frameworks that 
can bypass microsoft defender.
- This means there are a lot of computers with 
just defender, right?
- The tool is called Villain
- You can clone it from github.
- https://github.com/t3l3machu 
#### Start
- It have its own some commands
- This tool is Awesome for
    - Creating payload
    - No need to setup listener
    - You can share the session you 
got with your friends, and hack 
together….  
### Create Payload
- Villain will give u powershell code
- It is Easy to create.
- Also You can use these 3 methods to make it undetectable. 
### Running 
- We can run the command we got on our victim’s powershell And it is really amazing, you can bypass microsoft defender.
- To see the sessions(hacked 
PC)
    - sessions 
- To get into that session
    - shell <ID>
    - You can start the name and TAB  
#### But… we dont get the victims Powershell???
- Now it is time to think like a hacker and getting plan how you will give the 
payload to the person.
- There are serveral ways
    - You can create a exe file from that payload
    - You can build/get a aurorun usb and do USB drop Attack
    - You can do social engineering and help them to run it by their own. 
### Powershell script to exe
- https://ps2exe.azurewebsites.net/ 
-  You can also use some exe icon changer softwares to make it look legit. 
### Does it really work?
- WHen i clicked on the 
software(topsercte…exe) 
- It worked i got shell. 
- We have bypassed Defender but not some 
antivirus
- (as you see smadav has detected it but still 
didnt do nothing, if you block or not) 
### Payload on WAN.
- As you saw we were trying the payloads on LAN network. Does it run on 
WAN?
- TO do this we will need a thing called port forwarding.
- Port forwarding inherently gives people outside of your network more access to 
your computer. Giving access or accessing unsafe ports can be risky, as threat actors 
and other people with malicious intents can then easily get full control of your device 
## Ngrok
- Ngrok is one of the portforwarding tools.
    - You can host websites with it
    - You can listen to tcp connections
- To setup:
    - GOTO their website & create account
        - https://ngrok.com/
    - Verify the ngrok through the email  
- Download the ngrok
- Goto the download location
- Extract it 
- Add ngrok to the /usr/bin
- Copy the Auth-token
- And run it on your terminal 
### Starting ngrok
There are 2 modes.

1. TCP -> ngrok tcp <PORT>
2. HTTP -> ngrok http <PORT> 
- It gives some informations on its own 
dashboard
- It have GUI too 
### Hosting our website
Let us make our local web server 
international
- We need a webserver
- And http portforwarding with 
same port as our webserver
- ngrok http 80 
### For python server 
- When some one access your forwarded site it will log it here. 
- Now this can help us to do our Phishing page.
    - DOwnload the last time tools and you can use them now you have ngrok
- WAN payloads
    - Just replace the lhost parts with the link provided and then you are Good to 
go.
    - Just remember to do same Port with the ngrok
        - For villain the lport is 8080 
### Prevention
- Payloads are one of Malwares, so the prevention methods are same 
with Malware prevention methods.
- REMEMBER if you have strong antivirus software you are 80% safe. 
### StegnoGraphy.
- Steganography is the practice of hiding a secret message 
inside of (or even on top of) something that is not secret. 
- That something can be just about anything you want. 
- These days, many examples of steganography involve 
embedding a secret piece of text inside of a picture
- But also we can hide inside audio files and etc
- There are many tools for this.
    - The famous on is “steghide” 
#### steghide
1. Downlaod it
2. To hide text to image
3. To extract

### Caution
- WHen you share these steged files, it doesnt have to be compressed
Or use USB,CD 
### Keylogging 
- Keyloggers are activity-monitoring software programs or 
hardware device that give hackers access to your personal 
data.
- The passwords and credit card numbers you type, the webpages 
you visit – all by logging your keyboard strokes. 
- The software is installed on your computer, and records everything 
you type. 
### Python Keylogger
- The file will be saved as .pyw this will make the file to 
now show any pop up but still it runs on backgroud.
- You can see that in task manager. 
- When you run this , it will create a log file.