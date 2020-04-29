# -*- mode: ruby -*-
# vi: set ft=ruby :

#VAGRANTFILE_API_VERSION = "2"

Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.vm.provider :vbox do |vbox|
  config.vm.box_version = "=1811.01"
  vbox.memory = 3072
  end

# Centos 1
  config.vm.define "linux1" do |linux1|
    linux1.vm.hostname = "linux1"
    linux1.vm.box = "centos/7"
  end

# Centos 2
  config.vm.define "linux2" do |linux2|
    linux2.vm.hostname = "linux2"
    linux2.vm.box = "centos/7"
  end

# Centos 3
  config.vm.define "linux3" do |linux3|
    linux3.vm.hostname = "linux3"
    linux3.vm.box = "centos/7"
  end

# Ansible Playbook to do the dirty job
   config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "KernelUpdatePlaybook.yml"
   end
end
