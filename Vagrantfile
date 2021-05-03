# -*- mode: ruby -*-
# vi: set ft=ruby :

# VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(2) do |config|
    config.vm.define "server1" do |s|
        s.vm.box = "debian/testing64"
        # s.vm.box_url = "http://files.saas.hand-china.com/vagrant/bento_centos-7.8.box"
        s.vm.hostname = "server1"
        # s.vm.network "private_network", ip: "192.168.56.11"
        # s.vm.network "forwarded_port", guest: 6443, host: 6443
        # s.vm.network "forwarded_port", guest: 8443, host: 8443
        s.vm.synced_folder ".", "/vagrant", disabled: true
        # s.vm.provision "shell", inline: $centos_script
        s.vm.provider "Libvirt" do |l|
            l.memory = 4096
            l.cpus = 2
        end
    end

  # Ansible provisioner.
  # config.vm.provision :ansible do |ansible|
  #   ansible.playbook = "init-loan.yml"
  # end
end