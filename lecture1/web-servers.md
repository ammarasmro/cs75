# Web Servers

Apache is a very  common web server


## Configuration
* httpd.conf
* apache.conf
* apache2.conf
```
<VirtualHost *:80>
```
Defines a virtual host on port 80 on any IP address that the server has.

## SSL
SSL certificate needs to be signed by an authority.

## URL Rewrite
mod_rewrite

Status codes
* 301: moved permanently
* 302: moved temporarily

Example
```
RewriteEngine On
RewriteCond %{HTTP_HOST} !^www\.cs75\.net [NC]
RewriteRule (.*) https://www.cs75.net/$1 [R=301,L]
```

if user tried to access www.cs75.net, redirect to https version
R=301 moved permanently
L this is the end execute
```
(.*) ..... /$1
```
This is to get what page the user queried originally and include it in the redirect link

Another way to enforce https
```
RewriteCond %{HTTPS} != on
RewriteRule ......
```

`.htaccess` files have rules for each directory

## XAMPP
A package that makes it easier to turn a computer into a web server
