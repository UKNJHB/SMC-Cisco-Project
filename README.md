\# Smart Medical Center (SMC) - Cisco Packet Tracer Project



\## 📋 Project Overview



A comprehensive network infrastructure design for a Smart Medical Center using Cisco Packet Tracer. This project demonstrates advanced networking concepts including VLSM (Variable Length Subnet Masking), inter-VLAN routing, security protocols, and network testing.



\*\*Module:\*\* Conception de Réseau Informatique  

\*\*Supervisor:\*\* Mme Hajar RHILMANE  

\*\*Institution:\*\* CMC - OFPPT



\---



\## 🎯 Project Objectives



1\. Design an optimized network infrastructure using VLSM

2\. Implement secure inter-VLAN communication

3\. Configure security protocols (SSHv2, ACL, WPA2)

4\. Validate network connectivity and security policies

5\. Provide comprehensive documentation for future enhancements



\---



\## 🏗️ Network Architecture



\### Topology: Hierarchical Star Architecture

\- \*\*Core Layer:\*\* Multi-layer Switch L3 (Centralized Intelligence)

\- \*\*Distribution Layer:\*\* Access Switches (Layer 2)

\- \*\*Access Layer:\*\* End devices (PCs, Printers, WiFi APs)

\- \*\*External Connectivity:\*\* Internet Gateway



\### Equipment Inventory:

\- 1x Core Switch L3 (Routing \& Switching)

\- Multiple Layer 2 Access Switches

\- Wireless Access Points (WiFi)

\- End devices (PCs, Printers, Medical Devices)

\- Router (Internet Connectivity)



\---



\## 📊 IP Addressing Plan (VLSM - Variable Length Subnet Masking)



| Zone / Department | VLAN | Network IP | CIDR | Subnet Mask | Host Range | Broadcast |

|---|---|---|---|---|---|---|

| \*\*WiFi Guests\*\* | 80 | 10.0.0.0 | /22 | 255.255.252.0 | 10.0.0.1 - 10.0.3.254 | 10.0.3.255 |

| \*\*WiFi Staff\*\* | 70 | 10.0.4.0 | /23 | 255.255.254.0 | 10.0.4.1 - 10.0.5.254 | 10.0.5.255 |

| \*\*Doctors\*\* | 20 | 10.0.6.0 | /24 | 255.255.255.0 | 10.0.6.1 - 10.0.6.254 | 10.0.6.255 |

| \*\*Medical Devices\*\* | 60 | 10.0.7.0 | /24 | 255.255.255.0 | 10.0.7.1 - 10.0.7.254 | 10.0.7.255 |

| \*\*Admin\*\* | 10 | 10.0.8.0 | /25 | 255.255.255.128 | 10.0.8.1 - 10.0.8.126 | 10.0.8.127 |

| \*\*LAB\*\* | 30 | 10.0.8.128 | /25 | 255.255.255.128 | 10.0.8.129 - 10.0.8.254 | 10.0.8.255 |

| \*\*Imaging\*\* | 40 | 10.0.9.0 | /26 | 255.255.255.192 | 10.0.9.1 - 10.0.9.62 | 10.0.9.63 |

| \*\*Data Center\*\* | 50 | 10.0.9.128 | /26 | 255.255.255.192 | 10.0.9.129 - 10.0.9.190 | 10.0.9.191 |

| \*\*Security\*\* | 90 | 10.0.9.192 | /26 | 255.255.255.192 | 10.0.9.193 - 10.0.9.254 | 10.0.9.255 |



\*\*Base Network:\*\* 10.0.0.0/16



\---



\## 🔐 Security Implementation



\### 1. Access Control Lists (ACL)

\- Granular traffic filtering

\- Restriction of unauthorized access to sensitive departments

\- Guest WiFi isolated from critical infrastructure

\- Medical device network protected



\### 2. SSH Configuration (SSHv2)

\- Secure remote device management

\- Encrypted authentication

\- RSA key-based access

\- Elimination of telnet (insecure protocol)



\### 3. Port Security

\- MAC address-based access control

\- Protection against unauthorized device connections

\- Violation actions (shutdown, restrict, protect)



\### 4. Password Encryption

\- Type 7 → Type 5 encryption (enable secret)

\- Secure configuration storage

\- Prevention of plaintext password exposure



\### 5. WiFi Security

\- WPA2-AES encryption standard

\- Strong pre-shared keys (PSK)

\- Separate SSIDs for guests and staff

\- VLAN isolation for guest network



\---



\## 🔧 Configuration Highlights



\### Core Switch (L3) Configuration:

\- \*\*Routing Protocol:\*\* Static routes for inter-VLAN communication

\- \*\*VLAN Configuration:\*\* 9 VLANs for department segmentation

\- \*\*SVI (Switch Virtual Interfaces):\*\* Layer 3 routing on VLAN interfaces

\- \*\*Trunking:\*\* 802.1Q trunk links to access switches

\- \*\*Spanning Tree Protocol:\*\* Loop prevention and redundancy



\### Services:

\- \*\*DHCP:\*\* Dynamic IP assignment (per VLAN)

\- \*\*Static IPs:\*\* Gateway, servers, medical devices

\- \*\*DNS:\*\* Name resolution for network resources

\- \*\*NTP:\*\* Synchronized time across devices



\---



\## ✅ Testing \& Validation



\### Test Cases Covered:



\#### 1. Connectivity Verification

\- ✅ Ping between different VLANs

\- ✅ Inter-VLAN routing functionality

\- ✅ Gateway reachability



\#### 2. Security Validation

\- ✅ ACL blocking unauthorized traffic

\- ✅ Guest WiFi isolation confirmed

\- ✅ Medical data network protected

\- ✅ SSH connectivity verified



\#### 3. Troubleshooting

\- Anomaly detection and diagnosis

\- Root cause analysis

\- Configuration correction

\- Validation of fixes



\---



\## 📋 Detailed Project Structure



\### Technical Implementation:

1\. \*\*Physical Architecture Analysis\*\* - Equipment selection and placement

2\. \*\*Logical Addressing Design\*\* - VLSM implementation

3\. \*\*VLAN Segmentation\*\* - Department-based isolation

4\. \*\*Routing Configuration\*\* - Inter-VLAN communication

5\. \*\*Security Policies\*\* - ACL and protocol configuration

6\. \*\*Wireless Integration\*\* - WiFi design and security

7\. \*\*Internet Connectivity\*\* - External routing setup

8\. \*\*Testing \& Validation\*\* - Comprehensive verification

9\. \*\*Troubleshooting\*\* - Problem resolution procedures

10\. \*\*Documentation\*\* - Technical specifications



\---



\## 📚 Key Technical Concepts



✅ \*\*VLSM (Variable Length Subnet Masking)\*\*

\- Optimized IP allocation

\- Efficient address space utilization

\- Different subnet sizes for different departments



✅ \*\*Inter-VLAN Routing\*\*

\- Layer 3 switching capabilities

\- SVI (Switch Virtual Interface) configuration

\- Static route implementation



✅ \*\*Network Segmentation\*\*

\- VLAN-based isolation

\- Department-specific access control

\- Enhanced security posture



✅ \*\*Hospital Standards Compliance\*\*

\- Patient data protection (HIPAA considerations)

\- Secure communication channels

\- Redundancy for critical services



\---



\## 🚀 Future Enhancements (Phase 2)



\- \[ ] Advanced Redundancy Protocols (HSRP/VRRP)

\- \[ ] Enhanced Cybersecurity measures

\- \[ ] International hospital standards compliance (ISO 27001)

\- \[ ] Network monitoring and logging (Syslog)

\- \[ ] Disaster recovery procedures

\- \[ ] Load balancing implementation

\- \[ ] QoS (Quality of Service) configuration

\- \[ ] VoIP integration for medical communications



\---



\## 📁 Project Files



\- `PFM103BADRE BEN RABBAR.pkt` - Complete Cisco Packet Tracer topology with all configurations



\---



\## 📖 Report Contents



\*\*Sections Covered:\*\*

1\. Executive Summary

2\. Physical Analysis \& Architecture

3\. Logical Addressing Plan (VLSM)

4\. Configuration \& Implementation

5\. Infrastructure Security

6\. Testing, Verification \& Troubleshooting

7\. Technical Configuration Details

8\. Conclusion \& Recommendations

9\. Learning Outcomes



\---



\## 🎓 Learning Outcomes



This comprehensive project demonstrates:

\- ✅ Advanced network architecture design

\- ✅ VLSM subnetting optimization

\- ✅ VLAN configuration and segmentation

\- ✅ Inter-VLAN routing implementation

\- ✅ Security protocols (ACL, SSH, WPA2)

\- ✅ Network testing and troubleshooting

\- ✅ Technical documentation excellence

\- ✅ Healthcare IT requirements

\- ✅ Professional communication skills

\- ✅ Problem-solving methodology



\---



\## 👤 Author



\*\*Badre Ben Rabbar\*\*  

Network Engineering Student  

CMC - OFPPT  

Smart Medical Center Project



\---



\## 🙏 Acknowledgments



Special thanks to \*\*Mme Hajar RHILMANE\*\* for her exceptional mentorship, rigorous guidance, and emphasis on documentation excellence. Her expertise has been instrumental in transforming this project into a professional-grade network infrastructure design.



\---



\*\*Project Status:\*\* Phase 1 Complete ✅  

\*\*Last Updated:\*\* 2026-03-26  

\*\*Module:\*\* Conception de Réseau Informatique



\---



\##  How to Use This Project



1\. \*\*Open in Cisco Packet Tracer:\*\* Load `PFM103BADRE BEN RABBAR.pkt`

2\. \*\*Review Configuration:\*\* Check the device configurations

3\. \*\*Run Tests:\*\* Execute ping commands to validate connectivity

4\. \*\*Study ACL:\*\* Examine security policies

5\. \*\*Learn VLSM:\*\* Analyze subnet allocation strategy



\---



\*\*For questions or collaboration, feel free to reach out!\*\*

