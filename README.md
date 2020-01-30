# Playbooks

The project consist in create some users and some Virtuals Machine on Proxmox with Ansible.
This is only an educational program, do not use for professionnal use.

### I. Define my Hosts ? 

In the file hosts.yaml, you have to put the Ip Address of your Proxmox's server
We have 3 Proxmox server for this example, one master and two slave.
This file will be read for every command and be executed for every server.

### II. Add user on Proxmox ! 

It's pretty simple to add an user on Proxmox with Ansible. 
But firstly, you have to modify the file AddUserOnProxmox.yaml. 
Modify var username with the username you want :) 

For the password, you have to generate an encrypted password

Download Whois if it didn't work because you didn't have the right package & Use this command: 
```
mkpasswd --method=sha-512
```

After this, you will prompt your password, copy the encrypted password and paste it on the line password, in user's section.

Run this command with :

```
 ansible-playbook -i hosts.yaml  -u root AddUserOnProxmox.yaml -v
```


#### Alexia & Kevin


