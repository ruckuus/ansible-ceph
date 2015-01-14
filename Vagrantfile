# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "hashicorp/precise64"

  config.vm.define "ceph_admin" do |ans|
    ans.vm.hostname = "ceph-admin.foo"
    ans.vm.network "private_network", ip: "192.168.1.2"
    ans.vm.provision "ansible" do |ansible|
      ansible.playbook = "ceph-admin-node.yml"
    end
  end

   config.vm.define "ceph_cluster01" do |ans|
    ans.vm.hostname = "ceph-node-01.foo"
    ans.vm.network "private_network", ip: "192.168.1.100"
    ans.vm.provision "ansible" do |ansible|
      ansible.playbook = "ceph-cluster-node.yml"
    end
  end

   config.vm.define "ceph_cluster02" do |ans|
    ans.vm.hostname = "ceph-node-02.foo"
    ans.vm.network "private_network", ip: "192.168.1.101"
    ans.vm.provision "ansible" do |ansible|
      ansible.playbook = "ceph-cluster-node.yml"
    end
  end

   config.vm.define "ceph_cluster03" do |ans|
    ans.vm.hostname = "ceph-node-03.foo"
    ans.vm.network "private_network", ip: "192.168.1.102"
    ans.vm.provision "ansible" do |ansible|
      ansible.playbook = "ceph-cluster-node.yml"
    end
  end

  config.vm.define "ceph_mon01" do |ans|
    ans.vm.hostname = "ceph-node-04.foo"
    ans.vm.network "private_network", ip: "192.168.1.103"
    ans.vm.provision "ansible" do |ansible|
      ansible.playbook = "ceph-cluster-node.yml"
    end
  end
end
