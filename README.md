Role Name
=========

This role is designed to wrap up odoo PM into debian buster containers

Requirements
------------

All pre-requisites are embeded into the compose files

Role Variables
--------------

###### Better do not touch these avriables, to ensure docker up after server powercycle
docker_service_state: 
docker_service_enabled: 


###### Use this variable to set up a docker service enabled user
docker_users:

 ###### This variable could be uded to segragate odoo network from default docker network bridge ==> Next Step for my setup
odoo_network_name: 


##### Example Playbook
----------------
Define inventory and ensure server hostname is reachable from ansible host and run the bellow playbook as shown

* hosts: your_server_hosname
  * become: true
  * roles:
     * OdooDockerAnsibRole

user@ansiblehost# ansible-playbook -i inventory playbook.yaml 
License
-------

Use at your risk and do not forget to ping when enhanced

Author Information
------------------

Check meta for contact info
