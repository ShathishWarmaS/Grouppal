Task:Configure vagrant and create a couple of servers (centos7 and ubuntu)

Using Ansible deploy hello world index page another server need to copy the previous index file to the other nodes

Configure ansible in centos 7 inside the vagrant vm

One is dev. Another one is prod

1. Directory Structure

Create a project directory that holds all the necessary files for Vagrant, Ansible, and configurations.

Grouppal/
├── Vagrantfile
├── ansible/
│   ├── hosts.ini
│   └── deploy_hello_world.yml

2.	Start the VMs:
Run the following command to create and start the VMs:

vagrant up

3.	SSH into the CentOS 7 VM:
After the VMs are up, connect to the CentOS 7 server (the Ansible control node):
vagrant ssh centos7
4.	Run the Ansible Playbook:
On the CentOS 7 VM, navigate to the ansible/ directory and run the playbook:
cd /vagrant/ansible
ansible-playbook -i hosts.ini deploy_hello_world.yml