# -*- mode: ruby -*-
# vi: set ft=ruby
#

MASTER_IP="192.168.60.2"
NODE01_IP="192.168.60.3"

Vagrant.configure('2') do |config|

  # Atomic Master
  config.vm.define 'master' do |master|
    master.vm.box = 'centos/atomic-host'
    master.vm.network "private_network", ip: "#{MASTER_IP}"
  end

  # Atomic Node
  config.vm.define 'node01' do |node01|
    node01.vm.box = 'centos/atomic-host'
    node01.vm.network "private_network", ip: "#{NODE01_IP}"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "site.yml"
    ansible.sudo = true
    ansible.groups = {
      "master" => ["master"],
      "node" => ["node01"]
    }
  end

end
