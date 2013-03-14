# ColdFusion 10 Vagrant Environment

This is a Vagrant project for ColdFusion 10 development.

There are two Vagrantfiles for this project depending on how you are managing your Vagrant enviornments. 

* Vagrantfile.berks - If you are using [Berkshelf](http://berkshelf.com/)
* Vagrantfile.librarian - If you are using [Librarian-Chef](https://github.com/applicationsonline/librarian-chef)

## Using with Librarian

1. Clone this repository to your Vagrant project directory, i.e. `/vagrant/cf10`
2. Copy `Vagrantfile.librarian` to `Vagrantfile`
3. Run `librarian-chef install` in the Vagrant project directory
4. Download the 32bit Linux ColdFusion 10 installer from Adobe and place it in the Vagrant project directory, i.e. `/vagrant/cf10/ColdFusion_10_WWEJ_linux32.bin`
5. Run `vagrant up`
6. Browse to 192.168.33.10/CFIDE/administrator and login with username: admin, password: vagrant


## Using with Berkshelf

1. Clone this repository to your Vagrant project directory, `/vagrant/cf10`
2. Copy `Vagrantfile.berks` to `Vagrantfile`
3. Download the 32bit Linux ColdFusion 10 installer from Adobe and place it in the Vagrant project directory, i.e. `/vagrant/cf10/ColdFusion_10_WWEJ_linux32.bin`
5. Run `vagrant up`
6. Browse to 192.168.33.10/CFIDE/administrator and login with username: admin, password: vagrant







