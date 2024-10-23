dumping hashes 
	secretsdump.py <DOMAIN/user>: '<password>'@<IP>
		ex
			secretsdump.py MARVEL.local/tstark: 'Password2'@192.168.88.102
	you can also do it with hashes
		ex
			secretsdump.py administrator:192.168.88.101 -hashes ad3b435b51404eeaad3b435b51404ee:7facdc498ed1680c4fd1448319a8c04f
All accounts on the device besides: Guest, Default, WDGAUtilityAccount are worth looking at 

There is a chance to dump passwords in clear text
	passwords stored in the registry - they will appear in clear text
	if wdigest (older protocol) 
		enabled by default on older OS
			want to find an older OS via info gathering 
			this process might be enabled by default
when pentesting a real network, once we have a foothold on an acccount, use that account to spray the rest of the network, you can then find more accounts, and then spray again. this can allow you to finally find an domain admin or gain higher priv

Cracking passwords
	you only need the second portion (NT) 
	hashcast --help 
	hashcat --help | grep ntlm

