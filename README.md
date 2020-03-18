Ansible role: GCC
=========

[![Build Status](https://travis-ci.com/Provizanta/ansible-role-gcc.svg?branch=master)](https://travis-ci.com/Provizanta/ansible-role-gcc)

Build and install GNU Compiler Collection **from source**.

Requirements
------------

None

Role Variables
--------------

These variables are defined in [defaults/main.yml](./defaults/main.yml):

    gcc_install_from_source: false

    gcc_source_dir: "/tmp/gcc/"    # repo clone destination

    gcc_source_version: "8.3.0"

    gcc_source_install: true       # install after build

    gcc_source_build_args: []

    gcc_versions: []      # gcc versions to be installed from packages

Dependencies
------------

None

Example Playbook
----------------

    - name: Converge
      hosts: all
      roles:
        - role: gcc
          vars:
            gcc_version: "8.3.0"
            gcc_dir: "/tmp/"
            gcc_source_build_args:
              - "--prefix=/usr/local/gcc/8.3.0"
            gcc_install: true

License
-------

MIT

Author Information
------------------

Tibor Csóka
