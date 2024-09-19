# DevOps Training - Ansible Playbooks

This repository contains Ansible playbooks and roles designed for automating the deployment and configuration of a multi-tier architecture, 
which includes a web server, application server, and database server.
The purpose of this project is to demonstrate how to utilize Ansible for infrastructure provisioning in a consistent and repeatable manner.
## Introduction

In modern software development, a multi-tier architecture is commonly used to separate different concerns of an application, improving 
scalability and manageability. This repository focuses on automating the deployment of:

- **Web Server**: Serves static content and acts as a reverse proxy to the application server.
- **Application Server**: Hosts the application logic and communicates with the database.
- **Database Server**: Manages the data storage and retrieval for the application.

The use of Ansible helps streamline the configuration management process, making it easier to deploy applications reliably across different environments.

## Prerequisites

Before you begin, ensure that you have the following:

- **Ansible**: Ensure Ansible is installed on your control machine. You can add the PPA and install it using the following commands:

  ```bash
  sudo apt update
  sudo apt install software-properties-common
  sudo add-apt-repository --yes --update ppa:ansible/ansible
  sudo apt install ansible

-**Run the Playbook**: To run the Ansible playbooks, ensure you have an inventory file set up and use the following command to deploy the web server:
ansible-playbook -i inventory.ini deploy_webserver.yml
**SSH Access**: Ensure you have SSH access to all target servers defined in the inventory file.
