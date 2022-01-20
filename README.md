# Red Hat Ceph Storage 5  -  Installation  

This playbook will;

- Will work if  ansible controller is the bootstrap node itself, but also works if the controller is not the bootstrap node

- Will not update the OS packages at the bootstrap node , but this behaviour  can be easily changed if the ansible controller is not the bootstrap node.

- Register either to the CDN or Satellite, enable repos and install required packages into all nodes

- Tune the RHEL OS paramters as per the best practices

- Run some prechecks to validate all the nodes are ready for the deployment

- Define non-root user for ssh access

- Add new hosts to the cluster

- Apply Day-2 commands to create the cluster as per the labels defined at the all.yml file

- Will not provision  RGWs


For the installation;

- Create a vault  passwords.yml file for secrets. Sample passwords.yml file is;

```
vault_rhaccountpass: <rh account password>
vault_poolid: <pool id>
vault_username: admin
vault_userpass: redhat

```

- Change the variables at all.yml as per your requirements

- Provide clusterip of each host at inventory file

- Run the playbook

`#ansible-playbook -i hosts --ask-vault-pass main.yml`


NOTES:

- First node defined at the inventory file will be the bootstrap node and labeled with "_admin"




