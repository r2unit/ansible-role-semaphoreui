Ansible Role: SemaphoreUi
=========

Installation of SemaphoreUI on linux.

Requirements
------------

Docker

Role Variables
--------------

All variables are down here, all default values are in `defaults/main.yml`

All values that are not filled in are filled in by the default value. 

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

```dotenv
```
For when you use the Postgres database
```dotenv

```

For when you use the MySQL database
```dotenv
```
For when 
Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: example
  become: yes
  
  roles:
    - r2unit.semaphoreui
```

License
-------

MIT / BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
