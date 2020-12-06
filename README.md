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


