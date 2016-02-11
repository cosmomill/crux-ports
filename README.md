Getting the "ports collection"
--------------------

#####Enable wip repository

The easiest way probably is to download the wip.httpup file. Just select the newest one from the repository, download it to your /etc/ports directory and update the ports tree:

<pre>
wget -O /etc/ports/wip.httpup https://raw.githubusercontent.com/cosmomill/crux-ports/master/wip.httpup
ports -u wip
</pre>

Add the new ports directory to the /etc/prt-get.conf. Place it above other port directories can override them.

<pre>
prtdir /usr/ports/wip 
</pre>

Trying packages
--------------------

Change to the package's directory:

<pre>
cd /usr/ports/wip/packagename
</pre>

Take a look at the TODO file there. If the package seems finished enough, install, and try it out:

<pre>
prt-get depinst packagename --install-scripts
</pre>
