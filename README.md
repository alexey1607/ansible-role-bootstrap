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
