# Explore Google hacking and enumeration 

# AIM:

To use Google for gathering information and perform enumeration of targets

## STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various Google hacking keywords and enumeration tools as follows:


### Step 3:
Open terminal and try execute some kali linux commands

## Pen Test Tools Categories:  

Following Categories of pen test tools are identified:
Information Gathering.

Google Hacking:

Google hacking, also known as Google dorking, is a technique that involves using advanced operators to perform targeted searches on Google. These operators can be used to search for specific types of information, such as sensitive data that may have been inadvertently exposed on the web. Here are some advanced operators that can be used for Google hacking:

site: This operator allows you to search for pages that are within a specific website or domain. For example, "site:example.com" would search for pages that are on the example.com domain.
Following searches for all the sites that is in the domain yahoo.com

![image](https://github.com/Hariharan-061102/Enumeration/assets/93427270/924942f8-3bac-4d7f-9e66-25a216c781a0)

filetype: This operator allows you to search for files of a specific type. For example, "filetype:pdf" would search for all PDF files.
Following searches for pdf file in the domain yahoo.com

![image](https://github.com/Hariharan-061102/Enumeration/assets/93427270/94d5a3c3-752b-4e44-a5c1-279e60c58c12)

intext: This operator allows you to search for pages that contain specific text within the body of the page. For example, "intext:password" would search for pages that contain the word "password" within the body of the page.
![image](https://github.com/Hariharan-061102/Enumeration/assets/93427270/23452fa1-e224-4202-b948-555904b41c97)

inurl: This operator allows you to search for pages that contain specific text within the URL. For example, "inurl:admin" would search for pages that contain the word "admin" within the URL.
![image](https://github.com/Hariharan-061102/Enumeration/assets/93427270/ec397d49-2e9e-4819-9f7f-9e19bfc5975f)

intitle: This operator allows you to search for pages that contain specific text within the title tag. For example, "intitle:index of" would search for pages that contain "index of" within the title tag.
![image](https://github.com/Hariharan-061102/Enumeration/assets/93427270/d2f2d985-edaa-4602-867f-f43b8be7deb5)

link: This operator allows you to search for pages that link to a specific URL. For example, "link:example.com" would search for pages that link to the example.com domain.
![image](https://github.com/Hariharan-061102/Enumeration/assets/93427270/4541325a-afa8-4246-98b9-6c4a96ae1fa3)

cache: This operator allows you to view the cached version of a page. For example, "cache:example.com" would show the cached version of the example.com website.
![image](https://github.com/Hariharan-061102/Enumeration/assets/93427270/55597f22-dd3f-4e6d-99b0-4e884a7f159d)

 
## DNS Enumeration


### DNS Recon
provides the ability to perform:
Check all NS records for zone transfers
Enumerate general DNS records for a given domain (MX, SOA, NS, A, AAAA, SPF , TXT)
Perform common SRV Record Enumeration
Top level domain expansion

## OUTPUT:
![image](https://github.com/Hariharan-061102/Enumeration/assets/93427270/915eddf7-336b-4f0c-983c-220cf4d898fc)



### dnsenum
Dnsenum is a multithreaded perl script to enumerate DNS information of a domain and to discover non-contiguous ip blocks. The main purpose of Dnsenum is to gather as much information as possible about a domain. The program currently performs the following operations:

Get the host’s addresses (A record).
Get the namservers (threaded).
Get the MX record (threaded).
Perform axfr queries on nameservers and get BIND versions(threaded).
Get extra names and subdomains via google scraping (google query = “allinurl: -www site:domain”).
Brute force subdomains from file, can also perform recursion on subdomain that have NS records (all threaded).
Calculate C class domain network ranges and perform whois queries on them (threaded).
Perform reverse lookups on netranges (C class or/and whois netranges) (threaded).
Write to domain_ips.txt file ip-blocks.
This program is useful for pentesters, ethical hackers and forensics experts. It also can be used for security tests.

![image](https://github.com/Hariharan-061102/Enumeration/assets/93427270/b4b2eefe-41f4-4a31-8054-5f2f59abe6cf)


## smtp-user-enum
Username guessing tool primarily for use against the default Solaris SMTP service. Can use either EXPN, VRFY or RCPT TO.
![image](https://github.com/Hariharan-061102/Enumeration/assets/93427270/73dbf24d-0da9-4063-9a4b-0f8dc3b8e5da)


In metasploit list all the usernames using head /etc/passwd or cat /etc/passwd:
![image](https://github.com/Hariharan-061102/Enumeration/assets/93427270/0d24fa55-e177-4b1f-9cbc-7056af4a311a)

select any username in the first column of the above file and check the same
![image](https://github.com/Hariharan-061102/Enumeration/assets/93427270/1ba38355-f6f0-47c0-b6c5-0471bbdfa536)


## Telnet for smtp enumeration
Telnet allows to connect to remote host based on the port no. For smtp port no is 25
telnet <host address> 25 to connect
and issue appropriate commands

![image](https://github.com/Hariharan-061102/Enumeration/assets/93427270/180b44ca-5324-4ede-94d7-cec1de342ee9)


```
nmap –script smtp-enum-users.nse <hostname>
```
The smtp-enum-users.nse script attempts to enumerate the users on a SMTP server by issuing the VRFY, EXPN or RCPT TO commands. The goal of this script is to discover all the user accounts in the remote system.

![image](https://github.com/Hariharan-061102/Enumeration/assets/93427270/7e50ce53-0504-47c5-a673-9d5b9a35a8b3)


## RESULT:
The kali linux tools were identified successfully
