# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu14-cloudimage"
  config.vm.box_url = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"
  
  config.vm.define "webserverMachine" do |webserver|
# webserver.vm.provision "shell", path: "vagrant_provision.sh"
# A standard Ubuntu 16.04 LTS 62-bit box
  webserver.vm.box = "ubuntu/trusty64"
# Create a private network, which allows host-only access to the machine
# using a specific IP.
  webserver.vm.network "private_network", ip: "192.168.6.8"
  webserver.vm.network "forwarded_port", guest: 3386, host: 3389
  webserver.vm.hostname = "webserverHost"  
end 
end