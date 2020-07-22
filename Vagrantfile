# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos/8"
  config.vm.hostname = "centos8.local"
  config.vm.network :private_network, ip: "192.168.56.19"
  config.vm.provider :virtualbox do |vb|
    vb.name = "centos8"
    vb.customize ["modifyvm", :id, "--memory", "768"]
  end

  config.ssh.insert_key = false

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/ansible.yml"
    ansible.inventory_path = "provisioning/hosts"
    ansible.limit = 'all'
  end
end
