# Ansible Role: common

This role performs CPU configuration, network interface renaming and display system.

## Tasks
- `set_cpu`: 
   - Disabling C-state for all available CPUs;
   - Switching CPU governor to 'performance' mode.
      - ps: paid attention to do not overwrite existing "cmdline" 

- `rename_interface`: 
   - Rename the active network interface to 'net0'
      - ps: This could be done with quite few different ways incliding netplan and NetworkManager. Author tried to do it most common/old fashion way and without lock to OS.

- `display_info`: 
   - Display information about the renamed interface and disks. 
