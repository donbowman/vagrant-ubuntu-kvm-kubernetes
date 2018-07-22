Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu1804"
  config.vm.provider :libvirt do |domain|
    domain.cpu_mode = 'host-passthrough'
  end
  config.vm.provision "file",source: "kube-spawn", destination: "kube-spawn"
  config.vm.provision "file",source: "/opt/cni/", destination: "./opt/"
  config.vm.provision "shell", path: "setup"
end
