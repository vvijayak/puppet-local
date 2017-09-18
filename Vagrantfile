Vagrant.configure("2") do |config|
	
	#defualt virtualbox configuration
	config.vm.provider "virtualbox" do |v|
		v.memory = 2048
		v.cpus = 2
	end

	#puppet master config
	config.vm.define "puppetmaster" do |pm|
		pm.vm.box = "centos/7"
		pm.vm.network "private_network", ip: "192.168.33.10"
		pm.vm.hostname = "puppetmaster"
	end

	#puppet agent 
	config.vm.define "puppet-agent-centos" do |pac|
		pac.vm.box = "centos/7"
		pac.vm.network "private_network", ip: "192.168.33.11"
		pac.vm.hostname = "centos-agent"
	end

	#puppet agent 
	config.vm.define "puppet-agent-ubuntu" do |u|
		u.vm.box = "ubuntu/xenial64"
		u.vm.network "private_network", ip: "192.168.33.11"
		u.vm.hostname = "ubuntu-agent"
	end
end
