# -*- mode: ruby -*-


Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/jammy64"

  # ------------------------------------------------
  # VM 1: control (Ansible)
  # ------------------------------------------------
  config.vm.define "control" do |control|
    control.vm.hostname = "control"
    control.vm.network "private_network", ip: "192.168.56.20"
    control.vm.provider "virtualbox" do |vb|
      vb.name   = "control"
      vb.memory = "1024"
      vb.cpus = "1"
    end
  end

  # ------------------------------------------------
  # VM 2: webserver (nginx)
  # ------------------------------------------------
  config.vm.define "webserver" do |webserver|
    webserver.vm.hostname = "webserver"
    webserver.vm.network "private_network", ip: "192.168.56.21"
    webserver.vm.provider "virtualbox" do |vb|
      vb.name   = "webserver"
      vb.memory = "1024"
      vb.cpus = "1"
    end
  end

  # ------------------------------------------------
  # VM 3: database (PostgreSQL)
  # ------------------------------------------------
  config.vm.define "database" do |database|
    database.vm.hostname = "database"
    database.vm.network "private_network", ip: "192.168.56.22"
    database.vm.provider "virtualbox" do |vb|
      vb.name   = "database"
      vb.memory = "1024"
      vb.cpus = "1"
    end
  end

  # ------------------------------------------------
  # VM 4: client (testaren)
  # ------------------------------------------------
  config.vm.define "client" do |client|
    client.vm.hostname = "client"
    client.vm.network "private_network", ip: "192.168.56.23"
    client.vm.provider "virtualbox" do |vb|
      vb.name   = "client"
      vb.memory = "512"
      vb.cpus = "1"
    end
  end

end