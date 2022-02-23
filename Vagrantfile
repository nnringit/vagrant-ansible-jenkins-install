
Vagrant.configure("2") do |config|

  config.vm.box = "bento/ubuntu-20.04"

  config.vm.synced_folder ".", "/vagrant", disabled: false, type: 'rsync'

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "ansible-provisioner/jenkins-playbook.yaml"
    ansible.verbose = true
  end

  config.vm.network "forwarded_port", guest: 8080, host: 8080

end

