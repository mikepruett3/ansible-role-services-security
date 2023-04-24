Ansible Role: Services Security
=========

Ansible role to configure Services security settings on Linux servers.

Requirements
------------

The role does not require anything to run on Ubuntu, Debian or RHEL and its derivatives. This role assumes that you have the software package located on a web server somewhere in your environment.

Role Variables
--------------

Available variables are listed below, along with default values (see ```defaults/main.yml```):

``` yaml
software_url: "http://www.example.org"
package_name: "managesoft-17.3.0-1.x86_64.rpm"
```

```software_url``` **(Required)** The URL that hosts the Installer package. This should be either **http** or **https**.

```package_name``` **(Required)** The Installer package name.

Role variables can be stored with the ```hosts.yaml``` file, or in the main variables file.

Dependencies
------------

None.

Example Playbook
----------------

``` yaml
    - hosts: servers
      roles:
         - role: mikepruett3.coredump
           vars:
            software_url: "http://www.example.org"
            package_name: "flexera-agent-installer"
```

License
-------

MIT

Author Information
------------------

Role created by [mikepruett3](https://github.com/mikepruett3) on [Github.com](https://github.com/mikepruett3/ansible-role-services-security)
