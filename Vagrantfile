# -*- mode: ruby -*-
# vi: set ft=ruby :
userpath = "#{ENV['HOMEPATH']}"

Vagrant.configure("2") do |config|
  config.vm.define "cd" do |d|
    d.vm.box = "ubuntu/focal64"
    d.vm.network "private_network", ip: "10.100.98.200" 
    d.vm.provider "virtualbox" do |v|
	  v.memory = 4096
	  v.cpus = 2
    end
    d.vm.provision "shell", path: "./scripts/provision-dev-vm.sh"
  end
end