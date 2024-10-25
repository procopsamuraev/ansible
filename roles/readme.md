
## How to Run
1. Edit the inventory file with the appropriate variables.
2. Run the playbook:
   ```bash
   ansible-playbook -v -i inventory/inventory.yml prepare_server.yml -u $user
