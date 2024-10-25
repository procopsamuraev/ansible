# Ansible Role: common

This role performs CPU configuration, network interface renaming and system information display.
task: 
## Tasks
- `set_cpu`: paid attention to do not overwrite existing "cmdline" 
- `display_info`:
- 'rename_interface' This could be done with quite few different ways incliding netplan and NetworkManager. I tried to do it most common/old fashion way and without lock to OS.

# Ansible Role: encrypted

This role performs disk/partition encryption
## Tasks
Encryption done with combined passphrase:
- part1 passphrase from variable
- part2 passphrase from remote host saved on /root/.encrypted_passphrase
it could be improved by saving passphrase/key on vault. 


## How to Run
1. Edit the inventory file with the appropriate variables.
2. Run the playbook:
   ```bash
   ansible-playbook -v -i inventory/inventory.yml prepare_server.yml -u $user

