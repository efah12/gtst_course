# Reconnaissance (Information Gathering )
## Recon / Information Gathering / Footprint /
- Information Gathering is 
Collecting data about some
network/host/system.
- Footprinting => Footstep + 
printing(logging)
- Most of the people find 
Footprinting boring, but it is 
a very important part of 
Ethical Hacking. And the 
next section will tell you   
## Why do we need recon?
- Imagine, You are going to rob a bank… what do you do?
    - Know How much polices are there in the bank
    - Know the doors in and out 
    - Know if there is cctv
    - Know which person is the CEO
    - Know which time is Good for robbery 
- To Get access on system 1st you have to know the 
system.
- Knowing the system will lead you to know if the system 
is vulnerable
## Types of information gathering
- Based on how we do the recon
    1) Active Footprinting

    2) Passive Footprinting
    
1)  Active Footprinting
This kind is when we try to gather information directly by contacting 
that person.
Example: 
- When you go to the bank and ask for some informations.
- Chatting with person on social media to know about them.
Doing Active Footprinting with our permission is ILLEGAL!!
2) Passive Footprinting
- This kind of recon is when you gather informations 
from another person,3rd party or by checking public 
sources.
- Example: 
    - To know the bank working time i can see the posted 
texts.
    - To know someone name by reading the username.
## What type of information do you gather? 
- We gather information for different things
a. host

    - Websites
    - Computers
    - Smart Phone
    
b. networks

    - Home Network
    - Companie networks

c. Person/Organization

d. Application
## How do we gather information?
- Gathering info is classified as we saw early.
- There for the techniques and methods we use can be 
little different.
- Let us see 1 by 1 
### A. Websites 
- The informations we gather about a websites are
    - IP Addresses
    - Development frameworks
        - Web server version.
        - Technologies used
    - Name
    - Domain registrations
#### To get ip
- To get ip address of some website:
    - Active recon
         - ping <website link>
        - nslookup <website link>
    - Passive recon
        - www.nslookup.io       
#### To get development frameworks
- Use simple browser extension 
    - Wapplyzer
- Terminal tool
    - whatweb
#### Details about domains
- For this you can use whois 
terminal +website tool
    - sudo apt install whois
    -  who.is    
### B. Computers/Phone
- The informations we gather about a 
Computers/Hosts are
    - IP Addresses
    - OS informations
    - HostName
    - MAC address
    - Open services or ports
- Demo on next class   
### C. networks
- The informations we gather about a Networks are
    - IP Addresses
    - Ports,Services
    - Class and Type of Network
    - Hosts on that Network
    - Strength and security of that Network  
### D. Personal Informations
- The informations we gather about a Persons are
    - Full Name
    - Address
        - Physical Address
        - All Social Media Address
        - Phone address
    - What the person loves
    - Job
    - Friends
    - Status
    - skills 
    - …
- Persons information can be gathered by active and 
passive.
- There are many methods:...
### Getting social medias Addresses
- If you have Full name of 
a person, Just use 
search 
engines(google,bing,yahoo)
- Also you can use tool called sherlock from github
### Getting Physical Addresses 
- Peoples leak there living 
place on social medias 
info page.
- Else there are many 
methods: 
    - Sending links and when people access the link u can get the iP then you can just geolocate the place.
### IP geolocation
- If you got the ip address of 
someone you can insert it to 
https://www.iplocation.net 
- The method of getting the 
IP might be tricky but detail 
we will see it on Social 
Engineering Class
### E. Applications/Softwares
- The informations we gather about a Applications 
are
    - What they are made up of
        - Which programming language used
        - Which framework used
    - Source codes
    - Their logic and Function
    - …
## Reverse image search
Reverse image search is a technique of searching with images.
We all search with text but we can search with images to This can give as more information
Ex: think like user posted a picture with a background of some area, if the user didnt talk about 
the place we can just search the image and the search engines will give as some similar photos 
where they are taken in same place(not 100% accurate) 
We can use:
- https://tineye.com/
- https://www.labnol.org/reverse/
- https://images.google.com/
## Google Dorking(Google Hacking Database)
- it's not hacking into Google servers!
- Google hacking is using different Google operators to 
effectively optimize search results.
- It also involves using Google to identify vulnerabilities
in websites.
- Results are highly customizable.
- THIS IS THE MOST POWERFUL SKILL OF HACKER!
### Basic operators
- For inclusion of something common (+) 
    - Nathan Hailu +geeztech +ceo
- Terms you want to exclude (-)
    - Anti-virus -software
    - Georgia -america -state
- • Search for an exact term (“)
    - “How to eat food” 
    - “Nathan Hailu” => what is the difference?
- ( * ) any word (wild card)
    - If you include * within a query, it tells Google to try to 
treat the star as a placeholder for any unknown 
term(s) and then find the best matches.
    - Estonia parliament voted on the * bill
- ( | ) boolean ‘OR’
    - “Nathan Hailu” | “Natan Hailu”   
### Advanced Operators
- These are Syntaxes used by Google.
    - intitle
        - Google returns results with the word/phrase found within the 
title of the page
- intitle:index.of
    - inurl 
        - Finds a specific term within the URL
- inurl:view/index.shtml
- filetype
        - Searches for a specific filetype
- “Hacking” filetype:pdf
- filetype:txt
    - Intext
        - Google returns links that contains Texts from that link
- intext:”Hackers in Ethiopia”   
### Mixing Operators
- Inurl:securethiscompany.com 
intitle:index.of
- "mysql dump" Inurl: filetype:sql 
intext:password
- inurl:ftp "password" filetype:xls
- intitle:admin intitle:login
- intitle:phpMyAdmin “Welcome to 
phpMyAdmin ***” “running on * as 
root@*”    
## Hackers Power
- Hackers do anything with these operators
- When they Got errors or any problems they use the 
operators and other.
- Further on google dorking
    - https://www.exploit-db.com/google-hacking-dat
abase
