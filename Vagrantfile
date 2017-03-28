# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure(2) do |config|
#Vagrant.require_version ">= 1.7.0"
  config.vm.define "Jenkins" do |jenkins|
    jenkins.vm.box = "ubuntu/trusty64"
    jenkins.vm.network "private_network", ip: "192.168.0.2"
    jenkins.vm.hostname = "jenkins"
    jenkins.vm.provider "virtualbox" do |v|
      v.memory = 4096
      v.cpus = 2
  config.vm.provision :ansible do |ansible|
    ansible.playbook = "jenkins.yml"
    end
    end
  end
  config.vm.define "ansible" do |ansible|
    ansible.vm.box = "ubuntu/trusty64"
    ansible.vm.network "private_network", ip: "192.168.0.254"
    ansible.vm.hostname = "ansible"
  config.vm.provision :ansible do |ansible|
    ansible.playbook = "ansible.yml"
  end
  end
end
