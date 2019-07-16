Ansible role: GCC
=========

[![Build Status](https://travis-ci.com/Provizanta/ansible-role-gcc.svg?branch=master)](https://travis-ci.com/Provizanta/ansible-role-gcc)

Build and install GNU Compiler Collection from source.

Requirements
------------

None

Role Variables
--------------

Variables defined in defaults/main.yml:

    dir: "/tmp/gcc/"    # repo clone destination

    version: "8.3.0"

    install: true       # install after build

Other variables that can be set:

    build:
      args:             # arguments to be passed to the build
        - "--prefix={{ prefix }}"


Dependencies
------------

None

Example Playbook
----------------

    - hosts: localhost
      roles:
        - role: gcc
          vars:
            version: "8.3.0"
            dir: "/tmp/gcc/"
            build:
              args:
                - "--prefix=/usr/local/gcc/8.3.0"
            install: true

License
-------

MIT

Author Information
------------------

Tibor Csóka
