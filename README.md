# ansible_starter
Basic example setup of Ansible for a starting place.

# Things to do -
- remove `.dist` from any filename containing it.
- Update the vault variables in `vault.yml` in `group_vars/all`.
- Update vars.yml files in all locations as need - setting `ansible_host` will be required to do anything...
- `roles/shared_roles/bootstrap` and `roles/shared_roles/packages` are examples of things you can do.

Ansible guide can be found here: https://docs.ansible.com/ansible/latest/getting_started/index.html

Ansible playbook information can be found here: https://docs.ansible.com/ansible/latest/playbook_guide/index.html

If using vaults, the documentation for use is here: https://docs.ansible.com/ansible/latest/cli/ansible-vault.html

# To run the initial bootstrap process:
`ansible-playbook site-setup.yml --ask-vault-pass -t bootstrap`

# Then run packages:
`ansible-playbook site-setup.yml --ask-vault-pass -t packages`