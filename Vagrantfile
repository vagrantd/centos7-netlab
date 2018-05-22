# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.ssh.insert_key = false

  config.vm.provider "virtualbox" do |v|
    v.name = "build_centos7_netlab"
  end

  config.vm.provision "shell", inline: <<-SHELL
    sysctl -w net.ipv4.ip_forward=1
    yum install -y curl bind-utils net-tools traceroute wget
  SHELL
end
