--- 
layout: post
title: Enabling Dynamically Configured Name-based Virtual Hosting on Mac OS X
created: 1080529593
categories: 
- mac os x
- apache
- VirtualHost
- mod_vhost_alias
- Mac
- Web Development
---
<p>
	Enabling virtual hosting on your Mac OS X machine will allow you to serve web content from a single IP address for multiple domain names, including sub-domains. This is useful for having a local development environment on your laptop, as you never need to edit your web server config files, just create additional folders matching the site names you want to work with.</p>
<p>
	<em>Note: the original version of this document was created for pre-Leopard Mac OS X versions. See the <a href="http://bmannconsulting.com/node/1005/revisions/1973/view" title="Mac OS X 10.4 and earlier mass virtual hosting">previous revision here</a>. This version references Apache 2.2 on Mac OS X Leopard, and recommends editing the hosts file rather than using NetInfo.</em></p>
<!--break-->
<p>
	All the following involves editing Apache server config files, which requires admin privileges. They are located at <code>/etc/apache2/httpd.conf</code> (main config file) and <code>/etc/apache2/extras/httpd-vhosts.conf</code> (file that is included, keep all your virtual host related config here), and it&#39;s best to make a backup before you begin (just copy the original with a new extension like &quot;bak&quot;, e.g. <code>/etc/apache2/httpd.conf.bak</code>).</p>
<p>
	First, you need to uncomment the sections related to virtual host aliasing in your main httpd.conf file, by deleting the # in front of the following lines:</p>
<pre class="code">
#LoadModule vhost_alias_module libexec/httpd/mod_vhost_alias.so
#AddModule mod_vhost_alias.c
</pre>
<p>
	You&#39;ll also need to uncomment the include which will pull in the next file, again by removing the # from in front of Include.</p>
<pre class="code">
# Virtual hosts
#Include /private/etc/apache2/extra/httpd-vhosts.conf
</pre>
<p>
	Decide where you want to put all your web files. I placed them all in a directory next to the main, default server, at <code>/Library/WebServer/Hosts</code>. Create that directory.</p>
<p>
	Now add this snippet at the end of the <code>/etc/apache2/extras/httpd-vhosts.conf</code> file:</p>
<pre class="code">
#allow access to the Hosts directory where your sites are
&lt;Directory &quot;/Library/WebServer/Hosts&quot;&gt;
Options Indexes FollowSymLinks MultiViews
AllowOverride All
#you could configure the following to only allow access from localhost
Order allow,deny
Allow from all
&lt;/Directory&gt;

#get the server name from the Host: header
UseCanonicalName Off
VirtualDocumentRoot /Library/WebServer/Hosts/%0/html
</pre>
<p>
	Now restart your web server with the command <code>apachectl graceful</code> If you don&#39;t see any errors, everything should be working.</p>
<p>
	At this point, you should be able to add folders like /Library/WebServer/Hosts/example.bmannconsulting.com/html and you&#39;re good to go. You can also use symlinks, so have multiple domains point to the same content. Remember, you either need to have DNS for the domain set up correctly or edit your hosts file at <code>/etc/hosts</code>. An example of that would be adding a line like <code>127.0.0.0.1&nbsp;&nbsp;&nbsp;&nbsp;example.local</code> to the end of the file -- it&#39;s corresponding web directory would then be <code>/Library/WebServer/Hosts/example.local/html</code>.</p>
<p>
	Note: For those developing Drupal multisite, any additional sites you want to develop on the same codebase, just symlink to your base Drupal install. So, if your base install is at base.example.local, and you want to create newsite.example.local, symlink <code>/Library/WebServer/Hosts/newsite.example.local</code> to <code>/Library/WebServer/Hosts/base.example.local</code>. You will still need to create the directory for the newsite at <code>/Library/WebServer/Hosts/base.example.local/html/sites/newsite.example.local</code> for Drupal to properly pick it up.</p>
<p>
	<strong>Related Links</strong></p>
<ul>
	<li>
		<a href="http://httpd.apache.org/docs/2.2/vhosts/mass.html">Apache.org: Dynamically configured mass virtual hosting</a></li>
	<li>
		<a href="http://httpd.apache.org/docs/2.2/mod/mod_vhost_alias.html">Apache.org: Advanced directory matching for virtual and IP based hosting using mod_vhost_alias</a></li>
</ul>
