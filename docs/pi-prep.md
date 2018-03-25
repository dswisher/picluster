# Preparing the Raspberry Pis

* Copy [Raspbian Stretch Lite](https://www.raspberrypi.org/downloads/raspbian/) to a micro SD card. I used [Etcher](https://etcher.io/) and [Sandisk Ultra 64GB Micro SDXC UHS-I Card](https://www.amazon.com/gp/product/B073JYVKNX) cards, along with a Kingston [USB reader](https://www.amazon.com/dp/B00VAGX6MW)..
* Insert the SD card into the Pi and power it up with monitor and keyboard.
* Enable SSH using `sudo raspi-config` (Interfacing Options -> SSH)
* Run `ifconfig` and take note of the IP address.

On another machine:
* Use `ssh-copy-id pi@IP` to copy your SSH public key to the Pi to avoid typing in your password on every login.
* Ssh into the Pi using `ssh pi@IP`. You should not be prompted for a password..
* Change the Pi password, using `passwd`.

