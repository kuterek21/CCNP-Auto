# [CCIE-Auto Link](https://github.com/kuterek21/CCIE-AUTO/blob/main/README.md)
# CCNP Automation 

## Table of Content

- [Tools](#Tools)
- [Python part](#First_lesson)
- [Librarys](#Librarys)        
- [API](#API)
- [Ansible](#Ansible)
- [Git](#VCS_Version_Control_System)
- [PyATS](#PyATS)

## Tools
- Visual Studio Code
- PyCharm
- [PIP]()
- Git
- [venv](https://github.com/kuterek21/Python_for_Cisco/blob/main/VENV%20steps)

## Librarys

[pypi.org](https://pypi.org/project/netmiko/)

To be able to insall Libraires we need to install PIP
- Netmiko
- Paramiko
- PyATS
- Genie

## [First_lesson](http://github.com/kuterek21/Python_for_Cisco/blob/main/1.%20First%20lesson%20-%20print) 

    - print("Hello World")

## [Function](https://github.com/kuterek21/CCNP-Auto/blob/main/4.0%20Funcion)

to use it from another file:
 - import FILENAME
 - FILENAME.function_name()

or

from FILENAME import function_name

and call it

function_name()


## [Lists](https://github.com/kuterek21/Python_for_Cisco/blob/main/2.2.1%20Lists)

    - [a1, b2,c3,d4]
### Lists

    - example:
        my_list = [Palo_alto, Cisco, Aruba, F5, Juniper, Fortigate]

        -       form netmiko import ConnectHandler

                connect = ConnectHandler(
                  device_type = "cisco_ios",
                  host = "192.168.1.101",
                  username = "admin",
                  username = "cisco"
                )
                
                interface_details = ["interface loop 10","ip addreess 10.10.10.1 255.255.255.0","descr Test 1","no shut"]
                
                config = connect.sent_config_set(interface_details)

## [Loops](https://github.com/kuterek21/Python_for_Cisco/blob/main/3.%20Loops%20-%20multiple%20devicess)
    
    - for an_element in mylist:
          print(an_element)

## [Strings](https://github.com/kuterek21/Python_for_Cisco/blob/main/2.2.2%20Strings)

- lower
- upper
- format
- input

# [Week-2 Netmiko]

Prepare your device by installing:

### - [Netmiko-install](https://github.com/kuterek21/CCNP-Auto/blob/main/2.0%20Netmiko%20install)
     
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
    
 Connecting to the device with Netmiko run a script.

 ## [Second_lesson_Netmiko](https://github.com/kuterek21/Python_for_Cisco/blob/main/2.1%20Netmiko%20send_command())

SSH to the devices using Netmiko

        - send_command()    # executes command in Privileged mode 
        
        - send_config_set() # executes command in Config mode

# [Week-3 Netconf](https://github.com/kuterek21/CCNP-Auto/blob/main/6.%20Netconf)

Day 5


Day 6
    - Model driven programibility (MDP)
    - 



# [Ansible](https://github.com/kuterek21/Python_for_Cisco/blob/main/7.%20Ansible)
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


# [GIT](https://github.com/kuterek21/Python_for_Cisco/blob/main/8.%20Git)

## VCS_Version_Control_System

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


# [PyATS](https://github.com/kuterek21/Python_for_Cisco/blob/main/9.%20PyATS)

### Install PyATS use venv
        - python -m venv .
        - ls -a
        - source .venv/bin/activate
        - deactivate
 - pip install pyats[full]
 - pip show pyats 


        

