# 4.Execution_of_NetworkCommands

### Name: Pranitha S
### Reg. No.: 212225040312

## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<br>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<br>
All commands related to Network configuration which includes how to switch to privilege mode
<br>
and normal mode and how to configure router interface and how to save this configuration to
<br>
flash memory or permanent memory.
<br>
This commands includes
<br>
• Configuring the Router commands
<br>
• General Commands to configure network
<br>
• Privileged Mode commands of a router 
<br>
• Router Processes & Statistics
<br>
• IP Commands
<br>
• Other IP Commands e.g. show ip route etc.
<br>

## Program
### Ping

server.py
~~~
import socket, subprocess

s = socket.socket()
s.bind(("localhost", 5000))
s.listen(1)

c, addr = s.accept()
host = c.recv(1024).decode()

result = subprocess.getoutput("ping " + host)
c.send(result.encode())

c.close()
~~~

client.py
~~~
import socket

c = socket.socket()
c.connect(("localhost", 5000))

host = input("Enter website/IP: ")
c.send(host.encode())

print(c.recv(4096).decode())

c.close()
~~~

### tracert

trace.py
~~~
import subprocess

target = input("Enter website or IP: ")

subprocess.run(["tracert", target])
~~~

## Output

### ping

The ping command is used to test connectivity between two devices on a network. It sends ICMP echo request packets to a target host and measures the response time and packet loss to check if the host is reachable.

<img width="933" height="309" alt="ping" src="https://github.com/user-attachments/assets/d4076c78-a8f2-46a3-85f7-fb947516294a" />

<img width="584" height="124" alt="Screenshot 2026-03-11 155952" src="https://github.com/user-attachments/assets/4eb7ab64-7ce0-4c3b-a64c-3e81fac87087" />

<img width="701" height="342" alt="Screenshot 2026-03-11 160006" src="https://github.com/user-attachments/assets/501ee623-a9dd-448d-bae7-5cb029d0fde4" />


### tracert

The tracert command is used to trace the path that data packets take from your computer to a destination host. It shows each router (hop) along the route and the time taken for the packets to reach them.

<img width="930" height="499" alt="tracert" src="https://github.com/user-attachments/assets/53af1db0-e55a-4a5c-9282-34138b31039b" />

<img width="849" height="383" alt="Screenshot 2026-03-11 160114" src="https://github.com/user-attachments/assets/c904f2bb-3133-42f9-9c68-e9793d3dc3ab" />

### netstat

The netstat command is used to display network connections, listening ports, routing tables, and network statistics. It helps monitor active connections and troubleshoot network issues on a computer.

<img width="912" height="954" alt="netstat" src="https://github.com/user-attachments/assets/03368ef2-c544-457f-8f5c-d03c1acc97fd" />

### ipconfig

The ipconfig command is used to display the IP configuration of a computer, including the IP address, subnet mask, and default gateway of the network interface. It is also used to renew or release IP addresses.

<img width="1016" height="928" alt="ipconfig1" src="https://github.com/user-attachments/assets/d77aed3a-eaac-4804-9762-3b7421f1ebf0" />

### nslookup

The nslookup command is used to query a DNS server to find the IP address of a domain name or the domain name associated with an IP address. It helps troubleshoot DNS resolution issues.

<img width="918" height="357" alt="nslookup2" src="https://github.com/user-attachments/assets/a98fa76c-dcbf-400d-b520-cfe1332b3f2e" />

### getmac

The getmac command is used to display the MAC (Media Access Control) address of the network adapters on a computer. It helps identify the physical address of network interfaces.

<img width="1028" height="217" alt="getmac" src="https://github.com/user-attachments/assets/baf7f52b-101e-47d6-917d-6b83519581d6" />

### hostname

The hostname command is used to display the name of the computer (host) on a network. It identifies the system within a network.

<img width="909" height="77" alt="hostname" src="https://github.com/user-attachments/assets/e31a82b2-554f-4546-8550-4a727a9647c5" />

### nbstat

The nbtstat command is used to display NetBIOS over TCP/IP statistics, NetBIOS name tables, and active connections. It helps troubleshoot NetBIOS name resolution problems on a network.

<img width="1116" height="689" alt="nbtstat" src="https://github.com/user-attachments/assets/80123178-7a32-47e0-81e5-472a33c41566" />

### arp

The arp command is used to display and manage the ARP (Address Resolution Protocol) cache, which maps IP addresses to MAC addresses on a local network.

<img width="1049" height="776" alt="arp" src="https://github.com/user-attachments/assets/ed583a64-e060-4e72-a61d-d5c5ef66cc36" />

### systeminfo

The systeminfo command is used to display detailed information about a computer, including the operating system version, system configuration, hardware details, and installed updates.

<img width="1220" height="931" alt="systeminfo" src="https://github.com/user-attachments/assets/2fe1af41-e3ee-47da-ae0b-98cc9a5fc487" />

## Result
Thus Execution of Network commands Performed 
