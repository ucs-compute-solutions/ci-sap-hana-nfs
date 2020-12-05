OS Installation has been performed with customized Red Hat Enterprise Linux 8.1 ISO with kickstart. 

Example Kickstart file is located under os/kickstart

Post OS installation, server will be assigned with management IP address from the dhcp server reservation. 
inventory file will created, based on dhcp reservation

To configure OS for SAP HANA below are the list of tasks: 

01:	Set IP address for all the interface other than management interface eth0 (which gerts IP from dhcp server)

02:	Set the NTP server on the OS

03:	Set hostname as per SAP HANA

04:	Register the server for RedHat for SAP Solutions update

05:	Update the RedHat system with latest patches

06:	Configure OS for optimal settings SAP HANA as per SAP Notes
    
    RHEL System Roles for SAP is used for configuring kernel parameters and services. To use these roles install rhel-system-roles-sap and define role path in configuration file   
    
07:	Regenerate grub for persistent Kernel parameters

08:	Install Cisco enic and fnic drivers

11: For the servers with Intel DCPMM, install the tools required to manage PMEM

12: Configure Intel DCPMM for SAP HANA

21: Mount the volumes created on storage for SAP HANA persistent storage.




