view public share
	rsync --list-only {target_IP}::
view files in said share 
	rsync --list-only {target_IP}::public
copy a file to a file from the share in question
	rsync {target_IP}::public/flag.txt flag.txt