Vagrant.require_version ">= 1.8.0"

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.provision :ansible do |ansible|
    ansible.playbook = "build.yml"
  end
end
