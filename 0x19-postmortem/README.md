**Tinpear Learning Management System Insecure Connection Incident Report**

![image](https://github.com/nomaprof/alx-system_engineering-devops/assets/80814144/50b1d941-5b7f-468d-98c0-70d08efc8ee5)


**Issue Summary:**

Date of incident: 16 October, 2023.

A 'your connection is not private' error was experienced by most of our
customers from 11:07 am (WAT) till it was resolved at about 12:03 pm (WAT).

Our esteemed customers could not access our learning management platform
securely. Tutors and students could not access learning resources on all
our platforms because browsers kept reporting a 'connection not private'
error. This incident prevented 100% of our clients from logging into our
learning management platforms worldwide.

The root cause of the 'your connection is not private' error experienced on 
all our platforms were due to an expired secure socket layer (SSL) certificate
that caused the verification of secure connection with our servers by our customers
browser to fail.


**Timeline:**

* The incident started at 11:07 am (WAT)

* The incident was detected by our alert system integrated with the administrators'
  console at the headquarters.

* 11:10 am (WAT): We immediately put our servers on safe mode because we initially assumed it was 
  a hijack attempt by black hackers.

* 11:13 am (WAT): We restarted the servers but the issue persisted.

* 11:16 am (WAT): Calls started coming in from our customers complaining of being unable to log into
  our learning management platform and that their browsers kept saying that their 
  the connection was insecure.

* 11:20 am (WAT): All core devops engineers were trying to figure out what was going on and ruled that it was 
  neither a domain name server (DNS) nor a malicious redirection issue.

* 11:20 am (WAT): It was finally discovered that our SSL certificate had expired without any notice.

* 11:59 am (WAT): The SSL certificate was renewed and servers restarted.

* 12:03 pm (WAT): Service was fully restored and 100% of our customers could securely access our servers.


**Root Cause and Resolution:**

* An expired SSL certificate prevented all our customers' browsers from being able to verify that our
  servers can be securely accessed.

* The expired SSL certificate was renewed by contacting .tech domains, the host of our domain name.

* After payments, the servers were reconfigured with the new SSL credentials and restarted.


**Corrective and preventive measures:**

* We now have automatic renewal enabled with .tech domains (our domain registrar) and SSL certificate
  provider.

* We ensured the availability of different payment platforms to prevent any delay or interruption in SSL
  certificate renewal.


