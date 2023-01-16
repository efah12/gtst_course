# Scanning and Enumeration
## What is Scanning?
- Scanning is the 2nd phase of Ethical Hacking.
- It is the step which helps to test a system based on 
the information we gathered.
- Scanning is another essential step, which is 
necessary, and it refers to the package of techniques 
and procedures used to identify hosts, ports, and 
various services within a network
## Why do we do scanning?
- It helps to Identify HOST’s System detail
    - Operation System
    - Service versions
- To Discover Open Ports
- To Discover Live Systems 
## Network Scanning
- This A method of Scanning a network and getting 
more informations.
- There are Many kinds of scanning methods and tools 
for different purpose.
- For Network mainly, NMAP
- For Subdomain, Sublist3r,subfinder
- For website vulnerability, Nessus, Acunitix..  
## Nmap - Network Mapper
- Nmap is A network scanning and exploring tool used by network 
and security experts.
- It is used to scan Network,Ports,OS,...
- It is made for windows and linux
- ON kali linux it is built in.
- To check the existence of nmap on your system
    - nmap --version  
## Live System Discovery
- Discovering live system means, Checking up and 
running hosts(clients/servers) on a network.
- We have seen Host checking last time with ping 
sweep method.(getting ip with link)
- But How does the ping worked?   
## Ping Sweep
- This is a method of checking if host is up or down.
- It uses ICMP(Internet COntrol Message Protocol) packets for checking 
purpose
- It sends Echo request and waits for response if there ie Echo reply then that 
system is up!   
>> This is my ubuntu 
server and the ip is “ 
192.168.56.101 “  
## Let’s Check if my ubuntu 
server is UP! With ping Sweep   

     -> What do we do it you to know all the hosts on ur system but ping can take 1 ip 
only??   
### Nmap ping sweep
- Nmap can perform ping sweep too.
- Syntax: 
    - nmap -sn IP    
    
- Nmap result have lots of things inside of it.   
- Nmap can scan the whole range.
- Guess how?
- You can do the ping sweep with little modification on the IP
- Syntax:
    - nmap -sn GatewayIP-255
    - nmap -sn GatewayIP/networkBits(subnet mask)
        - Network bits depend on the IP Class.
- This will not work on Virtual machines network.   
## Warning+=1
- Doing ping sweep is not 
undetectable thing check this.
- You are trying to ping the ip 
192.168.56.102
- And you are trying to do 
security pentest on my system. 
And you are script kiddie
- But am a security Guy.so…   
## warning++
- Some Organizations or system admins, will block any ICMP requests
- Here the ping sweep wont work
- To make it work we just escape the some option
- Syntax: 
    - nmap -Pn IP
- This method will Jump host discovery because it will take the ip as 
Up and try to do port discoveries. 

## What is PORT?
- Port is process-specific or an application-specific software construct serving as a 
communication endpoint, which is used by the Transport Layer protocols of Internet 
Protocol suite, such as User Diagram Protocol (UDP) and Transmission Control Protocol 
(TCP)
- It is like a dor for some purpose/service
- Example: if you want to get in to your house by which method do u get it?
    - BY DOOR
- Here there are different types of inputs, like if air wanted in the house we might use 
windows.
- So here in there scenario
    - WIndows are for airs
    - Doorsrs are for human
- These are ports those can help u to get it.   
- Also you home can have different doors and th3 main gate in ur home can be 
1 then the salon door is number 2….
On computer there are different 65,536 ports with different same job(like 
the window and door)
- 1-1024 = reserved ports
Example: 
- HTTP(80) - unsecured Web port
- HTTPS(443) - secured web port
- FTP(21) - File transfering port
- SSH(22) - Secured shell port   
## Port status
Ports can be on different status
- Open ports
    - THESE are ports open for accepting any requests.
    - Having an open air can lead to any kind of gas(ጭስ) or air getting 
to our house.
- Closed ports
    - THESE are ports which are not accepting any request but there is 
some service running on it.
    - Having your home door close,still the door helps sometime.
- Filtered ports
    - These are ports which nmap is not sure of being open or closed.  
## Open port discovery
On some system ports can b3 open for some purpose
Example: anywhere when you access websites there is web port 
open(80,443), 
If you are getting some shell activity there is port 22 open
- We can use nmap to check which port is open/closed
- And this is called port discovery
- Syntax:
    - nmap IP => only the 1000 ports
    - nmap -p port 1,port2,port3 IP => only port 1,2,3
    - nmap -p- IP => All the 65K port  
## Scanning methods
Nmap scans network in different modes

    a. TCP connect (TCP scan)

    b. TCP SYN (Stealth scan)
    
    c. UDP scans 
    
    d. Xmas scan 
    
## TCP Scan
- As we saw last time TCP is the best on doing 
connection oriented Things. And
- it is reliable But how?
- This is Because it uses 3-way HANDSHAKE!!!
- What is 3way handshake?  
## 3 way handshake
- When you establish a TCP connections there is something going behind the scenes
- What was the packet sent while the Ping sweep, it was the ICMP.
    - Here When we start connection we will send a Synchronization flag.
    - When the server got and accepted our request it will reply with 
Synchronization and Acknowledgment.
    - Finally, we will send Acknowledgement or Reset(RST) and continue because 
we have connection/network now. 
It is like meeting someone.

1. You: hi.
2. They: hello
3. You: Nice to meet you..  
### TCP scan works like this, so nmap will send the SYN request to the 
ports and if they reply with SYN/ACK nmap will reply with ACK 
BOOM!!! That port is open!! Else the port is closed/filtered.
Syntax:
>> nmap -sT IP  
### Stealth Scan.
- This is TCP scan but here we dont send the last ACK flag.
- But we send the RESET flag.
- Syntax: 
>> sudo nmap -sS IP   
### UDP scan
- This is a method to scan if any service/ port is using UDP   
- It is slow process
- Syntax:
>> sudo nmap -sU IP  
### Xmas Scan
- Here, The 1st thing to send is FIN/PSH/URG instead of SYN.
- If there is response like RST flag Then the system is close
- If there is no response the system is open.
- Syntax: 
>> sudo nmap -sX IP  
## Operating System Detection
- Nmap have a feature to detect the operating system of the host.
- Syntax:
    - sudo nmap -O IP => OS detection only
    - sudo nmap -A IP => OS detection including version  
## Scan Speeds
- When nmap do its scan, it have a time waiting, after 
sending 1 packets to a host.
- There are 5 time waitings.
- The nmap time template is -T<0-5>
    - Insane -T5
    - Aggressive -T4
    - Normal -T3
    - Polite -T2
    - Sneaky -T1  
### Nmap Insane
- This template is used for sending packets insanely fast and waits 
only 0.3 seconds for the response. 
- This timing template makes the scan superfast but the accuracy is 
sacrificed sometimes. 
- Nmap gives-up on a host if it couldn’t complete the scan within 15 
minutes.
- Other than that, -T5 should be used only on a fast network and 
high-end systems as sending packets this fast can affect the working 
of the network or system and can result in system failure.
- Syntax:
    - nmap -T5 IP   
### Nmap Aggressive 
- This template is used for sending packets very fast and 
waits only 1.25 seconds for the response. 
- Nmap official documentation recommends using –T4 for 
“reasonably modern and reliable networks”.
- Syntax:
>> nmap -T4 ip 
### Nmap Normal
- This is a default namep timing
- Syntax:
    - nmap -T3 IP  
### Nmap Polite and Sneaky
- These are the slowest timing.
Being slow, helps to not be detected on some risky projects.
Syntax:
- nmap -T2 IP
- nmap -T1 IP  
## Nmap Script Engine( NSE )
- Nmap is capable of running some script on ports and services.
- These scripts are written in lua-programming language.
- These scripts are located in /usr/share/nmap/scripts
- Nmap contains a total number of 589 scripts (Version 7.70), there are a lot of 
scripts that are useful but not all of them works perfectly, it’s like other tools a 
better for that particular task, so we’ll look at how we can use the powerful 
NSE and what scripts to use.
- You can Write your own script too if you can do lua
- Syntax:
    - nmap -sC IP
    - nmap --script scriptname.nse IP  
- Some known scripts.
    - --script banner 
        - => grabbing 
some details
    - --script broadcast 
        - reveals 
broadcast 
information
    - --script vuln 
        - test if the ports 
are vulnerable.