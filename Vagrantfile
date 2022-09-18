

Vagrant.configure("2") do |config|
  config.vm.define "amaster" do |amaster|
    amaster.vm.box_download_insecure = true
    amaster.vm.box = "hashicorp/bionic64"
    amaster.vm.network "private_network", ip: "192.168.56.121"
    amaster.vm.hostname = "amaster"
    amaster.vm.provider "virtualbox" do |v|
      v.name = "amaster"
      v.memory = 2048
      v.cpus = 2
    end
  end

  config.vm.define "kmaster" do |kmaster|
    kmaster.vm.box_download_insecure = true
    kmaster.vm.box = "hashicorp/bionic64"
    kmaster.vm.network "private_network", ip: "192.168.56.122"
    kmaster.vm.hostname = "kmaster"
    kmaster.vm.provider "virtualbox" do |v|
      v.name = "kmaster"
      v.memory = 2048
      v.cpus = 2
    end
  end

  config.vm.define "kworker-1" do |kworker|
    kworker.vm.box_download_insecure = true
    kworker.vm.box = "hashicorp/bionic64"
    kworker.vm.network "private_network", ip: "192.168.56.123"
    kworker.vm.hostname = "kworker"
    kworker.vm.provider "virtualbox" do |v|
      v.name = "kworker-1"
      v.memory = 2048
      v.cpus = 2
    end
  end

  config.vm.define "kworker-2" do |kworker|
    kworker.vm.box_download_insecure = true
    kworker.vm.box = "hashicorp/bionic64"
    kworker.vm.network "private_network", ip: "192.168.56.124"
    kworker.vm.hostname = "kworker"
    kworker.vm.provider "virtualbox" do |v|
      v.name = "kworker-2"
      v.memory = 2048
      v.cpus = 2
    end
  end

end
# sudo pip3 install -r contrib/inventory_builder/requirements.txt
# cp -rfp inventory/sample inventory/kubecluster
# declare -a IPS=(192.168.56.122 192.168.56.123 192.168.56.124)
# CONFIG_FILE=inventory/kubecluster/hosts.yml python3 contrib/inventory_builder/inventory.py ${IPS[@]}
