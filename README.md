Vagrant sandbox
===============

This project contains a preconfigured Vagrant environment for running various systems in a single command:

| System                                       | Command                |
| -------------------------------------------- | ---------------------- |
| [Debian](https://www.debian.org)             | `vagrant up debian`    |
| [Ubuntu](https://www.ubuntu.com)             | `vagrant up ubuntu`    |
| [Fedora](https://getfedora.org)              | `vagrant up fedora`    |
| [CentOS](https://www.centos.org)             | `vagrant up centos`    |
| [Arch Linux](https://www.archlinux.org)      | `vagrant up archlinux` |
| [Gentoo](https://www.gentoo.org)             | `vagrant up gentoo`    |
| [Void Linux](http://www.voidlinux.eu)        | `vagrant up voidlinux` |
| [NixOS](https://nixos.org)                   | `vagrant up nixos`     |
| [OpenSUSE](https://www.opensuse.org)         | `vagrant up opensuse`  |
| [OpenBSD](https://www.openbsd.org)           | `vagrant up openbsd`   |
| [FreeBSD](https://www.freebsd.org)           | `vagrant up freebsd`   |
| [Solaris](http://www.oracle.com/solaris)     | `vagrant up solaris`   |
| [Windows](https://www.microsoft.com/windows) | `vagrant up windows`   |
| [MacOS](http://www.apple.com/macos)          | `vagrant up macos`     |


Prerequisites
-------------

  * [Vagrant](https://www.vagrantup.com)
  * [VirtualBox](https://www.virtualbox.org)

Usage
-----

   * Get the `Vagrantfile`:

            git clone https://github.com/nicoulaj/vagrant-sandbox.git
            cd vagrant-sandbox

   * Run `vagrant` to see the full list of available systems:

            This Vagrant environment can start the following systems:
              * ubuntu (default ubuntu xenial 64)          $ vagrant up ubuntu
                  ubuntu precise 32                        $ vagrant up ubuntu-precise-32
                  ubuntu precise 64                        $ vagrant up ubuntu-precise-64
                  ubuntu trusty 32                         $ vagrant up ubuntu-trusty-32
                  ubuntu trusty 64                         $ vagrant up ubuntu-trusty-64
                  ubuntu xenial 32                         $ vagrant up ubuntu-xenial-32
                  ubuntu xenial 64                         $ vagrant up ubuntu-xenial-64
              * debian (default debian jessie 64)          $ vagrant up debian
                  debian wheezy 32                         $ vagrant up debian-wheezy-32
                  debian wheezy 64                         $ vagrant up debian-wheezy-64
                  debian jessie 32                         $ vagrant up debian-jessie-32
                  debian jessie 64                         $ vagrant up debian-jessie-64
            ...

 * Start a virtual machine:
 
        $ vagrant up centos
