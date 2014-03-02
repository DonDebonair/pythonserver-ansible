# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "pythonbox" do |pythonbox|
    pythonbox.vm.box = "precise32"
    pythonbox.vm.box_url = "http://files.vagrantup.com/precise32.box"
    pythonbox.vm.network :private_network, ip: "192.168.33.10"

    pythonbox.vm.provision "ansible" do |ansible| 
      ansible.playbook = "pythonbox.yml"
    end 

  end

end