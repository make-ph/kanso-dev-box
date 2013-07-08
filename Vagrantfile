# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ringtail64-rvm"

  config.vm.network :private_network, ip: "192.168.33.11"

  config.vm.synced_folder ".", "/vagrant", id: "vagrant-root", :nfs => true

  chef_cookbooks_path = ["chef/cookbooks"]
  config.vm.provision :chef_solo do |chef|
    chef.cookbooks_path = chef_cookbooks_path
    chef.add_recipe "recipe[apt]"
    chef.add_recipe "recipe[build-essential]"
    chef.add_recipe "recipe[vim]"
  end
end
