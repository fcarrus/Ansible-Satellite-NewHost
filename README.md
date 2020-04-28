# Using Ansible to creating new Hosts in Satellite

The following playbook can be used to create several new Hosts in Satellite, by using structured data in a yaml file and no external plugins or modules. Just plain URIs.

It does not make use of the [Foreman Ansible Modules](https://github.com/theforeman/foreman-ansible-modules/). 

## What you need

* A Satellite 6.5 server (or later)
* Ansible 2.6 or later
* This repo
* Some new hosts to provision

## How to create new Hosts

* Edit the [sat_vars.yml](sat_vars.yml) file and define your Satellite URL and credentials.

* Edit the [servers.yml](servers.yml) file and define your new hosts to be created.

## Run the playbook

`$ ansible-playbook main.yml`

## TODOs

* Add code to manage Puppet-related info
* Add code to manage Realm-related info
* Perform single search in case of large number of hostgroups




