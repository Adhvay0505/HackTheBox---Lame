# HackTheBox---Lame Writeup


## Task 1
I used rustscan for this, you can use nmap, but I wanted to speed this up

![Screenshot From 2025-06-21 14-59-43](https://github.com/user-attachments/assets/ae3e8c1b-b248-4381-831a-22b287fe27bf)

4 ports out of the top 1000 ports are open

- **FTP** – 21  
- **SSH** – 22  
- **SMB** – 139, 445  


## Task 2

![Screenshot From 2025-06-21 15-01-08](https://github.com/user-attachments/assets/749d2364-4415-40df-a25c-5ec4198da39e)

It uses VSFTPd version 2.3.4, there is a famous backdoor in this version

![Screenshot From 2025-06-21 15-08-06](https://github.com/user-attachments/assets/8a568114-395b-4dd2-920e-3a6717673567)


## Task 3

i tried loading the metasploit exploit, but it was unsuccessful

![Screenshot From 2025-06-21 15-06-57](https://github.com/user-attachments/assets/37fa4975-ae6c-4c77-893a-da2a6606e51b)


## Task 4

![Screenshot From 2025-06-21 15-09-13](https://github.com/user-attachments/assets/14409581-2fa3-4e65-8642-b1a562a598f4)

Using smbmap we find out that the version of samba running on the machine is 3.0.20, also the tmp share has read & write access, 

![Screenshot From 2025-06-21 15-10-39](https://github.com/user-attachments/assets/c421ca58-b212-4f41-b9c7-93ab02cb1869)


## Task 5

![Screenshot From 2025-06-22 13-27-06](https://github.com/user-attachments/assets/1eaacbe7-544b-48ea-b33a-1fd861222de5)

This is the CVE associated with Samba 3.0.20, lets load the exploit on metasploit


## Task 6

![Screenshot From 2025-06-21 15-14-29](https://github.com/user-attachments/assets/fb620925-4dd4-46ea-a767-07baf3966f82)

running this exploit returns a shell as root user, splendid!


## Task 7

user flag 

![Screenshot From 2025-06-21 15-16-13](https://github.com/user-attachments/assets/706f606d-0aeb-4d62-9fd4-ed83b2365ae8)


## Task 8

root flag

![Screenshot From 2025-06-21 15-16-36](https://github.com/user-attachments/assets/c02a1a44-688e-4b44-b233-1016cb8ed39c)


