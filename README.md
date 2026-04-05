# 🚀 Windows Server Automation Lab with Ansible

This repository contains Ansible Playbooks designed to automate the management of a Windows Server 2022 environment within an Active Directory domain.

## 🛠️ Project Overview
* **Inventory Management:** Organized `hosts.ini` configuration for WinRM connectivity.
* **Security & Compliance:** Implementation of **Ansible Vault** to encrypt sensitive credentials.
* **Active Directory Automation:**
    * Automated creation of Organizational Units (OUs) and Groups.
    * Bulk user provisioning (20+ Developer accounts) using **Ansible Loops**.
* **File System & Permissions:**
    * Automated Shared Folder creation and ACL management.

## 🏗️ Lab Architecture
* **Control Node:** Ubuntu Server 22.04 LTS.
* **Managed Node:** Windows Server 2022 (Domain Controller).
* **Protocol:** WinRM over HTTPS (Port 5986).

## 🚀 How to Run
To execute these playbooks, you must provide the Ansible Vault password:

1. **Test Connectivity:**
   ```bash
   ansible dc -i hosts.ini -m win_ping --ask-vault-pass# ansible-windows-lab
