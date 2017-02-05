# Packer Template and Vagrantfile for Debian Etch
Packer Template and Vagrantfile to spin up a vanilla Debian Etch box from the network install ISO.

## Usages
You will need [Packer](https://www.packer.io/docs/installation.html) and [Vagrant](https://www.vagrantup.com/docs/installation/) in your path.

Debian Etch 4.0_r9 network install ISO: [Download](http://cdimage.debian.org/mirror/cdimage/archive/4.0_r9/i386/iso-cd/debian-40r9-i386-netinst.iso)

SHA256SUM `f451c3adf52feb2618cd458fdd758bf29330788f3eb721aaf9f5cba8c20b1d61`

(Notes: The iso file and its SHA256SUM provided in this repo are for reference only, it is recommended to download the iso image directly from `cdimage.debian.org` and [verify its authenticity](https://www.debian.org/CD/verify))

Debian Etch `example-preseed.txt`: [Link](https://www.debian.org/releases/etch/example-preseed.txt)

```
git clone https://github.com/tsondt/debian-etch-packer-vagrant
packer build debian4.json
vagrant box add --name debian4 debian4_virtualbox.box
vagrant up
ssh -p 2222 root@127.0.0.1
```

Default SSH username/password is `root`/`t00r`.

Clean up:

```
vagrant destroy
vagrant box remove debian4
rm -f debian4_virtualbox.box
```
