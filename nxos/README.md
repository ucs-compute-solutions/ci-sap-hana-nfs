To configure the Nexus swiches as per SAP HANA CVD.

Adapt the variables under group_vars/all.yml and host_vars/

Adapt the inventory file with Management IP of the switches and admin's password. 

To configure the switches completly run

    ansible-playbook -i inventory site.yml 

To run a single playbook run

    ansible-playbook -i inventory site.yml 01-features-gobal-settings.yml
