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
    :default_version => 'zesty',
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
      },
      'yakkety' => {
        '32' => 'ubuntu/yakkety32',
        '64' => 'ubuntu/yakkety64'
      },
      'zesty' => {
        '32' => 'ubuntu/zesty32',
        '64' => 'ubuntu/zesty64'
      }
    }
  },
  :debian => {
    :default_version => 'stretch',
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
      'stretch' => {
        '32' => 'remram/debian-9-i386',
        '64' => 'debian/stretch64'
      },
    }
  },
  :fedora => {
    :default_version => '32',
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
      },
      '25' => {
        '64' => 'bento/fedora-25'
      },
      '26' => {
        '64' => 'bento/fedora-26'
      },
      '32' => {
        '64' => 'bento/fedora-32'
      }
    }
  },
  :centos => {
    :default_version => '8',
    :default_arch => '64',
    :versions => {
      '5' => {
        '64' => 'bento/centos-5.11'
      },
      '6' => {
        '64' => 'bento/centos-6.8'
      },
      '7' => {
        '64' => 'bento/centos-7.3'
      },
      '8' => {
        '64' => 'bento/centos-8.2'
      },
    }
  },
  :archlinux => {
    :default_version => 'latest',
    :default_arch => '64',
    :versions => {
      'latest' => {
        '64' => 'wholebits/arch-64'
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
  :voidlinux => {
    :default_version => 'latest',
    :default_arch => '64',
    :versions => {
      'latest' => {
        '64' => 'antonio-malcolm/base-void-x86_64'
      },
    }
  },
  :nixos => {
    :default_version => '16.09',
    :default_arch => '64',
    :versions => {
      '16.09' => {
        '32' => 'nixos/nixos-16.09-i686',
        '64' => 'nixos/nixos-16.09-x86_64'
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
    :default_version => '12.0',
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
      },
      '12.0' => {
        '64' => 'freebsd/FreeBSD-12.0-STABLE'
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
  },
  :windows => {
    :default_version => '2012-standard',
    :default_arch => '64',
    :versions => {
      '7-enterprise' => {
        '32' => 'opentable/win-7-enterprise-i386-nocm',
        '64' => 'opentable/win-7-enterprise-amd64-nocm'
      },
      '7-home' => {
        '32' => 'opentable/win-7-homepremium-i386-nocm',
        '64' => 'opentable/win-7-homepremium-amd64-nocm'
      },
      '7-professional' => {
        '32' => 'opentable/win-7-professional-i386-nocm',
        '64' => 'opentable/win-7-professional-amd64-nocm'
      },
      '7-ultimate' => {
        '32' => 'opentable/win-7-ultimate-i386-nocm',
        '64' => 'opentable/win-7-ultimate-amd64-nocm'
      },
      '8-core' => {
        '32' => 'opentable/win-8-core-i386-nocm',
        '64' => 'opentable/win-8-core-amd64-nocm'
      },
      '8-enterprise' => {
        '32' => 'opentable/win-8-enterprise-i386-nocm',
        '64' => 'opentable/win-8-enterprise-amd64-nocm'
      },
      '8-pro' => {
        '32' => 'opentable/win-8-pro-i386-nocm',
        '64' => 'opentable/win-8-pro-amd64-nocm'
      },
      '8.1-core' => {
        '32' => 'opentable/win-8.1-core-i386-nocm',
        '64' => 'opentable/win-8.1-core-amd64-nocm'
      },
      '8.1-enterprise' => {
        '32' => 'opentable/win-8.1-enterprise-i386-nocm',
        '64' => 'opentable/win-8.1-enterprise-amd64-nocm'
      },
      '2008-datacenter' => {
        '32' => 'opentable/win-2008-datacenter-i386-nocm',
        '64' => 'opentable/win-2008-datacenter-amd64-nocm'
      },
      '2008-enterprise' => {
        '32' => 'opentable/win-2008-enterprise-i386-nocm',
        '64' => 'opentable/win-2008-enterprise-amd64-nocm'
      },
      '2012-datacenter' => {
        '64' => 'opentable/win-2012-datacenter-amd64-nocm'
      },
      '2012-essentials' => {
        '64' => 'opentable/win-2012-essentials-amd64-nocm'
      },
      '2012-foundation' => {
        '64' => 'opentable/win-2012-foundation-amd64-nocm'
      },
      '2012-standard' => {
        '64' => 'opentable/win-2012-standard-amd64-nocm'
      }
    }
  },
  :macos => {
    :default_version => 'sierra',
    :default_arch => '64',
    :versions => {
      'yosemite' => {
        '64' => 'jhcook/osx-yosemite-10.10'
      },
      'elcapitan' => {
        '64' => 'jhcook/osx-elcapitan-10.11'
      },
      'sierra' => {
        '64' => 'jhcook/macos-sierra'
      }
    }
  },
  :kali => {
    :default_version => 'acortespi20',
    :default_arch => 'v1.0',
    :versions => {
      'acortespi20' => {
        'v1.0' => 'acortespi20/kali'
      }
    }
  },
}

# Help
if ARGV.empty?
  puts 'This Vagrant environment can start the following systems:'
  systems.each do |system, system_data|
    puts '  * %-42s $ vagrant up %s' % ["#{system} (default #{system_data[:default_version]}/#{system_data[:default_arch]})", system]
    system_data[:versions].each do |version, version_data|
      puts '      %-40s $ vagrant up %s-%s' % ["version: #{version}", system, version]
      version_data.each do |arch, box|
        puts '        %-38s $ vagrant up %s-%s-%s' % ["arch: #{arch}", system, version, arch]
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
      config.vm.define "#{system}-#{version}", autostart: false do |node|
        node.vm.box = version_data[system_data[:default_arch]]
      end
      version_data.each do |arch, box|
        config.vm.define "#{system}-#{version}-#{arch}", autostart: false do |node|
          node.vm.box = box
        end
      end
    end
  end

end
