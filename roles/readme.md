# Ansible Role: encrypted_server

This role performs system preparation tasks, including disk encryption, CPU configuration, network interface renaming, and system information display.

## Role Variables
- `encrypted_disk`: Disk to encrypt
- `encrypted_partition`: Partition next to root to encrypt
- `new_interface_name`: New network interface name (default: `net0`)

## Tasks
- `encrypt_disks`:
- `rename_interface`:
- `set_cpu`:
- `display_info`:


## How to Run
1. Edit the inventory file with the appropriate variables.
2. Run the playbook:
   ```bash
   ansible-playbook -v -i inventory/inventory.yml prepare_server.yml -u $user

