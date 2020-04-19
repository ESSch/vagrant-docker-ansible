# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
  config.vm.box_check_update = false
  # config.ssh.insert_key = false
  config.vm.define 'ansible' do |machine|
    machine.vm.hostname = "ansible"
    machine.vm.box = "ubuntu/bionic64"
    # machine.vm.provision "ansible" do |ansible|
    #     ansible.verbose = "v"
    #     ansible.playbook = "pb_test.yml"
    # end
    machine.vm.provision "shell", inline: <<-SHELL
sudo apt-get update -qq;
sudo apt install ansible -y -qq;
sudo ansible-playbook /vagrant/pb_test.yml
SHELL
  end
end
