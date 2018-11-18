# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"

  # WEBrickのポートをマッピング
  config.vm.network :forwarded_port, host: 3000, guest: 3000

  # Ansibleによるプロビジョニング
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "site.yml"
    ansible.ask_vault_pass = true
  end
end
