Task 1 - 
Learned about nmap, furthur investigaton required.
Edit 1- 
   1.  nmap 14.139.34.0/24
      Output-
        Starting Nmap 7.01 ( https://nmap.org ) at 2018-02-01 19:49 IST
        Warning: 14.139.34.10 giving up on port because retransmission cap hit (10).
      The command ran for some time but sort of timed-out without giving any results.
   2. nmap -F 14.139.34.0/24
        "-F (Fast (limited port) scan) .
             Specifies that you wish to scan fewer ports than the default.
             Normally Nmap scans the most common 1,000 ports for each scanned
             protocol. With -F, this is reduced to 100."(From the man page of nmap).
      It showed ports of 9 hosts in 14 seconds
      "Nmap done: 256 IP addresses (9 hosts up) scanned in 14.32 seconds"
    3. sudo nmap -F -O 14.139.34.0/24
          The '-O' is to find the OS on the systems.
          It showed the ports all ips in 14.139.34.0/24 and guessed their OS.OS fingerprint was not ideal in most cases due       to various resoans.
          "Nmap done: 256 IP addresses (256 hosts up) scanned in 668.06 seconds".
          
          Will keep diiging...
          
      
   



Task 2 - It was bought on http://www.ernet.in
  
  How did I find it-
  Used WHOIS to find about the website.  
  
  Resources - 
  http://whois.domaintools.com/iitmandi.ac.in - Gave information about IP, DNS, Domain Registrar etc.
  http://www.ernet.in/domain.html - Confirmed that ERNET India has been appointed as an exclusive domain registrar of domains like ac.in.
  https://www.quora.com/How-do-I-find-the-ownership-history-of-a-domain-without-paying-a-fee
  https://www.sslshopper.com/ssl-checker.html#hostname=https://students.iitmandi.ac.in/
  
  What I learned-
  1. WHOIS can be use to get information about websites.
  2. About Domain registars
  3. SSL Client Certificate to student.iitmandi.ac.in was given by GoDaddy.com, Inc.(and it expires in DEC-19 :P)
  

Task 3 - DuckDuckGo owns ZERO data-centres, it runs on 4 AWS datacenters (California, Virginia, Singapore, Ireland).
  Resources -
  http://highscalability.com/blog/2013/1/28/duckduckgo-architecture-1-million-deep-searches-a-day-and-gr.html
  https://duck.co/help/company/architecture 

