# Deploy percona mysql master-slave
Use playbook to build percona mysql server 5.7 on Ubuntu 18.04
This playbook enabled audit plugin format JSON and validate password
Recommend use ansible vault to encrypt password for ansible variable file

Push host in group mysql and make sure following variables exist in each host
- mysql_master # define mysql master host
- mysql_slave # define mysql slave host
- mysql_id  # define mysql id

# RUN: 
``
ansible-playbook -i inventories/mycluster/hosts.yaml mysql-cluster.yml
``


# Author
quyetmv@gmail.com
