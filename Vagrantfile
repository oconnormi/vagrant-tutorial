# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = '2'

Vagrant.require_version '>= 1.5.0'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|


  config.vm.synced_folder "~/workspace", "/home/vagrant/workspace"    # Share a folder with the vm

  config.ssh.forward_x11 = true   # Configure X11 Forwarding

  config.vm.hostname =  'tutorial.vagrant.dev'      # Set the vm's hostname

  config.vm.box = 'chef/ubuntu-14.04'     # Base vm image to use

  config.vm.network :private_network, type: "dhcp"    # Network definition
  
  config.vm.provision :shell, path: "hello_world.sh"  # Execute a script
end
