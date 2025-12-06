# OpenWRT WallysTech DR5018S Wireless Mesh Project

[![WallysTech Official Website](https://img.shields.io/badge/WallysTech-Official_Website-blue?style=for-the-badge&logo=web)](https://www.wallystech.com/)
[![Contact Us](https://img.shields.io/badge/Contact-support%40wallystech.com-green?style=for-the-badge&logo=gmail)](mailto:support@wallystech.com)

## 🔥 Featured Product: WallysTech DR5018S

**Wallys Communications (Suzhou) Co., Ltd.** proudly introduces the **DR5018S High-Performance Wi-Fi 6 Router Board**, specifically designed for large-scale Mesh networking and enterprise-level applications.

### Core Product Advantages

- ✅ **Wi-Fi 6 Technology**: Supports 802.11ax standard with MU-MIMO and OFDMA technology
- ✅ **Multi-band Concurrent Operation**: Simultaneous operation on multiple frequency bands
- ✅ **Multiple Version Options**: (2.4GHz+5GHz+6GHz), (2.4GHz+5GHz+5GHz), (5GHz+5GHz)
- ✅ **Enterprise-Grade Stability**: Industrial-grade design for 7×24 hours continuous operation
- ✅ **Hardware Acceleration**: Integrated Qualcomm NSS network acceleration engine
- ✅ **Flexible Deployment**: Supports PoE power supply for convenient large-scale deployment

**Get product quotations and technical documentation now: support@wallystech.com**

## 📋 Project Overview

This project provides a complete OpenWRT custom firmware solution for the **WallysTech DR5018S** router board, specifically optimized for enterprise-level Mesh networking applications.

## 🚀 Key Features

### 1. **High-Performance Platform Based on IPQ5018**

   - Qualcomm IPQ5018 chip, dual-core ARM Cortex-A53 @ 1.0GHz
   - 512MB DDR3L system memory, 128MB NAND Flash storage
   - Hardware NAT acceleration supporting high-concurrency network connections

### 2. **Complete Mesh Network Support**

   - Natively integrated B.A.T.M.A.N. Advanced Mesh protocol
   - Supports multi-hop routing and dynamic topology discovery
   - Automatic link quality assessment and routing optimization

### 3. **Enterprise-Level Functions**

   - Supports WPA3 enterprise-grade security encryption
   - VLAN isolation and multi-SSID management
   - Centralized network management and monitoring
   - Supports Captive Portal and billing systems

## 📸 System Interface Display

### System Status Monitoring

![System Status](include/images/status.png)
*Figure 1: Overall system status monitoring interface*

### Mesh Network Overview

![Mesh Network Status](include/images/mesh1.png)
*Figure 2: Mesh network operation status and connection information*

### Network Topology Management

![Mesh Network Topology](include/images/mesh3.png)
*Figure 3: Mesh network topology structure visualization*

### Node Status Monitoring

![Mesh Peer Nodes](include/images/mesh4.png)
![Mesh Peer Nodes](include/images/mesh2.png)
*Figures 4 & 5: Mesh node status and neighbor information*

## 🔧 Technical Specifications

### Hardware Specifications

- **Main Chip**: Qualcomm IPQ5018
- **CPU Architecture**: Dual-core ARM Cortex-A53 @ 1.0GHz
- **System Memory**: 512MB DDR3L
- **Storage**: 8MB NOR Flash + 128MB NAND Flash
- **Wi-Fi Standard**: 802.11ax (Wi-Fi 6)
- **Frequency Band Support**: 2.4GHz (574Mbps) + 5GHz (1201Mbps)
- **Ethernet Interfaces**: 1× Gigabit WAN + 1× Gigabit LAN
- **Antenna Interfaces**: 4× MMCX (2.4GHz×2 + 5GHz×2)
- **Power Input**: 12V/2A DC or 802.3at PoE
- **Operating Temperature**: -20°C to 70°C

### Software Features

- **Mesh Protocol**: B.A.T.M.A.N. Advanced
- **Management Interface**: Web GUI + CLI + API
- **Security Features**: WPA3, Firewall, VPN support
- **Remote Management**: Supports TR-069, SSH, SNMP

**Detailed technical specifications available at: [WallysTech DR5018S Product Page](https://www.wallystech.com/WiFi6_product/DR5018S-wifi6-IPQ5018-2.4G-5G-6G-triband-11ax-MU-MIMO-OFDMA-QCN6122-QCN6102.html)**

## 🛠️ Quick Start

### Compilation Environment Setup

```bash
# Clone the project repository
git clone https://github.com/Wallystech/openwrt_DR5018.git
cd openwrt-dr5018s

# Update software sources
./scripts/feeds update -a
./scripts/feeds install -a

# Compile firmware (.config file is already in root directory, pre-configured for DR5018S optimization)
make V=99
```

## 🏢 About Wallys Communications

**Wallys Communications (Suzhou) Co., Ltd.** is a high-tech enterprise specializing in the research, development, and manufacturing of wireless communication equipment. With over 10 years of industry experience, we provide high-quality wireless communication solutions to global clients.

### Our Services

- **Product Customization**: Customize hardware and software according to customer requirements
- **Technical Support**: Provide professional technical support and solutions
- **Bulk Supply**: Support OEM/ODM, ensuring stable supply
- **Quality Assurance**: All products undergo strict quality testing

### Contact Us

- **Official Website**: [https://www.wallystech.com/](https://www.wallystech.com/)
- **Business Cooperation**: support@wallystech.com
- **Technical Support**: jason@wallystech.com

## 🤝 Contribution

We welcome submitting Issues and Pull Requests to help improve this project.

---

**For business cooperation or bulk purchases, please contact directly: support@wallystech.com**
