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

sudo nano /etc/vsftpd.conf</code></pre>

<h2 style="margin-left:48px"><span style="font-family:Courier New,Courier,monospace"><span style="font-size:11pt"><span style="color:#000000">Create user and password.</span></span></span></h2>

<h2 style="margin-left:48px"><span style="font-family:Courier New,Courier,monospace"><span style="font-size:11pt"><span style="color:#000000">Create dir for user and change its ownership</span></span></span></h2>

<pre>
<code class="language-markdown">chroot_local_user=YES

allow_writeable_chroot=YES

pasv_enable=YES

pasv_min_port=1024

pasv_max_port=1048

write_enable=YES</code></pre>

<p><span style="font-family:Courier New,Courier,monospace"><span style="font-size:11pt"><span style="color:#000000">Client:</span></span></span></p>

<p><span style="font-family:Courier New,Courier,monospace">No addiotal configuration required.</span></p>

<p>&nbsp;</p>
