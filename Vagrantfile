Vagrant.configure(2) do |config|
  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
    v.cpus = 2
  end

  config.vm.define "ubuntu1604" do |xenial|
    xenial.vm.box = "ubuntu/xenial64"
    xenial.vm.provision "shell", inline: <<-SHELL
      sudo su -
      cd /vagrant
      ./run_tests.sh
    SHELL
  end
end
