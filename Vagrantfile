# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.

  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.define "compass" do |compass|
    compass.vm.box = "trusty64"

    compass.vm.network "private_network", ip: "10.1.0.11"
    compass.vm.provision "ansible" do |ansible|
      ansible.playbook = "bring_up_compass.yml"
    end

    compass.vm.provider "virtualbox" do |vbox|
      vbox.memory = 2048
    end
  end
end
