# contrail-packer

contrail-packer provides [Packer](http://packer.io) templates for building the following environments for [Juniper's Contrail](http://www.juniper.net/us/en/products-services/sdn/contrail/):

- Vagrant boxes for VirtualBox and VMware (Workstation and Fusion)
- Amazon EC2 (AMI)
- DigitalOcean
- OpenStack
- others in the near future

Other than relying on Packer, this project builds upon the awesome work of [Tim Dysinger's baseboxes](https://github.com/dysinger/basebox) and [Opscode's Bento](https://github.com/opscode/bento).

To build these boxes locally, you will need ISO images, provided by Juniper,
and they must match the SHA-1 hashes that are present in the JSON templates.

# OS support

For now, only CentOS 6 will be supported, based on the available binary packages for the commercial version of Contrail.

# Requirements

For now, only Vagrant boxes are supported, so here's what you'll need:

- [Packer 0.3.9](http://www.packer.io/downloads.html) (or higher)
- [Vagrant 1.3.5](http://downloads.vagrantup.com/) (or higher)
- [Ruby 1.9.3](https://www.ruby-lang.org/en/) to run [Thor](http://whatisthor.com/) commands and peform tests.  [rbenv](https://github.com/sstephenson/rbenv) is recommended for Ruby, since it will automagically switch to `.ruby-version`
- [vagrant-omnibus](https://github.com/schisamo/vagrant-omnibus) is required, as it installs [Chef Solo](http://www.opscode.com/chef/) on the bare systems for provisioning

# Getting started

1. Clone this repository in git, and cd into it
2. Run `thor list` for available commands, as described in detail in the `Thorfile`

# Contributing

- Check [doc/TODO.md] for the list of current feature requests
- Open an issue on github, whether you want to contribute or make a feature request

# Author

- Author:: John Deatherage - (<john@routeoflastresort.com>)

Copyright:: 2013, John Deatherage (<john@routeoflastresort.com>)