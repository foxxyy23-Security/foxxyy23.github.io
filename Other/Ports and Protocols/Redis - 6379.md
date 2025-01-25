What is it?
	Redis (REmote DIctionary Server) is an open-source advanced NoSQL key-value data store used as a
	database, cache, and message broker. The data is stored in a dictionary format having key-value pairs. It is
	typically used for short term storage of data that needs fast retrieval. Redis does backup data to hard drives
	to provide consistency.

how to install the tools?
	sudo apt install redis-tools
How to access it?
	redis-cli -h <IP>

helpful commands
	info 
		database version
	select 
		chose the database number
	keys *
		view all keys present in the chosen database
	get 
		grabs key or file from server


		