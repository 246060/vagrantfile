# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

  config.vm.box = "centos/7"

  config.vm.define "ansible" do |node|
    
		node.vm.hostname = "ansible"
		node.vm.network "private_network", ip: "192.168.56.10" #, auto_config: false
		
		node.vm.provider "virtualbox" do |vb|
		  vb.name = "ansible"
		  vb.gui = false
		  vb.memory = "512"
		end
	  
		node.vm.provision "shell", inline: <<-SHELL
			yum install -y epel-release
			yum install -y ansible vim
		SHELL
	
  end


  config.vm.define "t1" do |node|
    
		node.vm.hostname = "t1"
		node.vm.network "private_network", ip: "192.168.56.11" #, auto_config: false
		
		node.vm.provider "virtualbox" do |vb|
		  vb.name = "t1"
		  vb.gui = false
		  vb.memory = "512"
		end
		
		node.vm.provision "shell", inline: <<-SHELL
			yum install -y vim
		SHELL
		
  end
  
    config.vm.define "t2" do |node|
    
		node.vm.hostname = "t2"
		node.vm.network "private_network", ip: "192.168.56.12" #, auto_config: false
		
		node.vm.provider "virtualbox" do |vb|
		  vb.name = "t2"
		  vb.gui = false
		  vb.memory = "512"
		end
		
		node.vm.provision "shell", inline: <<-SHELL
			yum install -y vim
		SHELL
		
  end

end
