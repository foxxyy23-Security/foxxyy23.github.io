

pip install bloodhound
	bloodhound it always being updated
	needed for the latest and greates hacks

first we need neo4j on 
	Sudo Neo4j console
after we start it, it will give us a link of where it started on our computer
	click the link and go to the IP/port
first time you will be asked to login
	neo4j neo4j
		Then need to change your password (NEW PASSWORD neo4j1)
next launch bloodhound
	sudo bloodhound
		neo4j login
in previous version, you had to manually gather the data
with new versions, we can now use an ingested to gather it for us

injester
	sudo bloodhound-python 
		-d Domain
		-u username
		-p passwrod
		-ns or DC
		-c (what are we collecting) All
	ex
		sudo bloodhound-python -d Marvel.local -u tstark -p Password1 -ns 192.168.88.100 -c All
	
