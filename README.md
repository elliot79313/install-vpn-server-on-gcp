# Install VPN Server on Google Cloud platform (using Debian 7)

-----

Prerequisite:
1. You have Google account
2. You are familiar with [Google cloud platform console](https://console.developers.google.com "Google Cloud Platform Console").
3. You know how to launch Google Computing VM with Debian 7. ([Quick Start](https://cloud.google.com/compute/docs/linux-quickstart, "Quick Start"))


-----

##Instructions:


###On Server:###

1. After you launch an instance, download <code>vpn-installtion.sh</code> into that instance.
2. Update the **TODO** (<code>IPSEC_PSK</code>, <code>VPN_USER</code>, <code>VPN_PASSWORD</code>, <code>PRIVATE_IP</code>, <code>PUBLIC_IP</code>)
3. run <code>
	sudo sh vpn-installtion.sh
</code>
4. Setup the network.
![Allow traffic to TCP port 500, and UDP ports 500 and 4500.](https://greenido.files.wordpress.com/2014/08/screenshot-2014-08-10-08-50-20.png?w=696)

-----

###On Client(Mac):###
1. Create a new connection. ![Create a new connection](https://raw.github.com/elliot79313/install-vpn-server-on-gcp/master/img/client_networksetup.png)
2. Fill in the Server Address and Account Name.
3. Click Authentication Settings. Fill in Machine Authentication Shared Secret with **IPSEC_PSK**
4. Click advanced button and check **Send all traffic** on options tab.
5. Click apply and connect.
6. [Optional] Setup dns server. In DNS tab, you can copy values in <code>/etc/resolv.conf</code> of VPN Server and fill into **search domain**.


-----

Feel free to open issues.



