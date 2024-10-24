GetNPUsers.py
- impacket GetNPUsers is a command-line tool within the Impacket suite, used for extracting Kerberos Pre-Authentication (PreAuth) users from a Windows domain. This tool helps in identifying potential attack vectors and identifying users that can be targeted for pass-the-hash (PtH) or pass-the-ticket (PtT) attacks.
- usage
	- -no-pass 
	- -dc-ip "IP address"
- One liner to paste user file
	- for user in $(cat users); do GetNPUsers.py -no-pass -dc-ip 10.10.10.161 htb/${user} | grep -v Impacket; donege