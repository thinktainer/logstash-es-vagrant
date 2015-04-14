# vi: ft=ruby:

Vagrant.configure(2) do |config|

  config.vm.box = "opscode/debian-7.8"

  config.vm.provider :vmware_fusion do |vmware|
    vmware.gui = false
    vmware.vmx["numvcpus"] = "2"
    vmware.vmx["memsize"] = "2048"
  end

  config.ssh.forward_agent = true
  config.vm.network "private_network", ip: "10.155.15.100"
  config.vm.provision :hosts

  config.vm.synced_folder "#{ENV['HOME']}/salt/roots", "/srv/salt"
  config.vm.synced_folder "#{ENV['HOME']}/salt/pillar", "/srv/pillar"


  config.vm.provision :salt do |salt|
    salt.minion_config = "salt/minion"
    salt.log_level = "info"
    salt.run_highstate = true
  end

end
