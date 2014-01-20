# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure("2") do |config|

  # Configure base box parameters
  config.vm.box = "WinTest"
  # config.vm.box_url = "./vagrant-windows7x64box"
  config.vm.guest = :windows
 
  config.vm.provider :virtualbox do |vb|
     vb.gui = true
  end

  config.windows.set_work_network = "1"
  config.winrm.host = "localhost"
  # Port forward WinRM and RDP
  config.vm.network :forwarded_port, guest: 3389, host: 3389
  config.vm.network :forwarded_port, guest: 5985, host: 5985, id: "winrm", auto_correct: true

end
