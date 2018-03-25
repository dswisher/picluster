# Upgrading Pi packages



On the control machine:

* `cd generic`
* Edit the `inventory` file to match your setup.
* Run `ansible-playbook -i inventory apt-upgrade.yml` to upgrade all apt packages. This may take a while.


