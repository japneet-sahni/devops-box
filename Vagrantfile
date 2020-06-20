Vagrant.configure(2) do |config|
	config.vm.define "devops-box" do |devbox|
		devbox.vm.box = "ubuntu/bionic64"
		devbox.vm.box_check_update = false
    		devbox.vm.network "private_network", ip: "192.168.5.50"
    		devbox.vm.hostname = "devops-box"
      		devbox.vm.provision "install-packages", type: "shell", :path => "scripts/install.sh"
      		devbox.vm.provision "setup-dns", type: "shell", :path => "scripts/update-dns.sh"
    		devbox.vm.provider "virtualbox" do |v|
    		  v.name = "devops-box"
    		  v.memory = 2048
    		  v.cpus = 2
    		end
	end
end
