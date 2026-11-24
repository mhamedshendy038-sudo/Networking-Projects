<img width="1920" height="646" alt="Cisco Packet Tracer - C__Users_HP_Cisco Packet Tracer 9 0 1_saves_network shendy 1 pkt 11_22_2026 12_42_09 AM" src="https://github.com/user-attachments/assets/96ddd9b9-f833-41b4-be1e-e6a94ece566a" />
# Enterprise Campus Network – Switching & Network Infrastructure

## Project Overview

This project focuses on designing and implementing an Enterprise Campus Network using **Cisco Packet Tracer**. The main goal is to build a structured and reliable network infrastructure that connects multiple departments while providing efficient communication, network segmentation, and redundancy.

The network follows the hierarchical campus design approach, with multiple switching layers and interconnected end devices, including PCs, laptops, and IP phones.

## Network Architecture

The network is divided into three main layers:

- **Core Layer:** Built using a Cisco Catalyst 3560 Multilayer Switch, responsible for handling inter-VLAN routing and providing connectivity between different parts of the network.
- **Distribution Layer:** Consists of multiple switches that connect the core to the access layer, providing redundancy and aggregated links.
- **Access Layer:** Uses Cisco Catalyst 2960 switches to connect end devices such as computers, laptops, and IP phones.

## Technologies & Features Implemented

### 1. VLAN Configuration

The network is divided into separate VLANs to organize devices and isolate traffic between departments.

- VLAN 10 – DEPT-A: `192.168.10.0/24`
- VLAN 20 – DEPT-B: `192.168.20.0/24`
- VLAN 30 – DEPT-C: `192.168.30.0/24`
- VLAN 40 – DEPT-D: `192.168.40.0/24`
- VLAN 50 – VOICE:  `192.168.50.0/24`
- VLAN 60 – MGMT:   `192.168.60.0/24`
### 2. Inter-VLAN Routing

Configured inter-VLAN communication using Switch Virtual Interfaces (SVIs) on the multilayer core switch. This allows devices in different VLANs to communicate with each other.

### 3. EtherChannel

Implemented EtherChannel between network switches to combine multiple physical connections into logical links, improving bandwidth utilization and providing link redundancy.

### 4. Spanning Tree Protocol (STP)

Configured STP to prevent Layer 2 switching loops and maintain a stable network topology.

- Configured primary and secondary root bridges.
- Enabled PortFast on end-device ports for faster connectivity.

### 5. VLAN Trunking Protocol (VTP)

Used VTP to simplify VLAN management and distribution across switches.

- Configured VTP Server and Client roles.
- Applied a common VTP domain and password.
- Enabled VLAN propagation between connected switches.

### 6. Voice VLAN Configuration

Configured IP phone connections to support both data and voice traffic through the same access port.

- Data traffic is assigned to the appropriate data VLAN.
- Voice traffic is assigned to VLAN 40.

### 7. DHCP Configuration

Configured DHCP services on the core multilayer switch to automatically assign IP addresses to network devices.

- Created separate DHCP pools for the different VLANs.
- Excluded reserved IP addresses.
- Configured Option 150 for IP phone provisioning.

### 8. Network Device Security

Applied basic security configurations to protect network devices and control administrative access.

- Console password protection.
- Enable secret configuration.
- SSH remote management using SSHv2.
- Local username and password authentication.

## Credentials & Device Access

The following credentials are used for accessing network devices in Cisco Packet Tracer:

- **Enable Secret Password:** `mohamed303`
- **Console Password:** `mohamed303`
- **SSH Username:** `admin`
- **SSH Password:** `mohamed303`
- **VTP Domain:** `instant.local`
- **VTP Password:** `mohamed303`

## Testing & Verification

After completing the configuration, several tests were performed to check the network operation:

- Verified connectivity between devices in different VLANs using Ping.
- Checked EtherChannel operation using `show etherchannel summary`.
- Verified trunk links and VLAN information using `show interfaces trunk`.
- Checked VLAN distribution across switches.
- Tested DHCP to ensure that end devices receive IP addresses automatically.
- Verified secure remote access through SSH.

## Tools Used

- Cisco Packet Tracer
- Cisco Catalyst 3560 Multilayer Switch
- Cisco Catalyst 2960 Switch
- PCs, Laptops, and IP Phones
- Cisco IOS CLI

## Project Files

The repository includes the Cisco Packet Tracer project file (`.pkt`) containing the network topology and device configurations, along with screenshots illustrating the network design.

## Conclusion

This project provided practical experience in building and managing an enterprise campus network. It combines several important switching technologies, including VLANs, inter-VLAN routing, EtherChannel, STP, VTP, DHCP, and network device security.

The implementation demonstrates how different network layers work together to provide a scalable, organized, and reliable network infrastructure.

---

**Simulation Tool:** Cisco Packet Tracer

**Project Type:** Enterprise Campus Network Design & Switching Implementation
