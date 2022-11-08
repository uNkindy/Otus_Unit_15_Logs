# -*- mode: ruby -*-
# vi: set ft=ruby :

require 'open3'
require 'fileutils'

Vagrant.configure("2") do |config| 

config.vm.define "web" do |web|
  config.vm.box = 'centos/7'

  web.vm.host_name = 'web'
  web.vm.network "private_network", ip: "192.168.56.240"

  web.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
    vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
  end
  end
end

Vagrant.configure("2") do |config| 

  config.vm.define "log" do |log|
    config.vm.box = 'centos/7'
  
    log.vm.host_name = 'log'
    log.vm.network "private_network", ip: "192.168.56.241"
  
    log.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
      vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    end
    end
  end
  