# Enumeration Challenge

## Challenge 1 : NetBIOS Enumeration
`nbstat -a <ip>` Only works if Window attack other windows.
If linux use `nmblookup` which shows same output as nbstat.
<img width="451" height="202" alt="Screenshot 2026-05-22 175942" src="https://github.com/user-attachments/assets/ae2a50ac-17df-4add-ad12-312134778232" />
<img width="428" height="263" alt="Screenshot 2026-05-22 180153" src="https://github.com/user-attachments/assets/750e7f0e-f3a0-49a2-a015-a2c9f54734f2" />

## Challenge 2 : Fast Nmap Scan
`nmap -F <target>` To quickly discover common open ports.<br>
<img width="565" height="231" alt="Screenshot 2026-05-22 180348" src="https://github.com/user-attachments/assets/44fd901b-21e4-419c-81c6-52cfc10e1d01" />

## Challenge 3 : DNS Records
`nslookup <domain>` used for simple DNS queries, mainly to resolve a domain name into its IP address. <br>
<img width="583" height="443" alt="Screenshot 2026-05-22 182311" src="https://github.com/user-attachments/assets/5ee9d9e1-c6bb-4ccf-b4f7-0b7a0e24b99d" />

`dig <domain>`<br> more advanced DNS query tool that can request specific record types <br>
<img width="661" height="354" alt="Screenshot 2026-05-22 182641" src="https://github.com/user-attachments/assets/bd3a5aa8-da09-4045-b8f8-9e24337351c7" />

`<dig mx <domain>`<br> "MX" is for Mail record <br>
<img width="679" height="402" alt="Screenshot 2026-05-22 182819" src="https://github.com/user-attachments/assets/8eb9697e-9ec9-449e-ab02-f8123111f13f" />

## Challenge 4 : TTL OS Fingerprinting
By using `ping`. It show which TTL the target use. <br>
<img width="648" height="221" alt="Screenshot 2026-05-22 190529" src="https://github.com/user-attachments/assets/7e005293-8952-4d32-814d-8c5f2e0b59cb" />
<br>255 Mean the target use Cisco/BSD 

## Challenge 5 : Anonymous LDAP Query 
`ldapsearch -x -H ldap://<IP> -b "dc=example,dc=com"` To see if the target has LDAP service running or not.<br>
<img width="543" height="86" alt="Screenshot 2026-05-22 191357" src="https://github.com/user-attachments/assets/8c76fa41-b22a-4e3a-a8b6-0ff85001978c" />
<br>If not it shows like this.

## Challenge 6 : Anonymous FTP Login 
`ftp <ip>` To login into Target's FTP but if the target doesn't have FTP it will shows like this :<br>
<img width="562" height="154" alt="Screenshot 2026-05-22 202240" src="https://github.com/user-attachments/assets/763678a4-6ecb-45e3-8efc-cde1198b53c1" />

## Challenge 7 : SMB NSE Enumeration ( INTERMEDIATE ENUMERATION )
Commands: <br>
`nmap --script smb-os-discovery -p445 <IP>` <br>
`nmap --script smb-enum-users -p445 <IP>`<br> To fingerprint Windows via SMB. <br>
<img width="570" height="176" alt="Screenshot 2026-05-22 193829" src="https://github.com/user-attachments/assets/a4b90865-fd39-4be2-ac1b-62121f3d0436" />


<img width="540" height="171" alt="Screenshot 2026-05-22 193909" src="https://github.com/user-attachments/assets/9ea67df1-7cc8-4560-bc7e-00e89221bbfc" />

## Challenge 8 : Enum4linux ( INTERMEDIATE ENUMERATION )
`enum4linux -a <IP>` to runs every enumeration module available. Specifically, it tries to gather OS information, NetBIOS name, User Account and ect. <br>
<img width="644" height="536" alt="Screenshot 2026-05-22 194036" src="https://github.com/user-attachments/assets/dca90e1c-90bd-4a36-90ca-47a559a07a0c" />

## Challenge 9 : SNMP NSE( INTERMEDIATE ENUMERATION )
Commands: <br>
`nmap -sU -p161 --script=snmp-sysdescr <IP>`<br>
`nmap -sU -p161 --script=snmp-processes <IP>`<br>
To runs the SNMP system description script, which queries the SNMP agent for basic system info (OS, hardware, description).<br>
<img width="554" height="182" alt="Screenshot 2026-05-22 194450" src="https://github.com/user-attachments/assets/753f8ddc-8951-40ca-b4f7-dc087cc178b9" />
<img width="574" height="179" alt="Screenshot 2026-05-22 194415" src="https://github.com/user-attachments/assets/4d249f63-110e-4740-b738-f9810ca7c8bb" />

## Challenge 10 : OS Detection  ( INTERMEDIATE ENUMERATION )
`nmap -O <IP>` Show Version and The Accuarcy of possibility of OS's target<br>
<img width="841" height="326" alt="Screenshot 2026-05-22 203253" src="https://github.com/user-attachments/assets/72bc98c0-ec88-4ef9-b3c8-66e0bb9f263e" />

