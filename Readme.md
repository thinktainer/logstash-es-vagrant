# Vagrant logstashAs a result of `vagrant up` one can expect redis listening on port 6379,elasticsearch on port 9200 and kibana on port 5601. Redis is configured to readdata from redis and push it into elasticsearch.## Requirements:### Salt:Clone [my salt repo](https://github.com/thinktainer/salt) to your $HOME/salt### Virtualbox:		vagrant box add opscode/debian-7.8 \		http://opscode-vm-bento.s3.amazonaws.com/vagrant/virtualbox/opscode_debian-7.8_chef-provisionerless.box \		--provider=virtualbox### VMWare:		vagrant box add opscode/debian-7.8 \		http://opscode-vm-bento.s3.amazonaws.com/vagrant/vmware/opscode_debian-7.8_chef-provisionerless.box \		--provider=vmware_desktop