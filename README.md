<p><span style="font-family:Courier New,Courier,monospace">All resourses created in AWS through Terraform(<a href="https://github.com/jdmedeiros/security-onion">https://github.com/jdmedeiros/security-onion</a>)</span></p>

<h1><span style="font-family:Courier New,Courier,monospace"><span style="font-size:22px"><strong><span style="color:#000000">Logins</span></strong></span></span></h1>

<table border="1" cellpadding="1" cellspacing="1" style="width:500px">
	<tbody>
		<tr>
			<td><span style="font-family:Courier New,Courier,monospace">Instance</span></td>
			<td><span style="font-family:Courier New,Courier,monospace">Username</span></td>
			<td><span style="font-family:Courier New,Courier,monospace">Password</span></td>
		</tr>
		<tr>
			<td><span style="font-family:Courier New,Courier,monospace">Kali</span></td>
			<td><span style="font-family:Courier New,Courier,monospace">kali</span></td>
			<td><span style="font-family:Courier New,Courier,monospace">Passw0rd</span></td>
		</tr>
		<tr>
			<td><span style="font-family:Courier New,Courier,monospace">Sift</span></td>
			<td><span style="font-family:Courier New,Courier,monospace">sansforensics</span></td>
			<td><span style="font-family:Courier New,Courier,monospace">forensics</span></td>
		</tr>
		<tr>
			<td><span style="font-family:Courier New,Courier,monospace">REMnux</span></td>
			<td><span style="font-family:Courier New,Courier,monospace">remnux</span></td>
			<td><span style="font-family:Courier New,Courier,monospace">malware</span></td>
		</tr>
		<tr>
			<td><span style="font-family:Courier New,Courier,monospace">Onion</span></td>
			<td><span style="font-family:Courier New,Courier,monospace">ubuntu</span></td>
			<td><span style="font-family:Courier New,Courier,monospace">Passw0rd</span></td>
		</tr>
	</tbody>
</table>

<h1><span style="font-family:Courier New,Courier,monospace"><span style="font-size:22px"><strong><span style="color:#000000">FTP</span></strong></span></span></h1>

<h2><span style="font-family:Courier New,Courier,monospace"><span style="font-size:11pt"><span style="color:#000000">Server</span></span></span></h2>

<pre>
<code class="language-bash">sudo apt-get update
sudo apt-get -y upgrade
sudo apt-get install vsftpd
sudo nano /etc/vsftpd.conf</code></pre>

<p>Change this line:</p>

<pre>
<code class="language-markdown">chroot_local_user=YES</code></pre>

<p>Add these lines at the end of the file:</p>

<pre>
<code class="language-markdown">allow_writeable_chroot=YES
pasv_enable=YES
pasv_min_port=1024
pasv_max_port=1048
write_enable=YES</code></pre>

<p><span style="font-family:Courier New,Courier,monospace">Create a user with a password.</span></p>

<p><span style="font-family:Courier New,Courier,monospace">Create a shared directory for the user.</span></p>

<pre>
<code class="language-bash">sudo mkdir /home/&lt;user&gt;/&lt;folder&gt;</code></pre>

<p><span style="font-family:Courier New,Courier,monospace">Change it&#39;s ownership</span></p>

<pre>
<code class="language-bash">sudo chmod a-w /home/&lt;user&gt;/&lt;folder&gt;</code></pre>

<p>&nbsp;</p>

<h2><span style="font-family:Courier New,Courier,monospace"><span style="font-size:11pt"><span style="color:#000000">Client</span></span></span></h2>

<p><span style="font-family:Courier New,Courier,monospace">Using filezilla, add a new connection and make sure that transfer mode is in passive.</span></p>

<p>&nbsp;</p>

<p>Catching FTP credentials with wireshark</p>

<p><img src="https://ckeditor.com/apps/ckfinder/userfiles/files/mstsc_G74ANxvPB4.png" style="height:982px; width:1654px" /></p>

<h1><span style="font-size:22px"><strong><span style="font-family:Courier New,Courier,monospace">MIB and SNMP</span></strong></span></h1>

<p><span style="font-family:Courier New,Courier,monospace"><span style="font-size:11pt"><span style="color:#000000">Server</span></span></span></p>

<pre>
<code class="language-bash">sudo apt-get update

sudo apt-get install snmpd

sudo nano /etc/snmp/snmpd.conf</code></pre>

<pre>
<code class="language-markdown">agentAddress udp:161,udp6:[::1]:161</code></pre>

<pre>
<code>sudo service snmpd restart</code></pre>

<p><span style="font-family:Courier New,Courier,monospace"><span style="font-size:11pt"><span style="color:#000000">Client/Installing agent</span></span></span></p>

<pre>
<code>sudo apt install snmpd snmp libsnmp-dev</code></pre>

<pre>
<code>sudo nano /etc/snmp/snmpd.conf</code></pre>

<pre>
<code class="language-markdown">agentAddress udp:161
rocommunity public 10.0.0.13 //Tag the other rocommunities</code></pre>

<pre>
<code class="language-bash">sudo service snmpd restart</code></pre>

<p>&nbsp;</p>

<h1><span style="font-size:22px"><span style="font-family:Courier New,Courier,monospace">Syslog</span></span></h1>

<p><span style="font-family:Courier New,Courier,monospace"><span style="font-size:11pt"><span style="color:#000000">Server</span></span></span></p>

<p>Download ManageEngine Eventviewer</p>

<p>Start service</p>

<pre>
<code class="language-bash">service eventloganalyzer start </code></pre>

<p><span style="font-family:Courier New,Courier,monospace"><span style="font-size:11pt"><span style="color:#000000">Client</span></span></span></p>

<pre>
<code class="language-bash">sudo apt-get install rsyslog</code></pre>

<pre>
<code class="language-bash">nano /etc/rsyslog.conf </code></pre>

<pre>
<code class="language-markdown">*.* @&lt;ip&gt;:514</code></pre>

<pre>
<code class="language-bash">systemctl restart rsyslog</code></pre>

<p>&nbsp;</p>

<p><span style="font-size:22px"><span style="font-family:Courier New,Courier,monospace">NTP</span></span></p>

<p>Stop OS NTP Service.</p>

<pre>
<code>sudo systemctl stop ntp</code></pre>

<p><span style="font-family:Courier New,Courier,monospace"><span style="font-size:11pt"><span style="color:#000000">Server</span></span></span></p>

<p><span style="font-family:Courier New,Courier,monospace"><span style="font-size:11pt"><span style="color:#000000">Install chrony and start it.</span></span></span></p>

<pre>
<code class="language-bash">sudo apt-get install chrony
sudo systemctl start chrony
sudo systemctl enable chrony
sudo systemctl status chrony</code></pre>

<p>&nbsp;</p>

<p>Chrony&#39;s configuration</p>

<pre>
<code class="language-bash">sudo nano /etc/chrony/chrony.conf</code></pre>

<pre>
<code class="language-markdown">pool 0.pt.pool.ntp.org iburst
allow 192.168.1.0/24 // example</code></pre>

<p>NTP Pools: <a href="https://www.pool.ntp.org/zone/pt">https://www.pool.ntp.org/zone/pt</a></p>

<p>The <code>iburst</code> option is used with the <code>server</code> directive to specify that Chrony should make an initial burst of four messages to the specified NTP server when it starts up, rather than the usual single message. The <code>iburst</code> option is intended to help Chrony quickly synchronize with the server and reduce the time it takes for the local clock to converge with the server&#39;s clock.</p>

<p>The <code>allow</code> option takes one or more IP address or network address/netmask pairs as arguments, separated by spaces. Each IP address or network address specifies the hosts that are allowed to send NTP requests to the Chrony server. By default, Chrony only accepts NTP requests from the loopback address (127.0.0.1/8 or ::1/128), but the <code>allow</code> option can be used to specify additional hosts.</p>

<pre>
<code class="language-bash">timedatectl set-ntp true
sudo systemctl restart chrony</code></pre>

<p><span style="font-family:Courier New,Courier,monospace"><span style="font-size:11pt"><span style="color:#000000">Client</span></span></span></p>

<pre>
<code class="language-bash">sudo systemctl stop ntp
sudo apt-get install chrony
sudo systemctl start chrony
sudo systemctl enable chrony
sudo nano /etc/chrony/chrony.conf</code></pre>

<p>Add the following:</p>

<pre>
<code class="language-markdown">server 10.0.0.13 // Server to sync
server master iburst</code></pre>

<p>&nbsp;Remove all the pools.</p>

<p>Uncomment this line:</p>

<pre>
<code>log tracking measurements statistics</code></pre>

<p>Comment these lines:</p>

<pre>
<code class="language-markdown">#confdir /etc/chrony/conf.d
#sourcedir /run/chrony-dhcp
#sourcedir /etc/chrony/sources.d
#leapsectz right/UTC</code></pre>

<p>&nbsp;Troubleshooting</p>

<pre>
<code class="language-bash">timedatectl set-ntp true
sudo systemctl restart chrony</code></pre>

<p>&nbsp;</p>
