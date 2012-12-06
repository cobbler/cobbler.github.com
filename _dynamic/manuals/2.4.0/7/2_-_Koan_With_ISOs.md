---
layout: manpage
title: Cobbler Manual
meta: 2.4.0
---
While most of cobbler installing is about enabling scripted network
installation, can also define image objects which track ISOs that
koan can find and see. Currently this only works when using koan
with qemu/KVM for installation (sorry, no Xen or VMware support
yet). This can be used, for instance, to install Windows via koan.

For this to work best, the ISO must be available by the same NFS
path on all hosts. It need not be mounted and cobbler nor koan will
copy it.

    cobbler image add --name=image_name --file=nfs://hostname.example.org:/path/example/acme-os-installer-image.iso [--virt-ram=512] [--virt-file-size=10] [...etc...]

And on the koan side, just run:

    koan --list=images --server=cobbler.example.org
    
    koan --virt --image=image_name --server=cobbler.example.org

koan will then mount the NFS location and begin a fully virtualized
installation using the virtual metadata and info stored in
cobbler.

You may remember that cobbler has objects like "distros" and
"profiles". Images are another type of object, but act similarly.

System objects in cobbler may also attach to an image instead of a
profile, though not all attributes of the system apply to an image
-- for instance, we may care about the number of interfaces, but
the networking configuraition automagic that normally happens as
part of a kickstart can't happen for an image based install.

Avoid image based installs if at all possible -- use kickstart
where you can, and images for foreign content where you can not.

n