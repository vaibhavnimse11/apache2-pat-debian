# apache2-pat-debian
Practical demonstration of Port Address Translation (PAT) using Apache2 on a Debian machine — Access redirected from port 80 to 8001.
# Apache2 Port Address Translation (PAT) on Debian

##  Objective
To demonstrate Port Address Translation (PAT) by redirecting Apache2 default web server from port 80 to port 8001 on a Debian machine.

---

#  System Used
- OS: Debian (CLI)
- Web Server: Apache2
- Apache2 IP: `192.168.80.128`


#Steps Performed

#1. Access Apache2 default page on port 80
```bash
http://192.168.80.128:80

## sudo iptables -t nat -A PREROUTING -p tcp --dport 8001 -j REDIRECT --to-port 80
  - by running this command we redirect the traffic from port 80 to 8001
