# useful_nginx_commands

to install nginx:
``` 
sudo apt-get install nginx
```
the directory to nginx:
```
cd /etc/nginx/
```
to see nginx help:
```
nginx -h
```
to see the nginx config:
```
less nginx.conf
```
to run nginx commands, you need to change to root:
```
sudo su
```
it's a good practice to make a copy of the conf file:
```
mv nginx.conf main-nginx.conf
```
```
touch nginx.conf
```
to test new nginx conf:
```
nginx -t
```
after making changes in the nginx.conf file we need to
restart or reload nginx (the diference is that, with reload the pid for master process doesn not change
but with the restart, a new pid will be generated)
```
systemctl restart nginx
```
```
systemctl reload nginx 
```
another way of reloading nginx is to use reload signal which still does not change pid for the master process(-s)
```
nginx -s reload
```
to see nginx status:
```
systemctl status nginx.service
```
to run nginx:
```
systemctl start nginx
```
to stop nginx:
```
systemctl stop nginx
```
by default when you restart your computer, the nginx will be disabled again.
if you want to keep nginx enable:
```
systemctl enable nginx
```
to see the working and master processes:
```
ps -ef | grep nginx
```
the place that nginx logs are stored:
```
/var/log/ngninx/
```
