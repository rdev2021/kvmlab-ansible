# KVM Labs using Ansible

Create VM with libvirtd using anisble playbook. Using the vm to setup k3s to trail out few kubernetes features.

Inspired from: https://www.redhat.com/sysadmin/build-VM-fast-ansible


# Setup

As of commiting the code the Fedora version is 38 and Ansible core is 2.14.7.

# Run playbook

### Setup: 
ansible-playbook -K vm_provision.yaml --extra-vars "ssh_pub_key=path to pub key base_image_storage_path=path to store isos"

### Teardown: 
ansible-playbook -K reset.yaml

### Dependency
<ul>
<li>ansible-galaxy collection install community.libvirt</li>
</ul>