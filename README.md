## Various Roles used to set up a Windows Server with Ansible.
<strong>NOTE: Must set up credentials in group_vars/`<hostname>`/vars.yml before using playbook</strong>

<ol>
  <li>Common Setup To Ensure Chocolatey Package Manager is Installed</li>
  <li>Setup IIS Server on Windows Server</li>
  <li>Rebooting Windows Servers</li>
  <li>Windows Ping</li>
</ol>

## Installation Requirements
Refer to https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html to prepare Ansible Client.

Refer to https://docs.ansible.com/ansible/latest/user_guide/windows.html to bootstrap the Windows Server Host for using Ansible.

Can use following example playbook to setup SSH on hosts provided in Ansible Inventory

```yml
  # Example playbook.yml
  - hosts: win-servers # should be defined in inventory "hosts" file

    roles:
    - common
    - setup-ssh
```

Use command in terminal to run Ansible playbook.

```bash
ansible-playbook playbook.yml
```
