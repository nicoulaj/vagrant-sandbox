Vagrant sandbox
==========

This project contains a preconfigured Vagrant environment for running various systems in a single command:

 * [Debian](https://www.debian.org)
 * [Ubuntu](https://www.ubuntu.com)
 * [Fedora](https://getfedora.org)
 * [CentOS](https://www.centos.org)
 * [Arch Linux](https://www.archlinux.org)
 * [Gentoo](https://www.gentoo.org)
 * [Void Linux](http://www.voidlinux.eu)
 * [NixOS](https://nixos.org)
 * [OpenSUSE](https://www.opensuse.org)
 * [OpenBSD](https://www.openbsd.org)
 * [FreeBSD](https://www.freebsd.org)
 * [Solaris](http://www.oracle.com/solaris)
 * [Windows](https://www.microsoft.com/windows)
 * [MacOS](http://www.apple.com/macos)
 
 Prerequisites
 ----------------
 
  * [Vagrant](https://www.vagrantup.com)
  * [VirtualBox](https://www.virtualbox.org)
  
  Usage
  -------
  
   * Get the `Vagrantfile`.
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
 
