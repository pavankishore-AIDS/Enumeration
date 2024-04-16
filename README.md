# Enumeration
Enumeration Techniques

# Explore Google Hacking and Enumeration 

# AIM:

To use Google for gathering information and perform enumeration of targets

## STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various Google hacking keywords and enumeration tools as follows

### Step 3:
Open terminal and try execute some kali linux commands

## Pen Test Tools Categories:  

Following Categories of pen test tools are identified:
Information Gathering.

## Google Hacking:

Google hacking, also known as Google dorking, is a technique that involves using advanced operators to perform targeted searches on Google. These operators can be used to search for specific types of information, such as sensitive data that may have been inadvertently exposed on the web. Here are some advanced operators that can be used for Google hacking:

site: This operator allows you to search for pages that are within a specific website or domain. For example, "site:yahoo.com" would search for pages that are on the example.com domain.
Following searches for all the sites that is in the domain yahoo.com
## Output:
![322669974-63dc4188-e890-4aaf-83f0-189054dbb22c](https://github.com/pavankishore-AIDS/Enumeration/assets/94154941/ce736378-72aa-4e32-869c-c3267c36c4b9)




filetype: This operator allows you to search for files of a specific type. For example, "filetype:pdf" would search for all PDF files.
Following searches for pdf file in the domain yahoo.com

## Output:

![322670271-1b3f4a33-ff59-4cdf-bad1-0faeb174ff5e](https://github.com/pavankishore-AIDS/Enumeration/assets/94154941/a190373e-527f-4ab2-b337-4e8d33be4f2b)



intext: This operator allows you to search for pages that contain specific text within the body of the page. For example, "intext:password" would search for pages that contain the word "password" within the body of the page.


## Output:

![322670492-c7ce576f-ec52-4b91-a023-e9574249933a](https://github.com/pavankishore-AIDS/Enumeration/assets/94154941/009b9fa0-ecad-4d34-a4e4-a24f6f7901c7)



inurl: This operator allows you to search for pages that contain specific text within the URL. For example, "inurl:admin" would search for pages that contain the word "admin" within the URL.


## Output:

![322670906-4cbb5993-fed6-4b11-840c-0e09860f860f](https://github.com/pavankishore-AIDS/Enumeration/assets/94154941/1a8b92f4-e5ac-461c-9082-2b6bf842c7b5)



intitle: This operator allows you to search for pages that contain specific text within the title tag. For example, "intitle:index of" would search for pages that contain "index of" within the title tag.


## Output:

![322671240-acd14200-b395-47c4-acc6-043ca3932b70](https://github.com/pavankishore-AIDS/Enumeration/assets/94154941/0beb3a90-b8f5-41d8-8043-07ccd054c74c)



link: This operator allows you to search for pages that link to a specific URL. For example, "link:amazon.in" would search for pages that link to the example.com domain.


## Output:

![322671392-c04a1135-281b-4da2-bd39-c1b3f07ca8f6](https://github.com/pavankishore-AIDS/Enumeration/assets/94154941/36f18a78-a0c2-4c0d-a24c-36359465243a)




cache: This operator allows you to view the cached version of a page. For example, "cache:amazon.in" would show the cached version of the example.com website.


## Output:

![322671607-a80f0d0f-136e-4908-b5f2-eefdf33e7e52](https://github.com/pavankishore-AIDS/Enumeration/assets/94154941/283fbf37-819d-434c-851f-c09d7dba8b81)



 
## DNS Enumeration

DNS Recon
Provides the ability to perform:
Check all NS records for zone transfers
Enumerate general DNS records for a given domain (MX, SOA, NS, A, AAAA, SPF , TXT)
Perform common SRV Record Enumeration
Top level domain expansion

## Output:

![322683907-cb31b378-3e73-41ac-b8bc-118201acac79](https://github.com/pavankishore-AIDS/Enumeration/assets/94154941/c5bcc4de-81ea-476a-9b67-38ad7845bcc2)




![322683929-9c26e4b4-271d-48a5-a4d3-18b6574b7dcb](https://github.com/pavankishore-AIDS/Enumeration/assets/94154941/2d2eff93-62e3-420f-b195-678e2b4f0307)





## dnsenum

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


## Output:

![322683970-99591c96-6662-45b8-b080-84f1942db996](https://github.com/pavankishore-AIDS/Enumeration/assets/94154941/e48b5c4a-5e1a-4931-b8e8-7020c8ec734c)




## smtp-user-enum
Username guessing tool primarily for use against the default Solaris SMTP service. Can use either EXPN, VRFY or RCPT TO.

## Output:

![322684037-02b18009-ff3d-4d1b-83b9-dca67e8fa9df](https://github.com/pavankishore-AIDS/Enumeration/assets/94154941/a8e149c3-07d8-4310-8c07-86ac274f3f46)




In metasploit list all the usernames using head /etc/passwd or cat /etc/passwd:

![322684064-65f3df74-70fc-4f32-a003-259eb6884157](https://github.com/pavankishore-AIDS/Enumeration/assets/94154941/3cb75bc0-ba64-458c-bb4f-219d4e69d52d)





Select any username in the first column of the above file and check the same

![322684129-cc6837e1-c5ec-477a-b53a-14942ad74c8d](https://github.com/pavankishore-AIDS/Enumeration/assets/94154941/2b81e8eb-2bab-4e34-ab18-713c6714be62)




  
## nmap --script smtp-enum-users.nse <hostname>

The smtp-enum-users.nse script attempts to enumerate the users on a SMTP server by issuing the VRFY, EXPN or RCPT TO commands. The goal of this script is to discover all the user accounts in the remote system.


## Output:

![322684153-f4a07c04-af5e-4d82-b6c1-9c0983222206](https://github.com/pavankishore-AIDS/Enumeration/assets/94154941/7aa4e472-a3cc-4277-bd56-d3cef5ae4749)





## RESULT:
The Google hacking keywords and enumeration tools were identified and executed successfully
