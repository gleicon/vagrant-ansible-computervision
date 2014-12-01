# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "cv" do |cv|
    cv.vm.box = "ubuntu/trusty64"
    cv.vm.network :private_network, ip: "192.168.33.21"

    cv.vm.provision "ansible" do |ansible| 
      ansible.playbook = "cv.yml"
    end 
  end

  config.vm.provider "virtualbox" do |v|
    v.customize ["modifyvm", :id, "--memory", "1024"]
  end

end
