# zeevo.container

Run a Docker container on a Linux server.

## Getting started

Install the `zeevo.container` role with `ansible-galaxy`

```bash
ansible-galaxy role install zeevo.container
```

Include the `zeevo.container` role in your playbook.

```yml
- name: postgres
  hosts: db
  become: true
  roles:
    - zeevo.container
```

Configure the role with variables. For example, running a database:

```yml
# group_vars/db.yml
container_image: postgres/latest
container_user: admin
container_environment:
  POSTGRES_PASSWORD: postgres
container_ports:
  - 5432:5432
```
