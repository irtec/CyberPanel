# CyberPanel
Centos 7
<h2>Install & Konfigurasi Cyberpanel</h2>
<p>1. Centos 7.x
<pre># yum update</pre>
Disabled terlebih dahulu SELinux sementara
<pre># nano /etc/sysconfig/selinux</pre>
<img src="https://raw.githubusercontent.com/irtec/CyberPanel/master/selinux.jpeg" style="width:104px;height:142px;">

# Install CyberPanel
<pre># sh <(curl https://cyberpanel.net/install.sh || wget -O - https://cyberpanel.net/install.sh)</pre>
<h2>Konfigurasi Cyberpanel</h2>

# Private Name Server
<p>DNS > Create Nameserver
<img src="https://raw.githubusercontent.com/irtec/CyberPanel/master/ns.jpeg" style="width:104px;height:142px;">
