# Local Environment Setup - Ansible Automation

## Table of contents
* [Overview](#overview)
* [Prerequisites](#prerequisites)
	* [Installing Git](#installing-git)
	* [Installing Ansible](#installing-ansible)
* [Running the Playbook](#running-the-playbook)
	* [Check Syntax](#check-syntax)
	* [Dry Run](#dry-run)
* [Custom Variables](#custom-variables)
* [Feedback](#feedback)

## Overview

In an attempt to find an excuse to learn some Ansible basics, I decided to write a playbook to install everything I needed on my local machine, with the idea being that all
I would need to do is install Ubuntu, git and ansible, then clone this repo and run the playbook. 

By choosing a project involving only local automation, I didn't need servers to connect to. I also didn't really see the need for an inventory, or elaborate error-handling. 
However, I could still learn how many of the components worked, as well as variable injection, and some Jinja2 tricks for default values and String-replace regex functions.

Ansible is a rapidly evolving beast, and Ubuntu has made some updates while I have worked on this too, so there has been some tweaking required along the way.

This project contains a simple Ansible playbook to set up a local development environment on an Ubuntu 20.04 machine. At the time of writing, these instructions 
would lead to installing Ansible version 2.9.6.

Running this playbook will install the following:

* OpenJDK11
* Maven (latest)
* Kotlin
* Go
* Curl
* Docker (latest)
* Docker-Compose (latest)
* .NET SDK 3.1
* .NET Core Runtime 3.1
* Python development environment packages
* NodeJS (latest)
* NPM (latest)
* create-react-app
* Angular CLI (latest)
* Notepad++
* Postman
* Insomnia
* PuTTY SSH Client
* IntelliJ IDEA Community
* Microsoft Visual Studio Code
* pgAdminIII
* MySQL Workbench
* MongoDB

## Prerequisites

To run this project, you will need the following installed:

* Ubuntu 20.04
* Git
* Ansible

#### Installing Git and Ansible

```
$ sudo apt update
$ sudo apt upgrade
$ sudo apt install git ansible
```

## Running the Playbook

```
$ ansible-playbook -vvvv -e ansible_become_pass=<sudoPassword> localEnvSetup.yml
```

### Check Syntax

```
$ ansible-playbook localEnvSetup.yml --syntax-check
```

### Dry Run

```
$ ansible-playbook -vvvv -e ansible_become_pass=<sudoPassword> localEnvSetup.yml --check
```  

## Custom Variables

Some installation versions have been parameterised. Others have not due to a personal preference of installing the latest of certain packages.

Custom variables:

* openjdk_version - default: "11"
* dotnet_version - default: "3.1"
* python_version - default: "3"

## Feedback

If you have any suggestions comments or feedback, please leave a GitHub Issue or feel free to submit a pull request.