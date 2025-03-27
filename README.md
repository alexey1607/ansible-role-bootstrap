Bootstrap
=========

Upgrade and install packages

Role Variables
--------------

The default values for the variables are set in ```defaults/main.yml```
```---
packages:
  - wget
  - curl
  - mc
  - tcpdump
  - htop
  - vim
  - unzip
  - iotop
  - atop
  - net-tools
  - iftop
  - nmap
  - jq
  - sysstat
  - netcat
  - traceroute
  - git
  - tmux
  - bzip2
  - zip
  - rsync
  - bind9-utils
  - ngrep
  - nicstat
  - iostat
  - ifstat
  - tree
  ```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```
- name: prepare server
  hosts: all
  roles:
    - bootstrap
```

License
-------

Apache-2.0

Author Information
------------------

Alexey

example config
```
[defaults]
roles_path = ./roles
log_path = ./main.log
gathering = smart
forks = 30
inventory = ./hosts.ini
fact_caching = ansible.builtin.jsonfile
fact_caching_connection = ./ansible_facts
cache_timeout = 36000
host_key_checking = False
remote_user = root
private_key_file =  ~/.ssh/id_rsa
# Use the YAML callback plugin.
stdout_callback = json
# Use the stdout_callback when running ad-hoc commands.
bin_ansible_callbacks = True

[privilege_escalation]
become = True
become_method = sudo
become_user = root
become_ask_pass = False

[ssh_connection]
pipelining = True
ssh_args = -o ControlMaster=auto -o ControlPersist=15m
transfer_method = piped

[inventory]
cache = yes
cache_connection = /tmp/ansible_inventory

```
