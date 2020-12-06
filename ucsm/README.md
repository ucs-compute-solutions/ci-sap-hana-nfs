To configure the Cisco UCS as per SAP HANA CVD.

Adapt the variables under group_vars/all.yml

Adapt the inventory file with Management IP of the Fabric Interconnect and admin's password. 

To configure the UCSM completly for SAP HANA Solution run

    ansible-playbook -i inventory site.yml

To run a single playbook, see example below. 

    ansible-playbook -i inventory 08-create-org.yml


To configure Cisco UCS for SAP HANA below are the task performed by respective playbook, all variables are defined in group_vars/all.yml

01: Add Block of IP Address for KVM

02: Configure UCS to synchronize with NTP Server

03: UCS Chassis discovery Policy

04: Enable Server ports

05: Modify QoS System Class required for SAP HANA

06: Enable Uplink ports

06: Enable Optional Uplink ports for Backup

07: Create Uplink Port-Channel

07: Optional Uplink Port-Channel for Backup

08: Create New Org

09: Create MAC Address Pool

10: Create UUID Suffix pool

11: Create IQN Pool for iSCSI Boot

12: Create IP Pools for iSCSI Boot

13: Modify Chassis Power Policy

14: Create Power Control Policy

15: Create Network Control Policy

16: Create Host Firmware Package Policy

17: Create Local Disk Configuration Policy

18: Create Server BIOS Policy for HANA

19: Create Serial Over LAN Policy

20: Update default Maintenance Policy

21: Create VLANs for HANA 

22: Create VLAN Groups

22: Create Optional VLAN Group for Backup

23: Create Ethernet Adapter Policy

24: Create QoS policy Platinum

25: Create vNIC Templates for HANA

26: Create vNIC Placement Policy

27: Create LAN Connectivity Policy for HANA Scale Up

28: Create LAN Connectivity Policy for HANA Scale Out

29: Create iSCSI Boot Policy

41: Create Service Profile Template for HANA Scale Up

42: Create Service Profile Template for HANA Scale Out

51: Create Service Profile from template for HANA Scale Up

52: Create Service Profile from template for HANA Scale Out

61: Associate Service Profile to Server

