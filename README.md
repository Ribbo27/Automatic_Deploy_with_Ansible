## AUTOMATICALLY DEPLOY A LARAVEL DISTRIBUTED APPLICATION EXAMPLE

These playbooks deploy a very basic implementation of a Laravel Application distributed in 3 containers:  
 - ```database```
 - ```web server```
 - ```Laravel application```

### HOW TO 

  - ```Ansible 2.7.1``` required.
  - ```Ubuntu hosts``` expected.
 
To use them, first edit the inventory file to contain ip of the machines on which you want to deploy, 
and the host_vars/vault.yml file to set any.

To encrypt vault.yml use ``` ansible-vault encrypt vault.yml``` command and choose a password to decrypt.
To decrypt use ```ansible-vault decrypt vault.yml``` and insert password you choose during encrypt. 

## DIRECTORY STRUCTURE

```shell
.
├── host_vars
│   └── vault.yml                 # Variables file
├── inventory                     # Hosts file
├── roles
│   ├── base
│   │   └── tasks
│   │       └── main.yml          # Tasks related to the basic setup of our server
│   └── setup
│       ├── handlers
│       │   └── main.yml          
│       └── tasks
│           ├── docker.yml        # Task for Docker and Docker-Compose install
│           └── main.yml          # 
└── simple_deploy.yml             # Main playbook that starts automatic deploy

7 directories, 7 files

```

## 
