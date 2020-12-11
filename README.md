# Cisco UCS Converged Infrastructure for SAP HANA with NFS Storage

Ansible playbooks to configure Cisco UCS, Cisco Nexus, OS Installation and Configuration for HANA

The anible playbooks can be used configure FlexPod Datacenter for SAP Solution: https://www.cisco.com/c/en/us/td/docs/unified_computing/ucs/UCS_CVDs/flexpod_sap_ontap96.html

To get started with Ansible for Cisco UCS, please refer to https://github.com/ciscoucs/ucsm-ansible

For latest Ansible collection for managing and automing Cisco UCS Manager envrionments please refer to https://galaxy.ansible.com/cisco/ucs

Below are the main steps to deploy complete SAP HANA solution:

1. Cisco Nexus Switch Configuration, please see README.md under nxos folder

2. Cisco UCS Manager Configuration, please see README.md under ucsm folder
      
3. Configure Storage as per SAP HANA TDI Storage requirement: This repo doesn't provide storage configuration playbooks.

4. Install Operating System on Servers and Configure Operating Systems as per SAP HANA requirement. Please see README.md under os folder. 

# Example Usage to configure the complete solution for SAP HANA.  

Once Ansible is installed please adopt inventory files and variable files to run playbooks. 

1. To configure Cisco Nexus Switches:

      ansible-playbook -i nxos/inventory nxos/site.yml
      
2. To configure Cisco UCS Manager: 

      ansible-playbook -i ucsm/inventory ucsm/site.yml

3. Configure the NFS Storage as SAP HANA TDI Storage Requirement. 

4. Install the RHEL Operating System on Servers with customized Red Hat Enterprise Linux ISO with kickstart and vMedia policy on UCS Manager. 

5. To configure Operating Systems as per SAP HANA requirement:

      ansible-playbook -i os/inventory os/site.yml

