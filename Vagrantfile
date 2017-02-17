# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
#
Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://atlas.hashicorp.com/search.
	
  config.vm.provision "shell",path: "backup_script.sh"


  config.vm.define "box1" do |box1|

  #config.vm.provision "shell", inline: <<-SHELL
  	    #sudo apt-get update
	    #SHELL
  box1.vm.provision "shell", inline: <<-SHELL
  	    	     sudo apt-get update
		     SHELL
	  box1.vm.box="ubuntu/trusty64"

	  box1.vm.network :forwarded_port, guest: 22, host: 10135, id: "ssh"
 
          box1.vm.network :private_network, ip: "192.168.56.101"

	  box1.vm.provider :virtualbox do |v|
	  
	  v.customize ["modifyvm", :id, "--memory", 1020]
	 end
 end
end