# DevOps Multi-VM Lab using Vagrant

This project sets up a **multi-virtual machine environment** using Vagrant and VirtualBox. It is designed to simulate a simple microservices architecture with different components running on separate VMs.

## 🧰 Tools Used
- **Vagrant**
- **VirtualBox**
- **CentOS Stream 9** and **Ubuntu 22.04 (Jammy)**
- **vagrant-hostmanager** plugin

## 💻 Virtual Machines Defined

| VM Name | OS               | IP Address      | Role       | Memory |
|---------|------------------|------------------|------------|--------|
| `db01`  | CentOS Stream 9  | `192.168.56.15`  | MySQL/DB   | 600MB  |
| `mc01`  | CentOS Stream 9  | `192.168.56.14`  | Memcached  | 600MB  |
| `rmq01` | CentOS Stream 9  | `192.168.56.13`  | RabbitMQ   | 600MB  |
| `app01` | CentOS Stream 9  | `192.168.56.12`  | Tomcat     | 800MB  |
| `web01` | Ubuntu Jammy 64  | `192.168.56.11`  | Nginx/Web  | 800MB  |

## 🚀 How to Run

1. Clone the repo:
   git clone https://github.com/your-username/devops-multi-vm-lab.git
   cd devops-multi-vm-lab

## Install Vagrant plugins (if not already)
   vagrant plugin install vagrant-hostmanager

## Start all VMs:
   vagrant up

## SSH Into any machine
   vagrant ssh db01

## To shut down all VMs:
   vagrant halt
