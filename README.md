# ansible-config-mgt

This is a simple Ansible playbook whose main purpose is to update the indexes for both Redhat 8 and Ubuntu 20.04 linux distos.

Before running this playbook, I defined my target servers in the dev.yml file located in the Inventory folder. I used AWS EC2 instances for this project, so i also specified the path to my ssh private key in the dev.yml file.

It sets the timezone to Europe/London, and then installs wireshark on all the servers.

Finally, it creates a www directory in /var on my webservers, and then creates a sample file inside of this directory.

Everytime I run the script, the sample files seems to be recreated afresh. I need to find a way to stop this from happening.

