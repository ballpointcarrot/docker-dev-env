# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.define "bpc_base" do |v|
    v.vm.provider "docker" do |d|
      d.build_dir = "ballpointcarrot_base"
      d.build_args = ["-t=bpc_base"]
    end
  end

  config.vm.define "ballpointcarrot" do |v|
    v.vm.provider "docker" do |d|
      d.cmd = ["/sbin/my_init", "--enable-insecure-key"]
      d.image = "bpc_base"
      d.has_ssh = true
    end
    
    v.ssh.username = "root"
    v.ssh.private_key_path = "bpc"
    v.ssh.forward_agent = true

    v.vm.provision "shell", inline: "echo hello", privileged: false
  end
end
