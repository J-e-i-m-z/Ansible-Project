# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # Configure the control node (Ansible controller)
  config.vm.define "control" do |control|
    control.vm.box = "ubuntu/focal64"
    control.vm.hostname = "control-node"
    control.vm.network "private_network", ip: "192.168.56.10"
    control.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
      vb.cpus = 1
      vb.name = "ansible-control"
    end
  end

  # Configure web server 1
  config.vm.define "web1" do |web1|
    web1.vm.box = "ubuntu/focal64"
    web1.vm.hostname = "web-server-1"
    web1.vm.network "private_network", ip: "192.168.56.11"
    web1.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
      vb.cpus = 1
      vb.name = "web-server-1"
    end
  end

  # Configure web server 2
  config.vm.define "web2" do |web2|
    web2.vm.box = "ubuntu/focal64"
    web2.vm.hostname = "web-server-2"
    web2.vm.network "private_network", ip: "192.168.56.12"
    web2.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
      vb.cpus = 1
      vb.name = "web-server-2"
    end
  end

  # Configure database server with Docker
  config.vm.define "db" do |db|
    db.vm.box = "ubuntu/focal64"
    db.vm.hostname = "db-server"
    db.vm.network "private_network", ip: "192.168.56.13"
    db.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = 2
      vb.name = "db-server"
    end
  end
end
