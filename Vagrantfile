# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "debian4"
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.provider "virtualbox" do |vb|
    vb.name = "Debian_Etch_40r9"
    vb.gui = true
    vb.memory = "512"
  end
  config.ssh.username = "root"
  config.ssh.password = "t00r"
  config.ssh.insert_key = false
end
