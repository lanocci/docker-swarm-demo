Vagrant.configure(2) do |config|
  config.proxy.http     = "http://proxy.example.com"
  config.proxy.https    = "http://proxy.example.com"
  config.proxy.no_proxy = "localhost,127.0.0.1"
  config.vm.box = "ubuntu/trusty64"
  config.vm.provision :shell, :path => "bootstrap.sh"
  config.vm.define :slave1 do | n1 |
    n1.vm.hostname = "slave1"
    n1.vm.network :private_network, ip: "192.168.33.10"
  end
  config.vm.define :slave2 do | n2 |
    n2.vm.hostname = "slave2"
    n2.vm.network :private_network, ip: "192.168.33.20"
  end
  config.vm.define :pharaoh do | ph |
    ph.vm.hostname = "pharaoh"
    ph.vm.network :private_network, ip: "192.168.33.30"
  end
end
