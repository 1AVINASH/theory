### Address Family
*  It defines the format of addresses used by the socket. 

### AF_INET
* In socket programming, socket.AF_INET specifies the address family for Internet Protocol version 4 (IPv4). It essentially tells the operating system that the socket will be used for communicating over the network using IPv4 addresses. For ipv6, we use AF_INET6

### SOCK_STREAM
* It is a constant that specifies the type of socket to be created. It indicates that the socket will use a connection-oriented, reliable, two-way communication protocol, specifically TCP (Transmission Control Protocol). TCP ensures that data is delivered in the correct sequence, without loss or duplication. socket.SOCK_STREAM is typically used for applications that require reliable data transfer, such as web browsing, file transfer, and email.

### SOCK_DGRAM
* SOCK_DGRAM specifies a UDP (User Datagram Protocol) socket, which is connectionless and unreliable.

### SO_REUSEPORT
* This option can be used when multiple processes want to listen to the same port

### CIDR (Classless Inter Domain Routing)
* It is a method used to allocate IP addresses and manage routing in IP networks. 
* CIDR replaced the older class-based IP addressing system (Class A, B, C) and allows for more flexibility and efficiency in IP address allocation.
* Think of it like `Instead of using fixed size blocks of addresses (like only large or only small blocks), CIDR lets you choose exactly how many addresses you need, leading to better use of available space.`
* CIDR allows for Variable Length Subnet Masks (VLSM), which means you can create subnets of different sizes based on your needs.
* If we are using 32bit IP addresses, then each part signifies 8 bit
* The first IP Address in the subnet range is reserved for Subnet identification, and is called the network id. The last ip is reserved for brocasting data to all devices in the subnet and is called the broadcast address
* Examples:
    * 10.0.0.0/8: Signifies that the IP address starts from 10.0.0.0 and only 8 bits are blocked for hosts. Hence total ip addresses available are 2^8=256.

### Subnet
* A subnet, or subnetwork, is a portion of a larger network that is logically separated into smaller, manageable segments. 
* It allows for more efficient routing of traffic and can improve network performance by minimizing the need for data to traverse unnecessary parts of a larger network. 
* Subnets are created by dividing a larger IP network into smaller, distinct groups (also called logical partitioning)
* Subnets can also be used to isolate different parts of a network, enhancing security and making it easier to manage different groups of devices. 

### Network Id:
* It is the first address in an IP subnet
* It identifies the subnet itself, not a specific device

### Broadcast Id
* Last address in an IP subnet
* Used to send data to all devices on the subnet simultaneously


### DHCP


### ARP (Address Resolution Protocol)


