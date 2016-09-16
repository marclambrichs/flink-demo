# neo4j test environment using vagrant

## Requirements

	virtualbox => https://www.virtualbox.org/
	vagrant    => https://www.vagrantup.com/

## Setup

	git submodule update --init

## Environments

### Single
1 node => neo4j community edition

	cd vagrant/single
	vagrant up

### HA
3 nodes => neo4j enterprise edition

	cd vagrant/ha
	vagrant up

## Quirks

### EOL problems on windows?

    git config --global core.autocrlf false


### proxy?
Configure your proxy in the Vagrantfile. The vagrant-proxyconf plugin has - conveniently -
already been added.

    config.proxy.http     = "http://yourproxy:8080"
    config.proxy.https    = "http://yourproxy:8080"
    config.proxy.no_proxy = "localhost,127.0.0.1"
