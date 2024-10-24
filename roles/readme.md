# Ansible Role: server

This role performs system preparation tasks, including disk encryption, CPU configuration, network interface renaming, and system information display.

## Role Variables
- `disk_partition`: Partition to encrypt (default: `/dev/sdb1`)
- `adjacent_partition`: Partition next to root to encrypt (default: `/dev/sda3`)
- `luks_passphrase`: Passphrase for LUKS encryption
- `mount_point`: Mount point for the encrypted disk (default: `/mnt/encrypted_disk`)
- `cpu_governor`: Desired CPU governor (default: `performance`)
- `network_interface`: Original network interface name
- `new_interface_name`: New network interface name (default: `net0`)

## How to Run
1. Edit the inventory file with the appropriate variables.
2. Run the playbook:
   ```bash
   ansible-playbook -i inventory playbooks/prepare_server.yml

