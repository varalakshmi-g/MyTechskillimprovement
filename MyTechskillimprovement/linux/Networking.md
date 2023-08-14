### Networking 

The connection of two or more devices/machines to communicate with each other is called as networking

The basic requirements for networking are :

1. NIC (Network Interface Controller or Card)

2. Media

3. Topology

4. Protocol

5. IP Address

### 1. Network Interface Controller/Card (NIC) :
- A Network Interface controller (also known as Network interface card, network adapter, LAN adapter and by simmilar terms ) is a computer hardware component that connects a computer to a computer network. Each NIC will be having a unique MAC addresses (Media Access Control Address) to avoid conflicts between same NIC adapters. 
- In linux, these NIC adapter is represented by word **"eth"**  EX; If there are two Ethernet adapters in the system then it will be denoted by eth0, eth1, etc

### 2. Media :
- Media is the medium through which two different computer's NIC card will be connected. The best example for media is Cable ex: RJ 45, cat 5 etc

### 3. Topology :
- Topology is the scheme or design in which the computers in the network will be connected to each other. Ex : Bus, ring, star, mesh, tree topologies. 

![image](https://user-images.githubusercontent.com/89054489/229574165-8e16c12e-2b54-4110-bdaa-3a70964f2706.png)

### 4. protocol
- A Network Protocol defines rules and conventions for communication between network devices. Protocols for computer networking all generally use packet switching technique to send and receive messages in the form of packets.

- Hundreds of different computer network protocols have been developed each designed for specific purposes and environments.

Example for protocols are **TCP/IP (Transmission control protocol), UDP(User Datagram Protocol), HTTP. The most widely and regularly used protocols for transferring data are TCP and UDP. 

| TCP/IP | UDP |
| --- | --- |
| Transmission control protocol | User datagram protocol |
| It is connection oriented | It is connectionless |
| Reliable | Non-Reliable |
| TCP Acknowledgement will be sent/received | No Acknowledgement for UDP |
| Slow communication | faster communication |
| protocol number for TCP is 6 | Protocol number for UDP is 17 |
| HTTP, FTP, SMTP uses TCP | DNS, DHCP uses UDP |

### IP Address
- Every computer that is on the internet has a unique IP address assigned, so that they communicate with each other. To understand IP address we need to understand some important aspects of IP address they are

  - IP address Classes
  - Subnet Mask
  - Gateway
  
  **IP Address Classes**
  - The IP addresses are further broken down into classes. These classes are A,B,C,D and E and their possible ranges can be seen in figure below :
  
  
| Class | Start | End | Default Subnet Mask | CIDR |
| --- | --- | --- | --- | --- |
| Class A | 0.0.0.0 | 127.255.255.255 | 255.0.0.0 | /8 |
| class B | 128.0.0.0 | 191.255.255.255 | 255.255.0.0 | /16 |
| class C | 192.0.0.0 | 223.255.255.255 | 255.255.255.0 | /24 |
| class D (multicast) | 224.0.0.0 | 239.255.255.255 | | |
| class E (reserved) | 240.0.0.0 | 255.255.255.255 |

CIDR - classless inter domain routing

127.0.0.0 to 127.255.255.255 is reserved for loopback address

**loopback**
- A special IP number (127.0.0.1) that is designated for the software loopback interface of a machine. 127.0.0.0 through 127.255.255.255 is also reserved for loopback and is used for internal testing on local machines

**Multicast**
- Multicasting allows a single message to be sent to a group of recipients. Emailing and teleconferencing are examples of multicasting. It uses the network infrastructure and standard to send messages.

**Subnet Mask**
- A subnet Mask allows users to identify which part of an IP address is reserved for the network and which part is available for host use. By looking at the IP address alone, especially now with classless inter-domain routing, users cannot tell which part of the address is which. Adding the subnet mask or netmask gives users all the information needed to calculate network and host portions of the address with ease. 
- In summary, Knowing the subnet mask can allow users to easily calculate whether IP addresses are on the same subnet or not.

A commonly used netmask is 24 bit netmask as seen below

| Netmask | 255. | 255. | 255. | 0 |
| Binary | 11111111 | 11111111 | 11111111 | 00000000 |
| Netmask length | 8 | 16 | 24 | -- |

**Gateway**

- A gateway is a network point that provides entrance into another network. 
- On the internet, a node or stopping point can be either a gateway node or host (end point) node. Both the computers of internet users and the computers that serve pages to users are host nodes. The computers that control traffic within your company's network or at your local internet service provider (ISP) are gateway nodes.

###### some important configuration files/directories of network configurations

`/etc/sysconfig/network-scripts` is the directory which keeps the configuration of network devices connected to the system.

`/etc/sysconfig/network` is a file which keeps the information about the hostname assigned to the system. if you want to change the hostname permanently, you need to change the hostname in this file

`/etc/hosts` a file which responsible for resolving hostname into IP locally, in other word it acts as local DNS if DNS server is not accessible

`/etc/resolv.conf` is the file which keeps the address of DNS server to which the clients will be accessing to resolve IP to hostname and hostname to IP.

| command | Description |
| --- | --- |
|`ifconfig` | To check IP address assign to all the interfaces |
|`ifconfig <adaptername>`| To check IP of a particular interface |
|`hostname`| To check the hostname of the system |
|`hostname -i` | To check Ip of host |
|`host <ip address>` or `nslookup <ipaddress>/<hostname>`| To check whether DNS is resolving or not |
|`dig`| The most common command used to DNS function |
|`dig -x <ip address>`| with Ip address to find DNS function |
|`ping <ipaddress>`| To check network connectivity using ping command |
|`ping -c <count> <ip address>`| To limit the pinging for specific number of counts |
|`hostname` | To check the hostname |
|`hostname <newname>`| To change the hostname |
|`vim /etc/sysconfig/network`| Go and make changes in this location to make the hostname permanent. above command is just for temporary change |
|`ethtool <adapter name>` | To know more about the NIC card/adapter |


