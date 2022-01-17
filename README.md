# rhcs5install
- Create a vault  passwords.yml file which contains the following variables:

vault_username
vault_userpass
vault_rhaccountpass
vault_poolid

- Change the variables at all.yml

- Run the playbook

$ansible-playbook -i hosts --ask-vault-pass main.yml
