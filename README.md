CIA - TRAID
 > C - CONFIDENTIALITY
 > I - INTERGRITY
 > A - AVAILABILITY

1. **CONFIDENTIALITY**: CONFIDENTIALITY MEANS **ONLY AUTHORIZED USERS CAN ACCESS DATA**
  > **EXAMPLE** : BANK LOGIN SYSTEM

2. **INTEGRITY** : INTEGRITY MEANS **DATA SHOULD NOT BE MODIFIED WITHOUT PERMISSION**
  > **EXAMPLE** : ONLINE EXAM RESULTS SHOULD NOT CHANGE
              SOFTWARE FILE SHOULD NOT BE TAMPERED

3. **AVAILABILITY** : AVAILABILITY MEANS **SYSTEMS AND DATA MUST BE ACCESSIBLE WHEN NEEDED**
 > **EXAMPLE** : COLLEGE WEBSITE DURING RESULTS TIME



1. **WHAT IS A NETWORK ?**
        A NETWORK IS A 'COLLECTION OF CONNECTED DEVICES' THAT CAN **COMMUNICATE**

2. **WHAT IS A NODE ?**
        A NODE IS 'ANY DEVICE CONNECTED' TO A **NETWORK**
        -> **EVERY DEVICE INSIDE A NETWORK = NODE**

3. **WHAT IS A HOST ?**
        A HOST IS 'A NODE THAT HAS AN IP ADDRESSS' AND CAN **SEND / RECEIVE DATA**

4. **WHAT IS CLIENT ?**
       A CLIENT IS **A DEVICE OR SOFTWARE** THAT 'REQUESTS DATA'

5. **WHAT IS SERVER ?**
       A SERVER IS 'A POWERFUL COMPUTER' THAT **PROVIDES SERVICES / DATA**
       -> SERVER WAITS FOR **CLIENT REQUEST AND RESPONDS**

6. **WHAT IS PROTOCOL ?**
       A PROTOCO IS 'A RULE THAT DEFINES HOW COMMUNICATION HAPPENS' .
       -> LIKE,
             **HTTP/HTTPS -> WEB COMMUNICATION
             TCP        -> RELIABLE DATA TRANSFER
             DNS        -> CONVERTS DOMAIN TO IP**
    > WITHOUT PROTOCOL -> DEVICES CANNOT UNDERSTAND EACH OTHER

7. **WHAT IS PACKET ?**
       A PACKET IS 'A SMALL UNIT OF DATA SENT OVER NETWORK' . LARGE DATA IS **BROKEN INTO SMALL PACKETS** .


    **BACKEND PROCESS**

   **STEP 1** : JUST TYPE EXAMPLE.COM
         **BROWSER = CLIENT**

   **SETP 2** : DNS PROCESS
       NOW **BROWSER ASK DNS SERVER** :
          **WHAT IS THE IP OF EXAMPLE.COM ?**
       AT NOW DNS REPLIES :
          **FOR EXAMPLE : 93.184.216.34**

   **STEP 3** : TCP CONNECTION
        AND NOW CLIENT CREATES CONNECTION USING THE **TCP PROTOCOL OR DESTINATION OF IP**

   **STEP 4** : HTTP REQUEST
   
   **STEP 5** : PACKET FORMATION
       AT NOW MY REQUEST IS BROKEN INTO :
       > MULTIPLE PACKETS
       > TRAVEL THROUGH INTERNET

   **STEP 6** : SERVER RECEIVES
       > **THE SERVER AT IP RECEIVES PACKETS
       > REASSEMBLES THEM
       > PROCESSES REQUEST**

   **STEP 7** : SERVER RESPONSES
       AT NOW SERVER SENDS :
       > **HTML
       > CSS
       > JS**

   **STEP 8** : BROWSER RENDERS
      > CLIRENT RECEIVES PACKETS
      > REBULIDS DATA
      > DISPLAYS WEBPAGE

                                        **NETWORKS**
   
   1. **WHAT IS LOOPBACK ?**
        A LOOPBACK ADDRESS IS A **SPECIAL IP ADDRESS** USED BY A DEVICE TO COMMUNICATE **WITH ITSELF**
           > ITS USED FOR
              1. TESTING
              2. CHECKING NETWORK STACK
      LOOPBACK ADDRESS (IPV4)
        > 127.0.0.1
      ITS AN ENTIRE RANGE IS : 127.0.0.0 - 127.255.255.255
      MOSTLY IT IS : 127.0.0.1
      FOR EXAMPLE:
      > IF I TYPE : ping 127.0.0.1 means
         I AM TESTING : TCP/IP NETWORKING

   2.**WHAT IS SUBNET MASK** ?
       WHICH PART OF AN IP ADDRESS BELONGS TO NETWORK , WHICH PART BELONGS TO HOST.
     IP STRUCTURE :
        EXAMPLE : 192.168.1.10  -> IT HAS NETWORK PORTION
                                -> NOST PORTION
     SUBNET MASK NOE TELL THATT WHERE TO SPLIT

    **EXAMPLE FOR SUBNET MASK :**
      255.255.255.0
    **ITS IN BINARY :**
      11111111.11111111.11111111.00000000
      IN THAT 1 IS NETWORK
              0 IS HOST
    192.168.1 | .10
    NETWORK      HOST

    **3. WHAT IS SUBNETTING ?**
         DIVIDING A LARGE NETWORK INTO SMALLER NETWORKS FOR BETTER SECURITY AND ALSO LESS TRAFFIC

       FOR EXAMPLE: 192.168.1.0
       SUBNET MASK : 255.255.255.0
       THIS WILL ALLOWS : 192.168.1.1 - 192.168.1.254
           NOW TOTAL USABLE HOST = 254

       INSTEAD OF THAT WRITTING -> 255.255.255.0
                       WE WRITE -> /24
          BECAUSE 24 BITS ARE 1
       FOR EXAMPLE : /8 = 255.0.0.0
                     /16 = 255.255.0.0
                     /24 = 255.255.255.0              

   **PRACTICAL SESSION**
   1. websites to choose
      testphp.vulnweb.com
      scanme.nmap.org
      hackthissite.org
       example.com
What subdomains did you discover?
**COMMAND :**
       sublist3r -d hackthissite.org
**OUTPUT :**
              ____        _     _ _     _   _____
                / ___| _   _| |__ | (_)___| |_|___ / _ __
                \___ \| | | | '_ \| | / __| __| |_ \| '__|
                 ___) | |_| | |_) | | \__ \ |_ ___) | |
                |____/ \__,_|_.__/|_|_|___/\__|____/|_|

                # Coded By Ahmed Aboul-Ela - @aboul3la
    
[-] Enumerating subdomains now for hackthissite.org
[-] Searching now in Baidu..
[-] Searching now in Yahoo..
[-] Searching now in Google..
[-] Searching now in Bing..
[-] Searching now in Ask..
[-] Searching now in Netcraft..
[-] Searching now in DNSdumpster..
[-] Searching now in Virustotal..
[-] Searching now in ThreatCrowd..
[-] Searching now in SSL Certificates..
[-] Searching now in PassiveDNS..
[!] Error: Virustotal probably now is blocking our requests
[!] DNSDumpster module failed: Could not find CSRF token on DNSDumpster page
[-] Total Unique Subdomains Found: 21
www.hackthissite.org
ctf.hackthissite.org
email.hackthissite.org
h5ai.hackthissite.org
irc.hackthissite.org
www.irc.hackthissite.org
lille.irc.hackthissite.org
wolf.irc.hackthissite.org
irc-ipv6.hackthissite.org
irc-v6.hackthissite.org
lille.irc-v6.hackthissite.org
wolf.irc-v6.hackthissite.org
irc-wolf.hackthissite.org
legal.hackthissite.org
mail.hackthissite.org
mirror.hackthissite.org
mta-sts.hackthissite.org
new-irc.hackthissite.org
psrp.hackthissite.org
status.hackthissite.org
status-new.hackthissite.org

-> 2. Which DNS record type revealed them?
   **IMPORTANT DNS RECORDS :**
   **RECORD**      **MEANING**
       A             IP address
       MX            Mail server
       NS            Nmae Server
       CNAME         Alias
  **COMMAND :**
    dig hackthissite.org 
   **OUTPUT :**
    <<>> DiG 9.20.15-2-Debian <<>> hackthissite.org
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 32478
;; flags: qr rd ra; QUERY: 1, ANSWER: 5, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 512
;; QUESTION SECTION:
;hackthissite.org.		IN	A

;; ANSWER SECTION:
hackthissite.org.	600	IN	A	137.74.187.101
hackthissite.org.	600	IN	A	137.74.187.104
hackthissite.org.	600	IN	A	137.74.187.102
hackthissite.org.	600	IN	A	137.74.187.100
hackthissite.org.	600	IN	A	137.74.187.103

;; Query time: 2196 msec
;; SERVER: 106.51.156.186#53(106.51.156.186) (UDP)
;; WHEN: Sat Mar 14 04:38:40 EDT 2026
;; MSG SIZE  rcvd: 125

-> 3. How many email addresses were discovered?
USE theharvester
**COMMAND** :
theHarvester -d hackthissite.org -b all
**OUTPUT:**
Read proxies.yaml from /etc/theHarvester/proxies.yaml
*******************************************************************
*  _   _                                            _             *
* | |_| |__   ___    /\  /\__ _ _ ____   _____  ___| |_ ___ _ __  *
* | __|  _ \ / _ \  / /_/ / _` | '__\ \ / / _ \/ __| __/ _ \ '__| *
* | |_| | | |  __/ / __  / (_| | |   \ V /  __/\__ \ ||  __/ |    *
*  \__|_| |_|\___| \/ /_/ \__,_|_|    \_/ \___||___/\__\___|_|    *
*                                                                 *
* theHarvester 4.8.2                                              *
* Coded by Christian Martorella                                   *
* Edge-Security Research                                          *
* cmartorella@edge-security.com                                   *
*                                                                 *
*******************************************************************

[*] Target: hackthissite.org 

Read api-keys.yaml from /etc/theHarvester/api-keys.ya

*] ASNS found: 1
--------------------
AS16276

[*] Interesting Urls found: 5
--------------------
https://hackthissite.org/
https://www.hackthissite.org/
https://www.hackthissite.org/missions/basic/11/
https://www.hackthissite.org/missions/basic/4/
https://www.hackthissite.org/user/view/unitedairlinesreservations

[*] No LinkedIn users found.



[*] LinkedIn Links found: 0
---------------------

[*] IPs found: 5
-------------------
137.74.187.100
137.74.187.101
137.74.187.102
137.74.187.103
137.74.187.104

[*] Emails found: 2
----------------------
sam@hackthissite.org
zine@hackthissite.org

[*] No people found.

[*] Hosts found: 175
---------------------
*.hackthissite.org
0-v3dev-cdn.hackthissite.org
0-v3dev-cdn.hackthissite.org:v3dev.hackthissite.org
0-v3dev-cdno.hackthissite.org
0-v3stage-cdn.hackthissite.org
0-v3stage-cdn.hackthissite.org:v3stage-cdn.hackthissite.org
0-v3stage-cdnk.hackthissite.org
1-v3dev-cdn.hackthissite.org
1-v3dev-cdn.hackthissite.org:v3dev.hackthissite.org
1-v3dev-cdnm.hackthissite.org
1-v3stage-cdn.hackthissite.org
1-v3stage-cdn.hackthissite.org:v3stage-cdn.hackthissite.org
1-v3stage-cdng.hackthissite.org
2-v3dev-cdn.hackthissite.org
2-v3dev-cdn.hackthissite.org:v3dev.hackthissite.org
2-v3dev-cdni.hackthissite.org
2-v3stage-cdn.hackthissite.org
2-v3stage-cdn.hackthissite.org:v3stage-cdn.hackthissite.org
2-v3stage-cdnc.hackthissite.org
3-v3dev-cdn.hackthissite.org
3-v3dev-cdn.hackthissite.org:v3dev.hackthissite.org
3-v3dev-cdns.hackthissite.org
3-v3stage-cdn.hackthissite.org
3-v3stage-cdn.hackthissite.org:v3stage-cdn.hackthissite.org
3-v3stage-cdne.hackthissite.org
4-v3dev-cdn.hackthissite.org
4-v3dev-cdn.hackthissite.org:v3dev.hackthissite.org
4-v3stage-cdn.hackthissite.org
4-v3stage-cdn.hackthissite.org:v3stage-cdn.hackthissite.org
4-v3stage-cdng.hackthissite.org
admin.hackthissite.org
admink.hackthissite.org
api.hackthissite.org
api.hackthissite.org:137.74.187.115
api.hackthissite.org:137.74.187.116
api.hackthissite.org:137.74.187.117
api.hackthissite.org:137.74.187.118
api.hackthissite.org:137.74.187.119
api.hackthissite.org:2001:41d0:8:ccd8:137:74:187:115
api.hackthissite.org:2001:41d0:8:ccd8:137:74:187:116
api.hackthissite.org:2001:41d0:8:ccd8:137:74:187:117
api.hackthissite.org:2001:41d0:8:ccd8:137:74:187:118
api.hackthissite.org:2001:41d0:8:ccd8:137:74:187:119
ctf.hackthissite.org
ctf.hackthissite.org:185.199.108.153
ctf.hackthissite.org:hackthissite.github.io
ctfg.hackthissite.org
daemon.hackthissite.org
daemon.hackthissite.org:70.85.54.213
data.hackthissite.org
dataa.hackthissite.org
dns.hackthissite.org
dnse.hackthissite.org
email.hackthissite.org
email.hackthissite.org:172.239.57.117
firewall.hackthissite.org
forum.hackthissite.org
forum.hackthissite.org:hackthissite.org
forumi.hackthissite.org
forums.hackthissite.org
forums.hackthissite.org:137.74.187.100
forums.hackthissite.org:hackthissite.org
git.hackthissite.org
git.hackthissite.org:137.74.187.145
git.hackthissite.org:2001:41d0:8:ccd8:137:74:187:145
gite.hackthissite.org
h5ai.hackthissite.org
h5ai.hackthissite.org:185.199.111.153
hp.hackthissite.org
hp.hackthissite.org:137.74.187.100
htsv4.hackthissite.org
htsv4.hackthissite.org:207.210.114.49
htsv4m.hackthissite.org
hub.irc.hackthissite.org:irc-hub.hackthissite.org
irc-hub.hackthissite.org
irc-hub.hackthissite.org:198.148.81.169
irc-hub.hackthissite.org:2610:150:8007:0:198:148:81:169
irc-ipv6.hackthissite.org
irc-lille.hackthissite.org
irc-lille.hackthissite.org:lille.irc.hackthissite.org
irc-lillee.hackthissite.org
irc-v6.hackthissite.org
irc-wolf.hackthissite.org
irc-wolf.hackthissite.org:185.24.222.13
irc-wolf.hackthissite.org:2a02:2770:9:0:21a:4aff:fe68:f705
irc-wolf.hackthissite.org:::
irc.hackthissite.org
irc.hackthissite.org:137.74.187.150
irc.hackthissite.org:185.24.222.13
irc.hackthissite.org:2a02:2770:9:0:21a:4aff:fe68:f705
ircg.hackthissite.org
jupiter.hackthissite.org:70.85.54.212
kagee.hackthissite.org
legal.hackthissite.org
legal.hackthissite.org:137.74.187.137
legal.hackthissite.org:137.74.187.138
legal.hackthissite.org:2001:41d0:8:ccd8:137:74:187:137
legal.hackthissite.org:2001:41d0:8:ccd8:137:74:187:138
legals.hackthissite.org
lille.irc-v6.hackthissite.org
lille.irc.hackthissite.org
lille.irc.hackthissite.org:137.74.187.150
lille.irc.hackthissite.org:137.74.187.151
lille.irc.hackthissite.org:137.74.187.152
lille.irc.hackthissite.org:2001:41d0:8:ccd8:0:1:bad:1dea
lille.irc.hackthissite.org:2001:41d0:8:ccd8:0:a:bad:1dea
lille.irc.hackthissite.org:2001:41d0:8:ccd8::bad:1dea
lille.irc.hackthissite.org:64:ff9b::894a:bb96
lille.irc.hackthissite.org:64:ff9b::894a:bb97
lille.irc.hackthissite.org:64:ff9b::894a:bb98
lilleo.irc.hackthissite.org
lilles.irc-v6.hackthissite.org
mail.hackthissite.org
mail.hackthissite.org:207.210.114.47
mailg.hackthissite.org
mirror.hackthissite.org
mirror.hackthissite.org:137.74.187.133
mirror.hackthissite.org:137.74.187.134
mirror.hackthissite.org:2001:41d0:8:ccd8:137:74:187:133
mirror.hackthissite.org:2001:41d0:8:ccd8:137:74:187:134
ns1k.hackthissite.org
ns2.hackthissite.org
paste.hackthissite.org
pastec.hackthissite.org
pbxe.hackthissite.org
pi.hackthissite.org:137.74.187.123
pii.hackthissite.org
psrp.hackthissite.org
psrp.hackthissite.org:172.239.57.117
qdb.hackthissite.org:137.74.187.153
qdbs.hackthissite.org
radio.hackthissite.org
radioc.hackthissite.org
shadow.hackthissite.org
shadow.hackthissite.org:207.210.114.45
speedtest.hackthissite.org
speedtest1.hackthissite.org
speedtest2g.hackthissite.org
speedtestc.hackthissite.org
staff.hackthissite.org
staff.hackthissite.org:137.74.187.146
staffc.hackthissite.org
stats.hackthissite.org:137.74.187.135
stats.hackthissite.org:137.74.187.136
stats.hackthissite.org:2001:41d0:8:ccd8:137:74:187:135
stats.hackthissite.org:2001:41d0:8:ccd8:137:74:187:136
statsi.hackthissite.org
status-newo.hackthissite.org
status.hackthissite.org
status.hackthissite.org:81.4.127.167
status.hackthissite.org:89.106.200.1
status.hackthissite.org:edge.redirect.pizza
v3dev-cdn.hackthissite.org
v3dev-cdn.hackthissite.org:v3dev.hackthissite.org
v3dev-cdne.hackthissite.org
v3dev.hackthissite.org
v3dev.hackthissite.org:198.148.81.145
v3dev.hackthissite.org:2610:150:8007:0:198:148:81:145
v3dev.hackthissite.org:64:ff9b::c694:5191
v3stage-cdn.hackthissite.org:198.148.81.146
v3stage-cdn.hackthissite.org:2610:150:8007:0:198:148:81:146
v3stage-cdnc.hackthissite.org
v3stage.hackthissite.org
v3stage.hackthissite.org:198.148.81.147
v3stage.hackthissite.org:2610:150:8007:0:198:148:81:147
vm-005.outbound.firewall.hackthissite.org:137.74.187.154
vm-099.outbound.firewall.hackthissite.org:137.74.187.159
vm-150.outbound.firewall.hackthissite.org:137.74.187.158
vm-200.outbound.firewall.hackthissite.org:137.74.187.157
wolf.irc-v6.hackthissite.org
wolf.irc.hackthissite.org
wolf.irc.hackthissite.org:185.24.222.13
wolf.irc.hackthissite.org:2a02:2770:9:0:21a:4aff:fe68:f705
wolfo.irc-v6.hackthissite.org
wwwc.hackthissite.org

-> 4. How many devices are active?
**COMMAND :**
 nmap hackthissite.org
**OUTPUT :**
Starting Nmap 7.95 ( https://nmap.org ) at 2026-03-14 04:41 EDT
Nmap scan report for hackthissite.org (137.74.187.100)
Host is up (0.20s latency).
Other addresses for hackthissite.org (not scanned): 137.74.187.103 137.74.187.101 137.74.187.104 137.74.187.102
Not shown: 997 filtered tcp ports (no-response)
PORT    STATE  SERVICE
22/tcp  closed ssh
80/tcp  open   http
443/tcp open   https

Nmap done: 1 IP address (1 host up) scanned in 16.66 seconds

-> 5. What is the mail server (MX record)?
**COMMAND:**
dig hackthissite.org MX
**OUTPUT:**
; <<>> DiG 9.20.15-2-Debian <<>> hackthissite.org MX
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 22914
;; flags: qr rd ra; QUERY: 1, ANSWER: 7, AUTHORITY: 0, ADDITIONAL: 2

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 512
;; QUESTION SECTION:
;hackthissite.org.		IN	MX

;; ANSWER SECTION:
hackthissite.org.	600	IN	MX	10 aspmx.l.google.com.
hackthissite.org.	600	IN	MX	20 alt1.aspmx.l.google.com.
hackthissite.org.	600	IN	MX	30 aspmx3.googlemail.com.
hackthissite.org.	600	IN	MX	20 alt2.aspmx.l.google.com.
hackthissite.org.	600	IN	MX	30 aspmx5.googlemail.com.
hackthissite.org.	600	IN	MX	30 aspmx2.googlemail.com.
hackthissite.org.	600	IN	MX	30 aspmx4.googlemail.com.

;; ADDITIONAL SECTION:
aspmx.l.google.com.	138	IN	AAAA	2404:6800:4003:c05::1a

;; Query time: 63 msec
;; SERVER: 106.51.156.186#53(106.51.156.186) (UDP)
;; WHEN: Sat Mar 14 04:42:18 EDT 2026
;; MSG SIZE  rcvd: 252

-> 6. What is the main IP address of the domain?
**COMMAND:**
nslookup hackthissite.org 
**OUTPUT:**
Server:		106.51.156.186
Server:		106.51.156.186
Address:	106.51.156.186#53

Non-authoritative answer:
Name:	hackthissite.org
Address: 137.74.187.103
Name:	hackthissite.org
Address: 137.74.187.101
Name:	hackthissite.org
Address: 137.74.187.104
Name:	hackthissite.org
Address: 137.74.187.102
Name:	hackthissite.org
Address: 137.74.187.100


Non-authoritative answer:
Name:	hackthissite.org
Address: 137.74.187.103
Name:	hackthissite.org
Address: 137.74.187.101
Name:	hackthissite.org
Address: 137.74.187.104
Name:	hackthissite.org
Address: 137.74.187.102
Name:	hackthissite.org
Address: 137.74.187.100

**MAIN IP IS : Address:	106.51.156.186#53**

-> 7.Who is the domain register?
**command**
whois hackthissite.org
**output :**
Domain Name: hackthissite.org
Registry Domain ID: REDACTED
Registrar WHOIS Server: http://whois.porkbun.com
Registrar URL: https://porkbun.com
Updated Date: 2025-07-15T23:08:30Z
Creation Date: 2003-08-10T15:01:25Z
Registry Expiry Date: 2026-08-10T15:01:25Z
Registrar: Porkbun LLC
Registrar IANA ID: 1861
Registrar Abuse Contact Email: abuse@porkbun.com
Registrar Abuse Contact Phone: +1.8557675286
Domain Status: clientDeleteProhibited https://icann.org/epp#clientDeleteProhibited
Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited
Name Server: c.ns.buddyns.com
Name Server: f.ns.buddyns.com
Name Server: g.ns.buddyns.com
Name Server: h.ns.buddyns.com
Name Server: j.ns.buddyns.com
DNSSEC: unsigned
URL of the ICANN Whois Inaccuracy Complaint Form: https://icann.org/wicf/
>>> Last update of WHOIS database: 2026-03-14T09:18:13Z <<<

For more information on Whois status codes, please visit https://icann.org/epp

Terms of Use: Access to Public Interest Registry WHOIS information is provided to assist persons in determining the contents of a domain name registration record in the Public Interest Registry registry database. The data in this record is provided by Public Interest Registry for informational purposes only, and Public Interest Registry does not guarantee its accuracy. This service is intended only for query-based access. You agree that you will use this data only for lawful purposes and that, under no circumstances will you use this data to (a) allow, enable, or otherwise support the transmission by e-mail, telephone, or facsimile of mass unsolicited, commercial advertising or solicitations to entities other than the data recipient's own existing customers; or (b) enable high volume, automated, electronic processes that send queries or data to the systems of Registry Operator, a Registrar, or Identity Digital except as reasonably necessary to register domain names or modify existing registrations. All rights reserved. Public Interest Registry reserves the right to modify these terms at any time. By submitting this query, you agree to abide by this policy.  The Registrar of Record identified in this output may have an RDDS service that can be queried for additional information on how to contact the Registrant, Admin, or Tech contact of the queried domain name.

**THE DOMAIN REGISTER : Registrar: Porkbun LLC**

->8.When was the domain created?
**COMMAND :**
whois hackthissite.org
**OUTPUT :**
Domain Name: hackthissite.org
Registry Domain ID: REDACTED
Registrar WHOIS Server: http://whois.porkbun.com
Registrar URL: https://porkbun.com
Updated Date: 2025-07-15T23:08:30Z
Creation Date: 2003-08-10T15:01:25Z
Registry Expiry Date: 2026-08-10T15:01:25Z
Registrar: Porkbun LLC
Registrar IANA ID: 1861
Registrar Abuse Contact Email: abuse@porkbun.com
Registrar Abuse Contact Phone: +1.8557675286
Domain Status: clientDeleteProhibited https://icann.org/epp#clientDeleteProhibited
Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited
Name Server: c.ns.buddyns.com
Name Server: f.ns.buddyns.com
Name Server: g.ns.buddyns.com
Name Server: h.ns.buddyns.com
Name Server: j.ns.buddyns.com
DNSSEC: unsigned
URL of the ICANN Whois Inaccuracy Complaint Form: https://icann.org/wicf/
>>> Last update of WHOIS database: 2026-03-14T09:18:13Z <<<

For more information on Whois status codes, please visit https://icann.org/epp

Terms of Use: Access to Public Interest Registry WHOIS information is provided to assist persons in determining the contents of a domain name registration record in the Public Interest Registry registry database. The data in this record is provided by Public Interest Registry for informational purposes only, and Public Interest Registry does not guarantee its accuracy. This service is intended only for query-based access. You agree that you will use this data only for lawful purposes and that, under no circumstances will you use this data to (a) allow, enable, or otherwise support the transmission by e-mail, telephone, or facsimile of mass unsolicited, commercial advertising or solicitations to entities other than the data recipient's own existing customers; or (b) enable high volume, automated, electronic processes that send queries or data to the systems of Registry Operator, a Registrar, or Identity Digital except as reasonably necessary to register domain names or modify existing registrations. All rights reserved. Public Interest Registry reserves the right to modify these terms at any time. By submitting this query, you agree to abide by this policy.  The Registrar of Record identified in this output may have an RDDS service that can be queried for additional information on how to contact the Registrant, Admin, or Tech contact of the queried domain name.

**THE DOMAIN CREATED : Creation Date: 2003-08-10T15:01:25Z**

-> 9.Which organization owns it?
**COMMAND :**
whois hackthissite.org
**OUTPUT :**
Domain Name: hackthissite.org
Registry Domain ID: REDACTED
Registrar WHOIS Server: http://whois.porkbun.com
Registrar URL: https://porkbun.com
Updated Date: 2025-07-15T23:08:30Z
Creation Date: 2003-08-10T15:01:25Z
Registry Expiry Date: 2026-08-10T15:01:25Z
Registrar: Porkbun LLC
Registrar IANA ID: 1861
Registrar Abuse Contact Email: abuse@porkbun.com
Registrar Abuse Contact Phone: +1.8557675286
Domain Status: clientDeleteProhibited https://icann.org/epp#clientDeleteProhibited
Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited
Name Server: c.ns.buddyns.com
Name Server: f.ns.buddyns.com
Name Server: g.ns.buddyns.com
Name Server: h.ns.buddyns.com
Name Server: j.ns.buddyns.com
DNSSEC: unsigned
URL of the ICANN Whois Inaccuracy Complaint Form: https://icann.org/wicf/
>>> Last update of WHOIS database: 2026-03-14T09:18:13Z <<<

For more information on Whois status codes, please visit https://icann.org/epp

Terms of Use: Access to Public Interest Registry WHOIS information is provided to assist persons in determining the contents of a domain name registration record in the Public Interest Registry registry database. The data in this record is provided by Public Interest Registry for informational purposes only, and Public Interest Registry does not guarantee its accuracy. This service is intended only for query-based access. You agree that you will use this data only for lawful purposes and that, under no circumstances will you use this data to (a) allow, enable, or otherwise support the transmission by e-mail, telephone, or facsimile of mass unsolicited, commercial advertising or solicitations to entities other than the data recipient's own existing customers; or (b) enable high volume, automated, electronic processes that send queries or data to the systems of Registry Operator, a Registrar, or Identity Digital except as reasonably necessary to register domain names or modify existing registrations. All rights reserved. Public Interest Registry reserves the right to modify these terms at any time. By submitting this query, you agree to abide by this policy.  The Registrar of Record identified in this output may have an RDDS service that can be queried for additional information on how 

**ORGANISATIONS OWNS IT : Porkbun LLC**

-> 10. Is a WAF present?
**COMMAND:**
wafw00f https://hackthissite.org
**OUTPUT:**
                ______
               /      \
              (  W00f! )
               \  ____/
               ,,    __            404 Hack Not Found
           |`-.__   / /                      __     __
           /"  _/  /_/                       \ \   / /
          *===*    /                          \ \_/ /  405 Not Allowed
         /     )__//                           \   /
    /|  /     /---`                        403 Forbidden
    \\/`   \ |                                 / _ \
    `\    /_\\_              502 Bad Gateway  / / \ \  500 Internal Error
      `_____``-`                             /_/   \_\\

                        ~ WAFW00F : v2.3.2 ~
        The Web Application Firewall Fingerprinting Toolkit
    
[*] Checking https://hackthissite.org
[+] Generic Detection results:
[-] No WAF detected by the generic detection
[~] Number of requests: 7

**ANSWER :  No WAF detected by the generic detection**

-> 11. Which firewall vendor is used?
**COMMAND :**
wafw00f https://hackthissite.org
**OUTPUT:**
              ______
               /      \
              (  W00f! )
               \  ____/
               ,,    __            404 Hack Not Found
           |`-.__   / /                      __     __
           /"  _/  /_/                       \ \   / /
          *===*    /                          \ \_/ /  405 Not Allowed
         /     )__//                           \   /
    /|  /     /---`                        403 Forbidden
    \\/`   \ |                                 / _ \
    `\    /_\\_              502 Bad Gateway  / / \ \  500 Internal Error
      `_____``-`                             /_/   \_\\

                        ~ WAFW00F : v2.3.2 ~
        The Web Application Firewall Fingerprinting Toolkit
    
[*] Checking https://hackthissite.org
[+] Generic Detection results:
[-] No WAF detected by the generic detection
[~] Number of requests: 7

**ANSWER :  The Web Application Firewall Fingerprinting Toolkit**

-> 12.What usernames were found in metadata?
**COMMAND:**
metagoofil -d hackthissite.org -t pdf,doc,xls -l 10 -n 10 -o results -f report.html**
**OUTPUT:**
**OUTPUT:**
