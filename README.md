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

```cisco
interface FastEthernet0/0.10
 encapsulation dot1Q 10
 ip address 192.168.1.1 255.255.255.0

###🔌 Switch VLAN Assignment


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




