Topics: #portscanning #nmap #enumeration

# nmap (network mapper)
	-T4 (speed of packets)
	-p- (All ports) no P = top 1000 ports (take away -  and add a number for the specific port)
	-A (all of it, everything)
	-sn (ping scans)
	-Pn (treat all hosts as oline)
	-sU (UDP scan )
	-SV (probe open ports to determine service/version)
	-sC 
	-O 

## Notes:
-A 
	Aggressive - scans everything
-Pn 
	treat host as online (used if machine does not respond to Ping)
-sU
	UDP port scan
-p-
	all ports65565
-p<port number>
	(-p80,443,22) scan only those ports
-O 
	(OS detection)
-script <ScriptName>
	Run specified Nmap scripts



## Other
### Scripts
Nmap scrips can be found in the following directly on Kali
```
/usr/share/nmap/scripts
```

## example
```
nmap -p- -A -Pn _IP_ -o output.txt
```
This command runs for all ports, aggressave/all, treat the host as online and put the results into a txt file