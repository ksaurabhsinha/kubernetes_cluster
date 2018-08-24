# Kubernetes Cluster

This is an attempt to create a 3 node Kubernetes Cluster through Ansible.

## Requirements

- 3 Virtual or Physical Nodes
- SSH Key pair - for access to the Nodes
- Ansible Installation on your host machine.

## Initial Steps
- Create 3 nodes
- Get their IP addresses and populate the hosts file

## Preparing the cluster

```sh
# Setting up the Kubernetes Dependencies
$ ansible-playbook -i hosts kube-dependencies.yml

# Setting up the master node
$ ansible-playbook -i hosts master.yml

# Setting up the worker nodes
$ ansible-playbook -i hosts workers.yml
```
