Vagrant.configure("2") do |config|

  config.vm.define "web01" do |web01|
    web01.vm.box = "ubuntu/focal64"
    web01.vm.hostname = "web01"
    web01.vm.network "private_network", ip: "192.168.56.51"
    web01.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
    end
    web01.vm.provision "shell", inline: <<-SHELL
      sudo apt update
      sudo apt install -y apache2
      sudo systemctl enable apache2
      sudo systemctl start apache2
    SHELL
  end

  config.vm.define "web02" do |web02|
    web02.vm.box = "ubuntu/focal64"
    web02.vm.hostname = "web02"
    web02.vm.network "private_network", ip: "192.168.56.52"
    web02.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
    end
    web02.vm.provision "shell", inline: <<-SHELL
      sudo apt update
      sudo apt install -y apache2
      sudo systemctl enable apache2
      sudo systemctl start apache2
    SHELL
  end

  config.vm.define "db01" do |db01|
    db01.vm.box = "centos/7"
    db01.vm.hostname = "db01"
    db01.vm.network "private_network", ip: "192.168.56.53"
    db01.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
    end
    db01.vm.provision "shell", inline: <<-SHELL
      sudo yum update -y
      sudo yum install -y mariadb-server
      sudo systemctl enable mariadb
      sudo systemctl start mariadb

    SHELL
  end

end
