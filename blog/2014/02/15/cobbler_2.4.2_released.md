<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en-us">
<head>
   <meta http-equiv="content-type" content="text/html; charset=utf-8" />
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <meta name="author" content="Cobbler development team" />

   <title>Cobbler 2.4.2 Released</title>

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
<div class="container">
 <div class="row-fluid">
  <div class="span9">
   <div class="row-fluid">
    <ul class="pager">
     
     <li class="previous"><a href="/blog/2014/03/09/cobbler_2.4.3_released.html"><i class="icon-angle-left"></i> Cobbler 2.4.3 Released</i></a></li>
     
     
     <li class="next"><a href="/blog/2014/02/03/cobbler_2.4.1_released.html">Cobbler 2.4.1 Released <i class="icon-angle-right"></i></a></li>
     
    </ul>
   </div>
   <div class="row-fluid posts">
    <div class="post">
     <h2 class="header">Cobbler 2.4.2 Released</h2>
     <div class="author"><i>Posted by Jörgen on Saturday, February 15, 2014</i></div>
     <div class="content"><p>Cobbler 2.4.2 is now officially available!</p>

<p>Improved Features:</p>

<ul>
<li>Add support for SLES 10 sp4 to distro_signatures</li>
</ul>


<p>Bugfixes:</p>

<ul>
<li>Major bugfix in distro detection routine for RHEL &amp; SuSE systems</li>
<li>Corrected AutoYaST XML generation when scripts are included</li>
<li>Fix elilo and yaboot filenames in dhcp configuration</li>
</ul>


<p>The (source) release can be found at: <a href="https://github.com/cobbler/cobbler/releases/tag/v2.4.2">https://github.com/cobbler/cobbler/releases/tag/v2.4.2</a></p>
</div>
     <div class="goback"><a href='/blog/page5/'><i class='icon-double-angle-left'></i> go back</a></div>
     <hr>
     <div id="disqus_thread"></div>
     <script type="text/javascript">
        /* * * CONFIGURATION VARIABLES: EDIT BEFORE PASTING INTO YOUR WEBPAGE * * */
        var disqus_shortname = 'cobbler'; // required: replace example with your forum shortname
        var disqus_identifier = '/posts/2014/02/15/cobbler_2.4.2_released';

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
   </div>
  </div>
  <div class="span3">
  <div class='posts related_by_date'><h4 class='header'>February, 2014</h4><div class='post'><div class='content current'>Cobbler 2.4.2 Released</div><div class='author'><i>Posted on February 15, 2014</i></div></div><div class='post'><div class='content current'><a href='/blog/2014/02/03/cobbler_2.4.1_released.html'>Cobbler 2.4.1 Released</a></div><div class='author'><i>Posted on February 03, 2014</i></div></div></div>
  </div>
 </div>
</div>


</div> <!-- end wrap -->

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
