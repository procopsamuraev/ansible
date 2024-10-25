# Ansible Role: encrypted

This role performs disk/partition encryption usung LUKS

## Tasks
- `encrypt_disks` - encrypt and mount disk and partition present on disk next to 'root' partition
Encryption done with combined passphrase:
   - part1 passphrase from variable
   - part2 passphrase from remote host saved on /root/.encrypted_passphrase

TODO: Do not keep passphrase on ansible code.
