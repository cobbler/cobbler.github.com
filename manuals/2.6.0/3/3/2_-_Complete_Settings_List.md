<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en-us">
<head>
   <meta http-equiv="content-type" content="text/html; charset=utf-8" />
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <meta name="author" content="Cobbler development team" />

   <title>Complete Settings List</title>

   <!-- CSS -->
   <link rel="stylesheet" type="text/css" href="http://code.jquery.com/ui/1.8.18/themes/base/jquery-ui.css" />
   <link rel="stylesheet" type="text/css" href="/lib/bootstrap/css/bootstrap.min.css" />
   <link rel="stylesheet" type="text/css" href="/lib/bootstrap/css/bootstrap-responsive.min.css" />
   <link rel="stylesheet" type="text/css" href="/lib/font/font-awesome.css" />
   <link rel="stylesheet" type="text/css" href="/lib/font/font-awesome-ext.css" />
   <link rel="stylesheet" type="text/css" href="/css/syntax.css" />
   <link rel="stylesheet" type="text/css" href="/css/style.css" />
   <link rel="stylesheet" type="text/css" href="/css/search.css" />

   <!-- Fonts -->
   <link rel='stylesheet' type='text/css' href='http://fonts.googleapis.com/css?family=Habibi|Roboto+Condensed' />

   <!--[if lt IE 9]>
     <script src="http://html5shim.googlecode.com/svn/trunk/html5.js"></script>
   <![endif]-->

   <!-- Icon -->
   <link rel="icon" type="image/png" href="/images/favicon.png" />

   <!-- JQuery/Bootstrap/custom scripts -->
   <script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.2/jquery.min.js"></script>
   <script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jqueryui/1.8.18/jquery-ui.min.js"></script>
   <script type="text/javascript" src="/lib/bootstrap/js/bootstrap.min.js"></script>
   <script type="text/javascript" src="/js/jquery.ba-hashchange.min.js"></script>
   <script type="text/javascript" src="/js/jquery.swiftype.search.js"></script>
</head>
<body class="pull_up">

<!-- ClickTale Top part -->
<script type="text/javascript">
var WRInitTime=(new Date()).getTime();
</script>
<!-- ClickTale end of Top part -->

<div class="navbar transparent navbar-inverse navbar-static-top">
 <div class="navbar-inner">
  <div class="container">
   <a class="brand" href="/"><img class="logo" src="/images/logo-brand.png" /></a>
   <div class="nav-collapse collapse">
    <ul class="nav pull-right">
     <li><a href="/about.html" title="About"><i class="icon-cloud icon-med"></i> About </a></li>
     <li class="dropdown">
       <a href="#" class="dropdown-toggle" data-toggle="dropdown"><i class="icon-question-sign icon-med"></i> Downloads <b class="caret"></b></a>
       <ul class="dropdown-menu">
         <li><a href="/downloads/2.8.x.html" title="Cobbler 2.8.x">2.8.x</a></li>
         <li><a href="/downloads/2.6.x.html" title="Cobbler 2.6.x">2.6.x</a></li>
         <li><a href="/downloads/2.4.x.html" title="Cobbler 2.4.x">2.4.x</a></li>
       </ul>
     </li>
     <li><a href="/blog/" title="Blog Posts"><i class="icon-bookmark icon-med"></i> Blog Posts</a></li>
     <li class="dropdown">
       <a href="#" class="dropdown-toggle" data-toggle="dropdown"><i class="icon-question-sign icon-med"></i> Manuals <b class="caret"></b></a>
       <ul class="dropdown-menu">
         <li><a href="/manuals/quickstart/" title="Quickstart Guide">Quickstart Guide</a></li>
         <li><a href="/manuals/2.8.0/" title="Version 2.8.x">User Manual 2.8.x</a></li>
         <li><a href="/manuals/2.6.0/" title="Version 2.6.x">User Manual 2.6.x</a></li>
         <li><a href="/manuals/2.4.0/" title="Version 2.4.x">User Manual 2.4.x</a></li>
         <li><a href="/manuals/developer/" title="Developer Guide">Developer Guide</a></li>
       </ul>
     </li>
     <li class="dropdown">
       <a href="#" class="dropdown-toggle" data-toggle="dropdown"><i class="icon-group icon-med"></i> Community <b class="caret"></b></a>
       <ul class="dropdown-menu">
         <li><a href="/community.html" title="How to Get Help">How to Get Help</a></li>
         <li><a href="/supporters.html" title="Supporters of Cobbler">Supporters</a></li>
         <li><a href="/users.html" title="Cobbler Users">Who's Using Cobbler</a></li>
       </ul>
     </li>
     <li class="dropdown">
       <a href="#" class="dropdown-toggle" data-toggle="dropdown"><i class="icon-github icon-med"></i> Github <b class="caret"></b></a>
       <ul class="dropdown-menu">
        <li><a href="https://github.com/cobbler/cobbler" title="Main Repository" target="_blank">Main Repo</a></li>
        <li><a href="https://github.com/cobbler/cobbler/issues" title="Issues" target="_blank">Issue Tracker</a></li>
        <li><a href="https://github.com/cobbler/cobbler/wiki" title="Github Wiki" target="_blank">Wiki</a></li>
       </ul>
     </li>
     <li>
      <form class="pull-right">
       <input type="text" id="st-search-input" class="st-search-input" />
      </form>
     </li>
    </ul>
    <!-- <div id="st-results-container"></div> -->
    <script type="text/javascript">
      var Swiftype = window.Swiftype || {};
      (function() {
        Swiftype.key = 'ybEhsDqz2mEFrMtBHiwB';
        Swiftype.inputElement = '#st-search-input';
        Swiftype.resultContainingElement = '#st-results-container';
        Swiftype.attachElement = '#st-search-input';
        Swiftype.renderStyle = "new_page";
        Swiftype.resultPageURL = '/search.html';
        var script = document.createElement('script');
        script.type = 'text/javascript';
        script.async = true;
        script.src = "//swiftype.com/embed.js";
        var entry = document.getElementsByTagName('script')[0];
        entry.parentNode.insertBefore(script, entry);
      }());
    </script>
   </div>
   <!--
   <form class="navbar-search pull-right" onsubmit="return false;">
    <input id="searchbox" type="text" class="search-query" placeholder="Search Manuals" />
   </form>
   -->
  </div>
 </div>
</div>


<!-- begin content -->

<div id="wrap" class="container">
 <div class="row">
  <div class="span8">
<ul class="breadcrumb"><li><a href="/manuals">manuals</a> <span class="divider">/</span></li><li><a href="/manuals/2.6.0">2.6.0</a> <span class="divider">/</span></li><li><a href="/manuals/2.6.0/3_-_General_Topics.html">3</a> <span class="divider">/</span></li><li><a href="/manuals/2.6.0/3/3_-_Cobbler_Settings.html">3</a> <span class="divider">/</span></li><li class="active">Complete Settings List</li></ul>
   <h1>Complete Settings List</h1>
<p>This page documents all settings <code>/etc/cobbler/settings</code> available for configuring both cobblerd and the cobbler CLI command. Be sure to restart the cobblerd service after making changes to this file.</p>

<p><strong>NOTE:</strong> The defaults shown here are noted via JSON syntax. The settings file is stored as YAML, so be sure to format it correctly or cobblerd and the CLI command will not work properly.</p>

<h3>allow_duplicate_hostnames</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 0</li>
</ul>


<h4>Description:</h4>

<p>If set, Cobbler will allow multiple systems to use the same FQDN for the --dns-name interface option. This field is used for system identification for things like configuration management integration, so take care when enabling it.</p>

<h3>allow_duplicate_ips</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 0</li>
</ul>


<h4>Description:</h4>

<p>If set, Cobbler will allow multiple systems to use the same IP address for interfaces. If enabled, this could impact managed services like DHCP and DNS where multiple active systems conflict.</p>

<h3>allow_duplicate_macs</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 0</li>
</ul>


<h4>Description:</h4>

<p>If set, Cobbler will allow multiple systems to use the same MAC address for interfaces. If enabled, this could impact managed services like DHCP and DNS where multiple active systems conflict.</p>

<h3>allow_dynamic_settings</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 0</li>
</ul>


<h4>Description:</h4>

<p>If enabled, Cobbler will allow settings to be modified on the fly without a restart to the cobblerd daemon. Please reference the <a href="/manuals/2.6.0/3/3/1_-_Dynamic_Settings.html">Dynamic Settings</a> section for more details.</p>

<h3>anamon_enabled</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 0</li>
</ul>


<h4>Description:</h4>

<p>If set, anamon will be enabled during the Anaconda kickstart process. This is specific to Red Hat style kickstarts only.</p>

<p>Please refer to the <a href="/manuals/2.6.0/Appendix/E_-_Anaconda_Monitoring.html">Anaconda Monitoring</a> section for more details.</p>

<h3>bind_chroot_path</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> ""</li>
</ul>


<h4>Description:</h4>

<p>This sets the path of the directory in which bind-chroot compatible configuration files will be created. In most situations, this should be automatically detected by default (set to an empty string).</p>

<p>Please refer to the <a href="/manuals/2.6.0/3/4/2_-_Managing_DNS.html">Managing DNS</a> section for more details.</p>

<h3>bind_master</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "127.0.0.1"</li>
</ul>


<h4>Description:</h4>

<p>The bind master to use when creating slave DNS zones.</p>

<p>Please refer to the <a href="/manuals/2.6.0/3/4/2_-_Managing_DNS.html">Managing DNS</a> section for more details.</p>

<h3>build_reporting_email</h3>

<ul>
<li><strong>type:</strong> Array of Strings</li>
<li><strong>default:</strong> ['root@localhost']</li>
</ul>


<h4>Description:</h4>

<p>A list of email addresses to send build reports to.</p>

<h3>build_reporting_enabled</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 0</li>
</ul>


<h4>Description:</h4>

<p>Setting this option enables build reporting emails.</p>

<h3>build_reporting_sender</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> ""</li>
</ul>


<h4>Description:</h4>

<p>The email address to use as the sender of a build report email (optional).</p>

<h3>build_reporting_smtp_server</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "localhost"</li>
</ul>


<h4>Description:</h4>

<p>The SMTP server to use for build report emails.</p>

<h3>build_reporting_subject</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> ""</li>
</ul>


<h4>Description:</h4>

<p>This setting allows you to override the default auto-generated subject lines for build report emails.</p>

<h3>build_reporting_to_address</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> ""</li>
</ul>


<h4>Description:</h4>

<p>Not currently used.</p>

<h3>buildisodir</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "/var/cache/cobbler/buildiso"</li>
</ul>


<h4>Description:</h4>

<p>The default directory to use as scratch space when building an ISO via Cobbler. This can be overridden on the command line.</p>

<p>Please refer to the <a href="/manuals/2.6.0/3/2/6_-_Build_ISO.html">Build ISO</a> section for more details.</p>

<h3>cheetah_import_whitelist</h3>

<ul>
<li><strong>type:</strong> Array of Strings</li>
<li><strong>default:</strong> ['random', 're', 'time']</li>
</ul>


<h4>Description:</h4>

<p>This setting creates a whitelist of python modules that can be imported in a template.</p>

<p>This is a security issue, as allowing certain python modules would allow users to create templates that overwrite system files (ie. the os module) or execute shell commands (ie. the subprocess module). Make sure you understand the capabilities a python module has before adding them to this whitelist.</p>

<h3>client_use_localhost</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 0</li>
</ul>


<h4>Description:</h4>

<p>If enabled, all commands will be forced to use the localhost address instead of the "server" setting. The cobbler client command can be used to manage remote cobblerd instances, so enabling this option would force all cobbler commands to operate locally only.</p>

<h3>cobbler_master</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> ""</li>
</ul>


<h4>Description:</h4>

<p>The default server to pull from when using the replicate command.</p>

<p>Please refer to the <a href="/manuals/2.6.0/3/2/8_-_Replication.html">Replicate</a> section for more details.</p>

<h3>consoles</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "/var/consoles"</li>
</ul>


<h4>Description:</h4>

<p>The path to the directory containing system consoles, used primarily for clearing logs and messages.</p>

<h3>createrepo_flags</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "-c cache -s sha --update"</li>
</ul>


<h4>Description:</h4>

<p>Default options to use for the createrepo command when creating new repositories during a reposync.</p>

<p>If you have createrepo >= 0.4.10, consider "-c cache --update -C", which can dramatically improve your "cobbler reposync" time. "-s sha" enables working with Fedora repos from F11/F12 from EL-4 or EL-5 without python-hashlib installed (which is not available on EL-4)</p>

<p>Please refer to the <a href="/manuals/2.6.0/3/7_-_Package_Management_and_Mirroring.html">Package Management and Mirroring</a> section for more details.</p>

<h3>default_deployment_method</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "ssh"</li>
</ul>


<h4>Description:</h4>

<p>Not currently used.</p>

<h3>default_kickstart</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "/var/lib/cobbler/kickstarts/default.ks"</li>
</ul>


<h4>Description:</h4>

<p>The default kickstart file to use if no other is specified. This option is effectively deprecated, as the default kickstart to use is now specified in the distro signatures configuration file. Please see the <a href="/manuals/2.6.0/3/2/3_-_Distro_Signatures.html">Distro Signatures</a> section for more details.</p>

<h3>default_name_servers</h3>

<ul>
<li><strong>type:</strong> Array of Strings</li>
<li><strong>default:</strong> []</li>
</ul>


<h4>Description:</h4>

<p>A list of name servers to assign to all systems and profiles that are built. This will be used both pre and post install.</p>

<h3>default_name_servers_search</h3>

<ul>
<li><strong>type:</strong> Array of Strings</li>
<li><strong>default:</strong> []</li>
</ul>


<h4>Description:</h4>

<p>A list of domains to search by default. This will be inserted into the resolv.conf file.</p>

<h3>default_ownership</h3>

<ul>
<li><strong>type:</strong> Array of Strings</li>
<li><strong>default:</strong> ['admin']</li>
</ul>


<h4>Description:</h4>

<p>A list of owners to assign to newly created objects. This is used only for Web UI authorization.</p>

<p>Please refer to the <a href="/manuals/2.6.0/5/3_-_Web_Authorization.html">Web Authorization</a> section for more details.</p>

<h3>default_password_crypted</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "$1$wrWZXfa7$Ts7jMmpdZkTlu0lSx1A/I/" (cobbler)</li>
</ul>


<h4>Description:</h4>

<p>The default hashed password to use in kickstarts. The default value is "cobbler" (hashed).</p>

<p>To generate a new hashed password, use the following command:</p>

<p><figure class="highlight"><pre><code class="language-bash" data-lang="bash">$ openssl passwd -1</code></pre></figure></p>

<p>Be sure to enclose the hash with quotation marks.</p>

<h3>default_template_type</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "cheetah"</li>
</ul>


<h4>Description:</h4>

<p>The default template type to use when parsing kickstarts and snippets. The default template type is Cheetah, and changing this value will currently break all snippets and templates currently shipped with Cobbler.</p>

<p>Please refer to the <a href="/manuals/2.6.0/4/6_-_Alternative_Template_Formats.html">Alternative Template Formats</a> section for more details.</p>

<h3>default_virt_bridge</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "xenbr0"</li>
</ul>


<h4>Description:</h4>

<p>The default bridge to assign virtual interfaces to.</p>

<h3>default_virt_disk_driver</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "raw"</li>
</ul>


<h4>Description:</h4>

<p>The default disk driver to use for virtual disks. Older versions of python-virtinst do not support changing this at build time, so this option will be ignored in those cases.</p>

<h3>default_virt_file_size</h3>

<ul>
<li><strong>type:</strong> Integer</li>
<li><strong>default:</strong> 5</li>
</ul>


<h4>Description:</h4>

<p>The default size (in gigabytes) to use for new virtual disks.</p>

<h3>default_virt_ram</h3>

<ul>
<li><strong>type:</strong> Integer</li>
<li><strong>default:</strong> 512</li>
</ul>


<h4>Description:</h4>

<p>The default size (in megabytes) of RAM to assign to new virtual machines.</p>

<h3>default_virt_type</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "xenpv"</li>
</ul>


<h4>Description:</h4>

<p>The default virtualization type to use for virtual machines created with the koan utility.</p>

<p>Please refer to the <a href="/manuals/2.6.0/6_-_Koan.html">Koan</a> section for more details.</p>

<h3>enable_gpxe</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 0</li>
</ul>


<h4>Description:</h4>

<p>If set, Cobbler will enable the use of gPXE.</p>

<p>Please refer to the <a href="/manuals/2.6.0/4/13_-_Using_gPXE.html">Using gPXE</a> section for more details.</p>

<h3>enable_menu</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 1</li>
</ul>


<h4>Description:</h4>

<p>If set, Cobbler will add each new profile entry to the default PXE boot menu. This can be overridden on a per-profile basis when adding/editing profiles with --enable-menu=0/1. Users should ordinarily leave this setting enabled unless they are concerned with accidental reinstalls from users who select an entry at the PXE boot menu. Adding a password to the boot menus templates may also be a good solution to prevent unwanted reinstallations.</p>

<h3>func_auto_setup</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 0</li>
</ul>


<h4>Description:</h4>

<p>If set, Cobbler will install and configure Func. This makes sure each installed machine is set up to use func out of the box, which is a powerful way to script and control remote machines.</p>

<p>Please refer to the <a href="/manuals/2.6.0/4/3/3_-_Func_Integration.html">Func Integration</a> section for more details.</p>

<h3>func_master</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "overlord.example.org"</li>
</ul>


<h4>Description:</h4>

<p>The Func master server (overlord) to use by default.</p>

<p>Please refer to the <a href="/manuals/2.6.0/4/3/3_-_Func_Integration.html">Func Integration</a> section for more details.</p>

<h3>http_port</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "80"</li>
</ul>


<h4>Description:</h4>

<p>The port on which Apache is listening. Only change this if your instance of Apache is listening on a different port (for example: 8080).</p>

<h3>isc_set_host_name</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 0</li>
</ul>


<h4>Description:</h4>

<p>Not currently used.</p>

<h3>iso_template_dir</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "/etc/cobbler/iso"</li>
</ul>


<h4>Description:</h4>

<p>The directory containing the buildiso.template, which is a SYSLINUX style configuration file for use in the buildiso process.</p>

<p>Please refer to the <a href="/manuals/2.6.0/3/2/6_-_Build_ISO.html">Build ISO</a> section for more details.</p>

<h3>kerberos_realm</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "EXAMPLE.COM"</li>
</ul>


<h4>Description:</h4>

<p>Not currently used (all kerberos configuration must currently be done manually).</p>

<p>Please refer to the <a href="/manuals/2.6.0/5/2/3_-_Kerberos.html">Kerberos Authentication</a> section for more details.</p>

<h3>kernel_options</h3>

<ul>
<li><strong>type:</strong> Dictionary</li>
<li><strong>default:</strong> {'ksdevice': 'bootif', 'lang': ' ', 'text': '~'}</li>
</ul>


<h4>Description:</h4>

<p>A dictionary of key/value pairs that will be added to the kernel command line during the installation only (post-installation options are specified at the distro/profile/etc. object level).</p>

<p>By default, each key/value pair will be show up as key=value in the kernel command line. Setting the value for a given key to '~' (tilde) will cause the option to be printed by itself with no '='.</p>

<div class="alert alert-info alert-block"><b>Note:</b> The kernel command line has a maximum character limitation of 256 characters. Cobbler will print a warning if you exceed this limit.</div>


<h3>kernel_options_s390x</h3>

<ul>
<li><strong>type:</strong> Dictionary</li>
<li><strong>default:</strong> {'vnc': '~', 'ip': False, 'RUNKS': 1, 'ramdisk_size': 40000, 'ro': '~', 'root': '/dev/ram0'}</li>
</ul>


<h4>Description:</h4>

<p>Same as the kernel_options setting, but specific to s390x architectures.</p>

<h3>ldap_anonymous_bind</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 1</li>
</ul>


<h4>Description:</h4>

<p>If set, the LDAP authentication module will use an anonymous bind when connecting to the LDAP server.</p>

<p>Please refer to the <a href="/manuals/2.6.0/5/2/2_-_LDAP.html">LDAP Authentication</a> section for more details.</p>

<h3>ldap_base_dn</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "DC=example,DC=com"</li>
</ul>


<h4>Description:</h4>

<p>The base DN to use for LDAP authentication.</p>

<p>Please refer to the <a href="/manuals/2.6.0/5/2/2_-_LDAP.html">LDAP Authentication</a> section for more details.</p>

<h3>ldap_management_default_type</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "authconfig"</li>
</ul>


<h4>Description:</h4>

<p>Not currently used.</p>

<p>Please refer to the <a href="/manuals/2.6.0/5/2/2_-_LDAP.html">LDAP Authentication</a> section for more details.</p>

<h3>ldap_port</h3>

<ul>
<li><strong>type:</strong> Integer</li>
<li><strong>default:</strong> 389</li>
</ul>


<h4>Description:</h4>

<p>The port to use when connecting to the LDAP server. If TLS is enabled and this port is the default of 389, cobbler will internally convert it to 636 for SSL.</p>

<p>Please refer to the <a href="/manuals/2.6.0/5/2/2_-_LDAP.html">LDAP Authentication</a> section for more details.</p>

<h3>ldap_search_bind_dn</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> ""</li>
</ul>


<h4>Description:</h4>

<p>The DN to use for binding to the LDAP server for authentication, used only if ldap_anonymous_bind=0.</p>

<p>Please refer to the <a href="/manuals/2.6.0/5/2/2_-_LDAP.html">LDAP Authentication</a> section for more details.</p>

<h3>ldap_search_passwd</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> ""</li>
</ul>


<h4>Description:</h4>

<p>The password to use when binding to the LDA server for authentication, used only if ldap_anonymous_bind=0.</p>

<p>Please refer to the <a href="/manuals/2.6.0/5/2/2_-_LDAP.html">LDAP Authentication</a> section for more details.</p>

<h3>ldap_search_prefix</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "uid="</li>
</ul>


<h4>Description:</h4>

<p>The prefix to use for searches when querying the LDAP server.</p>

<p>Please refer to the <a href="/manuals/2.6.0/5/2/2_-_LDAP.html">LDAP Authentication</a> section for more details.</p>

<h3>ldap_server</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> "ldap.example.com"</li>
</ul>


<h4>Description:</h4>

<p>The LDAP server to use for LDAP authentication.</p>

<p>Please refer to the <a href="/manuals/2.6.0/5/2/2_-_LDAP.html">LDAP Authentication</a> section for more details.</p>

<h3>ldap_tls</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 1</li>
</ul>


<h4>Description:</h4>

<p>If set, the LDAP authentication will occur over a SSL/TLS encrypted connection.</p>

<p>Please refer to the <a href="/manuals/2.6.0/5/2/2_-_LDAP.html">LDAP Authentication</a> section for more details.</p>

<h3>ldap_tls_cacertfile</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 1</li>
</ul>


<h4>Description:</h4>

<p>The CA certificate file to use when using TLS encryption.</p>

<p>Please refer to the <a href="/manuals/2.6.0/5/2/2_-_LDAP.html">LDAP Authentication</a> section for more details.</p>

<h3>ldap_tls_keyfile</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 1</li>
</ul>


<h4>Description:</h4>

<p>The certificate key file to use when using TLS encryption.</p>

<p>Please refer to the <a href="/manuals/2.6.0/5/2/2_-_LDAP.html">LDAP Authentication</a> section for more details.</p>

<h3>ldap_tls_certfile</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 1</li>
</ul>


<h4>Description:</h4>

<p>The certificate file to use when using TLS encryption.</p>

<p>Please refer to the <a href="/manuals/2.6.0/5/2/2_-_LDAP.html">LDAP Authentication</a> section for more details.</p>

<h3>manage_dhcp</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 0</li>
</ul>


<h4>Description:</h4>

<p>If enabled, Cobbler will rewrite the dhcpd.conf file based on the template <code>/etc/cobbler/dhcp.template</code>. If you are using static IP addresses for interfaces, you must enable this option so that static lease entries are written and available for the PXE phase of the installation.</p>

<p>Alternatively, if DNSMASQ is being used for DNS/DHCP, it will manage those configuration files.</p>

<p>Please refer to the <a href="/manuals/2.6.0/3/4/1_-_Managing_DHCP.html">Managing DHCP</a> section for more details.</p>

<h3>manage_dns</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 0</li>
</ul>


<h4>Description:</h4>

<p>If enabled, Cobbler will write the named.conf and BIND zone files based on templates and other settings.</p>

<p>Alternatively, if DNSMASQ is being used for DNS/DHCP, it will manage those configuration files.</p>

<p>Please refer to the <a href="/manuals/2.6.0/3/4/2_-_Managing_DNS.html">Managing DNS</a> section for more details.</p>

<h3>manage_forward_zones</h3>

<ul>
<li><strong>type:</strong> List of Strings</li>
<li><strong>default:</strong> []</li>
</ul>


<h4>Description:</h4>

<p>If enabled along with the manage_dns option, Cobbler will generate configurations for the forward-based zones specified in the list.</p>

<p>Please refer to the <a href="/manuals/2.6.0/3/4/2_-_Managing_DNS.html">Managing DNS</a> section for more details.</p>

<h3>manage_reverse_zones</h3>

<ul>
<li><strong>type:</strong> List of Strings</li>
<li><strong>default:</strong> []</li>
</ul>


<h4>Description:</h4>

<p>If enabled along with the manage_dns option, Cobbler will generate configurations for the reverse-based zones specified in the list.</p>

<p>Please refer to the <a href="/manuals/2.6.0/3/4/2_-_Managing_DNS.html">Managing DNS</a> section for more details.</p>

<h3>manage_rsync</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 0</li>
</ul>


<h4>Description:</h4>

<p>If set, Cobbler will generate the rsyncd.conf configuration file. This is required if using a system running cobblerd as a replica master.</p>

<p>Please refer to the <a href="/manuals/2.6.0/3/2/8_-_Replication.html">Replicate</a> section for more details.</p>

<h3>manage_tftpd</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 1</li>
</ul>


<h4>Description:</h4>

<p>If set, Cobbler will copy files required for the PXE netboot process to the TFTPD root directory and will also generate PXE boot configuration files for systems and profiles.</p>

<p>Please refer to the <a href="/manuals/2.6.0/3/4/4_-_Managing_TFTP.html">Managing TFTP</a> section for more details.</p>

<h3>mgmt_classes</h3>

<ul>
<li><strong>type:</strong> List of Strings</li>
<li><strong>default:</strong> []</li>
</ul>


<h4>Description:</h4>

<p>A default list of management class names to give all objects, for use with configuration management integration.</p>

<p>Please refer to the <a href="/manuals/2.6.0/4/3_-_Configuration_Management.html">Configuration Management</a> section for more details.</p>

<h3>mgmt_parameters</h3>

<ul>
<li><strong>type:</strong> Dictionary</li>
<li><strong>default:</strong> {'from_cobbler': 1}</li>
</ul>


<h4>Description:</h4>

<p>A default list of management parameters to give all objects, for use with configuration management integration.</p>

<p>Please refer to the <a href="/manuals/2.6.0/4/3_-_Configuration_Management.html">Configuration Management</a> section for more details.</p>

<h3>next_server</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "127.0.0.1"</li>
</ul>


<h4>Description:</h4>

<p>If manage_dhcp is enabled, this will be the default next-server value passed to systems that are PXE booting. This value can be overriden on a per-system basis via the --server option.</p>

<p>Please refer to the <a href="/manuals/2.6.0/4/7_-_Multi-Homed_Cobbler_Servers.html">Multi-Homed Cobbler Servers</a> section for more details.</p>

<h3>power_management_default_type</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "ipmitool"</li>
</ul>


<h4>Description:</h4>

<p>The default power management type, when using Cobbler's power management feature.</p>

<p>Please refer to the <a href="/manuals/2.6.0/4/5_-_Power_Management.html">Power Management</a> section for more details.</p>

<h3>power_template_dir</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "/etc/cobbler/power"</li>
</ul>


<h4>Description:</h4>

<p>The path to the directory containing templates that will be used for generating data sent to the various power management functions (typically provided by cluster fencing agents). As of 2.2.3, templates are no longer required for the default function of most fence agents.</p>

<p>Please refer to the <a href="/manuals/2.6.0/4/5_-_Power_Management.html">Power Management</a> section for more details.</p>

<h3>puppet_auto_setup</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 0</li>
</ul>


<h4>Description:</h4>

<p>If enabled, Cobbler will install and configure the <a href="http://puppetlabs.com/solutions/configuration-management/">Puppet configuration management</a> software on new systems.</p>

<p>Please refer to the <a href="/manuals/2.6.0/4/3/2_-_Puppet_Integration.html">Puppet Integration</a> section for more details.</p>

<h3>puppetca_path</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "/usr/sbin/puppetca"</li>
</ul>


<h4>Description:</h4>

<p>The path to the puppetca command, which is used by cobbler to auto-register and cleanup Puppet CA certificates during the build process for new systems.</p>

<p>Please refer to the <a href="/manuals/2.6.0/4/3/2_-_Puppet_Integration.html">Puppet Integration</a> section for more details.</p>

<h3>pxe_just_once</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 0</li>
</ul>


<h4>Description:</h4>

<p>If enabled, Cobbler will set the netboot_enabled flag for systems to 0 when the build process is complete. This prevents systems from ending up in a PXE reboot/installation loop which can happen when PXE is set to the default boot option.</p>

<p><strong>NOTE:</strong> This requires the use of the $SNIPPET('kickstart_done') in your %post (usually the last line of the %post script). This snippet is included in the sample*.ks files, so review those as a reference for use.</p>

<h3>pxe_template_dir</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "/etc/cobbler/pxe"</li>
</ul>


<h4>Description:</h4>

<p>The directory containing the templates used for generating PXE boot configuration files, when manage_tftpd is enabled.</p>

<h3>redhat_management_key</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> ""</li>
</ul>


<h4>Description:</h4>

<p>The default RHN registration key to use with the included RHN/Satellite/Spacewalk registration scripts. This can be overridden on a per-object basis, for instance when you want to use different registration keys to place systems in different RHN channels, etc.</p>

<h3>redhat_management_permissive</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 0</li>
</ul>


<h4>Description:</h4>

<p>If set, this will allow per-user access in the Web UI when using the authn_spacewalk module for authentication.</p>

<p>However, doing so will permit all Spacewalk/Satellite users with certain roles (config_admin and org_admin) to edit all of cobbler's configuration. Users should turn this on only if they want this behavior and do not have a cross-multi-org seperation concern. If you have a single org in your satellite, it's probably safe to turn this on to enable the use of the Web UI alongside a Satellite install.</p>

<p>Please refer to the <a href="/manuals/2.6.0/5/2/4_-_Spacewalk.html">Spacewalk Authentication</a> section for more details.</p>

<h3>redhat_management_server</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "xmlrpc.rhn.redhat.com"</li>
</ul>


<h4>Description:</h4>

<p>The default RHN server to use for registration via the included RHN/Satellite/Spacewalk registration scripts as well as the authn_spacewalk authentication module.</p>

<p>Please refer to the <a href="/manuals/2.6.0/5/2/4_-_Spacewalk.html">Spacewalk Authentication</a> section for more details.</p>

<h3>redhat_management_type</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "off"</li>
</ul>


<h4>Description:</h4>

<p>When using a Red Hat management platform in addition to Cobbler, this option is used to speficy the type of RHN server being used:</p>

<pre>
"off"    : I'm not using Red Hat Network, Satellite, or Spacewalk
"hosted" : I'm using Red Hat Network
"site"   : I'm using Red Hat Satellite Server or Spacewalk
</pre>


<p>Please refer to the <a href="/manuals/2.6.0/Appendix/C_-_Tips_for_RHN.html">Tips For RHN</a> section for more details.</p>

<h3>register_new_installs</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 0</li>
</ul>


<h4>Description:</h4>

<p>If enabled, this allows <code>/usr/bin/cobbler-register</code> (part of the koan package) to be used to remotely add new cobbler system records to cobbler. This effectively allows for registration of new hardware from system records, even during the build process when building a system based only on a profile.</p>

<p>Please refer to the <a href="/manuals/2.6.0/4/8_-_Auto-Registration.html">Automatic Registration</a> section for more details.</p>

<h3>remove_old_puppet_certs_automatically</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 0</li>
</ul>


<h4>Description:</h4>

<p>If enabled when using Puppet integration, Cobbler can be triggered (through the use of snippets) to automatically remove CA certificates for a given FQDN. This prevents failed Puppet registrations when a conflicting cert already exists.</p>

<p>Please refer to the <a href="/manuals/2.6.0/4/3/2_-_Puppet_Integration.html">Puppet Integration</a> section for more details.</p>

<h3>replicate_rsync_options</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "-avzH"</li>
</ul>


<h4>Description:</h4>

<p>This setting is used to specify additional options that are passed to the rsync command during the replicate process.</p>

<p>Please refer to the <a href="/manuals/2.6.0/3/2/8_-_Replication.html">Replicate</a> section for more details.</p>

<h3>reposync_flags</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "-l -n -d"</li>
</ul>


<h4>Description:</h4>

<p>This setting is used to specify additional options that are passed to the reposync command during the reposync process. This is specific to yum, and is not used with apt or other repository types.</p>

<p>Please refer to the <a href="/manuals/2.6.0/3/2/5_-_Reposync.html">Reposync</a> section for more details.</p>

<h3>restart_dhcp</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 1</li>
</ul>


<h4>Description:</h4>

<p>If enabled, Cobbler will restart the dhcpd or dnsmasq daemon during a "cobbler sync" and after all configuration files have been generated. This will only happen when manage_dhcp is enabled.</p>

<p>Please refer to the <a href="/manuals/2.6.0/3/4/1_-_Managing_DHCP.html">Managing DHCP</a> section for more details.</p>

<h3>restart_dns</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 1</li>
</ul>


<h4>Description:</h4>

<p>If enabled, Cobbler will restart the named or dnsmasq daemon during a "cobbler sync" and after all configuration files have been generated. This will only happen when manage_dns is enabled.</p>

<p>Please refer to the <a href="/manuals/2.6.0/3/4/2_-_Managing_DNS.html">Managing DNS</a> section for more details.</p>

<h3>restart_xinetd</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 1</li>
</ul>


<h4>Description:</h4>

<p>If enabled, Cobbler will restart the xinetd daemon during a "cobbler sync" and after all configuration files have been generated.</p>

<p>Please refer to the <a href="/manuals/2.6.0/3/4/4_-_Managing_TFTP.html">Managing TFTP</a> section for more details.</p>

<h3>run_install_triggers</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 1</li>
</ul>


<h4>Description:</h4>

<p>If disabled, no install triggers (whether old-style bash or newer python-based scripts) will be run. This is an easy way to lock down cobbler if this functionality is not desired, as these scripts are run as the root user and can present a security risk.</p>

<p><strong>NOTE:</strong> Disabling this will break the "cobbler status" command, which relies on installation triggers to generate the start and stop times for the builds.</p>

<p>Please refer to the <a href="/manuals/2.6.0/4/4/1_-_Triggers.html">Triggers</a> section for more details.</p>

<h3>scm_track_enabled</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 0</li>
</ul>


<h4>Description:</h4>

<p>If enabled, Cobbler will execute a trigger for all add/edit/sync events which uses the scm_track_mode option to revision control Cobbler's data objects.</p>

<p>Please refer to the <a href="/manuals/2.6.0/4/14_-_Data_Revision_Control.html">Data Revision Control</a> section for more details.</p>

<h3>scm_track_mode</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "git"</li>
</ul>


<h4>Description:</h4>

<p>If scm_track_enabled is set to true, Cobbler will use the source control method specified by this setting to revision control data objects. Currently, only "git" and "hg" are supported.</p>

<p><strong>NOTE:</strong> Only data in <code>/var/lib/cobbler</code> is revision controlled.</p>

<p>Please refer to the <a href="/manuals/2.6.0/4/14_-_Data_Revision_Control.html">Data Revision Control</a> section for more details.</p>

<h3>serializer_pretty_json</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 0</li>
</ul>


<h4>Description:</h4>

<p>If enabled, Cobbler will "pretty-print" JSON files that are written to disk, including those for all data object types. By default, the JSON is condensed into a single line, which can make them a bit difficult to read. The trade-off is a slightly larger file per object (though this size difference is negligable).</p>

<h3>server</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "127.0.0.1"</li>
</ul>


<h4>Description:</h4>

<p>This is the address of the cobbler server. As it is used by systems during the install process, it must be the address or hostname of the system as those systems can see the server. If you have a server that appears differently to different subnets (dual homed, etc), you can use the --server option to override this value.</p>

<p>This value is also used by the cobbler CLI command, unless the client_use_localhost setting is enabled.</p>

<p>Please refer to the <a href="/manuals/2.6.0/4/7_-_Multi-Homed_Cobbler_Servers.html">Multi-Homed Cobbler Servers</a> section for more details.</p>

<h3>sign_puppet_certs_automatically</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 0</li>
</ul>


<h4>Description:</h4>

<p>If enabled when using Puppet integration, Cobbler can be triggered (through the use of snippets) to automatically register CA certificates for a given FQDN, allowing puppet to be run during the %post section of the installation without issues.</p>

<p>Please refer to the <a href="/manuals/2.6.0/4/3/2_-_Puppet_Integration.html">Puppet Integration</a> section for more details.</p>

<h3>snippetsdir</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "/var/lib/cobbler/snippets"</li>
</ul>


<h4>Description:</h4>

<p>The default directory containing Cobbler's snippets. Any snippet referenced by the $SNIPPET('') call in a template must live under this directory, for security purposes. Snippets can be located in sub-directories here to aid in organization.</p>

<h3>template_remote_kickstarts</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 0</li>
</ul>


<h4>Description:</h4>

<p>If this option is enabled and a remote (non-local) kickstart file is specified for an object, Cobbler will fetch the file contents internally and serve a templated version of the file to the client. By default, Cobbler simply passes the remote URL directly to the client.</p>

<h3>virt_auto_boot</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 1</li>
</ul>


<h4>Description:</h4>

<p>If enabled, any VM created by Koan will be set to start at boot time.</p>

<p>Please refer to the <a href="/manuals/2.6.0/6_-_Koan.html">Koan</a> section for more details.</p>

<h3>webdir</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "/var/www/cobbler"</li>
</ul>


<h4>Description:</h4>

<p>The directory in which Cobbler will write all of its distribution, repo, and other web-related data.</p>

<h3>xmlrpc_port</h3>

<ul>
<li><strong>type:</strong> Integer</li>
<li><strong>default:</strong> 25151</li>
</ul>


<h4>Description:</h4>

<p>The port on which cobblerd will listen for XMLRPC connections, in connection with the address/hostname specified in the server setting.</p>

<p>The cobbler CLI command also relies upon this option for connecting to cobblerd unless the client_use_localhost setting is enabled.</p>

<h3>yum_distro_priority</h3>

<ul>
<li><strong>type:</strong> Integer</li>
<li><strong>default:</strong> 1</li>
</ul>


<h4>Description:</h4>

<p>The default yum repo priority for repos managed by Cobbler. If different repos provide the same package name, the one with the lower priority will be used by default. The lower the priorty number, the higher the priority (1 is the highest priority).</p>

<p>This option is only valid for yum repos, and is not used for apt or other repo types.</p>

<p>Please refer to the <a href="/manuals/2.6.0/3/7_-_Package_Management_and_Mirroring.html">Package Management and Mirroring</a> section for more details.</p>

<h3>yum_post_install_mirror</h3>

<ul>
<li><strong>type:</strong> Boolean</li>
<li><strong>default:</strong> 1</li>
</ul>


<h4>Description:</h4>

<p>If enabled, Cobbler will add yum.repos.d entries for all repos allocated to a system or profile. If disabled, these repos will only be used during the build process. Normally, this option should be left enabled unless you are using other configuration management systems to configure the repos in use after the build process is complete.</p>

<h3>yumdownloader_flags</h3>

<ul>
<li><strong>type:</strong> String</li>
<li><strong>default:</strong> "--resolve"</li>
</ul>


<h4>Description:</h4>

<p>Extra flags for the yumdownloader command, which is used to pull down individual RPM files out of a yum repo.</p>

<p>Please refer to the <a href="/manuals/2.6.0/3/7_-_Package_Management_and_Mirroring.html">Package Management and Mirroring</a> section for more details.</p>

     <hr>
     <div id="disqus_thread"></div>
     <script type="text/javascript">
        /* * * CONFIGURATION VARIABLES: EDIT BEFORE PASTING INTO YOUR WEBPAGE * * */
        var disqus_shortname = 'cobbler'; // required: replace example with your forum shortname
        var disqus_identifier = '';

        /* * * DON'T EDIT BELOW THIS LINE * * */
        (function() {
            var dsq = document.createElement('script'); dsq.type = 'text/javascript'; dsq.async = true;
            dsq.src = '//' + disqus_shortname + '.disqus.com/embed.js';
            (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(dsq);
        })();
     </script>
     <noscript>Please enable JavaScript to view the <a href="http://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
     <a href="http://disqus.com" class="dsq-brlink">comments powered by <span class="logo-disqus">Disqus</span></a>


  </div>
  <div class="span4">
<div class="toc"><ul class="dirtree"><li><a href="/manuals/2.6.0/3/3/1_-_Dynamic_Settings.html">1 - Dynamic Settings</a></li><li><a href="/manuals/2.6.0/3/3/2_-_Complete_Settings_List.html">2 - Complete Settings List</a></li></ul></div>
  </div>
 </div>
</div>
<!-- end content -->

<footer>
  <div class="container">
    <div class="row-fluid sections">
      <div class="span6 footmenu">
       <div class="row-fluid">
        <div class="span3 sitemap">
         <ul class="nav nav-list">
          <li class="nav-header">Pages</li>
          <li><a href="/">Home</a></li>
          <li><a href="/blog/">Blog Posts</a></li>
          <li><a href="/about.html">About Cobbler</a></li>
         </ul>
        </div>
        <div class="span2 sitemap">
         <ul class="nav nav-list">
          <li class="nav-header">Manuals</li>
          <li><a href="/manuals/quickstart/">Quickstart</a></li>
          <li><a href="/manuals/2.8.0/">2.8.x</a></li>
          <li><a href="/manuals/2.6.0/">2.6.x</a></li>
          <li><a href="/manuals/developer/">Developer</a></li>
         </ul>
        </div>
        <div class="span3 sitemap">
         <ul class="nav nav-list">
          <li class="nav-header">Community</li>
          <li><a href="/community.html">How to Get Help</a></li>
          <li><a href="/supporters.html">Supporters</a></li>
          <li><a href="/users.html">Who's Using Cobbler</a></li>
         </ul>
        </div>
        <div class="span4 sitemap">
         <ul class="nav nav-list">
          <li class="nav-header">Github</li>
          <li><a href="https://github.com/cobbler/cobbler">Code Repository</a></li>
          <li><a href="https://github.com/cobbler/cobbler/issues">Issue Tracker</a></li>
          <li><a href="https://github.com/cobbler/cobbler/wiki">Wiki</a></li>
         </ul>
        </div>
       </div>
    <div class="row-fluid">
    </div>
    <div class="row-fluid">
     <p class="ending">Best viewed in anything but Internet Explorer&#0153; Seriously, please consider switching.</p>
     <p class="browsers">
      <a href="https://www.mozilla.org/en-US/firefox/new/"><i class="icon-firefox icon-2x"></i></a>
      <a href="https://www.google.com/intl/en/chrome/browser/"><i class="icon-chrome icon-2x"></i></a>
      <a href="http://www.opera.com/"><i class="icon-opera icon-2x"></i></a>
      <a href="http://www.apple.com/safari/"><i class="icon-safari icon-2x"></i></a>
     </p>
    </div>
      </div>
      <div class="span3 posts">
        <p class="column_header">Recent Posts:</p>

        <div class="post">
          <p class="title"><a href="/blog/2018/11/23/cobbler_2.8.4_released.md">Cobbler 2.8.4 Released</a></p>
          <p class="author">Posted by Jörgen on Friday, November 23, 2018</p>
        </div>

        <div class="post">
          <p class="title"><a href="/blog/2018/05/04/cobbler_2.8.3_released.md">Cobbler 2.8.3 Released</a></p>
          <p class="author">Posted by Jörgen on Friday, May 04, 2018</p>
        </div>

        <div class="post">
          <p class="title"><a href="/blog/2017/09/16/cobbler_2.8.2_released.html">Cobbler 2.8.2 Released</a></p>
          <p class="author">Posted by Jörgen on Saturday, September 16, 2017</p>
        </div>

        <div class="post">
          <p class="title"><a href="/blog/2017/05/24/cobbler_2.8.1_released.html">Cobbler 2.8.1 Released</a></p>
          <p class="author">Posted by Jörgen on Wednesday, May 24, 2017</p>
        </div>

      </div>
      <div class="span3 credits">
        <div class="social">
          <a href="https://twitter.com/cobblerproject" class="twitter-follow-button" data-show-count="false" data-size="large" data-dnt="true" data-width="100%">Follow @cobblerproject</a>
          <script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0];if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src="//platform.twitter.com/widgets.js";fjs.parentNode.insertBefore(js,fjs);}}(document,"script","twitter-wjs");</script>
        </div>
        <div class="attributions">
          <p class="column_header">Attributions:</p>
          <div class="attribution">"Lens Flare", by <a href="http://creativity103.com/"><img src="/images/creativity103.gif" /></a></div>
          <div class="attribution">"Gears", by <a href="http://www.flickr.com/photos/17258892@N05/">Ralph Bijker</a></div>
        </div>
        <div class="copyright">
          <p>All other content, &copy; <span id="copyyear"></span><br/>by James Cammarata</p>
          <script>$("#copyyear").text((new Date).getFullYear());</script>
        </div>
      </div>            
    </div>
  </div>
</footer>

<!-- Google Analytics -->
<script type="text/javascript">
  var _gaq = _gaq || [];
  _gaq.push(['_setAccount', 'UA-27319020-1']);
  _gaq.push(['_trackPageview']);
  (function() {
    var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;
    ga.src = ('https:' == document.location.protocol ? 'https://ssl' : 'http://www') + '.google-analytics.com/ga.js';
    var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);
  })();
</script>
<!-- Google Analytics end -->

</body>
</html>
