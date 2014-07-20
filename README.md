OtterVPN
========

Website that provides configuration files for openvpn, browsers (with client certs), LDAP, etc.

This project is closely related to OtterCA:

 - OtterCA is responsible for key and certificate management

 - OtterVPN is responsible for application configuration


Output
------

The standard output consists of a zip file containing

 -  one zip file containing a CA certificate
 -  one or more zip files containing a certificate signed by that CA.

In the long term the client will be able to provide a set of certificate
requests that will be signed by the CA certificate and returned. In the
immediate term the app will also generate the private keys and they
will be returned with the certificates.

This sounds like a huge security hole - my application will know your
keys! - but in practice I have no idea where your keys will be used or
if it will even be publicly accessible. If you're seriously worried
the app is open source and you can easily set up your own server.

OpenVPN 
-------

This app will create one zip file per client and server. Each zip file
will contain the appropriate configuration file.

Web Services
------------

This app will create one zip file for each party. The files will allow
mutual authentication.

Web Application
---------------

This app will create one zip file for the server and an optional number
of zip files for individual clients. This allows mutual authentication, 
e.g., for use within a secured environment.

OpenLDAP
--------

This app will create one zip file per client and server. Each zip file
will contain the appropriate configuration file.

To Be Added
-----------

Ditto any other services identified in the future.
