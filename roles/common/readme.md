# Ansible Role: common

This role performs CPU configuration, network interface renaming and display system information.

## Tasks
- `set_cpu`: 
   - Disabling C-state for all available CPUs;
   - Switching CPU governor to 'performance' mode.
      - ps: 
         - Author paid attention to do not overwrite existing "cmdline" 
         - Author assume that host CPU cores are equal: CPU0 == CPU"N"
        

- `rename_interface`: 
   - Rename the active network interface to 'net0'
      - ps: This could be done with quite few different ways incliding netplan or NetworkManager configuration. Author tried to do it most common/old fashion way and without OS vendor lock.
      PS2: something went wrong with provided VM while playing this role - as  result author rewrtite some logic
      PS3: most likely the author didnt account stastic net configuration (was done all testing with dynamic IP on my vm)

- `display_info`: 
   - Display information about the renamed interface and disks. 
