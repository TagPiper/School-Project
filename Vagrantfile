Vagrant.configure("2") do |config|
	config.vm.provision "shell", inline: <<-SHELL
		sudo apt-get update
		sudo apt-get install -y apache2
		SHELL
	config.vm.define "apacheServer" do |apacheServer|
	apacheServer.vm.box="ubuntu/trusty64"
	apacheServer.vm.network :forwarded_port, guest: 22, host: 10122, id: "ssh"
	apacheServer.vm.network :private_network, ip: "192.168.1.199"
	apacheServer.vm.provider :virtualbox do |v|
		v.name = "apacheServer"
	v.customize ["modifyvm", :id, "--memory", 2048]
	end
	end
end
