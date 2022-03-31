
# DNS course

Author: Liran Cohen

Email: [liran@rct.co.il](mailto:liran@rct.co.il)

# Dns basics and intro

**<span style="text-decoration:underline;">Deliveries:</span>**



* How does DNS work?
* Why was DNS created (a piece of history)

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://aws.amazon.com/route53/what-is-dns/](https://aws.amazon.com/route53/what-is-dns/)
* https://www.cloudns.net/blog/dns-history-creation-first/

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 2h

**<span style="text-decoration:underline;">Deliveries:</span>**



* Dig
    * Question
    * Answer
    * statistics
* nslookup

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://phoenixnap.com/kb/linux-dig-command-examples](https://phoenixnap.com/kb/linux-dig-command-examples)
* https://www.pcwdld.com/nslookup-dns-records

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 5h


# Bind9 (named)

**<span style="text-decoration:underline;">Deliveries:</span>**



* Named quick start
* Named basic configuration

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://www.isc.org/bind/](https://www.isc.org/bind/)
* [https://kb.isc.org/docs/aa-00648](https://kb.isc.org/docs/aa-00648)
* [https://www.digitalocean.com/community/tutorials/how-to-configure-bind-as-a-private-network-dns-server-on-centos-7](https://www.digitalocean.com/community/tutorials/how-to-configure-bind-as-a-private-network-dns-server-on-centos-7)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 3h
* Frontal: 0.5h

**<span style="text-decoration:underline;">Drill</span>**



* Installed named (yum install named)


# Zone files 

**<span style="text-decoration:underline;">Deliveries:</span>**



* Familiarize with zone files
    * Primary and secondary zones
    * Zone files and domain names
    * subdomains
    * Record types:
        * A
        * AAAA
        * NS
        * CNAME
        * MX
        * NS
        * TXT
        * SOA
        * TTL
        * ORIGIN
        * SRV
        * PTR

**<span style="text-decoration:underline;">Reading materials:</span>**



* [http://www.steves-internet-guide.com/dns-zones-explained/](http://www.steves-internet-guide.com/dns-zones-explained/)
* [https://www.cloudflare.com/learning/dns/dns-records/](https://www.cloudflare.com/learning/dns/dns-records/)
* https://docs.oracle.com/cd/E19683-01/816-7511/6mdgu0h0d/index.html

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 8h
* Frontal: 0.5h

**<span style="text-decoration:underline;">Drill</span>**



* Create a new domain cadet.ts
* Create an A record


# In.addr.arpa zone (reverse)

**<span style="text-decoration:underline;">Deliveries:</span>**



* Why use reverse DNS?
* What is ARPA?
* How do reverse records work?

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://www.apnic.net/about-apnic/corporate-documents/documents/resource-guidelines/reverse-zones/](https://www.apnic.net/about-apnic/corporate-documents/documents/resource-guidelines/reverse-zones/)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 3h
* Frontal: 0.5h

**<span style="text-decoration:underline;">Drill</span>**


# Zone transfers

**<span style="text-decoration:underline;">Deliveries:</span>**



* Zone master and slave
* The zone file serial number
* What is ixfr?
* What are notifications?

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://jensd.be/197/linux/basic-master-and-slave-dns-setup-with-bind](https://jensd.be/197/linux/basic-master-and-slave-dns-setup-with-bind)
* [http://www.microhowto.info/howto/configure_bind_as_a_slave_dns_server.html](http://www.microhowto.info/howto/configure_bind_as_a_slave_dns_server.html)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 8h
* Frontal: 2h

**<span style="text-decoration:underline;">Drill</span>**



* Create a master-slave dns server deployment 
* Make the master reject queries and allow only zone transfers and make the slave accept queries.
* Add a record to the zone file and query the slave to get the updated result


# DNSSEC

**<span style="text-decoration:underline;">Deliveries:</span>**



* DNSsec principals

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://www.icann.org/resources/pages/dnssec-what-is-it-why-important-2019-03-05-en](https://www.icann.org/resources/pages/dnssec-what-is-it-why-important-2019-03-05-en)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 2h


# DDNS

**<span style="text-decoration:underline;">Deliveries:</span>**



* **<span style="text-decoration:underline;">Bind DDNS </span>**

**<span style="text-decoration:underline;">Reading materials:</span>**



* https://wiki.debian.org/DDNS

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 2h
* Frontal: 0.5h


# DNS server types

**<span style="text-decoration:underline;">Deliveries:</span>**



* Familiarity with different DNS server types:
    * Resolver
    * Authoritative
    * Root

**<span style="text-decoration:underline;">Reading materials:</span>**



* https://www.cloudflare.com/learning/dns/dns-server-types/

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 5h
* Frontal: 0.5h


# DNS Query types

**<span style="text-decoration:underline;">Deliveries:</span>**



* Familiarity with different DNS server types:
    * Recursive
    * Non-recoursive
    * iterative

**<span style="text-decoration:underline;">Reading materials:</span>**



* https://ns1.com/resources/dns-types-records-servers-and-queries

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 2h
* Frontal: 0.5h


# Bind

**<span style="text-decoration:underline;">Deliveries:</span>**



* Familiarity and installation drill of Bind

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://www.unixmen.com/dns-server-setup-using-bind-9-on-centos-7-linux/](https://www.unixmen.com/dns-server-setup-using-bind-9-on-centos-7-linux/)
* [https://www.digitalocean.com/community/tutorials/how-to-configure-bind-as-a-private-network-dns-server-on-centos-7](https://www.digitalocean.com/community/tutorials/how-to-configure-bind-as-a-private-network-dns-server-on-centos-7)
* https://www.isc.org/bind/

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 8h
* Frontal: 0.5h

**<span style="text-decoration:underline;">Drill</span>**



* Install a working Bind named DNS server


# FQDN

**<span style="text-decoration:underline;">Deliveries:</span>**



* Familiarity of FQDN

**<span style="text-decoration:underline;">Reading materials:</span>**



* https://www.networksolutions.com/blog/establish/domains/what-is-a-fully-qualified-domain-name--fqdn--#:~:text=An%20FQDN%20is%20a%20complete,ending%20with%20a%20trailing%20period.

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 3h
* Frontal: 0.5h
