# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "pythonbox" do |pythonbox|
    pythonbox.vm.box = "wheezy64"
    pythonbox.vm.box_url = "https://dl.dropboxusercontent.com/s/j887m9989t2g8zj/wheezy64.box"
    pythonbox.vm.network :private_network, ip: "10.1.14.100"

    pythonbox.vm.provision "ansible" do |ansible| 
      ansible.playbook = "pythonbox.yml"
      ansible.inventory_path = "inventories/vagrant"
    end 

  end

end