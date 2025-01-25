who are we? what permissions do we have? what can we do 

whoami
ID
![[Pasted image 20240330135142.png]]
sudo -l
![[Pasted image 20240330135224.png]]
cat /etc/passwd
![[Pasted image 20240330135302.png]]

/etc/shadow
![[Pasted image 20240330135417.png]]

history
![[Pasted image 20240330135444.png]]

sudo su -
	try and login to root account with user password

find / -group <group> 2>/dev/null
	find anything with that group name in the entire direcory
ls -la <file/path>
	permissions of a file
file <file/path>
	What file type is it how does it work