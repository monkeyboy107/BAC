# -*- mode: ruby -*-
# vi: set ft=ruby :
workspace_dir = File.expand_path(File.dirname(__FILE__))
Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.synced_folder ".", "/vagrant", disabled: "True"
  config.vm.synced_folder workspace_dir, "/vagrant", type: "virtualbox"
  config.vm.provider "virtualbox" do |virtualbox|
    virtualbox.memory = "2048"
  end
  config.vm.provision "shell", inline: <<-SHELL
    yum install -y epel-release
  SHELL
end
