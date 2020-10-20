# Writeup of Morty's

1. Starting with nmap scan, stealth scan on all ports:

![nmap all ports](nmap_all.png)

2. On nmap scan, the fingerprint of port 13337 gives one flag.

![fingerprint 13337](port_13337.png)

*Note: This could be confirmed by telnet*

3. Port 6000 metions Rick's half baked shell, using netcat to connect to it gives a simple shell to get next flag:

![baked shell](half_baked_shell.png)

4. Visiting the website on port 80 doesn't show anything relevant... But inspection of HTML gives a password:

![html](html.png)

5. Robots.txt has 3 entries:
  * /cgi-bin/root_shell.cgi
  * /cgi-bin/tracertool.cgi
  * /cgi-bin/*
 
 6. Starting wih the tracertool.cgi:
 
 ![tracertool](tracert.png)
