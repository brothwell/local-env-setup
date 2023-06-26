# Local Environment Setup - Ansible Automation

## Overview

This project contains a simple Ansible playbook to set up a local development environment on an Ubuntu 22.04 machine. Snapd installations were only used where absolutely necessary. 
At the time of writing, these instructions would lead to installing Ansible version 2.10.8.

Running this playbook will install the following:

* GU FW
* OpenJDK11
* Maven (latest)
* Kotlin
* Go
* Curl
* Kubectl
* Kustomize
* Docker (latest)
* Docker-Compose (latest)
* .NET Core (SDK and Runtime) 7
* Python development environment packages
* NodeJS 18
* NPM (latest)
* create-react-app
* Angular CLI (latest)
* Sublime Text
* Postman
* Insomnia
* PuTTY SSH Client
* OpenVPN Client
* IntelliJ IDEA Community
* Microsoft Visual Studio Code
* Microsoft Teams
* pgAdmin4
* MySQL Workbench
* MongoDB
* ClamAV & ClamTK

It will also disable the service that auto-adds network printers.

*NB: You will need to reboot after running this playbook for your user to have access to the Docker CLI*

## Prerequisites

To run this project, you will need the following installed:

* Ubuntu 20.04+
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
$ ansible-playbook -vvvvK -e username=<yourUsername> localEnvSetup.yml
```

### Check Syntax

```
$ ansible-playbook localEnvSetup.yml --syntax-check
```

### Dry Run

```
$ ansible-playbook -vvvvK -e username=<yourUsername> localEnvSetup.yml --check
```  

## Custom Variables

Some installation versions have been parameterised. Others have not due to a personal preference of installing the latest of certain packages.

Custom variables:

* openjdk_version - default: "11"
* node_version - default: "18"
* dotnet_version - default: "6"
* python_version - default: "3"

## Feedback

If you have any suggestions, comments or feedback, please leave a GitHub Issue or feel free to submit a pull request.
