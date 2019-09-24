Command line login
```
ftp IP
```
Try logging in with the username "anonymous"

Deeper scan on FTP services using nmap
```
nmap --script=ftp-anon,ftp-libopie,ftp-proftpd-backdoor,ftp-vsftpd-backdoor,ftp-vuln-cve2010-4221,tftp-enum -p 21 IP
```
Brute-force using hydra
```
hydra -t 1 -l admin -P /usr/share/john/password.lst -vV IP ftp
```
