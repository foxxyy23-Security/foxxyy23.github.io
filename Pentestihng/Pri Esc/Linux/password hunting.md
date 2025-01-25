grep --color=auto -rnw '/' -ie "PASSWORD" --color=always 2> /dev/null

![[Pasted image 20240330140156.png]]

locate password | more
![[Pasted image 20240330140349.png]]

find / -name authorized_keys 2> /dev/null
![[Pasted image 20240330140507.png]]