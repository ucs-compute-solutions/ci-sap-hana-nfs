OS Installation has been performed with customized Red Hat Enterprise Linux 8.1 ISO with kickstart. 

Example Kickstart file is located under os/kickstart.

Post OS installation, server will be assigned with management IP address from the dhcp server reservation. 
inventory file will created, based on dhcp reservation

To configure OS for SAP HANA below are the list of tasks: 

01:	Set IP address for all the interface other than management interface eth0 (which gets IP from dhcp server)

02:	Set the NTP server on the OS

03:	Set hostname as per SAP HANA
    
    Adapt the /etc/hosts file as per your requirement, example /etc/hosts file is in 
    os/config_files/su_hosts for scale up system  
    os/config_files/so_hosts for scale out system

04:	Register the server for RedHat for SAP Solutions update

05:	Update the RedHat system with latest patches

06:	Configure OS for optimal settings SAP HANA as per SAP Notes
    
    RHEL System Roles for SAP is used for configuring kernel parameters and services. To use these roles install rhel-system-roles-sap and define role path in configuration file   
    
07:	Regenerate grub for persistent Kernel parameters

08:	Install Cisco enic and fnic drivers

11: For the servers with Intel DCPMM, install the tools required to manage PMEM

12: Configure Intel DCPMM for SAP HANA

21: Mount the volumes created on storage for SAP HANA persistent storage.


To configure the RHEL OS as per SAP HANA CVD.

Adapt the variables under group_vars/all.yml and host_vars/

Adapt the inventory file with Management IP of the OS. 

To configure the OS for SAP HANA completly run

    ansible-playbook -i inventory site.yml 

To run a single playbook, see example below

    ansible-playbook -i inventory 99-reboot.yml
    
To configure Intel DCPMM for SAP HANA run 

    ansible-playbook -i inventory 11-optane-install-tools.yml
    ansible-playbook -i inventory 12-configure-optane.yml


