# rhcs5install
- Create a vault  passwords.yml file for secrets. Sample passwords.yml file is;

```
Vault password: <rh account username>
vault_rhaccountpass: <rh account password>
vault_poolid: <pool id>
vault_username: admin
vault_userpass: redhat

```

- Change the variables at all.yml

- Provide clusterip of each host at inventory file

- Run the playbook

`$ansible-playbook -i hosts --ask-vault-pass main.yml`
