# 🏛️ University Network Infrastructure Project


## 📋 Project Description

Implementation of a secure, segmented network infrastructure for Université Euro Méditerranéenne Fès using Cisco Packet Tracer. Features VLAN segmentation, inter-VLAN routing, DHCP services, and dynamic routing.

## 🔑 Key Features

- 🖧 VLAN segmentation by department/function
- 🔀 Inter-VLAN routing
- 🌐 DHCP services for automatic IP assignment
- ⚡ RIP dynamic routing
- 🔥 Firewall-protected Internet connection
- 🏷️ 802.1Q trunking
- 📡 Wireless access points integration

## ⚙️ Technical Specifications

| Category          | Details                                                                 |
|-------------------|-------------------------------------------------------------------------|
| **Devices**       | Cisco routers, multilayer switches, layer 2 switches                   |
| **Protocols**     | RIP v2, 802.1Q, DHCP, HTTP/HTTPS                                       |
| **VLANs**         | 10 VLANs (10-100) for different departments                            |
| **IP Scheme**     | 192.168.x.0/24 per VLAN                                                |
| **Security**      | Firewall filtering, VLAN isolation                                     |
| **Management**    | Remote access via HTTP/HTTPS                                           |

## 💻 Configuration Examples

### 🖥️ Router Sub-interface

Inter-VLAN routing configured on router sub-interfaces

DHCP services implemented for dynamic IP assignment

Separate DHCP pools for each VLAN/department

Includes default gateway and DNS server configuration

```cisco
Example configuration:

interface FastEthernet0/0.10
 encapsulation dot1Q 10
 ip address 192.168.1.1 255.255.255.0

###🔌 Switch VLAN Assignment Configuration

VLANs created and assigned to specific switch ports

Trunk ports configured for inter-switch and switch-router connections

Example configuration:

vlan 30
interface range GigabitEthernet1/0/5
switchport access vlan 30


Dynamic Routing

RIP version 2 implemented for routing between routers

Justified by:

Simplicity of configuration

Adequate for medium-sized university network

Configuration example:

router rip
version 2
network 10.0.0.0
network 192.168.1.0

Technical Justifications


VLAN Implementation
Segmentation: Isolates traffic by department/function

Security: Limits broadcast domains and contains potential security breaches

Efficiency: Improves network performance by reducing unnecessary traffic

Encapsulation (802.1Q)
Enables VLAN identification across network devices

Maintains VLAN separation when traffic traverses trunk links

Trunking
Essential for efficient inter-switch and switch-router connections

Maintains logical separation between VLANs while allowing traffic flow

Implementation Results
Successful network segmentation by department/function

Functional DHCP services for automatic IP assignment

Working inter-VLAN routing

Established dynamic routing between core routers


🎯 Project Outcomes

✅ Successful network segmentation by department

✅ Functional automatic IP assignment via DHCP

✅ Secure inter-department communication

✅ Scalable network architecture

✅ Optimized traffic flow with VLANs

✅ Redundant routing with RIP v2

📊 Network Topology Highlights

graph TD
    A[Internet] -->|Firewall| B[Core Router]
    B --> C[Multilayer Switch]
    C --> D[Department VLANs]
    C --> E[Lab VLANs]
    C --> F[Admin VLANs]
    B --> G[Secondary Router]


📚 Lessons Learned

📌 Importance of thorough VLAN planning

🔄 Benefits of dynamic routing protocols

⏱️ DHCP simplifies network management

🧮 Careful IP addressing prevents conflicts

🛡️ Security through segmentation




