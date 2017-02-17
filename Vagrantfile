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

<<<<<<< HEAD
	  box1.vm.network :forwarded_port, guest: 22, host: 10135, id: "ssh"
=======
	  box1.vm.network :forwarded_port, guest: 22, host: 10122, id: "ssh"
>>>>>>> 86b785a895c74a4932a194eb165ec5014fef3c47
 
          box1.vm.network :private_network, ip: "192.168.56.101"

	  box1.vm.provider :virtualbox do |v|
	  
	  v.customize ["modifyvm", :id, "--memory", 1020]
	 end
 end
<<<<<<< HEAD
end
=======
  config.vm.define "box2" do |box2|

  box2.vm.provision "shell", inline: <<-SHELL
  		    sudo apt-get update
		    sudo apt-get install -y nginx
		    SHELL
	  box2.vm.box="hashicorp/precise64"

	  box2.vm.network :forwarded_port, guest: 22, host: 10123, id: "ssh"

	  box2.vm.network :private_network, ip: "192.168.56.102"
 end

  config.vm.define "ubuntu_server" do |ubuntu_server|

	  ubuntu_server.vm.provision "shell",path: "apache_script.sh"

	  ubuntu_server.vm.box="ubuntu/trusty64"
	  
	  ubuntu_server.vm.network :forwarded_port, guest: 22, host: 10225, id: "ssh"

	  ubuntu_server.vm.network :private_network, ip: "192.168.56.104"

	  ubuntu_server.vm.hostname='ubuntuserver'
	  #ubuntu_server.ssh.username+'root'

	  #ubuntu.server.ssh.password='htc'

	  #ubuntu.server.ssh.insert_keys='true'

  end

   config.vm.define "win7" do |win7|
	   win7.vm.box="designerror/windows-7"

	   win7.vm.network :forwarded_port, guest: 22, host: 10226, id: "ssh"
	   
	   win7.vm. network :private_network, ip: "192.168.56.105"
	  
	   win7.vm.hostname="win7"
	
  end

   config.vm.define"win10" do |win10|
	   win10.vm.box="senglin/win-10-enterprise-vs2015community"

	   win10.vm.network :forwarded_port, guest: 22, host: 10227, id: "ssh"

	   win10.vm.network :private_network, ip: "192.168.56.106"

	   win10.vm.hostname="win10"

  end
   config.vm.define"winsrv12" do |winsrv12|
	   winsrv12.vm.box="opentable/win-2012r2-standard-amd64-nocm"

	   winsrv12.vm.network :forwarded_port, guest: 22, host: 10228, id: "ssh"
	   winsrv12.vm.network :private_network, ip: "192.168.56.107"

	   winsrv12.vm.hostname="winsrv12"

  end

  # Disable automatic box update checking. If you disable this, then
  # boxes will only be checked for updates when the user runs
  # `vagrant box outdated`. This is not recommended.
  # config.vm.box_check_update = false

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # config.vm.network "forwarded_port", guest: 80, host: 8080

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  # config.vm.network "private_network", ip: "192.168.33.10"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # config.vm.network "public_network"

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # config.vm.synced_folder "../data", "/vagrant_data"

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
  # config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #   vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
  #   vb.memory = "1024"
  # end
  #
  # View the documentation for the provider you are using for more
  # information on available options.

  # Define a Vagrant Push strategy for pushing to Atlas. Other push strategies
  # such as FTP and Heroku are also available. See the documentation at
  # https://docs.vagrantup.com/v2/push/atlas.html for more information.
  # config.push.define "atlas" do |push|
  #   push.app = "YOUR_ATLAS_USERNAME/YOUR_APPLICATION_NAME"
  # end

  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y apache2
  # SHELL
end
>>>>>>> 86b785a895c74a4932a194eb165ec5014fef3c47
