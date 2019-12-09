# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.

Vagrant.configure("2") do |config|
  
  # MySQL Cluster dengan 3 node
  (59..65).each do |i|
    config.vm.define "node1#{i}" do |node|
      node.vm.hostname = "node1#{i}"
      node.vm.box = "bento/ubuntu-16.04"
      node.vm.network "private_network", ip: "192.168.16.1#{i}"
      
      node.vm.provider "virtualbox" do |vb|
        vb.name = "node1#{i}"
        vb.gui = false
        vb.memory = "512"
      end
  
    end
  end

  config.vm.define "node110" do |node|
    node.vm.hostname = "node110"
    node.vm.box = "bento/ubuntu-16.04"
    node.vm.network "private_network", ip: "192.168.16.166"
    
    node.vm.provider "virtualbox" do |vb|
      vb.name = "node110"
      vb.gui = false
      vb.memory = "512"
    end

  end


end

