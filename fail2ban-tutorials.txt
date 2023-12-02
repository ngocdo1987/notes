1/ How To Protect an Nginx Server with Fail2Ban on Ubuntu 20.04
https://www.digitalocean.com/community/tutorials/how-to-protect-an-nginx-server-with-fail2ban-on-ubuntu-20-04

2/ Fail2Ban+Nginx (blocking repeated 404's, etc)
https://www.ericlight.com/fail2bannginx-blocking-repeated-404s-etc.html

3/ How to Secure an nginx Server with Fail2Ban
Our Security Requirements
Block anyone trying to run scripts (.pl, .cgi, .exe, etc)
Block anyone trying to use the server as a proxy
Block anyone failing to authenticate using nginx basic authentication
Block anyone failing to authenticate using our application's log in page
Block bad bots
Limit the number of connections per session
We could use ModSecurity to support these requirements, but it's not compatible with nginx. We want a lightweight and easy-to-use solution. We can fulfill all these requirements with fail2ban and nginx.
Configuring Fail2ban

https://snippets.aktagon.com/snippets/554-how-to-secure-an-nginx-server-with-fail2ban

4/ How to secure Nginx with Fail2ban from botnet attack
https://thelinuxnotes.com/index.php/how-to-secure-nginx-with-fail2ban-from-botnet-attack/#google_vignette
