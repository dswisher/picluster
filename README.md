# Raspberry Pi Cluster

This repo contains scripts and notes that I've used while setting up a Raspberry Pi cluster.
The purpose of the cluster is to experiment with various forms of distributed computing and devops tools.

[Ansible](http://docs.ansible.com/ansible/latest/intro_getting_started.html) is used to configure the Pis.
This requires a "Control Machine" where Ansible is run, and it uses ssh to access the Pis.
I use Windows Subsystem for Linux on my windows box for this purpose.


# Setup

First, configure the hosts.

* [Control Machine](docs/control-prep.md)
* [Raspberry Pi preparation](docs/pi-prep.md)

From now on, we'll use `ansible` to do all the work, so we'll be running on the control machine.

* Set up networking: [README](setup/networking/README.md)
* Edit the `inventory` file to match your systems, specifically the `pi3s` group. Add new hostname to local `/etc/hosts` file.
* Maintenance: `ansible-playbook maint.yml`  (upgrades apt packages, etc)
* Install my stuff: `ansible-playbook swish.yml`

# Useful Tips

* Ping: `ansible all -m ping`
* Shutdown: `ansible-playbook shutdown.yml`

# Links

* Ansible: [getting started](http://docs.ansible.com/ansible/latest/intro_getting_started.html) - [command line tools](https://docs.ansible.com/ansible/latest/command_line_tools.html) - [inventory](http://docs.ansible.com/ansible/latest/intro_inventory.html) - [playbooks](http://docs.ansible.com/ansible/latest/playbooks_intro.html)
* Ansible samples: [slack notification](https://github.com/hico-horiuchi/ansible-playbooks/blob/master/apt/apt.yml)
* Hadoop and Ansible: [dobachi](https://github.com/dobachi/ansible-hadoop) - [Daniel Watrous](https://github.com/dwatrous/hadoop-multi-server-ansible) - [godatadriven](https://github.com/godatadriven/ansible_cluster)
* Raspberry Pi [hardware](https://elinux.org/RPi_HardwareHistory) info; `cat /proc/cpuinfo` and use the table on the page to identify the board based on the `Revision`.
* Raspberry Pi Dramble by geerlingguy - [github](https://github.com/geerlingguy/raspberry-pi-dramble)

