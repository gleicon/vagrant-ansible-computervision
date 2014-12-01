# Vagrant file and ansible provisioning for SciPy/Opencv and friends

This repository contains a Vagrantfile and Ansible setup to create an Ubuntu 14.04 machine able to run opencv based applications.

# Requirements

    - Vagrant
    - Ansible installed locally
    - Internet connection

# Usage

## Locally with Vagrant

$ vagrant up 
$ vagrant ssh

## Remotely with your cloud of preference
    
    - Add your hostname to ansible hosts file (/etc/ansible/hosts or any other location, you can change that)
        [scipy]
        host1 ansible_ssh_host=192.168.1.1

    - Make sure you can ssh into it using keys
        ssh root@192.168.1.1

    - Run 
        ansible-playbook -l host scipy.yml

    - Send me a pull request in case it doesn't works.

