# CyberPanel
Centos 7
<h2>Install & Konfigurasi Cyberpanel</h2>
<p>1. Centos 7.x
<p>2. Install python 2.7
<pre># yum install gcc openssl-devel bzip2-devel</pre>
<pre># cd /usr/src
# wget https://www.python.org/ftp/python/2.7.15/Python-2.7.15.tgz</pre>
<pre>#tar xzf Python-2.7.15.tgz</pre>
<pre>#cd Python-2.7.15
# ./configure --enable-optimizations
# make altinstall</pre>
<pre># /usr/local/bin/python2.7 -V
Python 2.7.15</pre>
<p>3. Install PIP
<pre># curl "https://bootstrap.pypa.io/get-pip.py" -o "get-pip.py"
# python2.7 get-pip.py</pre>

<pre># yum update</pre>
Disabled terlebih dahulu SELinux sementara
<pre># nano /etc/sysconfig/selinux</pre>
# Install CyberPanel
<pre># sh <(curl https://cyberpanel.net/install.sh || wget -O - https://cyberpanel.net/install.sh)</pre>
<h2>Konfigurasi Cyberpanel</h2>
<p>Private Name Server
