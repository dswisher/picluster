# Raspberry Pi Cluster

This repo contains scripts and notes that I've used while setting up a Raspberry Pi cluster.
The purpose of the cluster is to experiment with various forms of distributed computing and devops tools.

Ansible is used to configure the Pis.
This requires a "Control Machine" where Ansible is run, and it uses ssh to access the Pis.
I use Windows Subsystem for Linux on my windows box for this purpose.


# Setup

First, configure the hosts.

* [Control Machine](docs/control-prep.md)
* [Raspberry Pi preparation](docs/pi-prep.md)

From now on, we'll use `ansible` to do all the work, so we'll be running on the control machine.

* [Upgrade packages](docs/upgrade.md)

# Links

* Raspberry Pi [hardware](https://elinux.org/RPi_HardwareHistory) info; `cat /proc/cpuinfo` and use the table on the page to identify the board based on the `Revision`.
* Raspberry Pi Dramble by geerlingguy - [github](https://github.com/geerlingguy/raspberry-pi-dramble)

