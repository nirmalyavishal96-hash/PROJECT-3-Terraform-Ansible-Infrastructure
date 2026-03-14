# Terraform + Ansible Infrastructure Automation

## Project Overview

This project demonstrates **Infrastructure as Code and Configuration Management** using Terraform and Ansible on AWS.

Terraform provisions cloud infrastructure, while Ansible automatically configures the server and deploys a containerized application.

---

## Architecture

Developer → Terraform → AWS EC2
EC2 → Ansible Configuration
Ansible → Install Docker
Docker → Run Nginx Container

Application exposed on port **5000**

---

## Tech Stack

* Terraform
* Ansible
* AWS EC2
* Docker
* Linux

---

## Project Structure

```
PROJECT-3-Terraform-Ansible-Infrastructure
│
├── terraform
│   ├── main.tf
│   ├── variables.tf
│   └── outputs.tf
│
├── ansible
│   ├── inventory
│   └── install-docker.yml
│
└── README.md
```

---

## Workflow

1. Terraform provisions AWS infrastructure.
2. EC2 instance is created with security groups.
3. Ansible connects to the instance using SSH.
4. Docker is installed automatically.
5. Nginx container is deployed.

---

## Run the Project

### Step 1 — Provision Infrastructure

```
cd terraform
terraform init
terraform apply
```

### Step 2 — Configure Server

```
cd ../ansible
ansible-playbook -i inventory install-docker.yml
```

---

## Result

Application runs on:

```
http://EC2_PUBLIC_IP:5000
```

---

## Author

**Nirmalya Das**
DevOps Engineer
