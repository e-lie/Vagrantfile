# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  # Default folder sharing
  config.vm.synced_folder ".", "/vagrant", id: "vagrant-root",
  owner: "root",
  group: "sudo",
  mount_options: ["dmode=775,fmode=774"]

  # Force guest type, because YunoHost /etc/issue can't be tuned
  config.vm.guest = :debian

  config.vm.define "__DOMAIN__" do |__VMNAME__|
    __VMNAME__.vm.box = "e-lie/yunohost-unstable"
    __VMNAME__.vm.network :private_network, ip: "192.168.33.82"
  end
end
