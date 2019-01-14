# CyberPanel
Centos 7
<h2>Install & Konfigurasi Cyberpanel</h2>
<p>1. Centos 7.x
<pre># yum update</pre>
Disabled terlebih dahulu SELinux sementara
<img src="https://raw.githubusercontent.com/irtec/CyberPanel/master/selinux.jpeg" style="width:104px;height:142px;">

<pre># nano /etc/sysconfig/selinux</pre>
# Install CyberPanel
<pre># sh <(curl https://cyberpanel.net/install.sh || wget -O - https://cyberpanel.net/install.sh)</pre>
<h2>Konfigurasi Cyberpanel</h2>
<p>Private Name Server
<img src="https://raw.githubusercontent.com/irtec/CyberPanel/master/ice_screenshot_20181230-142702.jpeg" style="width:104px;height:142px;">
