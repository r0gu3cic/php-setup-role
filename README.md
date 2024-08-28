# PHP-SETUP-ROLE

=========

This Ansible role is designed for setting up PHP, Composer, and WP-CLI on an Ubuntu server. This role prepares the server for production use, enabling efficient management and deployment of PHP-based applications.

## Requirements

------------

This role is designed to work with Ubuntu distributions. It requires the following:

- Ansible 2.10.8 or higher
- `sshpass` for running the playbook with SSH password authentication.

## Role Variables

------------

The following variables can be configured for this role:

- **`php.version`**: The version of PHP we want installed.

These variables can be defined in the playbook or in a `vars` file.

## Dependencies

------------

This role has no dependencies on other roles.

## Example Playbook

------------

```yaml
- hosts: servers
  become: yes
  vars:
    php:
      version: 8.1
  roles:
    - role: your_username.role_name
```

## License

------------

MIT License

## Testing Guide

------------

To run a local test for this role, use the following command:

```bash
ansible-playbook tests/test.yml -i tests/local_inventory.ini -u root -k
```

## Author Information

------------

This role was created by Stefan, aka enabler, aka r0gu3cic. For any inquiries or further information, please reach out via [GitHub](https://github.com/r0gu3cic).