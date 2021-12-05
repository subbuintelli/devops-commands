Vagrant.configure("2") do |config|
  config.vm.define "v", primary: true do |v|
    v.vm.box = "bento/ubuntu-18.04"
    v.vm.hostname = 'kubernetes'
    v.vm.network :private_network, ip: "192.168.56.101"    
	
	v.vm.provider :virtualbox do |v|
	  v.customize ["modifyvm", :id, "--name", "kubernetes"]
	  v.customize ["modifyvm", :id, "--memory", 2048]
	  v.customize ["modifyvm", :id, "--cpus", 2]
    end	 
 end
end