
Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |v|
    v.memory = 4096
    v.cpus = 2
  end
  config.vm.box = "generic/fedora28"
  # config.vm.synced_folder "src/", "/home/vagrant/src"
  config.vm.network "private_network", ip: "192.168.56.2"
  # config.vm.network :forwarded_port, guest: 3000, host: 3000
  # config.vm.network :forwarded_port, guest: 3010, host: 3010
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "src/playbook.yml"
  end
end
