## vagrant-ubuntu-kvm-kubernetes

This is designed to operate in conjunction with [kube-spawn](https://github.com/kinvolk/kube-spawn).
Build it and copy kube-spawn into this directory.

### Pre-requisites

Install base packages:

```
apt install libvirt qemu-kvm vagrant-mutate libvirt-daemon libvirt-clients  libvirt-dev ruby-dev qemu-img
wget -O /tmp/vagrant.deb https://releases.hashicorp.com/vagrant/2.1.2/vagrant_2.1.2_x86_64.deb
dpkg -i /tmp/vagrant.deb
```

The upgrade of [vagrant](https://releases.hashicorp.com/vagrant/2.1.2/vagrant_2.1.2_x86_64.deb) from [hashicorp](https://www.vagrantup.com/downloads.html) is required vs e.g. the one in the Ubuntu repo.


Install vagrant-libvirt:

```
vagrant plugin install vagrant-libvirt
```

Optional: Install vagrant-mutate

```
vagrant plugin install vagrant-mutate
```

Add a 'box':

```
vagrant box add generic/ubuntu1804 --provider=libvirt
```

### Usage

Create:

```
vagrant up
```
