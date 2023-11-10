# Ansible Playbook Repository: NOX Server Configuration

This repository contains Ansible playbooks to configure and manage the NOX server environment. It includes tasks for setting up and managing various services and components on the NOX server.

## Purpose

The repository covers the following tasks:

- **NOX Server Setup**: Configuring the NOX server environment.
- **Certificate Management**: Updating and managing certificates used by various services.
- **Service Management**: Restarting and managing essential services such as Dashboard, Manager, Indexer, and Filebeat.
- **Security**: Performing tasks related to security, such as generating random passwords and removing outdated database agents.

## Included Playbooks

### Update Certificate Dashboard
- **Purpose**: Update certificates for the Dashboard service.
- **Tasks**:
  - Delete old certificates.
  - Copy new certificate files.
  - Restart related services.

### Starting new NOX Server
- **Purpose**: Initialize a new instance of the NOX server.
- **Tasks**:
  - Remove old database agents.
  - Generate a random password for authd.
  - Create a file containing the random password.
  - Restart essential services.

## Usage

To utilize these playbooks:

1. Ensure Ansible is installed on the control machine.
2. Update necessary variables in the `certs_vars.yml` file.
3. Execute playbooks using `ansible-playbook` command:
    ```
    ansible-playbook <playbook_name>.yml
    ```

**Note**: Review and modify the playbooks according to specific environment requirements before execution.

## Contribution

Contributions are welcome. If you encounter issues or have improvements to suggest, feel free to open an issue or submit a pull request.
