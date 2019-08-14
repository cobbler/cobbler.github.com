<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en-us">
<head>
   <meta http-equiv="content-type" content="text/html; charset=utf-8" />
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <meta name="author" content="Cobbler development team" />

   <title>SELinux With Cobbler</title>

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
<ul class="breadcrumb"><li><a href="/manuals">manuals</a> <span class="divider">/</span></li><li><a href="/manuals/2.6.0">2.6.0</a> <span class="divider">/</span></li><li><a href="/manuals/2.6.0/4_-_Advanced_Topics.html">4</a> <span class="divider">/</span></li><li class="active">SELinux With Cobbler</li></ul>
   <h1>SELinux With Cobbler</h1>
<p>SELinux policies are typically provided by the upstream distribution (Fedora, Ubuntu, etc.). As new features are added to cobbler (and we do add new features frequently), those policies may become out-of-date leading to AVC denials and other problems. If you wish to run SELinux on your cobbler system, we expect you to know how to write policy and resolve AVCs.</p>

<p>Below are some of the more common issues you may run into with this release.</p>

<h2>ProtocolError: &lt;ProtocolError for x.x.x.x:80/cobbler_api: 503 Service Temporarily Unavailable&gt;</h2>

<p>If you see this when you run "cobbler check" or any other cobbler command, it means SELinux is blocking httpd from talking with cobblerd. The command to fix this is:</p>

<p><figure class="highlight"><pre><code class="language-bash" data-lang="bash">$ sudo setsebool -P httpd_can_network_connect true</code></pre></figure></p>

<h2>Fedora 16 / RHEL6 / CentOS6 - Python MemoryError</h2>

<p>When starting cobblerd for the first time (or after upgrading to 2.2.x), you may see a stack trace like the following:</p>

<p><figure class="highlight"><pre><code class="language-bash" data-lang="bash">Starting cobbler daemon: Traceback (most recent call last):
File &quot;/usr/bin/cobblerd&quot;, line 76, in main
api = cobbler_api.BootAPI(is_cobblerd=True)
File &quot;/usr/lib/python2.6/site-packages/cobbler/api.py&quot;, line 127, in init
module_loader.load_modules()
File &quot;/usr/lib/python2.6/site-packages/cobbler/module_loader.py&quot;, line 62, in load_modules
blip = import(&quot;modules.%s&quot; % ( modname), globals(), locals(), [modname])
File &quot;/usr/lib/python2.6/site-packages/cobbler/modules/authn_pam.py&quot;, line 53, in
from ctypes import CDLL, POINTER, Structure, CFUNCTYPE, cast, pointer, sizeof
File &quot;/usr/lib64/python2.6/ctypes/init.py&quot;, line 546, in
CFUNCTYPE(c_int)(lambda: None)
MemoryError</code></pre></figure></p>

<p>This error is caused by SELinux blocking python ctypes. To resolve this, you can use audit2allow to enable the execution of temp files or you can remove the authn_pam.py module from the site-packages/cobbler/modules/ directory (as long as you're not using PAM authentication for the Web UI).</p>

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
<div class="toc"><ul class="dirtree"><li><a href="/manuals/2.6.0/4/1_-_Advanced_Networking.html">1 - Advanced Networking</a></li><ul class="dirtree"><li><a href="/manuals/2.6.0/4/1/1_-_Bonding.html">1.1 - Bonding</a></li><li><a href="/manuals/2.6.0/4/1/2_-_VLANs.html">1.2 - VLANs</a></li><li><a href="/manuals/2.6.0/4/1/3_-_Bridging.html">1.3 - Bridging</a></li><li><a href="/manuals/2.6.0/4/1/4_-_Bonded_Bridging.html">1.4 - Bonded Bridging</a></li></ul><li><a href="/manuals/2.6.0/4/2_-_SELinux.html">2 - SELinux</a></li><li><a href="/manuals/2.6.0/4/3_-_Configuration_Management.html">3 - Configuration Management</a></li><ul class="dirtree"><li><a href="/manuals/2.6.0/4/3/1_-_Built-In_Configuration_Management.html">3.1 - Built-In Configuration Management</a></li><li><a href="/manuals/2.6.0/4/3/2_-_Puppet_Integration.html">3.2 - Puppet Integration</a></li><li><a href="/manuals/2.6.0/4/3/3_-_Func_Integration.html">3.3 - Func Integration</a></li></ul><li><a href="/manuals/2.6.0/4/4_-_Extending_Cobbler.html">4 - Extending Cobbler</a></li><ul class="dirtree"><li><a href="/manuals/2.6.0/4/4/1_-_Triggers.html">4.1 - Triggers</a></li><li><a href="/manuals/2.6.0/4/4/2_-_Modules.html">4.2 - Modules</a></li><li><a href="/manuals/2.6.0/4/4/3_-_Extending_Cheetah.html">4.3 - Extending Cheetah</a></li></ul><li><a href="/manuals/2.6.0/4/5_-_Power_Management.html">5 - Power Management</a></li><li><a href="/manuals/2.6.0/4/6_-_Alternative_Template_Formats.html">6 - Alternative Template Formats</a></li><li><a href="/manuals/2.6.0/4/7_-_Multi-Homed_Cobbler_Servers.html">7 - Multi-Homed Cobbler Servers</a></li><li><a href="/manuals/2.6.0/4/8_-_Auto-Registration.html">8 - Auto-Registration</a></li><li><a href="/manuals/2.6.0/4/9_-_Batch_Editing.html">9 - Batch Editing</a></li><li><a href="/manuals/2.6.0/4/10_-_Moving_to_a_New_Server.html">10 - Moving to a New Server</a></li><li><a href="/manuals/2.6.0/4/11_-_PXE-boot_Menu_Passwords.html">11 - PXE-boot Menu Passwords</a></li><li><a href="/manuals/2.6.0/4/12_-_Alternative_Storage_Backends.html">12 - Alternative Storage Backends</a></li><ul class="dirtree"><li><a href="/manuals/2.6.0/4/12/1_-_CouchDB.html">12.1 - CouchDB</a></li><li><a href="/manuals/2.6.0/4/12/2_-_MongoDB.html">12.2 - MongoDB</a></li><li><a href="/manuals/2.6.0/4/12/3_-_MySQL.html">12.3 - MySQL</a></li></ul><li><a href="/manuals/2.6.0/4/13_-_Using_gPXE.html">13 - Using gPXE</a></li><li><a href="/manuals/2.6.0/4/14_-_Data_Revision_Control.html">14 - Data Revision Control</a></li></ul></div>
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
