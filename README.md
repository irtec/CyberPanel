# CyberPanel
Centos 7
<h2>Install & Konfigurasi Cyberpanel</h2>
<p>1. Centos 7.x
<pre># yum update</pre>
Disabled terlebih dahulu SELinux sementara
<pre># nano /etc/sysconfig/selinux</pre>
<img src="https://raw.githubusercontent.com/irtec/CyberPanel/master/selinux.jpeg">

# Install CyberPanel
<pre># sh <(curl https://cyberpanel.net/install.sh || wget -O - https://cyberpanel.net/install.sh)</pre>
<h2>Konfigurasi Cyberpanel</h2>

<b>Private Name Server</b>
DNS > Create Nameserver
<img src="https://raw.githubusercontent.com/irtec/CyberPanel/master/ns.jpeg">
<b>private nameserver (Provider Domain)</b>
<br>
<img src="https://raw.githubusercontent.com/irtec/CyberPanel/master/PNS.jpeg">
<br>
Daftarkan kedua nameserver yang telah kamu buat pada server
<br>
<img src="https://raw.githubusercontent.com/irtec/CyberPanel/master/RegNS.jpeg">

# Add Domain
<b>Websites > Create Website
<br>
<img src="https://raw.githubusercontent.com/irtec/CyberPanel/master/adddom.jpeg">

# Manage DNS
<b>DNS > Add / Delete Records
<br>
<img src="https://raw.githubusercontent.com/irtec/CyberPanel/master/addrec.jpeg">
Tambahkan records di bawah ini dan sesuaikan
<pre>mail    3600    IPServerKamu</pre>
<pre>www    3600     daengweb.id</pre>
<pre>daengweb.id   3600   10   mail.daengweb.id</pre>
<br>
Ganti nameserver pada panel domain dengan target nameserver yang telah kita buat sebelumnya
