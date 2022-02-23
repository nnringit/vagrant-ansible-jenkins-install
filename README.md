# Install Jenkins CI server using Vagrant and ansible on a remote/guest VM

This is to install Jenkins CI server on a ubuntu VM  which gets created using Vagrant and will be provsioned by ansible CM tool which is get installed and configured automatically by the ansible_local vagrant's provisioner

## Pre-Reqs
1. Install Vagrant
2. Install VirtualBox

Run the following single command which performs the following all by vagrant itself for you
1. downloads ubuntu 20.04 virtual box
2. Provision a Ubuntu VM and bootstraps with ansible install and its setup
3. Runs ansible-playbook  which uses local ansible role and installs Jenkins Server
4. Exposes Jenkins consoles default port 8080 to host machine

```sh
vagrant up --provision
```

## Testing
  Access this Jenkins console URL from a browser and follw the instructions on Jenkins pages to finish the Jenkins Server setup
        http://localhost:8080


## Folder structure 
.
├── README.md
├── Vagrantfile
└── ansible-provisioner
    ├── jenkins-playbook.yaml
    └── roles
        └── install-jenkins
            └── tasks
                └── main.yaml

