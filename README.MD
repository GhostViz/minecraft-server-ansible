# Minecraft-Server-Ansible #

## How To Use ###
Create your inventory file and set the following vars.

```
minecraft_server_type = "<survival/creative>"
minecraft_server_download_url = "<url to server.jar you want to download>"
```

Once your inventory file is created you will run the ansible playbook from the minecraft-server-ansible directory.

```
ansible-playbook -i inventories/<your inventory file> playbook/site.yaml
```

## Compatible Operating Systems ##
* CentOS 7
* RHEL 7
* Ubuntu 16.04*
* Debian 9*

## Disclaimer ##
Extensive testing has not been done on Ubuntu / Debian. I primarily run CentOS/RHEL based systems, and that is what I initially made this installer for. Ubuntu / Debian support was added to make this more accessible to everyone.

## Testing With Vagrant ##
From the minecraft-server-ansible directory run the command `vagrant up`.

To test against CentOS 7 run the provision_development script in the bin directory.
```
sh bin/provision_development
```

Once testing is complete run the destroy script in the bin directory.
```
sh bin/destroy
```

If you'd like to test this playbook against different operating systems you can modify the `config.vm.box =` line in vagrant/shared.rb.
