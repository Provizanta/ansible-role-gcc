C++
=========

Install C++ environment.

Requirements
------------

None

Role Variables
--------------

compilers:
  gcc:
    last_stable: install also last stable version
    versions: list of version to install
  clang:
    last_stable: install also last stable version
    versions: list of version to install

Dependencies
------------

None

Example Playbook
----------------

    - hosts: localhost
      roles: dev/cpp
      vars:
        compilers:
          gcc:
            last_stable: yes
            versions:
              - 7
              - 8

License
-------

MIT

Author Information
------------------

Tibor Csoka
