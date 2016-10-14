# F5_lab

## Setup ##

### Required Software ###
Download and install VirtualBox.
Download and install Vagrant.

### Cumulus ###
Download the Cumulus VX box file for Vagrant.

Install the Cumulus Linux plugin for Vagrant:
`vagrant plugin install vagrant-cumulus`

Add the Cumulus VX Vagrant box file.
`vagrant box add cumulus-vx-<version downloaded> /<path to download>/cumulus-linux-<version downloaded>-vx-amd64-1471979027.dc7e2adza017cfb.box`

### Vagrant ###
N/A

### VirtualBox ###
N/A

## Tree ##
	.
	└── F5_Lab
	    ├── README.md
	    ├── Vagrantfile
	    └── nginx_install.sh