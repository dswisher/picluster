# Preparing the Ansible Control Machine

* Install Ansible using `pip install ansible`.
* Install Passlib using `pip install passlib`. This is used to set a password for accounts on the Pis. Refer to the Ansible [prompts](http://docs.ansible.com/ansible/latest/user_guide/playbooks_prompts.html) doc and password [FAQ](http://docs.ansible.com/ansible/latest/reference_appendices/faq.html#how-do-i-generate-crypted-passwords-for-the-user-module) for details, or look at the [sample](https://github.com/ansible/ansible-examples/blob/master/language_features/prompts.yml).
* Edit `~/.ansible.cfg` and set the following (tweaking for your environment):

```
[defaults]
inventory = /home/swish/git/picluster/inventory
```

