 =fwe can use this for many different things
https://codingo.io/tools/ffuf/bounty/2020/09/17/everything-you-need-to-know-about-ffuf.html
### BruteForcing

we can take a get request from Burp and copy and paste it into a txt file
from there change the password to "FUZZ"
	Fuzz is the variable fuzz will use to determine where the password is

then we need to add a few things in the command
	-request <file>
		the file we want to use 
	-request-proto http 
		protocol (in this, and most cases http)
	-w (wordlists)
		what word lists would you like to try against
	-mode <mode>
		clusterbomb
		sniper <defult>
final command
	fuff -request req.txt -request-proto http -w /usr/share/seclists/SecLists-Master/Passwords/xato-net-10-million-passwords-1000.txt
look for a chance in length or status

to grep results
	-fs <size>

you can set multiple variables 
FUZZUSER FUZZPASS

multiple variables clusterbomb example

ffuf -request req.txt -request-proto http -mode clusterbomb -w pass.txt:FUZZPASS -w /usr/share/seclists/Usernames/top-username-shortlist.txt:FUZZUSER 

