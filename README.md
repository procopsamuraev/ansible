## How to Run
2. Run the playbook:
   ```bash

## how to run play
1. Edit the inventory file with the appropriate variables.
2. Run the playbook:
   ```bash
   from playbook dir
   ansible-playbook -v -i inventory/inventory.yml prepare_server.yml -u ubuntu  --key-file "~/.ssh/key"
   ```
## todo

- no passnrases as plain text
- make lint test pass witn no warning