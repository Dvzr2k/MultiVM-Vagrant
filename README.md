# Multi-VM Setup with Vagrant

This repository contains a Vagrant configuration for setting up a multi-VM environment consisting of two web servers and one database server. This setup applies principles of Infrastructure as Code (IaC) to automate the creation and provisioning of virtual machines.

## Features

- **Automated Setup**: Utilizes Vagrant to automatically configure a multi-VM environment.
- **Infrastructure as Code**: Configuration and provisioning are scripted for consistency and reproducibility.
- **Web Servers**: Two web servers running Ubuntu 20.04 with Apache installed.
- **Database Server**: One database server running CentOS 7 with MariaDB installed.

## Prerequisites

- [Vagrant](https://www.vagrantup.com/downloads)
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

## Usage

1. Clone this repository to your local machine.
   git clone https://github.com/Dvzr2k/Ubuntu-Wordpress-Setup.git
2. Run the following commands to create and configure the virtual machine.
   ```sh
   git clone https://github.com/yourusername/MultiVm-Vagrant.git
   cd MultiVm-Vagrant-main
   vagrant up
3. Access to Vms
   ```sh
   vagrant ssh web01
   vagrant ssh web02
   vagrant ssh db01

Enjoy developing!


