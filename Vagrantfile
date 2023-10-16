Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-20.04"
  config.vm.hostname = "IMS"
#  config.vm.provision :shell, path: "vm_init.sh"
  config.vm.network "public_network", ip: "192.168.0.155"
  config.vm.network "public_network", ip: "192.168.200.202"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = 4000
    vb.cpus = 4
  end
end
