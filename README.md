CIS - Benchmark Collection
=========

Asible role to apply CIS Benchmark on
- CentOS 8 based
- Nginx


Requirements to CIS-CentOS8
------------

Create below partitions at the time of installation. The role will not create any of these partitions. 

```
1.1.6   | Ensure separate partition exists for /var (Scored)
1.1.7   | Ensure separate partition exists for /var/tmp (Scored)
1.1.11  | Ensure separate partition exists for /var/log (Scored)
1.1.12  | Ensure separate partition exists for /var/log/audit (Scored)
1.1.13  | Ensure separate partition exists for /home (Scored)

```

Support Matrix
--------------

| Destro | Status | Role |
| --- | --- | --- |
| CentOS 8 | Supported (Tested) | Centos |
| RHEL 8 | Supported (Tested) | Centos |
| Oracle Linux 8 | Supported (Tested) | Centos |
| Rocky Linux 8 | Supported (Tested) | Centos |
| Debian 11 | Supported (Tested) | Nginx |


Role Centos Variables
--------------

default/main.yml variables are pretty self explanatory. 


Example Playbook
----------------

```
  - name: CIS Baseline Setup
    hosts: centos
    become: yes

    roles:
      -centos8
      - nginx
