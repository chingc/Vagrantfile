# Vagrantfile Templates

Templates to create virtual machines with Vagrant.

## Usage

1. Install [Vagrant](https://www.vagrantup.com/)
1. Navigate to either the `linux`, `macos`, or `windows` directory
1. Run `vagrant up`

## Configuration

Generic settings can be found in `settings.rb`.  Settings more specific to each OS are in their respective `Vagrantfile`.

Provision scripts are located in the `run_once` and `run_always` directories.  The scripts under `run_once` are only executed if the machine hasn't been provisioned, while those under `run_always` will execute for every `vagrant up`.

The filename of each script is prefixed with a number so that it will run in a certain order.  A lower number has higher priority.  Scripts in `run_once` are processed before those in `run_always`.
