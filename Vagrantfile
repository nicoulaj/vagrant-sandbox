#!/usr/bin/env ruby
# Copyright (C) 2016 Julien Nicoulaud <julien.nicoulaud@gmail.com>
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, either version 3 of the License, or
# (at your option) any later version.
# 
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
# 
# You should have received a copy of the GNU General Public License
# along with this program.  If not, see <http://www.gnu.org/licenses/>.

# -*- mode: ruby -*-
# vi: set ft=ruby :

# Systems
systems = {
  :ubuntu => {
    :default_version => 'xenial',
    :default_arch => '64',
    :versions => {
      'precise' => {
        '32' => 'ubuntu/precise32',
        '64' => 'ubuntu/precise64'
      },
      'trusty' => {
        '32' => 'ubuntu/trusty32',
        '64' => 'ubuntu/trusty64'
      },
      'xenial' => {
        '32' => 'ubuntu/xenial32',
        '64' => 'ubuntu/xenial64'
      }
    }
  },
  :debian => {
    :default_version => 'jessie',
    :default_arch => '64',
    :versions => {
      'wheezy' => {
        '32' => 'puppetlabs/debian-7.8-32-nocm',
        '64' => 'debian/wheezy64'
      },
      'jessie' => {
        '32' => 'puppetlabs/debian-8.2-32-nocm',
        '64' => 'debian/jessie64'
      },
    }
  },
  :fedora => {
    :default_version => '24',
    :default_arch => '64',
    :versions => {
      '21' => {
        '64' => 'bento/fedora-21'
      },
      '22' => {
        '64' => 'bento/fedora-22'
      },
      '23' => {
        '64' => 'bento/fedora-23'
      },
      '24' => {
        '64' => 'bento/fedora-24'
      }
    }
  },
  :centos => {
    :default_version => '7',
    :default_arch => '64',
    :versions => {
      '6' => {
        '64' => 'centos/6'
      },
      '7' => {
        '64' => 'centos/7'
      },
    }
  },
  :archlinux => {
    :default_version => 'latest',
    :default_arch => '64',
    :versions => {
      'latest' => {
        '64' => 'terrywang/archlinux'
      },
    }
  },
  :gentoo => {
    :default_version => 'latest',
    :default_arch => '64',
    :versions => {
      'latest' => {
        '64' => 'cmiles/gentoo-amd64-minimal'
      },
    }
  },
  :opensuse => {
    :default_version => '13.2',
    :default_arch => '64',
    :versions => {
      '13.2' => {
        '64' => 'opensuse/openSUSE-13.2-x86_64'
      },
    }
  },
  :openbsd => {
    :default_version => '6.0',
    :default_arch => '64',
    :versions => {
      '5.9' => {
        '64' => 'kaorimatz/openbsd-5.8-amd64'
      },
      '5.8' => {
        '64' => 'kaorimatz/openbsd-5.9-amd64'
      },
      '6.0' => {
        '64' => 'kaorimatz/openbsd-6.0-amd64'
      }
    }
  },
  :freebsd => {
    :default_version => '11.0',
    :default_arch => '64',
    :versions => {
      '10.2' => {
        '64' => 'freebsd/FreeBSD-10.2-STABLE'
      },
      '10.3' => {
        '64' => 'freebsd/FreeBSD-10.3-STABLE'
      },
      '11.0' => {
        '64' => 'freebsd/FreeBSD-11.0-STABLE'
      }
    }
  },
  :solaris => {
    :default_version => '11',
    :default_arch => '64',
    :versions => {
      '10' => {
        '64' => 'tnarik/solaris10-minimal'
      },
      '11' => {
        '64' => 'jonatasbaldin/solaris11'
      }
    }
  }
}

# Help
if ARGV.empty?
  puts 'This Vagrant environment can start the following systems:'
  systems.each do |system, system_data|
    puts '  * %-42s $ vagrant up %s' % ["#{system} (default #{system} #{system_data[:default_version]} #{system_data[:default_arch]})", system]
    system_data[:versions].each do |version, version_data|
    version_data.each do |arch, box|
      puts '      %-40s $ vagrant up %s-%s-%s' % ["#{system} #{version} #{arch}", system, version, arch]
    end
    end
  end
end

# Vagrant configuration
Vagrant.configure("2") do |config|

  # VirtualBox configuration
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
  end

  # Nodes configuration
  systems.each do |system, system_data|
    config.vm.define system, autostart: false do |node|
      node.vm.box = system_data[:versions][system_data[:default_version]][system_data[:default_arch]]
    end
    system_data[:versions].each do |version, version_data|
      version_data.each do |arch, box|
        config.vm.define "#{system}-#{version}-#{arch}", autostart: false do |node|
          node.vm.box = box
        end
      end
    end
  end

end
