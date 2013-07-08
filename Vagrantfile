# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ringtail64-rvm"

  config.vm.network :private_network, ip: "192.168.33.11"

  config.vm.synced_folder ".", "/vagrant", id: "vagrant-root", :nfs => true
end
