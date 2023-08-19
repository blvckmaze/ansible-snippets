# Ansible Role: Docker Installation

This Ansible role facilitates the installation of Docker Community Edition on target machines. It provides a simple and streamlined way to ensure that Docker is properly installed and ready for use.

## Requirements

No specific requirements are necessary for using this Ansible role.

## Role Variables

The role contains a single variable that can be customized:

- `username`: This variable specifies the username for which Docker will be installed. By default, it is set to ubuntu. You can modify this variable to match the target machine's user account.

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
        username: target_host's_username
```

Replace your_target_hosts with the appropriate inventory group or hostname, and your_username_here with the desired username.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Author Information

This Ansible role was created by [blvckmaze](https://github.com/blvckmaze) for the purpose of simplifying Docker installation on target machines.
