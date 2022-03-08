# opencart-ansible-galaxy
Ansible role to install homebrew on Ubuntu 20.x


#### Prerequisites
- Ansible 2.x
- Docker (for local development)

#### Running basic ubuntu docker image with openssh-server (the ansible node) - can be achieved using the "Ansible Molecule" too.

<pre>
sudo docker build -t ansible_node_1 .
sudo docker run -d -p 2200:22 ansible_node_1
</pre>

#### Configure ansible hosts and credentials (for testing purposes, this should be configued with asymmetric encryption.) 
<pre>
sudo vim /etc/ansible/hosts
</pre>

<pre>
[lab]
127.0.0.1

[all:vars]
ansible_connection=ssh
ansible_user=test
ansible_ssh_pass=test
</pre>


#### List ansible inventory.
<pre>
ansible-inventory --list -y
</pre>

#### Testing the connection.
<pre>
ansible all -m ping -u test
</pre>

#### Running test Ad-Hoc commands.
<pre>
ansible all -a "df -h" -u test
</pre>

#### Execute the playbook
 
<pre>
ansible-playbook install-homebrew.yml -Kk
</pre>