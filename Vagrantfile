# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "bento/ubuntu-16.04"
  config.vm.network "forwarded_port", guest: 80, host: 8080

  config.ssh.insert_key = false

  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
    sudo apt-get install -y ansible
  SHELL

  # config.vm.provision :guest_ansible  do |ansible|
  #   ansible.playbook = "playbook.yml"
  # end
end
