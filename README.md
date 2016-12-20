Vagrant sandbox
==========

This project contains a preconfigured Vagrant environment for running various systems in a single command:

 * [Debian](https://www.debian.org)
 * [Ubuntu](https://www.ubuntu.com)
 * [Fedora](https://getfedora.org)
 * [CentOS](https://www.centos.org)
 * [Arch Linux](https://www.archlinux.org)
 * [Gentoo](https://www.gentoo.org)
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
              * fedora (default fedora 24 64)              $ vagrant up fedora
                  fedora 21 64                             $ vagrant up fedora-21-64
                  fedora 22 64                             $ vagrant up fedora-22-64
                  fedora 23 64                             $ vagrant up fedora-23-64
                  fedora 24 64                             $ vagrant up fedora-24-64
              * centos (default centos 7 64)               $ vagrant up centos
                  centos 6 64                              $ vagrant up centos-6-64
                  centos 7 64                              $ vagrant up centos-7-64
              * archlinux (default archlinux latest 64)    $ vagrant up archlinux
                  archlinux latest 64                      $ vagrant up archlinux-latest-64
              * gentoo (default gentoo latest 64)          $ vagrant up gentoo
                  gentoo latest 64                         $ vagrant up gentoo-latest-64
              * opensuse (default opensuse 13.2 64)        $ vagrant up opensuse
                  opensuse 13.2 64                         $ vagrant up opensuse-13.2-64
              * openbsd (default openbsd 6.0 64)           $ vagrant up openbsd
                  openbsd 5.9 64                           $ vagrant up openbsd-5.9-64
                  openbsd 5.8 64                           $ vagrant up openbsd-5.8-64
                  openbsd 6.0 64                           $ vagrant up openbsd-6.0-64
              * freebsd (default freebsd 11.0 64)          $ vagrant up freebsd
                  freebsd 10.2 64                          $ vagrant up freebsd-10.2-64
                  freebsd 10.3 64                          $ vagrant up freebsd-10.3-64
                  freebsd 11.0 64                          $ vagrant up freebsd-11.0-64
              * solaris (default solaris 11 64)            $ vagrant up solaris
                  solaris 10 64                            $ vagrant up solaris-10-64
                  solaris 11 64                            $ vagrant up solaris-11-64
              * windows (default windows 2012-standard 64) $ vagrant up windows
                  windows 7-enterprise 32                  $ vagrant up windows-7-enterprise-32
                  windows 7-enterprise 64                  $ vagrant up windows-7-enterprise-64
                  windows 7-home 32                        $ vagrant up windows-7-home-32
                  windows 7-home 64                        $ vagrant up windows-7-home-64
                  windows 7-professional 32                $ vagrant up windows-7-professional-32
                  windows 7-professional 64                $ vagrant up windows-7-professional-64
                  windows 7-ultimate 32                    $ vagrant up windows-7-ultimate-32
                  windows 7-ultimate 64                    $ vagrant up windows-7-ultimate-64
                  windows 8-core 32                        $ vagrant up windows-8-core-32
                  windows 8-core 64                        $ vagrant up windows-8-core-64
                  windows 8-enterprise 32                  $ vagrant up windows-8-enterprise-32
                  windows 8-enterprise 64                  $ vagrant up windows-8-enterprise-64
                  windows 8-pro 32                         $ vagrant up windows-8-pro-32
                  windows 8-pro 64                         $ vagrant up windows-8-pro-64
                  windows 8.1-core 32                      $ vagrant up windows-8.1-core-32
                  windows 8.1-core 64                      $ vagrant up windows-8.1-core-64
                  windows 8.1-enterprise 64                $ vagrant up windows-8.1-enterprise-64
                  windows 2008-datacenter 32               $ vagrant up windows-2008-datacenter-32
                  windows 2008-datacenter 64               $ vagrant up windows-2008-datacenter-64
                  windows 2008-enterprise 32               $ vagrant up windows-2008-enterprise-32
                  windows 2008-enterprise 64               $ vagrant up windows-2008-enterprise-64
                  windows 2012-datacenter 64               $ vagrant up windows-2012-datacenter-64
                  windows 2012-essentials 64               $ vagrant up windows-2012-essentials-64
                  windows 2012-foundation 64               $ vagrant up windows-2012-foundation-64
                  windows 2012-standard 64                 $ vagrant up windows-2012-standard-64
              * macos (default macos sierra 64)            $ vagrant up macos
                  macos yosemite 64                        $ vagrant up macos-yosemite-64
                  macos elcapitan 64                       $ vagrant up macos-elcapitan-64
                  macos sierra 64                          $ vagrant up macos-sierra-64

 * Start a virtual machine:
 
        $ vagrant up centos
 
