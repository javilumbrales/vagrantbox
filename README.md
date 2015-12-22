# About
This is a Vagrant box that installs Apache + PHP5.5 + MySQL (MariaDB) with a few common PHP extensions, including curl, gd, imagick, xdebug, ideal to run a php framework such as Magento or Symfony2.
It's been generated with https://puphpet.com/ and it almost hasn't been changed, other than to add the readme instructions.

# Requirements

This VM works properly within the following environment (it might well work in different, versions, but hasn't been tested):

- Mac OS X Yosemite/El Capitan

- VirtualBox 4.3.x

- Vagrant 1.7.4

# Installation

I had a few issues with an old box version and a missing NFS plugin to properly map the shared folder. In order to get it to run properly, just run the below commands:

- It was failing while provisioning at some point showing an error:

``default: Error: Could not parse for environment production: Is a directory```

Eventually, I managed to solve it by upgrading the vm running this command:

```vagrant box update```

If you want to use (and you should want to, for performance reasons) NFS shared folders, don't forget to run this command, otherwise the mapped user & group within the machine will be 502:dialout.:

```vagrant plugin install vagrant-bindfs```


# Usage

    vagrant up


Feel free to contribute, and contact me for any issues.

You can also drop us a comment at www.thedeveloperworldisyours.com
This Vagrant box is actively used and maintained by www.42moto.com

