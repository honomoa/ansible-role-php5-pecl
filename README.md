# Ansible Role: php5-pecl

PECL is a repository for PHP Extensions, providing a directory of all known extensions and hosting facilities for downloading and development of PHP extensions.

[https://pecl.php.net/](https://pecl.php.net/)

# Role Variables

```
php_root: /etc/php/5.6
```
root of php

```
php_pecl_install_pecl: false
```

wherther install pecl by pecl or not

```
php_pecl_install_command: "pecl install"
```

pecl install command

```
php_pecl_extensions: []
```

pecl extensions to install, for example:

- mongo

```
php_pecl_package: php-pecl
```

pecl package name

```
load_extensions: []
```

static object to load, for example:

- { name: 'mongo', so: 'mongo.so' }

# Example Playbook

```
- hosts: server
  vars:
    php_root: /etc/php/5.6
    php_pecl_install_pecl: false
    php_pecl_install_command: "pecl install"
    php_pecl_extensions: []
      - mongo

    php_pecl_package: php-pecl
    load_extensions: []
      - { name: 'mongo', so: 'mongo.so' }
  roles:
    - { role: honomoa.php5-pecl }
```
# Dependencies

[honomoa.php5](https://galaxy.ansible.com/honomoa/php5)

# License
CC BY-SA 3.0
