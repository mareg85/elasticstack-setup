Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.hostname = "monitoring"
#  config.vm.network "private_network", ip: "10.0.0.10", name: "vboxnet1"
#  config.ssh.insert_key = false
#  config.ssh.private_key_path = ["~/.ssh/id_rsa", "~/.vagrant.d/insecure_private_key"]
#  config.vm.provision "file", source: "~/.ssh/id_rsa.pub", destination: "~/.ssh/authorized_keys"
#  config.ssh.username = "vagrant"
#  config.ssh.password = "vagrant"

  config.vm.define "elasticsearch" do |el|
    el.vm.network "private_network", ip: "10.0.0.11", name: "vboxnet1"
    el.vm.provider "virtualbox" do |vb|
      vb.name = "elasticsearch-01"
      vb.memory = 2048
      vb.cpus = 1
    end
  end

  config.vm.define "kibana" do |kb|
    kb.vm.network "private_network", ip: "10.0.0.12", name: "vboxnet1"
    kb.vm.provider "virtualbox" do |vb|
      vb.name = "kibana-01"
      vb.memory = 1024
      vb.cpus = 1
    end 
  end
end
