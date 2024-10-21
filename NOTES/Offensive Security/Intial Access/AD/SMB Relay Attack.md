What is it? how does it work?
	instead of cracking the hashes we gathered during the LLMNR attack with responder, we can instead rely those hashes to specific machines and potentially gain access
attack requirements
	 - SMB signing must be disabled or not enforced on the target 
	 - reloyed user creds must be admin on machine for any real value

after that we can use a took called ntlmrelayx.py to relay the hashes to other machines
	we need a file of potential targets (targets.txt)
	we can run command to start it
		ntlmrelayx.py -tf targets.txt -smb2support
	This will relay the hash found from one machine to all of the others in the target files and also SAM dump all hahses for all users found on that machine
	can also use a -i (Interactive)  to spawn a shell on the machine
		then need to bind to it (port and ip will be shown)
			ex - nc 127.0.0.1 11002
		from here we have a shell to do many things
	we can also run commands directly from the relay script using -c "command here"
		ex- -c "whomai"
			this will take the hash and relay it to all 