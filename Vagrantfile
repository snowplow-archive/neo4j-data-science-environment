Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/trusty64"
  config.vm.hostname = "neo4j"
  config.ssh.forward_agent = true

  # Forward guest port 7474 to host port 7474 (for Neo4J)
  config.vm.network "forwarded_port", guest: 7474, host: 7474

  config.vm.provision "file", source: "~/.ssh/config", destination: "~/.ssh/config"

  config.vm.provider :virtualbox do |vb|
    vb.name = Dir.pwd().split("/")[-1] + "-" + Time.now.to_f.to_i.to_s
    vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    vb.customize [ "guestproperty", "set", :id, "--timesync-threshold", 10000 ]
    vb.memory = 5120
  end

  config.vm.provision :shell do |sh|
    sh.path = "vagrant/up.bash"
  end
