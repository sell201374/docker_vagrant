# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.provision "docker" do |d|
    d.run "sell201374/nodejs",
		args: "-p 8080:8080"
  end
  config.vm.network :forwarded_port, guest: 8080, host: 4567
end
