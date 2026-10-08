# Packet Tracer - Configure a Wireless Router and Clients

## 📌 Project Overview
This lab demonstrates how to set up a small home/SOHO network using Cisco Packet Tracer. The setup includes cabling physical devices (Coaxial and Copper Straight-Through), configuring a SOHO Wireless Router (DHCP, Wireless SSID, WPA2 Personal Security, and Admin Credentials), and validating end-to-end internet connectivity across wired and wireless hosts.

---

## 📐 Network Topology
![Network Topology](docs/topology.png)

---

## 🛠️ Configuration Summary

### 1. Physical Cabling & Connections
* **Coaxial:** Connected Cable Splitter (`Coaxial1` & `Coaxial2`) to Cable Modem (`Port 0`) and TV (`Port 0`).
* **WAN Link:** Cable Modem (`Port 1`) → Wireless Router (`Internet Port`).
* **LAN Connections:** 
  * Office PC (`FastEthernet0`) → Wireless Router (`GigabitEthernet 1`).
  * Bedroom PC (`FastEthernet0`) → Wireless Router (`GigabitEthernet 2`).

### 2. SOHO Wireless Router Configuration
* **DHCP Scope:** Set Maximum Number of Users to `10`.
* **Management Security:** Changed admin password to `MyPassword1!`.
* **2.4 GHz Wireless LAN:**
  * **SSID:** `MyHome`
  * **Security Mode:** `WPA2 Personal`
  * **Passphrase:** `MyPassPhrase1!`

### 3. Client IP Addressing & Connectivity
* **Office PC & Bedroom PC:** Configured via DHCP (`192.168.x.x` scope).
* **Laptop:** Connected wirelessly to `MyHome` SSID via WPA2 authentication.
* **Verification:** All endpoints successfully loaded `skillsforall.srv` via the built-in web browser.

---

## 🧪 Verification & Testing

| Device | Connection Type | IP Allocation | Tested Service | Status |
| :--- | :--- | :--- | :--- | :--- |
| **TV** | Coaxial | N/A | Cable TV Signal | ✅ Pass |
| **Office PC** | Wired (Ethernet) | DHCP | `http://skillsforall.srv` | ✅ Pass |
| **Bedroom PC**| Wired (Ethernet) | DHCP | `http://skillsforall.srv` | ✅ Pass |
| **Laptop** | Wireless (2.4 GHz) | DHCP | `http://skillsforall.srv` | ✅ Pass |

---

## 📁 Repository Contents
* `Packet-Tracer-Configure-a-Wireless-Router-and-Clients.pka`: Original Packet Tracer activity file with completed configurations.
* `docs/`: Contains screenshots verifying topology and connectivity tests.
