# 4.Execution_of_NetworkCommands
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

## Program
## Client:

import socket 
from pythonping import ping 
s=socket.socket() 
s.bind(('localhost'8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    hostname=c.recv(1024).decode() 
    try: 
        c.send(str(ping(hostname, verbose=False)).encode()) 
    except KeyError: 
        c.send("Not Found".encode())

## Server:

import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode())


## Output
## PING COMMAND:
## Client:
![WhatsApp Image 2024-05-10 at 11 38 50_00671e41](https://github.com/Purajiths/4.Execution_of_NetworkCommends/assets/145548193/3bf6498e-e6e8-4d6e-8201-a5c938a061da)

## Serve
![WhatsApp Image 2024-05-10 at 11 38 53_04471d90](https://github.com/Purajiths/4.Execution_of_NetworkCommends/assets/145548193/a3c6ac54-aca5-433f-b39e-91ae0ab117cc)
r:

## TRACERT C
![WhatsApp Image 2024-05-10 at 11 38 56_4172da6a](https://github.com/Purajiths/4.Execution_of_NetworkCommends/assets/145548193/4de32fb5-6c78-4f95-bbd7-f2ee4f629eaf)
OMMAND:



## Result
Thus Execution of Network commands Performed
