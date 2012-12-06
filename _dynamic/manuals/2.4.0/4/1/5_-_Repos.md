---
layout: manpage
title: Repos
meta: 2.4.0
---
Repository mirroring allows cobbler to mirror not only install trees ("cobbler import" does this for you) but also optional packages, 3rd party content, and even updates.   Mirroring all of this content locally on your network will result in faster, more up-to-date installations and faster updates.  If you are only provisioning a home setup, this will probably be overkill, though it can be very useful for larger setups (labs, datacenters, etc).  For information on how to keep your mirror up-to-date, see {% linkup title:"Reposync" extrameta:2.4.0 %}.

#### Example:
{% highlight bash %}
$ cobbler repo add --mirror=url --name=string [--rpmlist=list] [--creatrepo-flags=string] \
[--keep-updated=Y/N] [--priority=number] [--arch=string] [--mirror-locally=Y/N] [--breed=yum|rsync|rhn]
{% endhighlight %}

### mirror
The addresss of the yum mirror.  This can be an rsync:// URL, an ssh location, or a http:// or ftp:// mirror location.  Filesystem paths also work.

The mirror address should specify an exact repository to mirror -- just one architecture and just one distribution.  If you have a seperate repo to mirror for a different arch, add that repo seperately.

#### Example:
{% highlight bash %}
rsync://yourmirror.example.com/fedora-linux-core/updates/6/i386 (for rsync protocol)
http://mirrors.kernel.org/fedora/extras/6/i386/ (for http://)
user@yourmirror.example.com/fedora-linux-core/updates/6/i386  (for SSH)
{% endhighlight %}

Experimental support is also provided for mirroring RHN content when you need a fast local mirror.  The mirror syntax for this is --mirror=rhn://channel-name and you must have entitlements for this to work.  This requires the cobbler server to be installed on RHEL5 or later.  You will also need a version of yum-utils equal or greater to 1.0.4.

### name
This name is used as the save location for the mirror.  If the mirror represented, say, Fedora Core 6 i386 updates, a good name would be "fc6i386updates".  Again, be specific.

This name corresponds with values given to the --repos parameter of "cobbler profile add".  If a profile has a --repos value that matches the name given here, that repo can be automatically set up during provisioning (when supported) and installed systems will also use the boot server as a mirror (unless "yum_post_install_mirror" is disabled in the settings file).  By default the provisioning server will act as a mirror to systems it installs, which may not be desirable for laptop configurations, etc.

Distros that can make use of yum repositories during kickstart include FC6 and later, RHEL 5 and later, and derivative distributions.

See the documentation on "cobbler profile add" for more information.

### rpm-list
By specifying a space-delimited list of package names for --rpm-list, one can decide to mirror only a part of a repo (the list of packages given, plus dependencies).  This may be helpful in conserving time/space/bandwidth.  For instance, when mirroring FC6 Extras, it may be desired to mirror just cobbler and koan, and skip all of the game packages.  To do this, use --rpm-list="cobbler koan".

This option only works for http:// and ftp:// repositories (as it is powered by yumdownloader).  It will be ignored for other mirror types, such as local paths and rsync:// mirrors.

### createrepo-flags
Specifies optional flags to feed into the createrepo tool, which is called when "cobbler reposync" is run for the given repository. The defaults are ’-c cache’.

### keep-updated
Specifies that the named repository should not be updated during a normal "cobbler reposync".    The repo may still be updated by name.   The repo should be synced at least once before disabling this feature See "cobbler reposync" below.

### mirror-locally
When set to "N", specifies that this yum repo is to be referenced directly via kickstarts and not mirrored locally on the cobbler server.  Only http:// and ftp:// mirror urls are supported when using --mirror-locally=N, you cannot use filesystem URLs.

### priority
Specifies the priority of the repository (the lower the number, the higher the priority), which applies to installed machines using the repositories that also have the yum priorities plugin installed. The default priority for the plugin is 99, as is that of all cobbler mirrored repositories.

### arch
Specifies what architecture the repository should use.  By default the current system arch (of the server) is used, which may not be desirable.  Using this to override the default arch allows mirroring of source repositories (using --arch=src).

### yumopts
Sets values for additional yum options that the repo should use on installed systems.  For instance if a yum plugin takes a certain parameter "alpha" and "beta", use something like --yumopts="alpha=2 beta=3".
           
### breed
Ordinarily cobbler’s repo system will understand what you mean without supplying this parameter, though you can set it explicitly if needed.