# Automating WordPress Deployment with Ansible on Ubuntu LEMP Stack

Welcome to the Ansible-powered WordPress Deployment repository! 

This project serves as a comprehensive guide for deploying a WordPress website on a robust LEMP (Linux, Nginx, MySQL, and PHP) environment. Harness the power of Ansible automation to streamline the setup process, ensuring consistent and reliable deployments on Ubuntu servers.

## Repository Contents

### 1. Setup and Configuration Guide

Discover a step-by-step guide to prepare your Ubuntu server for Ansible deployment. Learn about SSH key setup, server configurations, and Ansible prerequisites.

### 2. Ansible Playbooks and Roles

Dive into the heart of this repository with ready-to-use Ansible playbooks and roles. These automation scripts facilitate the deployment of a LEMP environment and WordPress. Witness the magic of infrastructure-as-code in action.

### 3. Variables and Customization

Explore how to tailor the deployment process to your needs by adjusting variables within the Ansible playbooks. Customize the website's domain, database details, and more with ease.

### 4. Post-Deployment Steps

Learn about additional steps to take after the WordPress deployment is complete. From securing the environment to optimizing performance, these post-deployment insights will help you fine-tune your setup.

### 5. Troubleshooting and Best Practices

Delve into troubleshooting common issues that may arise during the deployment process. Discover Ansible best practices to enhance the maintainability and scalability of your automation workflows.

## Usage

- Clone or fork this repository to gain access to Ansible playbooks and deployment resources.
- Follow the setup and configuration guide to ensure your Ubuntu server is ready for Ansible deployments.
- Review the Ansible playbooks and roles provided for deploying the LEMP environment and WordPress.
- Modify variables within the playbooks to match your preferences and requirements.
- Run the Ansible playbooks to initiate the automated deployment process on your target server.

## Contributions

Contributions to this repository are highly encouraged. If you have insights, improvements, or additional Ansible playbooks related to WordPress deployment, LEMP stack, or automation best practices, feel free to submit pull requests. Together, we can build a valuable resource for the automation community.

Embark on your journey of automating WordPress deployments with Ansible, and experience the efficiency and reliability of Infrastructure as Code. Happy automating! 🚀🔧

*This playbook will install a WordPress website on top of a LEMP environment (Linux, Nginx, MySQL and PHP) on an Ubuntu20.04 machine.*

## Settings

- mysql_root_password: The desired password for the root MySQL account.
- mysql_db: The name of the MySQL database that should be created for WordPress.
- mysql_user: The name of the MySQL user that should be created for WordPress.
- mysql_password: The password for the new MySQL user.
- http_host: Your domain name.
- http_conf: The name of the configuration file that will be created within Apache.
- http_port: HTTP port for this virtual host, where 80 is the default.

## Running this Playbook

Quickstart guide for those already familiar with Ansible:

### 1. Obtain the playbook

```cmd
git clone https://github.com/do-community/ansible-lemp-wp.git
cd ansible-lemp-wp
```

### 2. Customize Options

```setting
#MySQL Settings
 mysql_root_password: "mysql_root_password"
 mysql_db: "wordpress"
 mysql_user: "sammy"
 mysql_password: "password"

#HTTP Settings
 http_host: "your_domain"
 http_conf: "your_domain.conf"
 http_port: "80"
```

### 3. Run the Playbook

```cmd
ansible-playbook -l [target] -i [inventory file] -u [remote user] playbook.yml
```
