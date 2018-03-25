# Preparing the Ansible Control Machine

* Install Ansible using `pip install ansible`.
* Edit `~/.ansible.cfg` and set the following (tweaking for your environment):

```
[defaults]
inventory = /home/swish/git/picluster/inventory
```

