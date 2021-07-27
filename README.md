# ansible-config-mgt

# Intro
This project provides a basic walkthrough for configuration management using Ansible on AWS EC2 instances. My infrastructure consists of:
- 3 Redhat 8 Instances
- 2 Ubuntu 20.04 Instances
# Usage
Before running this playbook, I defined my target servers in the dev.yml file located in the Inventory folder. I used AWS EC2 instances for this project, I also imported my private key into ssh-agent so I don't have to include the path in the dev.yml file. Below are tasks included with this playbook:

- This is a simple Ansible playbook whose main purpose is to update the indexes for both Redhat 8 and Ubuntu 20.04 linux distos.

- It sets the timezone to Europe/London, and then installs wireshark on all the servers.

- Finally, it creates a www directory in /var on my webservers, and then creates a sample file inside of this directory.

# Challenge
Everytime I run the script, the sample files seems to be recreated afresh. I need to find a way to stop this from happening.
Resolved the challenge by including a task which checks if the file already exists, and then skips creating a new file once it finds the file already exists on the webservers.
