
Vagrant.configure("2") do |config|
  
  config.vm.box = "bento/ubuntu-22.04"

  config.ssh.insert_key = false

  config.vm.synced_folder ".", "/vagrant", disabled: false

  config.vm.provider :virtualbox do |v|
    v.memory = 512
    v.linked_clone = true
  end

  # Worstation
  config.vm.define "ws" do |ws|
    ws.vm.hostname = "ws"
    ws.vm.network :private_network, ip: "192.168.60.10"
  end


  # minikube
  config.vm.define "node" do |node|
    node.vm.hostname = "node"
    node.vm.network :private_network, ip: "192.168.60.11"
   
    node.vm.provider "virtualbox" do |nodev|
	nodev.memory = 4096
    end
  end

 

end
