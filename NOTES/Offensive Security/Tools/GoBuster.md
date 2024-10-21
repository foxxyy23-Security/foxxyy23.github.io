Date: 2024-05-19

Topics: #enumeration #directoryBusting #enumeration #infogathering

Notes:
Installing go lang 
	sudo apt install golang-go
installing gobuster
	go install github.com/OJ/gobuster/v3@latest

sudo git clone https://github.com/OJ/gobuster.git
cd gobuster
go get && go build
go install

example command
	sudo gobuster dir -w /usr/share/wordlists/dirb/common.txt -u <IP>



