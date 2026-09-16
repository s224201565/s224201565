## Hi there 👋

<!--
**s224201565/s224201565** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.
 Berlin Campus Network — Cisco Configurations

Enterprise campus network design and configuration for a multi-layer switched environment, built as part of the Advanced Diploma in Information Technology at Nelson Mandela University.

## Network overview

A three-tier campus network (access, distribution, core) with full redundancy, implementing:

| Feature | Purpose |
|---------|---------|
| **VLANs & VTP** | 13 VLANs segmenting departments, voice, guest, and management traffic |
| **Trunk links** | Inter-switch VLAN traffic with native VLAN 99 |
| **OSPF** | Dynamic routing across the network (Area 0) |
| **HSRP v2** | First-hop redundancy — MLS1 active for VLANs 10–50, MLS2 active for 60–115 |
| **STP (Rapid PVST+)** | Loop prevention with PortFast and BPDU Guard |
| **DHCPv4** | Automatic IP addressing per VLAN with split-scope redundancy |
| **NAT (PAT)** | Overload NAT on dual WAN links for internet access |
| **ACLs** | Traffic filtering and access control |
| **Port security** | MAC sticky learning with restrict violation mode |
| **SSH v2** | Secure remote management (RSA 2048-bit, local auth) |
| **Telephony (CME)** | Voice VLAN 110 with Cisco Unified CallManager Express (8 phones) |
| **Unused port hardening** | Shutdown + VLAN 999 assignment on all unused ports |

## Network topology

```
        [ISP1]────Serial────[Berlin1]────Serial────[ISP2]
                              │    │                 │
                             f0/0  f0/1             │
                              │    │           [Berlin2]
                              │    │            │    │
                    ┌─────────┘    └──────┐    f0/0  f0/1
                    │                     │    │     │
                 [B.MLS1]─────────────[B.MLS2]─┘     │
                 (VTP Server)        (VTP Server)────┘
                    │                     │
          ┌────┬───┼───┬────┐    ┌────┬───┼───┬────┐
        ALS1 ALS2 ALS3 ALS4  ALS5 ALS6 ALS7 ALS8
        V10  V20  V30  V40   V50  V60  V70  V80
```

## Devices configured

- **Access-layer switches:** ALS1–ALS8 (VTP clients, port security, PortFast)
- **Distribution/core multilayer switches:** B.MLS1, B.MLS2 (VTP servers, HSRP, OSPF, DHCP)
- **Edge routers:** Berlin1, Berlin2 (OSPF, NAT, CME telephony, SSH)
- **ISP routers:** ISP1, ISP2 (WAN simulation)

## IP addressing

| Network | Subnet | Purpose |
|---------|--------|---------|
| 172.16.10.0/24 | VLAN 10 | Accounting & Finance |
| 172.16.20.0/24 | VLAN 20 | ICT Services |
| 172.16.30.0/24 | VLAN 30 | Human Resources |
| 172.16.40.0/24 | VLAN 40 | Executive Management |
| 172.16.50.0/24 | VLAN 50 | Legal |
| 172.16.60.0/24 | VLAN 60 | Sales & Marketing |
| 172.16.70.0/24 | VLAN 70 | Operations |
| 172.16.80.0/24 | VLAN 80 | Research & Development |
| 172.16.90.0/24 | VLAN 90 | Guest |
| 172.16.100.0/24 | VLAN 100 | Management |
| 172.16.110.0/24 | VLAN 110 | Voice |
| 172.16.115.0/24 | VLAN 115 | Wireless |
| 208.0.0.0/30, /30, /30, /30 | WAN | Public ISP links |

## Tools used

- Cisco Packet Tracer / GNS3
- Cisco IOS CLI

## Repository structure

```
├── README.md
└── configs/
    ├── ALS1.txt        # Access switch — VLAN 10 (Accounting & Finance)
    ├── ALS2.txt        # Access switch — VLAN 20 (ICT Services)
    ├── ALS3.txt        # Access switch — VLAN 30 (Human Resources)
    ├── ALS4.txt        # Access switch — VLAN 40 (Executive Management)
    ├── ALS5.txt        # Access switch — VLAN 50 (Legal)
    ├── ALS6.txt        # Access switch — VLAN 60 (Sales & Marketing)
    ├── ALS7.txt        # Access switch — VLAN 70 (Operations)
    ├── ALS8.txt        # Access switch — VLAN 80 (Research & Development)
    ├── B.MLS1.txt      # Core MLS — HSRP active VLANs 10-50, DHCP, OSPF
    ├── B.MLS2.txt      # Core MLS — HSRP active VLANs 60-115, DHCP, OSPF
    ├── Berlin1.txt     # Edge router — NAT, OSPF, CME telephony
    ├── Berlin2.txt     # Edge router — NAT, OSPF, CME telephony
    ├── ISP1.txt        # ISP router (WAN simulation)
    └── ISP2.txt        # ISP router (WAN simulation)
```

## Author

**Singalakha Nguluzane**
Advanced Diploma in Information Technology — Nelson Mandela University
Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
