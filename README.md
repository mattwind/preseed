# Preseed files

Fully automatic unattended linux install can be used to speed up the process and remove human error.

### Generate password hash

`mkpasswd -m sha-512`

### Post boot script

This script will get executed after the installation.

### Kernel boot parameter

You can use any of the Debian mini or netboot iso images.

Option 1) Hit tab on boot up and pass the following parameters.

`append auto preseed/url=https://raw.githubusercontent.com/mattwind/preseed/master/preseed.cfg keyboard-configuration/xkb-keymap=us priority=critical locale=en_US`

Option 2) Modify the iso and edit the linux boot command.

On linux the easiest method is to install `isomaster`

`wget http://ftp.debian.org/debian/dists/stable/main/installer-amd64/current/images/netboot/mini.iso`

Launch isomaster and just copy the `txt.cfg` file to the root directory of the iso.
