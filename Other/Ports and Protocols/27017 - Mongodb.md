Downloading mongodb utility 
	curl -O https://fastdl.mongodb.org/linux/mongodb-linux-x86_64-3.4.7.tgz
extract it 
	tar xvf mongodb-linux-x86_64-3.4.7.tgz
navigate to the dir 
	cd mongodb-linux-x86_64-3.4.7/bin
access the database
	./mongo mongodb://{target_IP}:27017

helpful db commands
	show dbs;
		show databases
	use <db>
		picks what collection you want to go into
	show <db>
		shows everything in that collection
	