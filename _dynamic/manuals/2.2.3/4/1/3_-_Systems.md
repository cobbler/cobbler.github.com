---
layout: manpage
title: Systems
meta: 2.2.3
---
System records map a piece of hardware (or a virtual machine) with the cobbler profile to be assigned to run on it.  This may be thought of as chosing a role for a specific system.

Note that if provisioning via koan and PXE menus alone, it is not required to create system records in cobbler, though they are useful when system specific customizations are required.   One such customization would be defining the MAC address.  If there is a specific role inteded for a given machine, system records should be created for it.

System commands have a wider variety of control offered over network details.  In order to use these to the fullest possible extent, the kickstart template used by cobbler must contain certain kickstart snippets (sections of code specifically written for Cobbler to make these values become reality).   Compare your kickstart templates with the stock ones in /var/lib/cobbler/kickstarts if you have upgraded, to make sure you can take advantage of all options to their fullest potential.  If you are a new cobbler user, base your kickstarts off of these templates.  Non-kickstart based distributions, while supported by Cobbler, may not be able to use all of these features.

Read more about networking setup at: https://fedorahosted.org/cobbler/wiki/AdvancedNetworking

#### Example:
{% highlight bash %}
$ cobbler system add --name=string --profile=string [--mac=macaddress] [--ip=ipaddress] \
[--hostname=hostname] [--kopts=string] [--ksmeta=string] [--kickstart=path] [--netboot-enabled=Y/N] \
[--server-override=string] [--gateway=string] [--dns-name=string] [--static-routes=string] \
[--power-address=string] [--power-type=string] [--power-user=string] [--power-password=string] \
[--power-id=string]
{% endhighlight %}

Adds a cobbler System to the configuration.  Arguments are specified as per "profile add" with the following changes:

### name
The system name works like the name option for other commands.

If the name looks like a MAC address or an IP, the name will implicitly be used for either --mac or --ip of the first interface, respectively.   However, it’s usually better to give a descriptive name -- don’t rely on this behavior.

A system created with name "default" has special semantics.  If a default system object exists, it sets all undefined systems to PXE to a specific profile.  Without a "default" system name created, PXE will fall through to local boot for unconfigured systems.

When using "default" name, don’t specify any other arguments than --profile ... they won’t be used.

### --mac
Specifying a mac address via --mac allows the system object to boot directly to a specific profile via PXE, bypassing cobbler’s PXE menu.  If the name of the cobbler system already looks like a mac address, this is inferred from the system name and does not need to be specified.

MAC addresses have the format AA:BB:CC:DD:EE:FF. It’s higly recommended to register your MAC-addresses in Cobbler if you’re using static adressing with multiple interfaces, or if you are using any of the advanced networking features like bonding, bridges or VLANs.

Cobbler does contain a feature (enabled in /etc/cobbler/settings) that can automatically add new system records when it finds profiles being provisioned on hardware it has seen before.  This may help if you do not have a report of all the MAC addresses in your datacenter/lab configuration.

### --ip
If cobbler is configured to generate a DHCP configuratition (see advanced section), use this setting to define a specific IP for this system in DHCP.  Leaving off this parameter will result in no DHCP management for this particular system.

#### Example:
{% highlight bash %}
--ip=192.168.1.50
{% endhighlight %}

Note for Itanium users:  this setting is always required for IA64 regardless of whether DHCP management is enabled.
           
If DHCP management is disabled and the interface is labelled --static=1, this setting will be used for static IP configuration.

Special feature: To control the default PXE behavior for an entire subnet, this field can also be passed in using CIDR notation.  If --ip is CIDR, do not specify any other arguments other than --name and --profile.

When using the CIDR notation trick, don’t specify any arguments other than --name and --profile... they won’t be used.

### --dns-name
If using the DNS management feature (see advanced section -- cobbler supports auto-setup of BIND and dnsmasq), use this to define a hostname for the system to receive from DNS.

#### Example:
{% highlight bash %}
--dns-name=mycomputer.example.com
{% endhighlight %}

This is a per-interface parameter.  If you have multiple interfaces, it may be different for each interface, for example, assume a DMZ / dual-homed setup.

### --gateway and --subnet
If you are using static IP configurations and the interface is flagged --static=1, these will be applied.

Subnet is a per-interface parameter.  Because of the way gateway is stored on the installed OS, gateway is a global parameter.  You may use --static-routes for per-interface customizations if required.

### --hostname
This field corresponds to the hostname set in a systems /etc/sysconfig/network file.  This has no bearing on DNS, even when manage_dns is enabled.  Use --dns-name instead for that feature.

This parameter is assigned once per system, it is not a per-interface setting.

### --power-address, --power-type, --power-user, --power-password, --power-id
Cobbler contains features that enable integration with power management for easier installation, reinstallation, and management of machines in a datacenter environment.  These parameters are described online at https://fedorahosted.org/cobbler/wiki/PowerManagement.  If you have a power-managed datacenter/lab setup, usage of these features may be something you are interested in.

### --static
Indicates that this interface is statically configured.  Many fields (such as gateway/subnet) will not be used unless this field is enabled.

This is a per-interface setting.

### --static-routes
This is a space delimited list of ip/mask:gateway routing information in that format.  Most systems will not need this information.

This is a per-interface setting.

### --virt-bridge
**(Virt-only)** While --virt-bridge is present in the profile object (see above), here it works on an interface by interface basis.  For instance it would be possible to have --virt-bridge0=xenbr0 and --virt-bridge1=xenbr1.  If not specified in cobbler for each interface, koan will use the value as specified in the profile for each interface, which may not always be what is intended, but will be sufficient in most cases.

This is a per-interface setting.

### --kickstart
While it is recommended that the --kickstart parameter is only used within for the "profile add" command, there are limited scenarios when an install base switching to cobbler may have legacy kickstarts created on a per-system basis (one kickstart for each system, nothing shared) and may not want to immediately make use of the cobbler templating system.  This allows specifing a kickstart for use on a per-system basis.  Creation of a parent profile is still required.  If the kickstart is a filesystem location, it will still be treated as a cobbler template.

### --netboot-enabled
If set false, the system will be provisionable through koan but not through standard PXE.  This will allow the system to fall back to default PXE boot behavior without deleting the cobbler system object.  The default value allows PXE.   Cobbler contains a PXE boot loop prevention feature (pxe_just_once, can be enabled in /etc/cobbler/settings) that can automatically trip off this value after a system gets done installing.  This can prevent installs from appearing in an endless loop when the system is set to PXE first in the BIOS order.

### --ldap-enabled, --ldap-type
Cobbler contains features that enable ldap management for easier configuration after system provisioning. If set true, koan will run the ldap command as defined by the systems ldap_type. The default value is false.

### --monit-enabled
If set true, koan will reload monit after each configuration run.  The default value is false.

### --repos-enabled
If set true, koan can reconfigure repositories after installation.  This is described further on the Cobbler Wiki, https://fedorahosted.org/cobbler/wiki/ManageYumRepos.

### --dhcp-tag
If you are setting up a PXE environment with multiple subnets/gateways, and are using cobbler to manage a DHCP configuration, you will probably want to use this option.  If not, it can be ignored.

By default, the dhcp tag for all systems is "default" and means that in the DHCP template files the systems will expand out where $insert_cobbler_systems_definitions is found in the DHCP template.  However, you may want certain systems to expand out in other places in the DHCP config file.  Setting --dhcp-tag=subnet2 for instance, will cause that system to expand out where $insert_cobbler_system_definitions_subnet2 is found, allowing you to insert directives to specify different subnets (or other parameters) before the DHCP configuration entries for those particular systems.

This is described further on the Cobbler Wiki.

### --interface
By default flags like --ip, --mac, --dhcp-tag, --dns-name, --subnet, --virt-bridge, and --static-routes operate on the first network interface defined for a system (eth0).  However, cobbler supports an arbitrary number of interfaces.  Using --interface=eth1 for instance, will allow creating and editing of a second interface.

#### Interface naming notes:
Additional interfaces can be specified (for example: eth1, or any name you like, as long as it does not conflict with any reserved names such as kernel module names) for use with the edit command.  Defining VLANs this way is also supported, if you want to add VLAN 5 on interface eth0, simply name your interface eth0:5.

#### Example:
{% highlight bash %}
$ cobbler system edit --name=foo --ip=192.168.1.50 --mac=AA:BB:CC:DD:EE:A0
$ cobbler system edit --name=foo --interface=eth0 --ip=192.168.1.51 --mac=AA:BB:CC:DD:EE:A1
$ cobbler system report foo
{% endhighlight %}

Interfaces can be deleted using the --delete-interface option.

#### Example:
{% highlight bash %}
$ cobbler system edit --name=foo --interface=eth2 --delete-interface
{% endhighlight %}

### --interface-type, --interface-master and --bonding-opts/--bridge-opts
One of the other advanced networking features supported by Cobbler is NIC bonding and bridging. You can use this to bond multiple physical network interfaces to one single logical interface to reduce single points of failure in your network, or to create bridged interfaces for things like tunnels and virtual machine networks. Supported values for the --interface-type parameter are "bond", "bond_slave", "bridge" and "bridge_slave". If one of the "_slave" options is specified, you also need to define the master-interface for this bond using --interface-master=INTERFACE. Bonding and bridge options for the master-interface may be specified using --bonding-opts="foo=1 bar=2" or --bridge-opts="foo=1 bar=2", respectively.

**Note:** The options "master" and "slave" are deprecated, and are assumed to me "bond" and "bond_slave" when encountered. When a system object is saved, the deprecated values will be overwritten with the new, correct values.

#### Example:
{% highlight bash%}
$ cobbler system edit --name=foo --interface=eth0 --mac=AA:BB:CC:DD:EE:00 --interface-type=bond_slave \
--interface-master=bond0
$
$ cobbler system edit --name=foo --interface=eth1 --mac=AA:BB:CC:DD:EE:01 --interface-type=bond_slave \
--interface-master=bond0
$
$ cobbler system edit --name=foo --interface=bond0 --interface-type=bond \
--bonding-opts="mode=active-backup miimon=100" --ip=192.168.0.63 --subnet=255.255.255.0 \
--gateway=192.168.0.1 --static=1
{% endhighlight %}

More information about networking setup is available at https://fedorahosted.org/cobbler/wiki/AdvancedNetworking

To review what networking configuration you have for any object, run "cobbler system report" at any time:

#### Example:
{% highlight bash %}
$ cobbler system report --name=foo
{% endhighlight %}
