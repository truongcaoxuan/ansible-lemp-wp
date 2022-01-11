# ansible-lemp-wp
Wordpress on Ubuntu 20.04 LEMP

*This playbook will install a WordPress website on top of a LEMP environment (Linux, Nginx, MySQL and PHP) on an Ubuntu20.04 machine.*
# Settings
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
```
git clone https://github.com/do-community/ansible-lemp-wp.git
cd ansible-lemp-wp
```
### 2. Customize Options
```
---
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
```
ansible-playbook -l [target] -i [inventory file] -u [remote user] playbook.yml
```
