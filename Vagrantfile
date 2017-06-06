# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  # Ubuntu 16.04
  config.vm.box = "ubuntu/xenial64"

  # Ubuntu 14.04
  # config.vm.box = "ubuntu/trusty64"

  # Debian jessie
  # config.vm.box = "debian/jessie64"

  config.vm.hostname = "otrs"
  config.vm.box_check_update = false

  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "private_network", ip: "192.168.150.150"

  config.vm.provider "virtualbox" do |vb|
   vb.memory = "1024"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "test.yml"
  end
end
