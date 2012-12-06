---
layout: manpage
title: Advanced Networking - Bonded Bridging
meta: 2.4.0
---

Some situations, such as virtualization hosts, require more redundancy in their bridging setups. In this case, 2.4.0 introduced a new interface type - the bonded_bridge_slave. This is an interface that is a bond master to one or more physical interfaces, and is itself a bridged slave interface.

You can create a bonded_bridge_slave in cobbler in the following way:

{% highlight bash %}
$ cobbler system edit --name=foo --interface=eth0 --mac=AA:BB:CC:DD:EE:F0 \
                      --interface-type=bond_slave --interface-master=bond0
$ cobbler system edit --name=foo --interface=eth1 --mac=AA:BB:CC:DD:EE:F1 \
                      --interface-type=bond_slave --interface-master=bond0
$ cobbler system edit --name=foo --interface=bond0 --interface-type=bonded_bridge_slave \
                      --bonding-opts="miimon=100 mode=1" --interface-master=br0
$ cobbler system edit --name=foo --interface=br0 --interface-type=bridge \
                      --bridge-opts="stp=no" --ip-address=192.168.1.100 \
                      --netmask=255.255.255.0 --static=1
{% endhighlight %}

**NOTE** Please reference the {% linkup title:"Advanced Networking - Bonding" extrameta:2.4.0 %} and {% linkup title:"Advanced Networking - Bridging" extrameta:2.4.0 %} sections for requirements specific to each of these interface types.
