Vagrant.configure("2") do |config|
 
  config.vm.provider :virtualbox do |v|
    v.memory = 2048
    v.cpus = 2
  end

  config.vm.define "webserver" do |web|
    web.vm.box = "debian/stretch64"
    web.vm.box_version = "9.9.0"
    web.vm.hostname = "webserver"
    web.vm.network :private_network, ip: "10.10.10.10"
    web.vm.provision "ansible" do |ansible|
    ansible.playbook = "site.yml"
  end
 
 end
  
end
