
# Ansible Playbook for Installing Docker

This Ansible playbook automates the installation of Docker on target machines. Docker is a popular platform for developing, shipping, and running applications inside containers. This playbook simplifies the process of setting up Docker, ensuring consistency across your infrastructure.

## Table of Contents

- [Ansible Playbook for Installing Docker](#ansible-playbook-for-installing-docker)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Prerequisites](#prerequisites)
  - [Usage](#usage)
  - [Example Inventory File](#example-inventory-file)
  - [Running the Playbook](#running-the-playbook)

## Introduction

This Ansible playbook simplifies the process of installing Docker on target machines. Docker provides a consistent environment for applications by packaging them in containers. This playbook uses Ansible roles to automate the installation steps, making it easy to manage Docker installations across your infrastructure.

## Prerequisites

Before running this playbook, ensure you have the following prerequisites:

- Ansible installed on the machine where you'll run the playbook.
- SSH access to the target machines.
- A valid inventory file that lists the target machines where you want to install Docker.

## Usage

1. Clone this repository:

   ```bash
   git clone https://github.com/mohamedAhmed97/ansible-docker-install.git
   ```

2. Change into the project directory:

   ```bash
   cd ansible-docker-install
   ```

3. Create or update your Ansible inventory file with the target machine(s) where you want to install Docker (see [Example Inventory File](#example-inventory-file)).

4. Run the playbook using the `ansible-playbook` command (see [Running the Playbook](#running-the-playbook)).



## Example Inventory File

Here's an example inventory file (`inventory.yml`) that lists the target machines:

```yaml
[docker_ec2_server]
192.168.154.221

[docker_ec2_server:vars]
ansible_ssh_private_key_file=~/.ssh/ansible-servers.pem
ansible_user=ubuntu
```

Ensure you replace `yourusername` and the IP addresses with your actual values.

## Running the Playbook

Use the `ansible-playbook` command to run the playbook and install Docker on the target machines. Here's the command:

```bash
ansible-playbook -i ansilbe/hosts ansilbe/docker-playbook.yaml
```

Replace `ansilbe/hosts` with your inventory file if it has a different name.


