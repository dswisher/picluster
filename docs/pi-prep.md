# Preparing the Raspberry Pis


## Using Monitor and Keyboard

* Copy [Raspbian Stretch Lite](https://www.raspberrypi.org/downloads/raspbian/) to a micro SD card. I used [Etcher](https://etcher.io/) and [Sandisk Ultra 64GB Micro SDXC UHS-I Card](https://www.amazon.com/gp/product/B073JYVKNX) cards, along with a Kingston [USB reader](https://www.amazon.com/dp/B00VAGX6MW)..
* Insert the SD card into the Pi and power it up with monitor and keyboard.
* Enable SSH using `sudo raspi-config` (Interfacing Options -> SSH)
* Run `ifconfig` and take note of the IP address.
* Proceed to the "Finishing" step, below.

## Headless

* Copy [Raspbian Stretch Lite](https://www.raspberrypi.org/downloads/raspbian/) to a micro SD card. I used [Etcher](https://etcher.io/) and [Sandisk Ultra 64GB Micro SDXC UHS-I Card](https://www.amazon.com/gp/product/B073JYVKNX) cards, along with a Kingston [USB reader](https://www.amazon.com/dp/B00VAGX6MW)..
* Remount the SD card in windows. For me, it showed up as a drive called `boot`. Create an empty file called `ssh` on the root of that partition (PS: `New-Item ssh -ItemType file`)
* Unmount the SD card and put it in the Pi, and boot up the Pi.
* Use an IP scanner to find the IP. I used "Angry IP Scanner" (`ipscan-win64-3.5.2.exe`). Take note of the IP.
* Proceed to the "Finishing" step, below.

## Finishing

On another machine:
* Use `ssh-copy-id pi@IP` to copy your SSH public key to the Pi to avoid typing in your password on every login.
* Ssh into the Pi using `ssh pi@IP`. You should not be prompted for a password..
* Change the Pi password, using `passwd`.

