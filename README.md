# master_conf
master_conf
=========

This role should be applied after master-instance role. It will run all necessary commands for master configuration and master will be in READY state. 

Requirements
------------

Pre-requirements for this are your dynamic inventory should be ready and configuration file should be working. Also boto library need to be installed. You also need to add some scripts. The commands which need to written in the script and script name is located in /tasks/main.yml file.
/root/kubectl.txt should have line: sudo yum install -y kubelet kubeadm kubectl --disableexcludes=kubernetes
/root/kubeadm.txt should have line: kubeadm init --pod-network-cidr=10.244.0.0/16 --ignore-preflight-errors=NumCPU --ignore-preflight-errors=Mem

Role Variables
--------------

There are no role variables

Dependencies
------------

Other roles required are master_instance, slave_instance, slave_conf

Example Playbook
----------------

    - hosts: k8s_master_an
      roles:
         - master_conf
