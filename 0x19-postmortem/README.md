Tinpear learning Management System Insecure Connection Incident Report

Issue Summary:

A 'your connection is not private' error was experienced by most of our
customers from 11:07am (WAT) till it was resolved at about 12:03pm (WAT).

Our esteemed customers could not access our learning management platform
securely. Tutors and students could not access learning resources on all
our platforms because browsers kept reporting a 'connection not private'
error. This incident prevented 100% of our clients from logging into our
learning management platforms all over the world.

The root cause of the 'your connection is not private' error experienced on 
all our platforms was due to an expired secure socket layer (SSL) certificate
that caused the verification of secure connection with our servers by our customers'
browers to fail.


Timeline:

* The incident started at 11:07am (WAT)

* The incident was detected by our alert system integrated with the administrators'
  console at the headquarters.

* 11:10am (WAT): We immediately put our servers on safe-mode because we initially assumed it was 
  an hijack attempt by black hackers.

* 11:13am (WAT): We restarted the servers but the issue persisted.

* 11:16am (WAT): Calls started coming in from our customers complaining of being unable to log into
  our learning management platform and that their browsers kept saying that their 
  connection was insecure.

* 11:20am (WAT): All core devops engineers were trying to figure what was going on and ruled that it was 
  neither a domain name server (DNS) nor malicious redirection issue.

* 11:20am(WAT): It was finally discovered that our SSL certificate has expired without any notice.

* 11:59am (WAT): The SSL certificate was renewed and servers restared.

* 12:03pm (WAT): Service was fully restored and 100% of our customers could securely access our servers.


Root Cause and Resolution:

* An expired SSL certificate prevented all our customers' browsers from being able to verify that our
  servers can be securely accessed.

* The expired SSL certificate was renewed by contacting .tech domains, the host of our domain name.

* After payments were made, the servers were reconfigured with the new SSL credentials and restarted.


Corrective and preventive measures:

* We now have automatic renewal enabled with .tech domains (our domain registrar) and SSL certificate
  provider.

* We ensured the availability of different payment platforms to prevent any delay or interrupt in SSL
  certificate renewal.


