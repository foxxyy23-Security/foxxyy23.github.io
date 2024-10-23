what are we doing? 
	we are taking the password that we already got, and we are passing it around to different machines and trying to use that to login

tool
	crackmapexec 
		smb <ip/ip range> -u <username> -d <domain> -p <Password> -H <hash> --local-auth (what authentication mechanism are we using? )
		-sam 
			we can dump the sam on every device we login to
				example
					we can take a local admin hash and use that to try and login to every machine on the network and dump thier SAM to try and get more credentials 
		--shares 
			we can see more shares on each devices
			maybe there are others we were not aware of that are only on specific servers
		--lsa
			dump the local security authority 
		-M 
			modules 
		examples
			crackmapexec smb 192.168.88.0/24 -u tstark -d MARVEL.local -p Password2
		it also has a built in Database to house everything that you did
			which machines you got into and what not
			hashes dumped
			accounts dumped
			 
	secretesdump.py 
		this can dump the hashes whcih we can also send around the network
to view your database of all of the data you found while using crackmapexec
	cmedb