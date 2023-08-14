# Introduction to Networking

## what is networking ?
- The interconnection of computing devices to exchange data and share resources with eachother. By using a set of rules called **protocols** to do this task is called Networking.

![image](https://user-images.githubusercontent.com/89054489/233817998-7376ea0f-54ae-403c-8eb4-2f8a4a0e2cdf.png)

Each device on the network can be referred to as a **Nodes** or **client** and each node has
a unique address to communicate with each other, we call it an IP address e.g.
192.168.0.11, 203.214.242.38, etc

![image](https://user-images.githubusercontent.com/89054489/233818140-dd41e7bb-c1f1-40a5-a19d-2981053f5ac4.png)




------------------------------------
what is network & networking ?
**network** : collection of computing devices connected via communication medium to exchange the information and the resources 
**networking**: it is the practice of creating , maintaining, securing and troubleshooting  the network.
![image](https://user-images.githubusercontent.com/89054489/235904896-d17ecf51-7d36-4011-a0b8-36c241858650.png)

## Types of computer network  ?

There are multiple types of networking they are

1. Local Area Network ( LAN )
2. Wide Area Network ( WAN )
3. Metropolitan Area Network ( MAN )
4. Wireless Local Area Network ( WLAN )
5. peer-to-peer(P2P) networks
6. Storage Area Network (SAN)
7. Virtual Private Network (VPN)
8. Cloud COmputing Network (CCN)

1. Local Area Network ( LAN ) : A **LAN**, or **local area network**, is a group of connected computers within a small area that share a centralized Internet connection 
- A LAN connects devices in a limited geographical area such as floor, building, or campus.
- LAN commonly use the ethernet standard for connecting devices and usually have a high data-transfer rate. 
- Wireless technology is also commonly used for a LAN.
![image](https://user-images.githubusercontent.com/89054489/235902759-ec6d4e5e-e0f8-4f20-9e8f-b53ecde6a484.png)


2. Wide Area Network ( WAN ) : 
- A WAN connects devices in a large geographical area, such as in multiple cities or countries. 
- WANs are used to connect LANs and use technologies such as fiber-optic cables and satellites to transmit data. 
- The internet is considered to be the largest WAN.
![image](https://user-images.githubusercontent.com/89054489/235902832-c7481ee8-2212-4352-86c2-4d16ff74598c.png)

3. Metropolitan Area Network ( MAN )
4. Wireless Local Area Network ( WLAN )
5. peer-to-peer(P2P) networks
6. Storage Area Network (SAN)
7. Virtual Private Network (VPN)
8. Cloud COmputing Network (CCN)


![image](https://user-images.githubusercontent.com/89054489/235827661-1a985224-f35e-48ad-aab8-e18431aba611.png)


**HOST** : Any device having IP address is called as HOST . EX: PC/Laptop/Server

**Router** : The connection of two or more different networks is called as Router
![image](https://user-images.githubusercontent.com/89054489/235827170-bd945f67-46e6-4d10-9dae-474e7c8b8cd4.png)

**switch** :
- A network switch is networking hardware that connects devices on a computer network by using packet switching to receive and forward data to the destination device. - A network switch is a multiport network bridge that uses MAC addresses to forward data at the data link layer of the OSI model
![image](https://user-images.githubusercontent.com/89054489/235828512-dd05db5c-3b58-4742-a67d-f8e1a452dc13.png)
![image](https://user-images.githubusercontent.com/89054489/235828536-602dbc55-5d6c-4d1f-87f7-7640f32bd876.png)

- bridges and switches only route traffic towards their addressed destinations.
- bridges and switches work with MAC addresses at Layer 2
**Hub** :
- hubs operate at Layer 1 of the OSI model
- Hubs broadcast incoming traffic on all ports
- An Ethernet hub, active hub, network hub, repeater hub, multiport repeater, or simply hub is a network hardware device for connecting multiple Ethernet devices together and making them act as a single network segment.
![image](https://user-images.githubusercontent.com/89054489/235828278-3f13687e-3d93-446c-97c2-dc063be293e0.png)

**Modem :** It is used for modulation and demodulation.
- A modem converts data to a signal so it can be easily sent and received over a phone line, cable, or satellite connection.
- ![image](https://user-images.githubusercontent.com/89054489/235828991-a01c3e8d-96c8-4de5-8424-33d2349eccb3.png)

| SWTICH | HUB |
| --- | --- |
| It is unicast (1-1) | It is broadcast (1-all) |
| It stores MAC address | It works on signals |
| It is an intelligent device | It is a tier-1 device (not much intelligent) |
| More no.of ports | less no.of ports |



BRIDGE :
- To connect hubs
- It reduces broadcast
- It uses MAC address

### IP classes
- what is IP address :
    >> AN IP address is a numerical label in a decimal format. 
    >> Each node in a network has a unique IP address that identifies it.
    >> With this arrangement, traffic can flow to the specific node on the network  for which it is included.
    >> You can think of an IP address as a mailing address that identifies each node on the network.
    
    
    -  The IP address is constructed of a set of four numbers separated by dots. 
    -  Each of these sets of numbers represents 8 bits, represented in binary format. Machines convert the binary format into decimal number format.
    -  Let's take a look at how this works. 
    -  You'll start by looking at the binary format. 
    -  Each of the 8 bits in any given section of IP address has a placeholder numeric value.
    -  All of these values that are represented with a binary 1 are added together.

- The result is the decimal number for the section of the IP address. 
- These sets of numbers can range from 0 to 255. Because it has four sections, the IP address is considered to be 32 bits in lenght.
- In the example, only the values 128 and 64 are represented in binaray format with 1. Therefore, 128 and 64 are added together to give you 192 for this section of the IP address. 

- Different types of IP addresses

There are 2 types of IP addresses they are 1. IPV4 address and 2. IPV6 address.

IPV4 vs IPV6

| IPV4 | IPV6 |
| --- | --- |
| EX: 192.0.2.0 | EX: 2600:1f18:22ba:8c00:ba86:a05e:a5ba:00ff |
| 32 bit length | 128 bits in length |
| provides upto 4.3 billion IP addresses | provides a practically unlimited number of IP addresses |
| Is more commonly used and established | Accommodate more user devices |
| Is supported by all VPNs (unlike IPV6, which currently is not) | will eventually replace IPV4 |


IP address structure

![image](https://user-images.githubusercontent.com/89054489/235903284-6daa78ec-4a61-4cc3-8ced-b76e85261ac1.png)

![image](https://user-images.githubusercontent.com/89054489/235903365-4ef35454-db39-462d-b43b-bf5f1941d707.png)

![image](https://user-images.githubusercontent.com/89054489/235903481-cd9cda6c-56ac-4bc5-8ef5-95d67ac481ac.png)

![image](https://user-images.githubusercontent.com/89054489/235903550-5407c19d-4372-45ef-9a9b-c5738ed69918.png)

## CIDR (Classless Inter-Domain Routing):

- When you are setting up your network, you need to decide on the range of IP Addresses that will be contained in it.
- A common method to define a network's IP range is a Classless Inter-Domain Routing (CIDR) block. 
- The CIDR block address is expressed as follows :
    - An IP address is the first address of the network. A portion of this number will become your network identifier.
    - Next is a slash character followed by a number. This portion of the CIDR block is called as **Netmask**
    - The number tells you how many of the 32 bits of the routing prefix must be fixed or allocated for the network identifier.
    - The bits that are not fixed are allowed to change to give you a group of IP addresses that are consecutive to each other.
    - In this way , the netmask determines the number of IP addresses in your network.
![image](https://user-images.githubusercontent.com/89054489/235903868-b1838161-1c20-4a5d-a19b-145331a6443f.png)


![image](https://user-images.githubusercontent.com/89054489/235904042-ceb9edce-17d2-452f-9776-80a157b6bdcf.png)

- In this example you are looking at an IPV4 32-bit IP address. 
- The CIDR block address is 192.0.2.0/24. The netmask, 24 tells you that the first 24 bits ( from left to right ) cannot change.
- The last 8 bits are flexible. As a result, the IPs 
- 
![image](https://user-images.githubusercontent.com/89054489/235904193-fe20ff2b-f1d0-423e-a655-351c5484e3a6.png)

![image](https://user-images.githubusercontent.com/89054489/235904376-a41d57a5-aeb0-4c2d-8a37-ecf9c8323b2a.png)


![image](https://user-images.githubusercontent.com/89054489/236692345-23545f19-1633-4d36-84c4-abefa911b56e.png)

![image](https://user-images.githubusercontent.com/89054489/236692337-6fa20e2d-2c5e-4557-9284-50b278a54adc.png)

![image](https://user-images.githubusercontent.com/89054489/236692329-eeb1f9c5-f363-4988-9c67-291c34c39f36.png)

![image](https://user-images.githubusercontent.com/89054489/236692398-90cfc209-0445-46cb-8019-23c3a9b18a10.png)


--> The lesser the netmask number More free IP addresses.

- commands related to it
- Decimal to binary
- How IP classes are identified/defined ?

### IANA (Internet assign number authority )
- ARIN ( America)
- APNIC ( asia )
- LATNIC (latin america)\
- RIPC (Russia)
- AFRNIC (Africa)

RIR -Regional Internet Registries

## OSI REFERENCE MODEL

- OSI Model is a suite of protocols, or rules to govern how computers communicate with one another.
- OSI model is a conceptual model by international organisation for standardisation, The purpose of OSI model is to visualize how data moves through the computer network. 
- Devices within a network communicate by using a suit of protocols


![image](https://user-images.githubusercontent.com/89054489/235888434-71da3922-180e-4502-9e1f-c50e0b392276.png)

**OSI Model Layers :**

- Physical layer (layer 1)
- Data link layer (layer 2)
- Network layer (layer 3)
- Transport layer ( layer 4 )
- Session layer ( layer 5 )
- Presentation layer ( layer 6 )
- Application layer ( layer 7 )


Physical layer ( layer 1 ) :
- The physical layer defines standards for transmitting raw data (bits) over transmission media to connect network nodes.
- The physical layer provides an electrical, mechanical, and procedural interface to the transmission medium

Data link layer ( layer 2 ) 
- The data link layer defines standards for transfering data between adjacent network nodes in a wide area network (WAN) or between nodes on the same local area network(LAN) segment
- This layer can provide the means to detect and possibly correct errors that might occur in the physical layer

Network layer ( layer 3 )
- The network layer is responsible for communication across different networks. 
- It provides the means for transferring variable-length network packets from a source to a destination host through one or more networks.

Transport layer ( layer 4 )
- The transport layer provides transparent transfers of data  between users, and it provides reliable data transfer services to the upper layers. 
- The transport layer controls the reliability of a given link through flow control, segmentation and desegmentation, and error control
- This layer also provides the acknowledgement of the successful data transmission and send the next data if no errors occured.

Session layer ( layer 5 )
- The session layer  provides the mechanism for opening, closing, and managing a session between user application processes
- Communication sessions consist of requests and response that occur between applications

presentation layer ( layer 6 ) 
- The presentaion layer is responsible for formatting and delivering information to the application layer for further processing or display. 
- It transfers data based on the syntax that the application accepts.

Application layer ( layer 7 )
- The application layer is closest to the user, which means that both the OSI application layer and the user interact directly with the software application.
- Application layer functions typically include identifying communication partners, determining resource availability, and synchronizing communication.

![image](https://user-images.githubusercontent.com/89054489/235888513-6f8ac739-6f8f-49a5-a23a-5756d00e6752.png)

Network Models  :

**Peer-to-Peer Model Diagram**
- A **Peer-to-Peer** refers to the computer systems or peers that are connected to each other for the purpose of distributing workloads
- They could also be used for sharing resources such as files, printers, and storage
- In a peer-to-peer network model, each node has its own data and applications and is responsible for its own management and security 
- Peers are equally privileged participants in the architecture.

EX: Fiiles can be shared directly between systems on the network without the need for a center servers.
- Use cases :
    - Users are responsible for backing up each node
    - Security requirements are not restrictive
    - A limited number of peers are used.

![image](https://user-images.githubusercontent.com/89054489/235902502-3b6ec14f-5c7e-465a-9be7-f1a80b96ff36.png)

**Client-Server Model Diagram**
- In a **Client-Server** model, the data management and application hosting are centralized at the server and distributed to the clients.
- All clients on the network must use the designated server to access shared files and information that are storing on the serving computer
- if the server goes down, no client is able to access the network until the server is restored.
- The following are the examples of client-server models :
    File server and desktop clients
    Print server and desktop clients
    ![image](https://user-images.githubusercontent.com/89054489/235902606-30644aa2-8dda-4bde-83b8-2a92c7739141.png)

  Use case: Most business networking architectures
## TCP/IP MODEL

| TCP | UDP |
| --- | --- |
| TCP stands for transmission control protocol | UDP stands for User datagram protocol |
| It is Reliable | It is not reliable |
| It has Retranmission capability | It doesn't have Retranmission capability |
| It is connection Oriented | It is connection less |
| It has more overhead <br> 20 bytes on every packet | Less overhead <br> 8 bytes on every packet |

**Internet :** It is a network of networks ( or ) Interconnection of network.

### subnetting
- subnetting is the process of dividing a network into smaller networks
- subnet mask represents network bits
- subnetting can happen in both private and public IP's

public IP - Able to route with internet
Private IP - Not able to route with internet

- A subnet or subnetwork is a network within a network. Each subnet comprises a specified range of consecutive IP addresses for this partition of the network.
- Therefore, you can have fine-grained control over entities of IP addresses that are grouped together in a subnet. 
- with this access control  over subnets, you can decide which subnets in the network can communicate with each other. With a subnet, traffic can reach its destination in a shorter amount of time.
- For EX: if an IP address needs to reach an IP in another subnet, then it must travel through the router.

- However, suppose that you have a node that needs to send data to another node in the same subnet. In this situation, the transfer does not need to travel through routers because both nodes have IP addresses that are located in the same subnet. The data transfers locally within the subnet which the two IP addresses are located.
- This technique reduces the bandwidth on the routers because they need to manage traffic for only IPs that are sending information outside the originating subnet. Strategic placement of subnets and IPs within the subnet helps to reduce network complexities and reduces network loads for more effecient traffic flow.

NOTE : subnet CIDR blocks cannot overlap . 

CIDR Block review :

**Things to remember about CIDR blocks**
- First and last IPs are reserved. Depending on your network provider, others might be reserved.
- CIDR can't change.
    >> Plan ahead. Make sure that your CIDR block range can accomdate enough IP addresses for current and future IP needs.
 - Subnet CIDR blocks cannot overlap with each other.
    >> For ex, you cannot have two subnets with a 10.0.0.0/26 CIDR block.
        >> If one subnet has 10.0.0.0/26 which gives you 64 IP addresses (0-63) then the next subnet should have a 10.0.0.64/26 CIDR block.

- The smaller the netmask number, the more IP addresses you will have .
    >> For ex: a /24 netmask gives you 256 IP addresses. A /16 netmask gives you 65,536 IP addresses.

**Public subnets** : It allows internet traffic that is routed through an internet gateway to reach the subnet. A public subnet might make a good choice if you have a website that is targeting customers.
![image](https://user-images.githubusercontent.com/89054489/236693595-b918187f-8e98-4c13-a738-914a57562996.png)

**Private Subnets** : A private subnet denies traffic to the subnet that is routed from the public internet. you should use a private subnet if your network must connect to services outside your network but must restrict external services from initiating a connection to your network. Access to the public internet from a private subnet requires a NAT device.

![image](https://user-images.githubusercontent.com/89054489/236693587-36b6658c-f732-45fb-90bb-e8e8e059ec71.png)

### DHCP (Dynamic host configuration protocol)
### Telnet
#### port number
##### ANDing process
vpc

- With the expansion of computing into the cloud, cloud providers offer you the option to bring your network centers into the cloud. A virtual private cloud, or VPC provides you with a cloud, or clouds within the cloud.

- It is essentially a portion of the cloud that you can use to setup network environments where you can provision servers and other IT resources. With a VPC, you control the network and security configuration so that access is granted only according to your specifications.


![image](https://user-images.githubusercontent.com/89054489/235904667-db7efbb3-e1be-4f0e-9a5c-a6c5f1bc9bfc.png)


-------------------------------------
Cloud Computing Networking 
----------------------------------
Amazon VPC :

It is a virtual networking environment that gives you full control over your virtual networking environment, which includes resource placement, connectivity and security.

![image](https://user-images.githubusercontent.com/89054489/236694396-7148003a-41d4-42d4-972c-28a623082bf2.png)

>> Amazon VPC is a logically isolated virtual network dedicated to your AWS account where you can launch AWS resources such as Amazon EC2 and Amazon RDS instances. You can use Amazon VPC to create managed networks in the cloud. 
>> use your VPC to host multi-tier web applications, enforce security rules on inbound and outboound connections, and define connectivity between your servers.
>> The Amazon VPC virtual network closely resembles a traditional network that you can operate in your own data center, but it has the benefit of using scalable infrastructure of AWS.
>> Amazon VPC is a private environment and you have full control over how to configure your VPC.
>> Amazon VPC is highly available, when you launch your VPC, you choose the region. Then you launch subnets in availability zones.
>> You can launch one or more subnet in each availability zone . Set the route tables to route traffic between subnets, other networks or out to the internet.
>> All you need to do is set the destinations, and Amazon VPC will do the rest.
>> Amazon vpc provides an improved security posture because you can control two types of security measures that you can apply to your VPC. 
>> Security groups act as firewalls to allow only the traffic that you authorize and route the traffic only the parts of your network that you permit.
>> You can use security group configuration and network ACLs to keep your network safe and secure.
>> VPC is cost effective there are no additional charges for creating and using a VPC. your costs are based on optional VPC capabilities with usage based charges such as NAT gateway and IP Address Manager. Each of this has hourly usage charges.
>> Easily monitor your VPC with VPC flow logs. VPC flow logs can be used for network monitoring, security analysis, and expense optimization.
>> Amazon VPC can handle all your networking needs and offers you the elasticity to make changes based on business needs at the most affordable cost. 

![image](https://user-images.githubusercontent.com/89054489/236695359-4f826a6a-a87a-4a9f-8bb6-f187ae2a1c34.png)

![image](https://user-images.githubusercontent.com/89054489/236696408-c7a92d59-1347-40fb-a94c-93eb65b3c6c5.png)

![image](https://user-images.githubusercontent.com/89054489/236696442-8dda9775-f2eb-44e7-8543-de3687f469d4.png)

![image](https://user-images.githubusercontent.com/89054489/236696482-ae99dc17-3bd7-4f31-bcb6-ea34f548d3cf.png)

![image](https://user-images.githubusercontent.com/89054489/236696509-ed6284fa-0289-4e56-aa03-e1fb816c4fcd.png)

![image](https://user-images.githubusercontent.com/89054489/236696541-71c95583-16c7-4e22-a832-7e105b2ef50c.png)

using Amazon VPC :

![image](https://user-images.githubusercontent.com/89054489/236696657-d9992d92-3312-43a3-a796-a079a7e8f6b3.png)

![image](https://user-images.githubusercontent.com/89054489/236696729-946c49c8-ffa4-4d73-b36b-d402c56f951a.png)

Network Gateway :

- A Network gateway is a gateway that determines the traffic that will be given access to your network. Two of the most common gateways are internet gateways and private gateways. 

![image](https://user-images.githubusercontent.com/89054489/236697159-f82c8d13-028c-4764-895e-c17401e904bc.png)

![image](https://user-images.githubusercontent.com/89054489/236697179-ff52300d-c8d0-4657-816b-27aeb81dcad5.png)

**Route Tables**
- Route tables are the mechanism that directs traffic in VPC . They contain a set of rules, called routes. That direct network traffic from your subnet.
- Each route specifies a destination and target. The destination is the destination CIDR block where you want traffic  from your subnet to go. The target is the connection that the destination traffic is sent through.

![image](https://user-images.githubusercontent.com/89054489/236697456-f4b7631e-ac0a-4f0f-97f4-72c772608789.png)

![image](https://user-images.githubusercontent.com/89054489/236697487-3e17176b-c843-45d8-9cd8-16b1a45ae198.png)


![image](https://user-images.githubusercontent.com/89054489/236697520-7fc2b15f-7b80-4f14-a7b5-5b224f194f56.png)

![image](https://user-images.githubusercontent.com/89054489/236697541-9892f639-422e-4bff-b4d0-8edbbf999818.png)


![image](https://user-images.githubusercontent.com/89054489/236757040-733518e0-6dc1-43fc-93df-831762914db4.png)

![image](https://user-images.githubusercontent.com/89054489/236757546-9add362b-8ed1-403c-9961-2d7a982545f7.png)

![image](https://user-images.githubusercontent.com/89054489/236759027-8b42f50b-98a9-4932-a57c-08b00a4efaee.png)


Scenario :

![image](https://user-images.githubusercontent.com/89054489/236761415-21acb46d-64da-4d1c-8f56-e917f853d61b.png)

![image](https://user-images.githubusercontent.com/89054489/236761505-840a0102-bd27-4749-b637-a4fcb09a7e36.png)

![image](https://user-images.githubusercontent.com/89054489/236761603-36c1dee9-5456-41e4-84ac-dd0723e713fe.png)

![image](https://user-images.githubusercontent.com/89054489/236761741-5d2cde63-029b-4b3c-be66-db8f20cc60ea.png)

![image](https://user-images.githubusercontent.com/89054489/236762036-51208fa2-a844-4306-8525-b34fa52f9e89.png)

![image](https://user-images.githubusercontent.com/89054489/236763634-f1a3c414-1e40-44f7-a5e1-cc73275df8bc.png)

**Managing your network**

- ![image](https://user-images.githubusercontent.com/89054489/236764850-e8388a3c-2a28-4483-8053-aea45edc069a.png)

![image](https://user-images.githubusercontent.com/89054489/236765048-43092650-a24d-4418-bada-d58404b9d164.png)

![image](https://user-images.githubusercontent.com/89054489/236765274-9ce6afb8-6ebb-4959-ae5d-a4629c6c79d7.png)

VPC End points :

![image](https://user-images.githubusercontent.com/89054489/236765499-3cbe0804-9798-410d-bca9-84573e33da7e.png)

![image](https://user-images.githubusercontent.com/89054489/236765565-aaa2c2dc-cbfd-4b72-a932-8d4fdfbf285f.png)

VPC Peering

![image](https://user-images.githubusercontent.com/89054489/236765918-439ff256-155f-4233-bedb-ab40642736e6.png)

![image](https://user-images.githubusercontent.com/89054489/236766842-fcf1d992-e055-4ec3-b555-31b577e81297.png)

![image](https://user-images.githubusercontent.com/89054489/236767150-4444f498-d1d4-4040-8db6-74a370ae1d98.png)


![image](https://user-images.githubusercontent.com/89054489/236767266-6f028b2c-fa5a-4eb8-8d7d-e0aed0af4bf0.png)

![image](https://user-images.githubusercontent.com/89054489/236767303-dbed2a33-689d-4db4-958d-0fa5c3a4b5c1.png)


![image](https://user-images.githubusercontent.com/89054489/236767358-5b30d2f6-5185-47db-a43d-8c0ba939e725.png)


