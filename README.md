# Ansible: Wings

Installs [Pterodactyl](https://pterodactyl.io) Wings onto any number of Debian 12 nodes. Before running the playbook, ensure each host has a Pterodactyl config file in `files/`, where the filename is the `inventory_hostname_short` of the node. For example, if your node is called `node1.example.com`, then the config file will be called `node1.yml`.

Using the playbook is simple:

```shell
pip install -r requirements.txt
ansible-playbook deploy.yml --ask-become-pass
```

## Portainer Agent

Optionally, this playbook can also installed Portainer Agent onto a node. This can be configured on a per-node basis by setting the `install_portainer_agent` variable to `true`.
