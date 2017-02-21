# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.box_check_update = false
  config.vm.network "private_network", ip: "192.168.33.10"
  # config.vm.network "public_network"
  # config.vm.synced_folder "../data", "/vagrant_data"
  config.vm.provider "virtualbox" do |vb|
    vb.gui = false 
    vb.memory = "512"
  end
  config.vm.provision "shell", inline: <<-SHELL
    apt-get -y update
    apt-get -y upgrade
  SHELL
end
