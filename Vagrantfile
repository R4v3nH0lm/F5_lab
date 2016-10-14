Vagrant.configure("2") do |config|
  
  config.vm.define "leaf1" do |leaf1|
    leaf1.vm.box = "cumulus-linux-3.1.1"
    leaf1.vm.provider :virtualbox do |vb|
      vb.name = "leaf1"
      vb.customize ["modifyvm", :id, "--memory", "512"]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", "50"]
    end
    leaf1.vm.hostname = "leaf1"
    leaf1.vm.network "private_network", virtualbox__intnet: "swp1"
    leaf1.vm.network "private_network", virtualbox__intnet: "swp2"
    #leaf1.vm.network "private_network", virtualbox__intnet: "swp3"
    #leaf1.vm.network "private_network", virtualbox__intnet: "swp4"
  end

  config.vm.define "leaf2" do |leaf2|
    leaf2.vm.box = "cumulus-linux-3.1.1"
    leaf2.vm.provider :virtualbox do |vb|
      vb.name = "leaf2"
      vb.customize ["modifyvm", :id, "--memory", "512"]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", "50"]
    end
    leaf2.vm.hostname = "leaf2"
    leaf2.vm.network "private_network", virtualbox__intnet: "swp1"
    #leaf2.vm.network "private_network", virtualbox__intnet: "swp2"
    leaf2.vm.network "private_network", virtualbox__intnet: "swp3"
    #leaf2.vm.network "private_network", virtualbox__intnet: "swp4"
  end

  config.vm.define "web1" do |web1|
    web1.vm.box = "centos/7"
    web1.vm.provider :virtualbox do |vb|
      vb.name = "web1"
      vb.customize ["modifyvm", :id, "--memory", "512"]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", "50"]
    end
    web1.vm.hostname = "web1"
    #web1.vm.network "private_network", virtualbox__intnet: "swp1"
    web1.vm.network "private_network", virtualbox__intnet: "swp2", ip: "10.0.0.2"
    #web1.vm.network "private_network", virtualbox__intnet: "swp3"
    #web1.vm.network "private_network", virtualbox__intnet: "swp4"
    web1.vm.provision "shell", path: "nginx_install.sh"
  end

  config.vm.define "web2" do |web2|
    web2.vm.box = "centos/7"
    web2.vm.provider :virtualbox do |vb|
      vb.name = "web2"
      vb.customize ["modifyvm", :id, "--memory", "512"]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", "50"]
    end
    web2.vm.hostname = "web2"
    #web2.vm.network "private_network", virtualbox__intnet: "swp1"
    #web2.vm.network "private_network", virtualbox__intnet: "swp2"
    web2.vm.network "private_network", virtualbox__intnet: "swp3", ip: "10.0.0.3"
    #web2.vm.network "private_network", virtualbox__intnet: "swp4"
    web2.vm.provision "shell", path: "nginx_install.sh"
  end

end
