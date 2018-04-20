# Preseed files

Fully automatic unattended linux install can be used to speed up the process and remove human error.

### Generate password hash

`mkpasswd -m sha-512`

Change the hash in the preseed.cfg with the generated one

### Boot Options

You can use any of the Debian mini or netboot iso images.

#### Method 1 - boot parameter

Hit tab on boot up and pass the following parameters.

`append auto preseed/url=https://raw.githubusercontent.com/mattwind/preseed/master/preseed.cfg keyboard-configuration/xkb-keymap=us priority=critical locale=en_US`

#### Method 2 - custom iso

First download the Debian installation ISO.

`wget http://ftp.debian.org/debian/dists/stable/main/installer-amd64/current/images/netboot/mini.iso`

On linux the easiest way to edit the ISO by using isomaster.

`apt install isomaster`

Launch isomaster and just copy the `txt.cfg` file to the root directory of the ISO and save to preseed.iso
