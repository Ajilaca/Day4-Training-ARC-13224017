# Day4-Training-ARC-13224017
Topology
Topology You will receive one of three possible topologies.
| Device    | Interface | IP Address              | Default Gateway |
|-----------|-----------|-------------------------|----------------|
| College   | G0/0      | 10.10.10.1/24           | N/A            |
|           |           | 2001:DB8:ACAD:100::1/64 | N/A            |
|           | G0/1      | 10.10.11.1/24           | N/A            |
|           |           | 2001:DB8:ACAD:200::1/64 | N/A            |
| Class-A   | VLAN 1    | 10.10.10.100/24         | 10.10.10.1     |
| Class-B   | VLAN 1    | 10.10.11.100/24         | 10.10.11.1     |
| Student-1 | NIC       | 10.10.10.101/24         | 10.10.10.1     |
|           |           | 2001:DB8:ACAD:100::50/64| FE80::2        |
| Student-2 | NIC       | 10.10.10.102/24         | 10.10.10.1     |
|           |           | 2001:DB8:ACAD:100::60/64| FE80::2        |
| Student-3 | NIC       | 10.10.11.101/24         | 10.10.11.1     |
|           |           | 2001:DB8:ACAD:200::50/64| FE80::3        |
| Student-4 | NIC       | 10.10.11.102/24         | 10.10.11.1     |
|           |           | 2001:DB8:ACAD:200::60/64| FE80::3        |

Objectives
- Complete the network documentation.
- Perform basic device configurations on a router and a switch.
- Verify connectivity and troubleshoot any issues.

Scenario
Your network manager is impressed with your performance in your job as a LAN technician. She would like you to demonstrate your ability to configure a router that connects two LANs. Your tasks include configuring basic settings on a router and a switch using the Cisco IOS. You will also configure IPv6 addresses on network devices and hosts. You will verify the configurations by testing end-to-end connectivity. Your goal is to establish connectivity between all devices.

Note: The VLAN1 interfaces on the switches will not be reachable over IPv6.
In this activity, you will configure the College router, Class-B switch, and the PC hosts.
Note: Packet Tracer will not score some configured values, however these values are required to accomplish full connectivity in the network.
Konfigurasi Router

Jalankan perintah berikut pada mode konfigurasi router untuk mengaktifkan IPv6 dan mengonfigurasi antarmuka jaringan:
## Router Configuration

```bash
enable
configure terminal
ipv6 unicast-routing
interface g0/0
 ipv6 address 2001:DB8:ACAD:100::1/64
 ipv6 enable
 no shutdown
 exit
interface g0/1
 ipv6 address 2001:DB8:ACAD:200::1/64
 ipv6 enable
 no shutdown
 exit
exit

