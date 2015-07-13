# Django Development

This is a basic django development machine with postgresql database that is provisioned with
`ansible`, `vagrant`, and `virtualbox`.

## Requirements

- ansible>=1.9.1 : See [installation](http://docs.ansible.com/intro_installation.html) documentation.
- vagrant>=1.7.2 : Install from [downloads](http://www.vagrantup.com/downloads.html) page.
- virtualbox>=4.3.14 : Install from [downloads](https://www.virtualbox.org/wiki/Downloads) page (optional).
    - The default `Vagrantfile` uses virtualbox, however you may obviously use something else and adjust your setup accordingly.

### Playbooks

The default example ansible setup requires the following playbook(s).

- ANXS.postgresql, v1.1.2

These playbooks can be install with the following command:

```bash
sudo ansible-galaxy install ANXS.postgresql
```

## Getting Started

Once you've installed the required packages.

1. Copy or rename the following `ansible.Example`, `Vagrantfile.Example`, and `.gitignore.Example` to the same name without the `.Example` ending.
2. Make any desired changes to your local files `Vagrantfile` and `.gitignore` and `ansible` tasks and roles.
3. Run `vagrant up` to start up your vagrant machine. It will build the machine on the first time running the command.
