Vagrant sandbox
==========

This project contains a preconfigured Vagrant environment for running various systems in a single command:

 * [Debian](https://www.debian.org)
 * [Ubuntu](https://www.ubuntu.com)
 * [Fedora](https://getfedora.org)
 * [CentOS](https://www.centos.org)
 * [Arch Linux](https://www.archlinux.org)
 * [OpenBSD](https://www.openbsd.org)
 * [FreeBSD](https://www.freebsd.org)
 
 Prerequisites
 ----------------
 
  * [Vagrant](https://www.vagrantup.com)
  * [VirtualBox](https://www.virtualbox.org)
  
  Usage
  -------
  
   * Get the `Vagrantfile`.
   * Run `vagrant` to see the full list of available systems:

         $ vagrant
         This Vagrant environment can start the following systems:
           * ubuntu (default ubuntu xenial 64)          $ vagrant up ubuntu
               ubuntu precise 32                        $ vagrant up ubuntu-precise-32
               ubuntu precise 64                        $ vagrant up ubuntu-precise-64
               ubuntu trusty 32                         $ vagrant up ubuntu-trusty-32
               ubuntu trusty 64                         $ vagrant up ubuntu-trusty-64
               ubuntu xenial 32                         $ vagrant up ubuntu-xenial-32
               ubuntu xenial 64                         $ vagrant up ubuntu-xenial-64
           * centos (default centos 7 64)               $ vagrant up centos
               centos 6 64                              $ vagrant up centos-6-64
               centos 7 64                              $ vagrant up centos-7-64
           * archlinux (default archlinux latest 64)    $ vagrant up archlinux
               archlinux latest 64                      $ vagrant up archlinux-latest-64

 * Start a virtual machine:
 
         $ vagrant up centos
 