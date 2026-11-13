# NETWORKWALKSSERGIOPAENDONG-B084-WK2-PM2-OSINT-GOOGLE-DORKING
PENETRATION TESTING REPORT
FOOTPRINTING & NETWORK SCANNING PHASES
W2-PM-FINAL | CYBERSECURITY |  NETWORKWALKS

Pentester Name
(Cybersecurity Professional)	Sergio Paendong
Program/Batch	B084-Networkwalks
Date	12 November 2026
Modules completed	W2-PM2 (Google Dorking GHDB)
Client/Target	Networkwalks (secured written permission already)
Permission secured from client?	Yes
Phases covered	Phase 1: Reconnaissance & Footprinting




1. Liability Disclaimer
I have performed these activities only on the systems & devices where I had secured written permission or the devices/systems that I own myself. All these materials are for education and research purpose only. Do not use anything from here to break the law. The instructor, the authors and Networkwalks are not responsible for what you do with this knowledge. Every action you take is your own responsibility. Misuse can lead to criminal charges, heavy fines, loss of your job and a permanent record. In most countries unauthorised access is a crime even when nothing is damaged.
 
2. Introduction
This report covers reconnaissance and footprinting of the networkwalks.com domain using Google Dorking via the Google Hacking Database (GHDB) for W2-PM2. One module covers the footprinting and search phase using GHDB, and the other covers the network scanning phase. Together, they demonstrate how an attacker moves from passive open-source intelligence (OSINT) gathering to active mapping of live hosts on a network. It is the Week 2 part of my ongoing internship program at Networkwalks. 

3. Tools Used
The table below lists each tool used in this report and its purpose.
Tool	Purpose
DHGB	Repository of advanced Google search queries used to find exposed files, directories, and sensitive data.
Exploit-db	Platform hosting the Google Hacking Database (GHDB) and documented vulnerabilities for security research.
intitle:" " -com	Search operator used to locate open directory listings or specific page titles while excluding standard .com domains.
intitle:"Index of" "DCIM/camera"	Google Dork query used to identify exposed open web directories containing unauthenticated camera and image files.

4. Activities Performed
4.1 Footprinting & Reconnaissance

I performed passive reconnaissance and information gathering using the Google Hacking Database (GHDB) hosted on Exploit-DB. By utilizing advanced Google search operators ("Google Dorks"), I searched for publicly indexed directories, exposed media files, and misconfigured web servers without directly probing or interacting with the target systems.

First, I accessed the Exploit-DB platform to browse the GHDB repository and select verified search queries categorized under sensitive directories and exposed files. This provided ready-to-use dork syntax designed to uncover unintended public disclosures.

Next, I used the search operator intitle:" " -com in Google Search to filter for specific page titles while excluding standard .com domains. This helped narrow down search results to open index pages and non-commercial servers that often lack strict access controls.

Finally, I executed the GHDB query intitle:"Index of" "DCIM/camera". The results identified publicly accessible web directories containing unauthenticated camera folders and personal media files, demonstrating how improper server permissions allow search engines to index private data.



 
5. Risk Analysis / Impact
Based on the information collected during the footprinting and network scanning activities, I identified the following potential risks.
	Risk / Finding	Evidence / Observation	Potential Impact	Risk Level
1	Exposed public webcams	GHDB dorks (e.g., intitle:"webcamXP") identified unauthenticated live webcams	Unauthorized surveillance and viewing of private physical environments	● Medium
2	Open directories with sensitive media	Dorks like intitle:"Index of" "DCIM/camera" revealed exposed camera folders	Unintended public disclosure of personal photos, videos, and local files	● Medium
3	Exposed device management portals	Search queries uncovered open administrative interfaces and web server ports (e.g., port 8080)	Attackers can interact with management interfaces and attempt further exploitation	● Medium
4	Default or hardcoded credentials	Discovered devices (such as NoVus IP cameras) exposing default login credentials (Root/1234)	Full administrative takeover and compromise of the affected hardware device	● High
5	Internal network topology disclosure	Directory listings and device naming conventions exposed internal routing and naming structures	Assists attackers in mapping organizational layouts before targeted attacks	● Medium
6	Search engine indexing vulnerabilities	Sensitive configurations and files indexed publicly by web crawlers due to missing robots.txt or proper access controls	Allows attackers to bypass network perimeters entirely using passive OSINT	● Medium

Risk level key:  ● Critical  ● Medium  ● Low
The risks above are observations from the footprinting and scanning exercises, not confirmed vulnerabilities.
The practical exercises primarily involved information gathering and host discovery. No exploitation or vulnerability validation was performed as part of these two modules.
Therefore, the presence of information such as a software version, IP address or DNS record does not by itself mean that the system is vulnerable. Further authorized security testing would be required to confirm any actual vulnerability.

6. Recommendations
Based on the observations from these Google Dorking and OSINT activities, I recommend the following security improvements:

1.	Monitor and restrict indexed search engine content
Organizations should use proper robots.txt configurations and meta tags to prevent sensitive directories, configuration files, and private endpoints from being indexed by web crawlers.
2.	Secure open web directories
Disable directory listing/indexing (Options -Indexes) on web servers to prevent the public exposure of internal media directories, camera files, and system paths.
3.	Strengthen authentication on connected hardware
Ensure all IP cameras, routers, and IoT devices behind web interfaces require strong, unique credentials instead of relying on default or hardcoded factory passwords.
4.	Audit publicly exposed administration portals
Move administrative management interfaces and service ports (such as port 8080) behind a secure VPN or restrict access to trusted internal IP ranges.
5.	Perform regular OSINT and dorking audits
Conduct routine passive reconnaissance and Google Dork checks to verify whether sensitive organizational data, logs, or backups have leaked into public search engine indexes.
6.	Implement strict access controls on media assets
Ensure user uploads, camera storage directories (such as DCIM/camera), and file archives enforce proper authentication checks before serving content.
7.	Remove sensitive configuration backups
Regularly scan web root directories for leftover backup archives, configuration notes, or text snippets that could be discovered via advanced search queries.
8.	Educate staff on digital footprint exposure
Train personnel on the risks of exposing internal infrastructure details, file structures, or server paths that can be leveraged during passive reconnaissance.
9.	Perform security testing with authorization
Reconnaissance, dorking, and vulnerability assessments should only be performed against systems and networks where explicit authorization has been granted. 

7. Conclusion
During Week 2 of my Cybersecurity & Ethical Hacking internship, I completed practical activities covering passive reconnaissance, footprinting, and Google Dorking using the Google Hacking Database (GHDB).
In the footprinting activity, I used advanced Google search operators and GHDB queries to discover exposed webcams, open directories, sensitive media files, and insecure administrative portals without directly interacting with the target systems. I learned how search engine indexing and improper access controls can inadvertently expose private information and system vulnerabilities to the public.
In the analysis component, I documented potential attack surfaces and evaluated risks associated with hardcoded credentials and configuration disclosures. Overall, this module demonstrated how attackers leverage passive OSINT and search queries for intelligence gathering before conducting active attacks.
The exercises showed me that passive information gathering is a critical part of cybersecurity. Even before attempting to interact with or exploit a target system, a security professional can uncover a significant amount of sensitive data simply by analyzing what search engines have publicly indexed. 
I also learned that technical findings must be documented clearly. A strong cybersecurity report should explain the exact search query or method used, what was discovered, what the exposure means, the severity of the risk it creates, and what steps can be taken to remediate it. 
Finally, I learned that reconnaissance and OSINT gathering must always be conducted ethically and within an authorized scope. These activities were completed strictly as part of the assigned educational cybersecurity lab.



-End-


👤 Author
Sergio Paendong
Cybersecurity Professional B084
LinkedIn: www.linkedin.com/in/sergio-paendong
________________________________________
📌 Project Information
Program Name: Cybersecurity program at Networkwalks | Week: 02 | Repository: GitHub

