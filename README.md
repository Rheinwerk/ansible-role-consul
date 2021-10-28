consul installation
=========

This role can be used to install consul and consul-template

[![Build Status](https://github.com/Rheinwerk/ansible-role-consul/actions/workflows/ci.yml/badge.svg)](https://github.com/Rheinwerk/ansible-role-consul/actions/workflows/ci.yml)

Notice that it will not create any configuration files, but just install
the binaries and create startup scripts and default files. The service
is not enabled by default.

Requirements
------------

The target machine must have `unzip` installed.

Role Variables
--------------

There is one main variable that drives this role: `_consul`. It is a map that contains all configuration and settings for this role.
Please see `defaults/main.yml` for details.

Dependencies
------------

None.


Example Playbook
----------------

The general contract of this role is to take the variables map `_consul` from `defaults/main.yml` as a template for your configuration and pass that configuration as a parameter to this role.

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      var:
        CONSUL:
          ...
      roles:
         - { role: consul, tags: [ 'consul' ], _consul: "{{ CONSUL }}" }

License
-------

Please see LICENSE.

Author Information
------------------

Original author is [Daniel Schneller](https://github.com/dschneller) as member of the [Rheinwerk](https://github.com/Rheinwerk) project.

