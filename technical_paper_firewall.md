# Firewall

## What is Firewall
A firewall is a software program or hardware that helps to screen out hackers, viruses, and worms that try to reach your computer over the internet. There are two types of firewalls which are hardware and software.

1. A software firewall is a program that is installed on our device.
2. A hardware firewall is a device that is placed in between your network and an untrusted network.

## Why is Firewall
1. If more than one computer is connected to your network, then it is necessary to protect your network from the untrusted internet via a hardware firewall. 
2. It is also necessary to protect each computer in your network with a software firewall, so that if one computer is infected with a virus in your network, then the remaining computers will remain free from the viruses. 
All most all operating systems have inbuilt software firewalls.
3. The basic task of a firewall is to regulate the flow of traffic in between computer networks of different trust levels.
4. All incoming messages from the internet are passed through a firewall, if these messages pass the security criteria defined by the firewall, then only these messages will be passed to the receiver.
5. If we turn off the Firewall all the messages pass through the firewall freely without passing any security criteria. As a result, hackers can easily hack our sensitive data by passing malicious software through the data over the internet.
## How the Firewall Works
* Internet is an untrusted network of connected computers. When we send a request to a server on the internet from our network by using browsers like chrome, the corresponding server on the internet will take the request and then processes the request and will send the response to us. During this communication, a hacker can hack the connection and send his data (malicious data) to us to get our sensitive data. But the firewalls protect us by checking the incoming data with some security criteria before we receive the response from the internet.
* Firewalls maintain a list of Allowed and not Allowed computers, this list is called Access Control List. When the hacker sends his data by hacking the connection, the firewall checks if the device from which we receive the data, is in the access list. If yes, it will else, won’t allow the messages.
* Firewall notices which website you are currently using. Suppose assume you are using youtube, firewall maintains a conversation list that contains your computer name and the application or server name you are using. Because you are using youtube, you should receive the data only from the youtube server, suppose a hacker hacks the connection and tries to send some malicious data through the video content you are seeing, firewalls checks where you are receiving the data from, if it is in your conversation list, it will allow else won’t allow the data.
## Types of Firewall
1. Packet Filtering Firewall.
2. Application / Proxy Firewall.
3. Hybrid Firewall.

Before moving into the firewall types, we need to know what is a data packet or IP packet.<br />
While we download some data from the internet, then the corresponding server sends the data by dividing it into packets every second, instead of sending the entire file at once. Each packet contains the sender’s IP address, receiver’s IP address, and Payload (which means some part of the data we request).

### 1. Packet Filtering Firewall
* Before sending the request to the server on the internet, the Firewall maintains an access control list that contains the sender’s IP address and receiver’s IP address, Port number of the server. when the data packet arrives from the internet, the firewall checks the sender’s and receiver’s IP address, the port number in the data packet with the access control list it has, if the details are the same, then it will allow the data to pass through it, else it will block the data.
* Packet Firewalls come by default with Routers. These are cheaper.
* Only the limitation in these firewalls is, they don't verify the payload in the data packet. Hackers can pass the malicious software through this payload.

### 2. Application / Proxy Firewall
* This type of firewall doesn’t let the internet know who the actual user is, by not disclosing the user’s IP address. When we send the request to the server, this firewall takes the request and then modifies the user’s IP address with its own IP address in the data packet and then sends this modified data packet to the server, so the server thinks that the Proxy firewall is the actual user.
* After receiving the packet from the internet, this firewall checks the receiver's IP address using its checklist, if it is the original server, it will modify its IP address in the data packet with the User’s Ip address and send it to the user, else it will block that data. Along with it, a proxy firewall also checks the payload, so the hacker can not send the malicious software through the payload.
* A proxy firewall hides the Original User’s IP address from the internet and at the same time, it verifies the sender’s IP address, receiver’s IP address, Port Number, and Payload.
* Finally, the Proxy firewall provides better security than the Packet Filtering Firewall.

### 3. Hybrid Firewall
* A hybrid Firewall means the combination of Packet Filtering Firewall and Proxy Firewall. If these two firewalls are connected parallelly, then the security is reduced to the parameters defined by the Packet Firewall, then there will be no use of a proxy firewall. For this reason, a Hybrid firewall uses packet filtering and proxy firewalls in series. As a result, a hybrid firewall provides the best security compared to Packet filtering and Proxy firewalls.

**Among all these three firewalls, which one should be used is purely depends on the implementation environment. For example,** 
```
1. For low-risk environments like a florist shop, a packet filtering firewall would be the best choice.
2. For medium-risk environments like universities, a Proxy firewall would be the best choice.
3. For high-risk environments like Hospitals, a hybrid firewall would be the best choice.
```
## Hardware and Software Firewalls
### Hardware Firewall
1. It is a device that is existed in between your network and other networks.
2. It protects the entire network, it is assigned to.
3. It filters the traffic of the network, it is assigned to.
4. It has its own hardware(CPU and RAM).

### Software Firewall
1. It is a software program that is installed on your computer.
2. It protects only the computer in which it is installed.
3. It filters the traffic of the Computer in which it is installed.
4. It consumes the CPU, RAM of the device in which it is installed.

## Firewall Limitations
1. Firewalls maintain an access control list that contains the trusted programs, non trusted programs. When firewalls receive the packet from the internet, then they check whether it belongs to a trusted or non trusted program. If it belongs to a trusted program, it will allow else, won’t allow the data. But hackers can create fake data packets containing trusted IP addresses so that they can hack our computers.

2. when our computer is connected to a public wifi network and there is a hardware firewall in between this public wifi network and the internet. Hackers can not attack from the internet. But what if the hackers are present in your network?. So to prevent this type of attack, your firewall software in your computer should always be on.

3. while installing software on our computer, it displays a checkbox showing that “add an exception for this software in Firewall”. If you check that box, the Firewall doesn’t verify the data coming to this software from the internet and vice versa. So the hackers can send the malicious software through this data without being detected by the firewall.

4. Firewalls maintain some trusted networks list in their access control list. So whenever they receive the data packets from trusted networks, they will allow that data. But what if a hacker is connected to a trusted network and sends the malicious software through those trusted networks, so this will become a problem sometimes. So we have to maintain some anti-virus and anti-malware software in our computers additionally.

5. Hackers can easily obtain the employee’s identity and log in as an employee. Firewalls can’t stop the hackers from that masquerading.
