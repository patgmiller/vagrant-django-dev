# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.require_version ">= 1.7.0"

Vagrant.configure('2') do |config|

    config.vm.provider :virtualbox do |box|
        box.name = "django dev"
      
        # use more than one core for speed.
        box.customize ["modifyvm", :id, "--ioapic", "on"]
        # memory you want the vm to use
        box.customize ["modifyvm", :id, "--memory", "2048"]
        # the # of virtual cores the vagrant machine gets
        box.customize ["modifyvm", :id, "--cpus", "2"] 
    
        box.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
        box.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
        
    end
    
    config.vm.define :dev do |dev|
        dev.vm.box = 'ubuntu/trusty64'
        dev.vm.network :private_network, ip: '192.168.88.22'
        dev.vm.hostname = 'vagrantbox'
    
        dev.vm.provision :ansible, run: 'always' do |ansible|
            ansible.playbook = 'ansible/main.yml'
            ansible.sudo = true
            ansible.host_key_checking = false
        end
            
        dev.vm.synced_folder ".", "/vagrant", type: "nfs", mount_options: ['nolock,vers=3,udp,noatime,actimeo=1']
    end
end