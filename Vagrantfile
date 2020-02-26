
Vagrant.configure("2") do |config|
	  config.vm.box = "generic/arch"
	# config.vm.box = "archlinux/archlinux"
	  config.vm.synced_folder "code", "/mnt/vagrant"

  config.vm.define "servervictim" do |servervictim|
	  servervictim.vm.box = "ubuntu/trusty64"
	  servervictim.vm.network "private_network", ip: "10.0.0.10", netmask: "255.0.0.0"
	  servervictim.vm.hostname = "servervictim"
	  # servervictim.vm.provision :shell, path: "init_server_victim.sh"
  end
 
  config.vm.define "iotvictim" do |iotvictim|
	  iotvictim.vm.box = "RIOT/ubuntu1604"
   	  iotvictim.vm.network "private_network", ip: "10.0.0.20", netmask: "255.0.0.0"
          iotvictim.vm.hostname = "iotvictim"
          # iotvictim.vm.provision :shell, path: "init_iot_victim.sh"
  end

  config.vm.define "scan" do |scan|
    	  scan.vm.network "private_network", ip: "10.0.0.30", netmask: "255.0.0.0"
    	  scan.vm.hostname = "scan"
          # scan.vm.provision :shell, path: "init_scan.sh"
  end

  config.vm.define "botmirai" do |botmirai|
    	  botmirai.vm.network "private_network", ip: "10.0.0.40", netmask: "255.0.0.0"
    	  botmirai.vm.hostname = "botmirai"
          # botmirai.vm.provision :shell, path: "init_bot_mirai.sh"
  end

  config.vm.define "victim" do |victim|
    	  victim.vm.network "private_network", ip: "10.0.0.50", netmask: "255.0.0.0"
    	  victim.vm.hostname = "victim"
     	  # victim.vm.provision :shell, path: "init_victim.sh"
  end
end
