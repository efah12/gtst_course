# Network Hacking
## What is Network Hacking?
- Network Hacking is gathering and exploiting of networks.
- The networks can be WAN or LAN.
- Networking Hacking is an offensive branch of computer security 
related to networks hacking and the penetration of a target via the 
networking services or equipment. 
- This includes
- Network information gathering
- Sniffing
- Network Attacks  
## Network footprinting
- Network Hacking is generally means gathering information about domain by using tools

1. Ping: used for ping sweep 
2. traceroute 

    a. It is used to trace out the route taken by the certain information

    b. i.e. data packets from source to destination.  
### Network sniffing
- Sniffing is the process of monitoring and capturing all the packets 
passing through a given network using sniffing tools. It is a form of 
“tapping phone wires” and get to know about the conversation
- Sniffing is ማሽተት
- So we will sniff their networks. 
### Types of sniffing
1. Passive sniffing

    a. In passive sniffing, the traffic is locked but it is not altered in any way. Passive sniffing allows listening only. 

    b. It works with Hub devices. On a hub device, the traffic is sent to all the ports. In a network that uses hubs to connect systems, all hosts on the network can see the traffic. Therefore, an attacker can easily capture traffic going through.
    
    c. The good news is that hubs are almost obsolete nowadays. Most modern networks use switches. Hence, passive sniffing is no more effective.

2. Active Sniffing

    a. In active sniffing, the traffic is not only locked and monitored, but it may also be altered in some way as determined by the attack. 

    b. Active sniffing is used to sniff a switch-based network.   
### Sniffing networks…
- Let’s Sniff some networks
- For this purpose we use a program called Wireshark.
- It is One popular passive monitoring tool.
- Wireshark technically is referred to as a “protocol analyzer”, but it 
uses only passive observation of network traffic. 
- Wireshark supports both live and offline analysis, has a graphical 
user interface, and can be used for analyzing multiple protocols
- It is for windows and linux.  
##### wireshark
To start it
- You can type it 
on terminal
- You can search 
it on the 
applications. 
- After choosing a network 
interface, it will start 
capturing  
### Tshark
- Tshark is a command line tool like the 
wireshark it can capture  
### What is ARP /Address Resolution Protocol/
- Address Resolution Protocol (ARP) is a 
procedure for mapping a dynamic IP 
address to a permanent physical machine 
address in a local area network (LAN). The 
physical machine address is also known as a 
media access control (MAC) address.
- The reason why we need ARP is because 
computers need to know both the IP 
address and the MAC address of a 
destination before they can start network 
communication 
###### demo
- Look at the below wireshark capture.
In this case the source is my router.  
### searching…
- On the search bar you can 
search 
protocols(ICMP,ARP,HTTP..) 
or some ip addresses as 
shown.
- It also try to suggest you and 
complete it for you.  
### Mac flooding
- MAC Flooding is one of the most common network attacks. 
- Unlike other web attacks, MAC Flooding is not a method of attacking any host machine in the network, 
but it is the method of attacking the network switches. 
- However, the victim of the attack is a host computer in the network.
- the switches maintain a table structure called MAC Table. 
- This MAC Table consists of individual MAC addresses of the host computers on the network which are 
connected to ports of the switch.
- This table allows the switches to direct the data out of the ports where the recipient is located.
    - As we’ve already seen, the hubs broadcast the data to the entire network allowing the data to
reach all hosts on the network but switches send the data to the specific machine(s) which the 
data is intended to be sent.
    - This goal is achieved by the use of MAC tables.
- The aim of the MAC Flooding is to takedown this MAC Table. 
- In a typical MAC Flooding attack, the attacker sends Ethernet Frames in a huge number. When sending 
many Ethernet Frames to the switch, these frames will have various sender addresses. The intention of 
the attacker is consuming the memory of the switch that is used to store the MAC address table. 
- The MAC addresses of legitimate users will be pushed out of the MAC Table.
- Now the switch cannot deliver the incoming data to the destination system. So considerable number of 
incoming frames will be flooded at all ports.   
#### demo.
- I have set ping sweep on 
my windows to check the 
connection
- Wireshark to see the 
package
- And used macof tool for 
the mac flood.
- Also can be sent to 
specific 1 destination /ip 
- The command needs 
    - sudo 
- Masof will send a lot of fake MAC’s to the switch 
and makes if confused, and do stop proper 
functioning this can cause , disconnections
between hosts.
- As you see google is now disconnected from host. 
>> This can cause huge damge on the network, it is fixed by rebooting the router. DONT try it on your network  
### Prevention

1. Port Security – Limits the no of MAC addresses connecting to a single 
port on the Switch.

2. MAC Filtering – Limits the no of MAC addresses to a certain extent. 
## ARP Spoof
- ARP translates Internet Protocol (IP) addresses to a Media Access Control (MAC) 
address
- Most commonly, devices use ARP to contact the router or gateway that enables them 
to connect to the Internet.
- An ARP spoofing, also known as ARP poisoning, is a Man in the Middle (MitM) attack that allows 
attackers to intercept communication between network devices. The attack works as follows:
    a. The attacker must have access to the network. They scan the network to determine the IP 
addresses of at least two devices—let’s say these are a workstation and a router.

    b. The attacker uses a spoofing tool, to send out fake ARP responses. 
    
    c. The fake responses advertise that the correct MAC address for both IP addresses, belonging 
to the router and workstation, is the attacker’s MAC address. This fools both router and 
workstation to connect to the attacker’s machine, instead of to each other.
    
    d. The two devices update their ARP cache entries and from that point onwards, communicate 
with the attacker instead of directly with each other.
    
    e. The attacker is now secretly in the middle of all communications 
### ARP poisoning
#### demo

1) We will get the mac of our gateway

2) We will get our linux machine mac
    
    a) arp -g

3) Enable ip forward

    a) sudo sysctl net.ipv4.ip_forward=1

4) Start the spoofing with arpspoof tool

    a) Arpspoof -i interface -t target -r defaultgatewayip

- NOTE: 
    - ip of attacker: 192.168.1.8
    - Ip of victim: 192.168.1.3
    - gatewap : 192.168.1.1   
>>> After i started the arpspoof now the mac of the gateway is same with the attacker/kali machine. 
#### demo 

1) Install bettercap

2) Start bettecap

3) Scan the network
    
    a) net.probe on

    b) net.show => to see the network

4) Start arp spoofing

    a) set arp.spoof.targets <ip>

    b) arp.spoof on

5) Start Mitm
    
    a) net.sniff on

    b) net.sniff off 
### Prevention 
1. Using static ARP tables: manually setted

2. Switch security: some feature for ARP poisoning

3. Encryption: not for arp but in case of leaks 
### Simple python topro  

1) Write a program that accepts input from the user and check if the 
link is up or down.
    
    a) use os package/module

    b) os.popen("ping -n 1 google.com").read()
    
    c) This will tell you if 

    d) And try algorithm like searching from the result of the upper hint
        i) If (“hello world” or “best”) in “hello world is the best quote.”: -> on 
python this will work fine

e) Try to understand the difference between the result of down ping and 
up ping 