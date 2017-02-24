# -*- mode: ruby -*-
# vi: set ft=ruby :


##############
require 'yaml'

settings = YAML.load_file(".settings.yml")
puts "Setting bridge interface #{settings['interface']}"
Vagrant.configure(2) do |config|
config.vm.box = "ubuntu/trusty64"
config.vm.provider "virtualbox" do |vb|
	vb.memory = "512"
	vb.cpus = "1"
#config.vm.network "forwarded_port", guest: 3000, host: 3001, auto_correct: true
end
   config.vm.network "public_network", bridge: settings['interface']
   config.vm.provision :ansible do |ansible|
        ansible.playbook = "playbook.yml"
   end
end
