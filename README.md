# LITMUS^RT Vagrant Virtual Machine

This is a Vagrant repository for getting up and running with LITMUS^RT
development.

## Getting Started

First follow the instructions at http://www.vagrantup.com/ to install
Vagrant on your system. Vagrant is a configuration-management software
used mostly for deploying VM's in large clouds environments, but we're
going to use it to ease LITMUS^RT development :-)

To fire up the VM, do the following:

    $ cd /path/where/you/downloaded/litmus-vm-tools
    $ vagrant up

That's it! After it boots up, you should now be able to SSH into the VM
with the following:

    $ vagrant ssh

NOTE:  to prevent Vagrant from downloading the image each time, it is
recommended that you instead add the box once to your system and then
run vagrant like so:

    $ vagrant box add litmus http://sighack.com/litmus.box
    $ cd /path/where/you/downloaded/litmus-vm-tools
    $ vagrant up

To instead get the SSH config of the running VM, do the following:

    $ vagrant ssh-config

You may also just want to just append this to you SSH configuration file:

    $ vagrant ssh-config >> $HOME/.ssh/config


## The VM Environment

The VM image is based on Ubuntu Precise Pangolin 64-bit (LTS release
supported till 2017). The latest (at the time of writing this) LITMUS^RT
kernel has been installed and automatically booted.

You will be logged in as root automatically. There is a 'litmus' folder
present in the home directory for the root user (/root/litmus/) which
contains a bunch of useful stuff. See /root/litmus/README in the VM for
further details.

Happy hacking! (and remember to post back patches upstream!)
