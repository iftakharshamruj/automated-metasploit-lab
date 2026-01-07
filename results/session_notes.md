Date: 2026.01.07
Target: 192.168.253.129

- Exploit used: vsftpd 2.3.4 / Samba trans2open
- Shell obtained: yes/no
- Session ID: X
- Commands run inside session:
  - id
  - uname -a
  - pwd
  - ip addr
  - ls
- Observations:
  - What worked
1. 
The Metasploit database connected successfully, allowing db_nmap and services to run without errors.
2. 
The Nmap scan inside Metasploit correctly identified all open ports and services on Metasploitable2.
3. 
The vsftpd 2.3.4 exploit successfully triggered the backdoor and opened a root shell on the target.
  - What failed
1. 
Running the vsftpd exploit with exploit -j (background mode) did not create a session.
This exploit is unstable when run as a background job and works best in foreground mode.
2. 
The Samba trans2open exploit failed with:
“This target is not a vulnerable Samba server (Samba 3.0.20-Debian)”  
This is expected — Metasploitable2’s Samba version is not vulnerable to this exploit.
3. 
The payload for the Samba exploit initially failed because cmd/unix/interact is not valid for that module.

  - Ideas for improvement
