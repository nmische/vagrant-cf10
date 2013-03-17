# ColdFusion 10 Vagrant Environment
This is a [Vagrant](http://vagrantup.com) project for [ColdFusion 10](http://www.adobe.com/products/coldfusion-family.html) development.

There are two Vagrantfiles for this project depending on how you are managing your Vagrant environments. 

* Vagrantfile.librarian - If you are using [Librarian-Chef](https://github.com/applicationsonline/librarian-chef)
* Vagrantfile.berks - If you are using [Berkshelf](http://berkshelf.com/)

## Prerequietes
1. [Vagrant](http://downloads.vagrantup.com) installed
 - Requires [VirtualBox](https://www.virtualbox.org/wiki/Downloads) installed
1. [Ruby](http://www.ruby-lang.org/en/downloads) installed 
1. [Git](http://git-scm.com/downloads) installed  
1. Either Librarian or Berkshelf installed
1. [Downloaded](https://www.adobe.com/cfusion/tdrc/index.cfm?product=coldfusion) **32bit Linux** ColdFusion 10 installer from Adobe 

## Using with Librarian
1. Clone this repository to your Vagrant project directory, i.e. `/vagrant/cf10`
1. Copy `Vagrantfile.librarian` to `Vagrantfile`
1. Run `librarian-chef install` in the Vagrant project directory
1. Place 32bit Linux ColdFusion 10 installer from Adobe in the Vagrant project directory, i.e. `/vagrant/cf10/ColdFusion_10_WWEJ_linux32.bin`
1. Run `vagrant up`
1. Browse to `http://192.168.33.10/CFIDE/administrator` and login with username: admin, password: vagrant

For example:
    
    $ git clone git@github.com:nmische/vagrant-cf10.git /vagrant/cf10
    $ cd /vagrant/cf10
    $ cp Vagrantfile.librarian Vagrantfile
    $ librarian-chef install
    # download installer from adobe.com to current directory
    # /vagrant/cf10/ColdFusion_10_WWEJ_linux32.bin
    $ vagrant up

## Using with Berkshelf
1. Clone this repository to your Vagrant project directory, `/vagrant/cf10`
1. Copy `Vagrantfile.berks` to `Vagrantfile`
1. Place 32bit Linux ColdFusion 10 installer from Adobe in the Vagrant project directory, i.e. `/vagrant/cf10/ColdFusion_10_WWEJ_linux32.bin`
1. Run `vagrant up`
1. Browse to `http://192.168.33.10/CFIDE/administrator` and login with username: admin, password: vagrant

For example:
    
    $ git clone git@github.com:nmische/vagrant-cf10.git /vagrant/cf10
    $ cd /vagrant/cf10
    $ cp Vagrantfile.berks Vagrantfile
    # download installer from adobe.com to current directory
    # /vagrant/cf10/ColdFusion_10_WWEJ_linux32.bin
    $ vagrant up

## Where does my application go?
There is a shared drive between the Vagrant virtual machine and your host computer. Adding/editing files here will immediately be available at `http://192.168.33.10/`

For example:

    /vagrant/cf10/wwwroot