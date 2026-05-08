# CCNP Automation  / CCIE

## Table of Content

- [Tools]
- [Python part](#First_lesson)
   - Netmiko
- [Ansible](#Ansible)
- [Git](#VCS_Version_Control_System)

## Tools
- Visual Studio Code
- PyCharm
- Git
## First_lesson 

 - print("Hello World")
 - String - letters, symbols
 - Integers - full numbers
 - Floats - decimal numbers
 - Boolean True/False

-Netmiko



   
## Ansible

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
  

