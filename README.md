# Local Environment Setup

## Table of contents
* [Overview](#overview)
* [Prerequisites](#prerequisites)
	* [Installing Git](#installing-git)
	* [Installing Ansible](#installing-ansible)
* [Running the Playbook](#running-the-playbook)
	* [Check Syntax](#check-syntax)
	* [Dry Run](#dry-run)
* [Custom Variables](#custom-variables)

## Overview

This project contains a simple Ansible playbook to set up a local development environment on an Ubuntu 20.04 machine. 
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
