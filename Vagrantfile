Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
    config.vm.hostname = "xenial"
    config.vm.network :private_network, ip: "192.168.33.78" 
    config.vm.synced_folder("./", "/var/www/html", :nfs => true)
    config.vm.provider "virtualbox" do |machine|
      machine.memory = 2024
      machine.cpus = 2
      machine.name = "xenial"
    end
    config.vm.provision :shell, path: "setup.sh"
end
