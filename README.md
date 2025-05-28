Ansible Role: SemaphoreUi
=========

Installation of open-source SemaphoreUI on linux. 

Requirements
------------

For now, this role has only been tested on the following systems. 

| Distribution | Version |  Architecture  |  Supported  |
|:------------:|:-------:|:--------------:|:-----------:|
|    Debian    |   12    | `arm64`, `amd64` |   yes   |



Role Variables
--------------

All variables are down here, all default values are in `defaults/main.yml`

If a variable is left blank, it is given the default value.

```dotenv
semaphoreui_version: "v2.14.9"
semaphore_port: "3000"
semaphore_data_dir: ""
semaphore_config_dir: ""
semaphore_temp_dir: ""
semaphore_admin: "admin"
semaphore_admin_name: "admin"
semaphore_admin_email: "admin@example.com"
semaphore_admin_password: "insecure" 
```

For when you use the **Postgres** database
```dotenv
postgres_user: "postgres"
postgres_password: "insecure"
postgres_db: "semaphore"
```

For when you use the **MySQL** database
```dotenv
mysql_user: "semaphore"
mysql_password: "insecure"
mysql_database: "semaphore"
mysql_random_root_password: "yes"
```

Dependencies
------------

None

Example Playbook
----------------

If you want to use the role without any difficulty with the default database use the following:

```yaml
- hosts: example
  become: yes
  
  roles:
    - r2unit.semaphoreui
```
If you want to use the role with **Postgres** use the following example.
```yaml
- hosts: example
  become: yes
  
  vars:
    semaphore_db_type: postgres
    postgres_user: "postgres"
    postgres_password: "insecure"
    postgres_db: "postgres"

  roles:
    - r2unit.semaphoreui
```

If you want to use the role with **MySQL** use the following example.
```yaml
- hosts: example
  become: yes
  vars:
    semaphore_db_type: mysql
    mysql_user: "semaphore"
    mysql_password: "insecure" 
    mysql_database: "semaphore"
    mysql_random_root_password: "yes"
      
  roles:
    - r2unit.semaphoreui
```

License
-------

MIT / BSD

Author Information
------------------

This role is created by me for the open-source community.
