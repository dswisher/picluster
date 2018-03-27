# Raspberry Pi Networking Setup

This is based on the setup from geerlingguy, [here](https://github.com/geerlingguy/raspberry-pi-dramble/tree/master/setup/networking).

I tweaked it to (I think) work for Stretch.

To run the playbook:
* Edit `inventory` to include your host IPs (the ones assigned by DHCP on initial boot).
* Edit `vars.yml` to include the mapping between MAC address and IP address/hostname.
* Run `ansible-playbook -i inventory main.yml`


