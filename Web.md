# Web Application Penetration Testing

## Tools
- Burp Suite
- Nikto
- Dirbuster
- curl
- sublist3r
- nmap
- more...

## Overview
- Scanning & Enumeration & Information gathering & Reconnaissance
- Exploitation & Gaining access
- Maintaining access
- Cleanup

## Scanning & Enumeration & Information gathering & Reconnaissance
### Types
- Passive
- Active

### Workflow
- Target Validation
- Finding Subdomains
- Fingerprinting
- Data breaches

### Steps
- Ensure target exists by going to the site
- Use sublist3r or crt.sh to find subdomains to gain clues about the target
- Use burp to test the site and see the data that comes back in the target tab
- Use securityheader.io to find any issues with the headers if you see this in burp
- Find out what tech stack, hardware they use by using wappalyzer
- Find out more details about the target using nikto
- Find out more details about the target using nmap
- Use hunter.io to find email, user info for users at the target website
- Use ethical data breach sites to find out user info and relate that to target website

## Exploitation & Gaining access
### Cross site scripting / XSS Types
- Reflected XSS (AKA Non-Persistent or Type I)
- Stored XSS (AKA Persistent or Type II)
- DOM Based XSS (AKA Type-0)

### XSS prevention / exploitation steps
- Encoding
- Filtering
- Validation
- Sanitation

### UI Bypassing
- Exploiting browser inspection tools to manipulate UI/Javascript
- Exploit source page html or JS
- XSS payloads to bypass UI like form, search bars, etc.
- Inspect the element to see if the UI can be altered like text fields

### Cookies
- Need a secure flag
- Need the attribute HttpsOnly

### Broken Access Control
- Accessing other users info or activity 
- Accessing browser data like session storage, etc.
- Exploiting open data stored in the browser
- Modify api payload to perform an action with someone else's credentials
- Being able to intercept api data to the server with manipulated data

### SQLi
- [Overview](https://portswigger.net/web-security/sql-injection)
- An attack in which malicious SQL statements are injected into a SQL db
- SQL injection is easy to avoid, but still happens often
- If successful, we can read sensitive databases, extract information, modify databases and potentially even get a shell.
- Use the sqlmap tool to test all the different permutations and combinations
- Use the sleep command as a way to find out if the sql injection is working

### XXE
- Stands for XML External Entities. It means attacking systems that parse XML input
- We can abuse the system entity and get malicious
- Attacks include denial of service, local file disclosure, remote code execution and more
- Manipulating the api payload such as setting admin to true, etc


### Input validation
- Intercept api call and edit the payload
- Intercept api payload to set key, value pairs to what we want. Example is {isAdmin: true}
- Inputting invalid entries that do not do what they are intended to do. Example {quantity: -100}

## Maintaining access

## Cleanup

## Resources
### Juice Shop
  - [resource 1](https://github.com/bkimminich/juice-shop#setup)
  - [resource 2](https://bkimminich.gitbooks.io/pwning-owasp-juice-ship/content/)
### OWASP Testing Guides
  - [resource 1](https://www.owasp.org/images/1/19/OTGv4.pdf)
  - [resource 2](https://github.com/tanprathan/OWASP-Testing-Checklist)
### Bug Bounties
  - [resource 1](https://bugcrowd.com/)
  - [resource 2](https://hackerone.com/)
  - [resource 3](https://www.synack.com/red-team/)
  - [resource 4](https://www.guru99.com/bug-bounty-programs.html)
### Education
  - [resource 1](https://www.elearnsecurity.com/course/web_application_penetration_testing/)
  - [resource 2](https://porswigger.net/web-security)
  - [resource 3](https://www.giac.org/certification/web-application-penetration-tester-gwapt)
  - [resource 4](https://www.amazon.com/Web-Application-Hackers-Handbook-Exploiting/dp/1118026470)