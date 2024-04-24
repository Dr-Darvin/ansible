Roles are used to minimize the comlexity of a large playbook.

We can divide large play book to serverral parts using Roles

we can  use roles in several ways like application wise or organizational requirements

once we define the roles we can define them in the main file
  /etc/ansible/roles
    inside the role directory taks are definded in main files as bellow.
    apache2/taks/main.yaml
    nttpd/tasks/main.yaml
##############################

then finally we add the roles to the main.yaml file

---
- name: Install apache2
  hosts: all
  roles:
    - apache2
    - nttpd

##########################



    