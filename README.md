# CCNP Automation  / CCIE

## Table of Content

- [Tools](#Tools)
- [Python part](#First_lesson)
- [Librarys](#Librarys)
- [Ansible](#Ansible)
- [Git](#VCS_Version_Control_System)

## Tools
- Visual Studio Code
- PyCharm
- PIP
- Git
## First_lesson 

    - print("Hello World")
    - String - letters, symbols
    - Integers - full numbers
    - Floats - decimal numbers
    - Boolean True/False
    - Lists - [a1,b2,c3 ]
    
1. Function
   - def greeting():   // create a content of that funcion which you want to resue in the future
     -   print("welcome")
     -   print("to the course")
     -   print("Cisco Auto")
   - greetint()    // to run it - just call that funcion

To import we use either
import greeting
to call it
test.greeting()
or
from FILE_NAME import greeting
and then I use it as
greeting()
or
from FILE_NAME
Funcions def


## Librarys

[pypi.org](https://pypi.org/project/netmiko/)

To be able to insall Libraires we need to install PIP

- Netmiko
- Paramiko
- PyATS

### - PIP
     
    - sudo apt-get install pip

### - Netmiko
    
    - sudo apt-get install python3-netmiko

    - pip show netmiko 
    
#### Netmiko elements

        - ConnectHandler()
        - send_command()
        - send_config_set()
##### Netmiko examples

    from netmiko import ConnectHandler
    
    print("We are going to test our network ")
    print("--------------------------------------------------------------------------")
    
    connect = ConnectHandler(
        device_type = "cisco_ios",
        host = "192.168.1.101",
        username = "admin",
        password = "cisco"
    )
    
    ssh = connect.send_command("show ver | i uptime ")
    print(ssh)
    print("-------------------------------------------------------------------------")


##################################################################################################################
# Ansible
### Install dependencies

- pip install paramiko
- pip show paramiko - to check if paramiko is available
!
// sudo apt insall software-properties-common
// sudo apt-add-reposirtory --yes --update ppa:ansible/ansible
// sudo apt install ansible
--------------------------------------------------------------
mkdir ansible // create your folder
cd ansible

### touch inventory.ini

- R1 ansible_host=
- R1 ansible_user=
- R1 ansible_password=
- R1 ansible_network_os=ios
### touch myplaybook.yml    
---
- name: Play_1
    tasks:
        - name: task1

        - name: task2

        - name: task3

- name: Ansible_playbook
  hosts: all // all the devices specified in the inventory file
//hosts: Switches o  r Routers or R1,R2
  gather_facts: false
  connection: network_cli 
  tasks: 
     - name: Configure Loopback on R1
       description: Configured by Ansible
       enabled: true
     - name: task2
     - name: task3
# GIT
## VCS_Version_Control_System
  " Git "
### Install GIT
   -   sudo apt install git
### Git config 
   - git config --global user.name "Mariusz"
   - git config --global user.email "m@wp.pl"
### Git commands
 - git status // to check to state of our repo
 - git init // initiate emty git repo in a folder ( .git )
 - // to delete git file - rm -rf .git/
 - git add test.py
 - git commit -m "Add a note"
### Git upload to GitHub
 - GitLab / profile / personal access tokens / Generate token
 -  git psuh --set-upstream https://gitlab.com/kuterek21/GIT_FUNDEMANTALS_2026.git main
  

