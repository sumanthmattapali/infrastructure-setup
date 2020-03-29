Playbook
=========

This playbook has below roles:

    - jenkins-installation-role

All common variables are reused from common/defaults/main.yml


To run this Playbook
----------------

To configure Jenkins on your CentOS or MacOS just paste the below commands in terminal:


Local machine
----------------

    Command to run:  ansible-playbook -i inventory/local playbook.yml
    
Remote machine
----------------

Pre-requisites:

Create a new inventory file like staging, uat or production

    inventory/staging
        [group-name]
        centos ansible_host=<ip_address_of_the_remote_machine> ansible_user=<user_of_remote_machine>

    Command to run:  ansible-playbook -i inventory/local playbook.yml -k ( Will prompt to enter remote machine password )


