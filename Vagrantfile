# -*- mode: ruby -*-
# vi: set ft=ruby
#

Vagrant.configure('2') do |config|

  # Atomic Master
  config.vm.define 'master' do |master|
    master.vm.box = 'centos/atomic-host'
    master.vm.network :private_network, ip: "192.168.60.2"
  end

  # Atomic Node
  config.vm.define 'node01' do |node01|
    node01.vm.box = 'centos/atomic-host'
    node01.vm.network :private_network, ip: "192.168.60.3"
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
