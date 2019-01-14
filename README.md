# CyberPanel
Centos 7
<h2>Install & Konfigurasi Cyberpanel</h2>
<p>1. Centos 7.x
<pre># yum update</pre>
Disabled terlebih dahulu SELinux sementara
<pre># sudo setenforce 0</pre>
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
<br>
<b>A Record
<pre>mail    3600    IPServer</pre>
<b>CNAME
<pre>www    3600     domain.pro</pre>
<b>MX
<pre>domain.pro   3600   10   mail.domain.pro</pre>
<br>
Ganti nameserver pada panel domain dengan target nameserver yang telah kita buat sebelumnya
<pre>ns1.domain.pro
ns2.domain.pro</pre>

# Install IonCube loader on OpenLiteSpeed
<b>Download Ioncube loader
<pre>wget https://downloads.ioncube.com/loader_downloads/ioncube_loaders_lin_x86-64.zip
unzip ioncube_loaders_lin_x86-64.zip</pre>

<b>Copy extension to respective PHP versions
PHP 7.0
<pre>cp ioncube/ioncube_loader_lin_7.0.so /usr/local/lsws/lsphp70/lib64/php/modules/ioncube_loader_lin_7.0.so</pre>

PHP 7.1
<pre>cp ioncube/ioncube_loader_lin_7.1.so /usr/local/lsws/lsphp71/lib64/php/modules/ioncube_loader_lin_7.1.so</pre>

PHP 7.2
<pre>cp ioncube/ioncube_loader_lin_7.2.so /usr/local/lsws/lsphp72/lib64/php/modules/ioncube_loader_lin_7.2.so</pre>

<b>Create configuration files
PHP 7.0
<pre>echo "zend_extension = /usr/local/lsws/lsphp70/lib64/php/modules/ioncube_loader_lin_7.0.so" \
    > '/usr/local/lsws/lsphp70/etc/php.d/00-ioncube.ini'</pre>

PHP 7.1
<pre>echo "zend_extension = /usr/local/lsws/lsphp71/lib64/php/modules/ioncube_loader_lin_7.1.so" \
    > '/usr/local/lsws/lsphp71/etc/php.d/00-ioncube.ini'</pre>

PHP 7.2
<pre>echo "zend_extension = /usr/local/lsws/lsphp72/lib64/php/modules/ioncube_loader_lin_7.2.so" \
    > '/usr/local/lsws/lsphp72/etc/php.d/00-ioncube.ini'</pre>

Restart OpenLiteSpeed:
<pre>systemctl restart lsws</pre>

<h2>Done!!</h2>
