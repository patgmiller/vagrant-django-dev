# Django Development

This is a basic django development machine with postgresql database that is provisioned with 
`ansible`, `vagrant`, and `virtualbox`.

## Requirements

- vagrant>=1.7.2 : Install from [downloads](http://www.vagrantup.com/downloads.html) page.
- ansible>=1.9.1 : See [installation](http://docs.ansible.com/intro_installation.html) documentation.   

### Playbooks

Requires the following ansible playbook(s). 

- ANXS.postgresql, v1.1.2

These playbooks can be install with the following command: 

```bash
sudo ansible-galaxy install ANXS.postgresql 
```

## Getting Started

Once you've installed the required packages simply run `vagrant up` to start up your vagrant machine. It will build the machine on the first time running the command.

 