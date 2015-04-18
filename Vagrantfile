# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "chef/fedora-21"

  config.vm.provider :virtualbox do |vb|
    vb.memory = 2048
    vb.cpus = 2
  end
  config.vbguest.auto_update = true

  # View the documentation for the provider you're using for more
  # information on available options.
  config.vm.provision :ansible do |ansible|
    ansible.limit = "all"
    ansible.playbook = "site.yml"
  end
end
