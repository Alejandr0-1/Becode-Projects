# Building a simple network


# Components:

## Local Network:

- 1 router
- 1 switch
- 3 PCs

## Simulated Internet Access:

- 1 external router
- 1 web server
- 1 switch

## Simulated Website Access:

- 1 DNS server



# Step-by-step Configuration:

- Link the PCs together:

Connect the 3 PCs to the switch's first 3 ports (FastEthernet 0/1, 0/2, 0/3)
using their respective FastEthernet0 ports.
Configure the IP addresses and subnet masks on the PC interfaces as follows:


- PC-Robert: IP - 192.168.1.10, Mask - 255.255.255.0

- PC-Camille: IP - 192.168.1.11, Mask - 255.255.255.0

- PC-Renaud: IP - 192.168.1.12, Mask - 255.255.255.0

  - Ensure that the interfaces are up and running on both the PCs and the switch.
  Add the router for internet access:

- Connect the local router's GigabitEthernet 0/0 port to the switch's GigabitEthernet 0/1 port.

- Configure the IP address and subnet mask on the router's interface: IP - 192.168.1.254, Mask - 255.255.255.0.

- Ensure that the interface is up and running on the router.

- Set the router's IP (192.168.1.254) as the default gateway for the 3 PCs.


## Simulate internet access with a web server:

- Configure the local router's interface connected to the web server with the IP address and subnet mask: IP - 192.168.3.254, Mask - 255.255.255.0.

- Configure the web server's interface with the IP address and subnet mask: IP - 192.168.3.1, Mask - 255.255.255.0.

-Set the default gateway for the web server to 192.168.3.254.

-Ensure connectivity between the external router and the web server by testing ping.


## Enable communication between the networks:

- Connect the routers together using their Serial 0/1/0 ports.

- Configure the local router's interface with the IP address and subnet mask: IP - 192.168.2.1, Mask - 255.255.255.0.

- Configure the external router's interface with the IP address and subnet mask: IP 192.168.2.2, Mask - 255.255.255.0.

- Test connectivity between the routers using ping.

- Add a route on the local router to reach network 192.168.3.0 with the mask 255.255.255.0 through the next hop 192.168.2.2.

- Add a route on the external router to reach network 192.168.1.0 with the mask 255.255.255.0 through the next hop 192.168.2.1.

## PCs can now reach the web server on the other network. Accessing 192.168.3.1 in a browser will display the default Cisco Packet Tracer webpage.

## Set up the DNS server:

- Connect the DNS server's FastEthernet0 port to the switch's FastEthernet 0/1 port.

- Configure the IP address and subnet mask on the DNS server's interface

- 192.168.3.1, Mask - 255.255.255.0.


- Set the default gateway for the DNS server to 192.168.3.254.
-Enable the DNS service on the DNS server.
-Add an entry on the DNS server with the name "www.cisco.com" and the address 192.168.3.15.
-Configure all devices to use 192.168.3.1 as the DNS server address.
- The PCs can now access "www.cisco.com" through their browsers.
