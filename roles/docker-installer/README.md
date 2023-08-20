# Ansible Role: Docker Installation

This Ansible role facilitates the installation, configuration, and management of Docker Community Edition on target machines. It provides a simple and streamlined way to ensure that Docker is properly installed, configured to start on boot, and grants the specified user rights to run Docker commands.

## Requirements

No specific requirements are necessary for using this Ansible role.

## Role Variables

The role contains a single variable that can be customized:

- `username`: This variable specifies the username for which Docker will be installed and configured. By default, it is set to `ubuntu`. You can modify this variable to match the target machine's user account.

## Dependencies

No dependencies on other Ansible roles are required for this role.

## Example Playbook

Here's an example playbook on how to use this Ansible role:

```Yaml
- name: Install Docker on target machines
  hosts: your_target_hosts
  become: yes

  roles:
  - role: role_name
      vars:
        username: target_host_username
```

Replace `your_target_hosts` with the appropriate inventory group or hostname, and `target_host_username` with the desired username.

## Role Functionality

This role performs the following tasks:

1. Installs Docker Community Edition on the target machine.
2. Ensures that the Docker service is started and configured to start on boot.
3. Grants the specified user (`username`) rights to run Docker commands without requiring root privileges.

## License

This project is licensed under the GPL 3.0 License. See the LICENSE file for details.

## Author Information

This Ansible role was created by [blvckmaze](https://github.com/blvckmaze) for the purpose of simplifying Docker installation on target machines.
