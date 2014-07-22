# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "pythonbox" do |pythonbox|
    pythonbox.vm.box = "ubuntu/trusty64"
    pythonbox.vm.network :private_network, ip: "10.1.14.100"

    pythonbox.vm.provision "ansible" do |ansible| 
      ansible.playbook = "pythonbox.yml"
      ansible.inventory_path = "inventories/vagrant"
      ansible.verbose = "vvv"
    end 

  end

end