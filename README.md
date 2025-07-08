# ansibleColin

This repository contains Ansible resources for installing Grafana, Prometheus, Loki and Promtail on target servers.

## Structure

- `inventories/` – inventory file with connection details.
- `playbooks/` – contains the main playbook `install_grafna.yml`.
- `roles/` – individual roles for each component:
  - **grafana**
  - **prometheus**
  - **loki**
  - **promtail**

Each role installs and configures its component using tasks defined under `roles/<role>/tasks/main.yml`.

## Usage

1. Update `inventories/inventory.yml` with your hosts and variables.
2. Run the playbook (requires Ansible installed):
   ```bash
   ansible-playbook playbooks/install_grafna.yml
   ```

The playbook installs Grafana, Prometheus, Loki, and Promtail on the hosts defined in the inventory.
