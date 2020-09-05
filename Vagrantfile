# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "db_server" do |node|
    node.vm.box = "bento/centos-7"
    node.vm.box_version = "202008.16.0"
    node.vm.network "private_network", ip:"192.168.33.11"
    node.vm.synced_folder ".", "/vagrant"
  end

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "playbook.yml"
  end

  config.vm.provider "virtualbox" do |v|
    v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    v.gui = true
  end

end