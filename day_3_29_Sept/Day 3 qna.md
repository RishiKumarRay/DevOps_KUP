​                                             **Day 3 - Questions and answers** 

**Que - 1: How Many Tables are there in iptables?**

There are 5 tables in iptables :

-  Input table
-  NAT table
-  Mangle table
-  Raw table 
-  Security 

 **Que 2: What are prot, opt , Source , and Destinations ?**

   prot:-This defines the protocol (TCP,IP) of the packet.

   source:- This tells the source address of the packet.

   destination:- This defines the destination address of the packet

   opt :- Special options for that specific rule

**Que 3:  Why rules are added to the top?**

The Rules we set in the iptables are checked from the topmost rules to the bottom. Whenever a packet passes any of the top rules, it is allowed to pass the firewall. The lower rules are not checked, So that's why rules are added to the top.

**Que 4: What types of rules we can add to the iptables?**

There are basically 3 rules or policies that we can add in the iptables:

-  ACCEPT
- DROP
- REJECT

ACCEPT - when the traffic passes the rules in its specified chain then iptables accept the traffic and it opens it gates and allows it to pass.

DROP - when the traffic is unable to pass the rules then the iptable blocks the traffic.

Reject - here this is similar to Reject but in this case a message is sent to the sender which states that the transfer is not reachable or its failed.

**Que 5:  Can we block a website by its domain name only ?**

Yes we can do this and we can block the website by its domain name with using this command :

iptable -I INPUT -s www.facebook.com -j DROP

**Que 6: How can we persist rules in an iptable?**

Inorder to do this first we have to download persistant package then we can run this command

These can be saved in a file with the command `iptables-save` for IPv4.

sudo iptables-save > /etc/iptables/rules.v4  

**Que 7:  What is the difference between UFW and Iptables?**

|                             UFW                              |                           IPtable                            |
| :----------------------------------------------------------: | :----------------------------------------------------------: |
| UFW is a simplified firewall mechanism that is implemented on top of iptables. | Iptables is a kernel level ip filtering mechanism. It does allow you to make routing decisions and so on on IP packets. |
| UFW is not as flexible but is easier to configure for common scenarios. | To use IPtables you need to understand TCP/IP connections, more complicated protocols |



**Que 8 - What are public and private keys?**

An SSH key relies upon the use of two related keys, a public key and a private key, that together create a key pair that is used as the secure access credential. The private key is secret, known only to the user, and should be encrypted and stored safely. The public key can be shared freely with any SSH server to which the user wishes to connect.

**Que 9: How SSH works ?**

The SSH protocol is based on the client-server model. Therefore, an SSH client must initiate an SSH session with an SSH server. Most of the connection setup is conducted by the SSH client and public key is used to verify the identity of the SSH server, and then symmetric key encryption and hashing algorithms are used.

**Que 10 - What is the difference between HTTP and HTTPs?**

HTTPS is HTTP with encryption. The difference between the two protocols is that HTTPS uses TLS (SSL) to encrypt normal HTTP requests and responses. As a result, HTTPS is far more secure than HTTP. 

**Ques 11 - How can we save rules in iptables?**

there is a package with the name "iptables-persistent" which takes over the automatic loading of the saved iptables rules. To do this, the rules must be saved in the file  /etc/iptables/rules.v4  for IPv4 and /etc/iptables/rules.v6 for IPv6.

**Que 12- What is SSL ?**

SSL stands for Secure Sockets Layer, a security protocol that creates an encrypted link between a web server and a web browser Also an SSL certificate is a digital certificate that authenticates a website's identity and enables an encrypted connection.

**Que 13 - What is the difference between apt update and apt-upgrade ?**

 “apt-get update” updates the package sources list to get the latest list of available packages in the repositories and “apt-get upgrade” updates all the packages presently installed in our Linux system to their latest versions.

**Que 14 - What do repositories contain in a linux system?**

A Linux repository is a storage location from where your system retrieves and installs updates and applications also each repository is a collection of the software that are hosted on a remote server and intended to be used for installing and updating software packages on Linux systems. 

**Que 15 - What does the number represent after the file permissions ?**

It represents the number of files

**Que 16 - What are difference between apt and apt-get ?**

The basic difference between apt and apt-get is  apt shows the number of packages that can be upgraded while it is not in the case of the apt-get also in the case of apt there is a improve design and additional details.

