Enumerate for users
```
smtp-user-enum -M VRFY -U /usr/share/wordlists/metasploit/unix_users.txt -t $ip
```
```
use auxiliary/scanner/smtp/smtp_enum
```
```
for server in $(cat smtpmachines); do echo "******************" $server "*****************"; smtp-user-enum -M VRFY -U userlist.txt -t $server;done #for multiple servers
```
Command to check if a user exists
```
VFRY root
```
Command to ask the server if a user belongs to a mailing list
```
EXPN root
```
Scan for vulnerabilities
```
nmap --script=smtp-commands,smtp-enum-users,smtp-vuln-cve2010-4344,smtp-vuln-cve2011-1720,smtp-vuln-cve2011-1764 -p 25 IP
```
