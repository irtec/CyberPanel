# CyberPanel
Centos 7
<h2>Install & Konfigurasi Cyberpanel</h2>
<p>1. Centos 7.x
<p>2. Install python 2.7
<br>
<pre>yum update</pre>
Disabled terlebih dahulu SELinux sementara
<pre>nano /etc/sysconfig/selinux</pre>
Install CyberPanel
<pre>sh <(curl https://cyberpanel.net/install.sh || wget -O - https://cyberpanel.net/install.sh)</pre>
<h2>Konfigurasi Cyberpanel</h2>
<p>Private Name Server
