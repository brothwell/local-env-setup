# Local Environment Setup

## Table of contents
* [Overview](#overview)
* [Prerequisites](#prerequisites)
	* [Installing Git](#installing-git)
	* [Installing Ansible](#installing-ansible)
* [Running the Playbook](#running-the-playbook)

## Overview

This project contains an Ansible playbook to set up a local development environment on an Ubuntu 19.10 machine. 
Running this playbook will install the following:

* OpenJDK9
* Maven (latest)
* Curl
* Docker (latest)
* .NET SDK 3.1
* ASP .NET Core Runtime 3.1
* .NET Core Runtime 3.1
* Python development environment packages
* Notepad++
* Postman
* PuTTY SSH Client
* Remmina Remote Desktop Client
* IntelliJ IDEA Community
* Microsoft Visual Studio Code
* pgAdminIII

## Prerequisites

To run this project, you will need the following installed:

* Ubuntu 19.10
* Git
* Ansible

#### Installing Git

```
$ sudo apt update
$ sudo apt upgrade
$ sudo apt install git
```

#### Installing Ansible

```
$ sudo apt update
$ sudo apt install software-properties-common
$ sudo apt-add-repository --yes --update ppa:ansible/ansible
$ sudo apt install ansible
```
	
## Running the Playbook

```
$ ansible-playbook -vvvv -e ansible_become_pass=<sudoPassword> localEnvSetup.yml
```