Secure-Multi-Site-WAN-using-OSPF-HSRP-and-VLANs
📖 Project Overview-

This project simulates a secure enterprise network consisting of a Headquarters (HQ) and two Branch Offices interconnected through a Wide Area Network (WAN).

The network was designed and implemented in Cisco Packet Tracer to demonstrate enterprise networking concepts including:

VLAN Segmentation
Inter-VLAN Routing
OSPF Dynamic Routing
HSRP High Availability
WAN Connectivity
ACL-Based Access Control
Branch-to-HQ Communication

🎯 Project Objectives-

Connect Headquarters and Branch Offices through a WAN infrastructure.
Segment departments using VLANs.
Enable communication using OSPF Dynamic Routing.
Provide gateway redundancy using HSRP.
Implement network security using ACLs.
Simulate a real-world enterprise network.

🏢 Network Architecture-

Headquarters (HQ):

Router2 (HQ WAN Router)
Multilayer Switch 0 (HSRP Active)
Multilayer Switch 1 (HSRP Standby)
Access Switch
IT Department
Finance Department
HR Department
Server Network

Branch A:

Router0
Access Switch
Sales VLAN
Finance VLAN

Branch B:

Router1
Access Switch
Sales VLAN
Finance VLAN

🛠 Technologies Used-

Cisco Packet Tracer
VLANs
Inter-VLAN Routing
Router-on-a-Stick
OSPF (Open Shortest Path First)
HSRP (Hot Standby Router Protocol)
ACLs (Access Control Lists)
WAN Connectivity
Layer 3 Switching

🌐 IP Addressing Plan
Headquarters
VLAN 30 - IT
Device	IP Address
HSRP Virtual Gateway	192.168.30.1
MLS0	192.168.30.2
MLS1	192.168.30.3
IT PC	192.168.30.10
Network: 192.168.30.0/24

VLAN 40 - Finance
Device	IP Address
HSRP Virtual Gateway	192.168.40.1
MLS0	192.168.40.2
MLS1	192.168.40.3
Finance PC	192.168.40.10
Network:192.168.40.0/24

VLAN 50 - HR
Device	IP Address
HSRP Virtual Gateway	192.168.50.1
MLS0	192.168.50.2
MLS1	192.168.50.3
HR PC	192.168.50.10
Network:192.168.50.0/24

VLAN 60 - Servers
Device	IP Address
HSRP Virtual Gateway	192.168.60.1
MLS0	192.168.60.2
MLS1	192.168.60.3
Server	192.168.60.10
Network:192.168.60.0/24

Branch A
VLAN 10 - Sales
Device	IP Address
Gateway	10.1.1.1
Sales PC	10.1.1.2
Network:10.1.1.0/29

VLAN 20 - Finance
Device	IP Address
Gateway	10.1.1.9
Finance PC	10.1.1.10
Network:10.1.1.8/29

Branch B
VLAN 10 - Sales
Device	IP Address
Gateway	10.1.2.1
Sales PC	10.1.2.2
Network:10.1.2.0/29

VLAN 20 - Finance
Device	IP Address
Gateway	10.1.2.9
Finance PC	10.1.2.10
Network:10.1.2.8/29

🌍 WAN Connectivity-
Branch A ↔ Headquarters
Device	IP Address
Router0 WAN Interface	100.100.100.1/30
Router2 WAN Interface	100.100.100.2/30
Branch B ↔ Headquarters
Device	IP Address
Router1 WAN Interface	100.100.100.5/30
Router2 WAN Interface	100.100.100.6/30

🔗 Internal HQ Routing Links
Router2 ↔ MLS0
Device	IP Address
Router2	172.16.1.5/30
MLS0	172.16.1.6/30
Router2 ↔ MLS1
Device	IP Address
Router2	172.16.1.9/30
MLS1	172.16.1.10/30

🔄 OSPF Dynamic Routing-
OSPF was configured to exchange routes automatically between Headquarters and Branch Offices.

Verification Commands
show ip ospf neighbor
show ip route
OSPF Benefits
Dynamic Route Learning
Faster Network Convergence
Reduced Administrative Overhead
Scalable Enterprise Routing

🔁 HSRP High Availability-
HSRP was configured between both Headquarters Multilayer Switches.

Active Device:

MLS0

Standby Device:

MLS1

HSRP Benefits:

Gateway Redundancy
Automatic Failover
Increased Availability
Business Continuity

HSRP Verification:

show standby brief

Failover Testing:

Active VLAN Interface Shutdown
Automatic Standby Takeover
Continuous Network Connectivity

🔒 Access Control Lists (ACL)-

ACLs were implemented to restrict unauthorized access between departments.

Example Security Policy:

Finance VLAN cannot access HR VLAN.
Server VLAN remains accessible.
IT VLAN retains administrative access.

Verification Command:

show access-lists

✅ Testing Performed-

VLAN Verification
show vlan brief
Trunk Verification
show interfaces trunk
OSPF Verification
show ip ospf neighbor
show ip route
HSRP Verification
show standby brief
ACL Verification
show access-lists
Connectivity Tests

✅ Branch A PC → HQ Server

✅ Branch B PC → HQ Server

✅ HQ IT PC → Branch A PC

✅ HQ IT PC → Branch B PC

✅ Inter-VLAN Routing

✅ OSPF Route Exchange

✅ HSRP Failover


📚 Key Learning Outcomes-

Enterprise WAN Design
VLAN Segmentation
Inter-VLAN Routing
Dynamic Routing with OSPF
Gateway Redundancy using HSRP
ACL-Based Security
Layer 3 Switching
Multi-Site Enterprise Networking
WAN Architecture Design

💻 Software Used-

Cisco Packet Tracer

📂 Repository Contents-

README.md
Secure-Multi-Site-WAN-using-OSPF-HSRP-and-VLANs.pkt
Topology.png
Screenshots/

🚀 Project Highlights-

Multi-Site WAN Connectivity
Dynamic Routing using OSPF
Gateway Redundancy using HSRP
VLAN-Based Department Segmentation
ACL-Based Access Restriction
Enterprise Network Design
High Availability Architecture

Author-
Developed as an Enterprise Networking Project using Cisco Packet Tracer to demonstrate WAN Infrastructure, OSPF Routing, HSRP High Availability, VLAN Segmentation, and Network Security.





