<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en-us">
<head>
   <meta http-equiv="content-type" content="text/html; charset=utf-8" />
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <meta name="author" content="Cobbler development team" />

   <title>Command Line Search</title>

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
<ul class="breadcrumb"><li><a href="/manuals">manuals</a> <span class="divider">/</span></li><li><a href="/manuals/2.6.0">2.6.0</a> <span class="divider">/</span></li><li><a href="/manuals/2.6.0/3_-_General_Topics.html">3</a> <span class="divider">/</span></li><li><a href="/manuals/2.6.0/3/2_-_Cobbler_Direct_Commands.html">2</a> <span class="divider">/</span></li><li class="active">Command Line Search</li></ul>
   <h1>Command Line Search</h1>
<p>Command line search can be used to ask questions about your cobbler
configuration, rather than just having to run "cobbler list" or
"cobbler report" and scanning through the results. (The
<a href="Cobbler%20Web%20Interface">Cobbler Web Interface</a> also
supports search/filtering, for those that want to use it, though
that is not documented on this page)</p>

<p>Command line search works on all distro/profile/system/and repo
objects.</p>

<pre><code>cobbler distro find --help
cobbler profile find --help
cobbler system find --help
cobbler repo find --help
</code></pre>

<p>NOTE: Some of these examples are kind of arbitrary. I'm sure you
can think of some more real world examples.</p>

<h2>Examples</h2>

<p>Find what system record has a given mac address.</p>

<pre><code>    cobbler system find --mac=AA:BB:CC:DD:EE:FF
</code></pre>

<p>If anything is using a certain kernel, delete that object and all
it's children (profiles, systems, etc).</p>

<pre><code>    cobbler distro find --kernel=/path/to/kernel | xargs -n1 --replace cobbler distro remove --name={} --recursive
</code></pre>

<p>What profiles use the repo "epel-5-i386-testing" ?</p>

<pre><code>    cobbler profile find --repos=epel-5-i386-testing
</code></pre>

<p>Which profiles are owned by neo AND mranderson?</p>

<pre><code>   cobbler profile find --owners="neo,mranderson"
   # lists need to be comma delimited, like this, with no unneeded spaces
</code></pre>

<p>What systems are set to pass the kernel argument "color=red" ?</p>

<pre><code>   cobbler system find --kopts="color=red"
</code></pre>

<p>What systems are set to pass the kernel argument "color=red" and
"number=5" ?</p>

<pre><code>   cobbler system find --kopts="color=red number=5"
   # space delimited key value pairs
   # key1=value1 key2 key3=value3
</code></pre>

<p>What systems set the kickstart metadata variable of foo to the
value 'bar' ?</p>

<pre><code>   cobbler system find --ksmeta="foo=bar"
   # space delimited key value pairs again
</code></pre>

<p>What systems are set to netboot disabled?</p>

<pre><code>   cobbler system find --netboot-enabled=0
   # note, this also accepts 'false', or 'no'
</code></pre>

<p>For all systems that are assigned to profile "foo" that are set to
netboot disabled, enable them.</p>

<pre><code>   cobbler system find --profile=foo --netboot-enabled=0 | xargs -n1 --replace cobbler system edit --name={} --netboot-enabled=1
   # demonstrates an "AND" query combined with xargs usage.
</code></pre>

<h2>A Note About Types And Wildcards</h2>

<p>Though the cobbler objects behind the scenes store data in various
different formats (booleans, hashes, lists, strings), it all works
fom the command line as text.</p>

<p>If multiple terms are specified to one argument, the search is an
"AND" search.</p>

<p>If multiple parameters are specified, the search is still an "AND"
search.</p>

<p>The find command understands patterns such as "*" and "?". This is
supported using Python's fnmatch.</p>

<p>To learn more:</p>

<pre><code>pydoc fnmatch.fnmatch
</code></pre>

<p>All systems starting with the string foo:</p>

<pre><code>cobbler system find --name="foo*"
</code></pre>

<p>This is rather useful when combined with xargs. This is a rather
tame example, reporting on all systems starting with "TEST".</p>

<pre><code>cobbler system find --name="TEST*" | xargs -n1 --replace cobbler system 
report --name={}
</code></pre>

<p>By extension, you could use this to toggle the --netboot-enabled
systems of machines with certain hostnames, mac addresses, and so
forth, or perform other kinds of wholesale edits (for instance,
deletes, or assigning profiles with certain names to new distros
when upgrading them from F8 to F9, for instance).</p>

<h2>API Usage</h2>

<p>All of this functionality is also exposed through the API</p>

<pre><code>#!/usr/bin/python
import cobbler.api as capi
api_handle = capi.BootAPI()
matches = api_handle.find_profile(name="TEST*",return_list=True)
print matches
</code></pre>

<p>You will find uses of ".find()" throughout the cobbler code that
make use of this behavior.</p>

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
<div class="toc"><ul class="dirtree"><li><a href="/manuals/2.6.0/3/2/1_-_Check.html">1 - Check</a></li><li><a href="/manuals/2.6.0/3/2/2_-_Sync.html">2 - Sync</a></li><li><a href="/manuals/2.6.0/3/2/3_-_Distro_Signatures.html">3 - Distro Signatures</a></li><li><a href="/manuals/2.6.0/3/2/4_-_Import.html">4 - Import</a></li><li><a href="/manuals/2.6.0/3/2/5_-_Reposync.html">5 - Reposync</a></li><li><a href="/manuals/2.6.0/3/2/6_-_Build_ISO.html">6 - Build ISO</a></li><li><a href="/manuals/2.6.0/3/2/7_-_Command_Line_Search.html">7 - Command Line Search</a></li><li><a href="/manuals/2.6.0/3/2/8_-_Replication.html">8 - Replication</a></li><li><a href="/manuals/2.6.0/3/2/9_-_Validate_Kickstart.html">9 - Validate Kickstart</a></li><li><a href="/manuals/2.6.0/3/2/10_-_ACL_Setup.html">10 - ACL Setup</a></li><li><a href="/manuals/2.6.0/3/2/11_-_Dynamic_Settings.html">11 - Dynamic Settings</a></li><li><a href="/manuals/2.6.0/3/2/12_-_Version.html">12 - Version</a></li></ul></div>
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
