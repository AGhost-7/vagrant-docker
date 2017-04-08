# vi: set ft=ruby:

Vagrant.configure(2) do |config|
	config.vm.box = 'ubuntu/trusty64'
	config.ssh.insert_key = false
	config.vm.provision :shell, privileged: false, inline: <<-SCRIPT
	sudo apt-get update
	sudo apt-get install build-essential -y
	sudo apt-get install python-dev python-pip -y

	sudo apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D
	echo 'deb https://apt.dockerproject.org/repo ubuntu-trusty main' | sudo tee /etc/apt/sources.list.d/docker.list
	sudo apt-get update
	sudo apt-get install docker-engine -y
	sudo pip install docker-compose
	# installer already adds the docker group, just need to add current user to group
	sudo usermod -aG docker $USER
	sudo service docker restart
	SCRIPT
end

