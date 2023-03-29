<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">Logins</span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">Kali:</span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">User: kali</span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">Password: Passw0rd</span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">Sift:</span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">User:</span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">Password:</span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">REMnux:</span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">User:</span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">Password:</span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">Onion:</span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">User:</span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">Password:</span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">FTP</span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">Server:</span></span></span></p>

<p style="margin-left:48px"><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">sudo apt-get update &amp;&amp; sudo apt-get -y upgrade</span></span></span></p>

<p style="margin-left:48px"><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">sudo nano /etc/vsftpd.conf /etc/vsftpd.conf</span></span></span></p>

<p style="margin-left:48px"><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">Create user and password</span></span></span></p>

<p style="margin-left:48px"><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">Create dir for user and change it&rsquo;s ownership</span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">Client:</span></span></span></p>

<p>&nbsp;</p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">Server configuration:</span></span></span></p>

<p>&nbsp;</p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">chroot_local_user=YES</span></span></span></p>

<p><br />
&nbsp;</p>

<p style="margin-left:96px"><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">allow_writeable_chroot=YES</span></span></span></p>

<p style="margin-left:96px"><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">pasv_enable=YES</span></span></span></p>

<p style="margin-left:96px"><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">pasv_min_port=1024</span></span></span></p>

<p style="margin-left:96px"><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">pasv_max_port=1048</span></span></span></p>

<p style="margin-left:96px"><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">write_enable=YES</span></span></span></p>

<p>&nbsp;</p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">MIB/SNMP</span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">sudo apt-get update</span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">sudo apt-get install snmp-mibs-downloader</span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">sudo apt-get install snmp</span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">sudo systemctl restart snmpd</span></span></span></p>

<p><br />
<br />
&nbsp;</p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000"><img src="https://lh4.googleusercontent.com/9gUjY20McsX0aiz--p8b9mxpxMjdGishmT6vf07FndsMRc4CTofs1hHvLMhMqRwko0obiuhYcq9khN3p3jsDrInbRGUxhgMpL1yCnZU48d3xUq5BqS2USe40e7lgg6EtR8VdY1SV5bycF1d2TVVBqeI" style="height:296px; width:624px" /></span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">Syslog</span></span></span></p>

<p>&nbsp;</p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">Server configuration</span></span></span></p>

<p style="margin-left:48px"><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">sudo apt-get update</span></span></span></p>

<p style="margin-left:48px"><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">sudo apt-get install rsyslog</span></span></span></p>

<p style="margin-left:48px"><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">sudo nano /etc/rsyslog.conf</span></span></span></p>

<p>&nbsp;</p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">Client configuration</span></span></span></p>

<p style="margin-left:48px"><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">sudo apt-get update</span></span></span></p>

<p style="margin-left:48px"><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">sudo apt-get install rsyslog</span></span></span></p>

<p style="margin-left:48px"><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">sudo nano /etc/rsyslog.conf</span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">*.* &nbsp; @remote-syslog-server:port</span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">sudo service rsyslog restart</span></span></span></p>

<p>&nbsp;</p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">Testing</span></span></span></p>

<p><span style="font-size:11pt"><span style="font-family:Arial"><span style="color:#000000">sudo tail -f /var/log/syslog</span></span></span></p>

<p>&nbsp;</p>
