# madcap #

The increasing number of devops tools out there are making it easier to develop and deploy scalable apps in the cloud. 
This repo is my personal template for projects which are developed for use with coreos using fleet, etcd and docker.

This is a direct copy of https://github.com/coreos/coreos-vagrant with modifications for personal projects and for learning.

## Requirements ##

	* Vagrant 1.6.0 and greater.
	* VirtualBox 4.3.10 and greater.

## Setup ##

The normal routine to get a development testbed setup is as follows:

	1. Copy and edit config.rb for vagrant specific settings, such as number of cores.
	2. Create a token at https://discovery.etcd.io/new
	3. Modify user-data to use this token in coreos: etcd: discovery:
	4. Specify any additional configuration parameters for using services in user-data

Finally, issue the normal:

	$ vagrant up

## Updating ##

To get the latest coreos box updates with Vagrant, periodically you should:

	$ vagrant halt
	$ vagrant destroy
	$ vagrant box remove coreos --provider virtualbox

