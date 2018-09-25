[![No Maintenance Intended](http://unmaintained.tech/badge.svg)](http://unmaintained.tech/)

easy_rsa
========

[![Build Status](https://travis-ci.org/kbrebanov/ansible-easy_rsa.svg?branch=master)](https://travis-ci.org/kbrebanov/ansible-easy_rsa)

Installs and configures easy-rsa

Requirements
------------

This role requires Ansible 1.9 or higher.

Role Variables
--------------

| Name                    | Default                | Description                                  |
|:------------------------|:-----------------------|:---------------------------------------------|
| easy_rsa_ca_expire      | 3650                   | Number of days that CA is valid for          |
| easy_rsa_clients        | []                     | List of client certificates/keys to generate |
| easy_rsa_clients_revoke | []                     | List of client certificates/keys to revoke   |
| easy_rsa_key_city       | "SanFrancisco"         | City                                         |
| easy_rsa_key_country    | "US"                   | Country                                      |
| easy_rsa_key_email      | "me@myhost.mydomain"   | Email address                                |
| easy_rsa_key_expire     | 3650                   | Number of days that key is valid for         |
| easy_rsa_key_name       | "EasyRSA"              | Name of server key                           |
| easy_rsa_key_org        | "Fort-Funston"         | Organization                                 |
| easy_rsa_key_ou         | "MyOrganizationalUnit" | Organizational Unit                          |
| easy_rsa_key_province   | "CA"                   | Province                                     |
| easy_rsa_key_size       | 2048                   | Diffie-Hellman key size                      |

Dependencies
------------

None

Example Playbook
----------------

Install easy-rsa
```yaml
- hosts: all
  roles:
    - kbrebanov.easy_rsa
```

Install easy-rsa and generate a client cert/key
```yaml
- hosts: all
  vars:
    easy_rsa_clients:
      - client1
  roles:
    - kbrebanov.easy_rsa
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
