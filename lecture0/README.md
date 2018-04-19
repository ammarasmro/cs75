# HTTP Requests

w.x.y.z

GET / HTTP/1.0

http://www.google.com/

protocol://hostname.domainname.tld/path

https uses cryptography
ftp for files

Internal IP address:
192.168.x.x used by home routers
172.16.y.y
10.z.z.z Class A IP addresses gives millions of addresses

TCP: Transmission Control Protocol

HTTP: TCP 80
HTTPS: TCP 443
SMTP: TCP 25

Always use standard ports to avoid getting blocked

To start a website, first purchase a domain name.

Domains are bought from registrars such as:
* Namecheap
* GoDaddy

Then, host the website somewhere. It is best to have two DNS's one primary and one for backup.

* NS a record in a DNS server that tells the world what the IP address is for that domain.
* A record domain name -- to --> IP address like a spreadsheet
* CNAME is like an alias. domain name --- map to ---> another domain name, instead of an IP address
* MX record is a mail exchange record. What is the IP address of the server that should handle inbound mail requests

------------------

## Web Hosting

Cheap web hosting means more than one website shares the same machine. This causes the website to compete for resources. Here, there is no administration access.
* DreamHost is a cheap and very popular web hosting service provider

## Virtual Private Server (VPS)
Get the illusion of having a dedicated server. There is a possibility for resource contention. Administrative access. However, the people who have physical access also have the root access as you do.

Transfer: in & out of the server

## Secure Shell (SSH)
A way to access a remote server

## SFTP
Let's you drag and drop files between servers on Windows

## DHCP
Dynamic Host Configuration Protocol

-------

## Response codes
* 200: OK
* 301,302: redirects
* 404: not found
* 502: server error

## Commands

**telnet** is like ssh but unencrypted. It uses TCP port 21
```bash
telnet www.google.com # won't work
```
Try another port
```bash
telnet www.google.com 80
# Connected msg
GET / HTTP/1.1
# Response msg
```

**nslookup** name server lookup
```bash
nslookup www.google.com
```

**nslookup** name server lookup
```bash
sudo vi /etc/hosts
```
Then add the name
```bash
216.58.216.142 amory.com
```
This will allow local access to google.com through amory.com
