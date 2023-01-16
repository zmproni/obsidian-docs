# How to set up a custom DNS on your linux system

In linux distros, the usual file that is used to configure the system's Domain Name Server (DNS) resolver is located at and called [/etc/resolv.conf](debian/files). By editing the contents of the file we should be able to change the DNS resolver the system connects to with a custom value. 

My personal favourite DNS resolver is Cloudflare's '1.1.1.1'. It advertises one of the fastest speeds, and privacy. Two side effects of using this Cloudflare's DNS server are: it opens up access to some sites blocked by ISPs as well as reduce latency in certain games and website loading. 

Use the following command to edit the contents of the file.
```bash 
sudo nano /etc/resolv.conf
```

Replace the contents of the file with this text. 
```
nameserver 1.1.1.1
nameserver 1.0.0.1
nameserver 2606:4700:4700::1111
nameserver 2606:4700:4700::1001
```
Save the file and exit. 

Back in  the terminal type the command:
```bash
sudo systemctl restart networking
```
Your machine should now be using Cloudflare's DNS server.

You can use this [link](https://www.top10vpn.com/tools/what-is-my-dns-server/) to check if the DNS resolver has been configured correctly. 