DevNexus-2017
=============
Slide deck and code samples for the 
[Modern Service Management With Consul and Vault](http://devnexus.com/s/devnexus2017/presentations/17234) session, 
presented at DevNexus 2017.

Framework-agnostic config management demo
-----------------------------------------
A demo of using Consul and Vault to manage configuration properties across multiple environments, and multiple 
applications within each (including local development, loading from a properties file instead of Consul/Vault).  
Allows for separation between "non-secret" properties that can be managed by developers (e.g. JDBC URL's), versus
"secret" properties that should be managed only be authorized persons (e.g. usernames/passwords).  Works with any 
JVM application.

* [config-properties](https://github.com/steve-perkins/config-properties) - Properties files, and a batch processor 
  that syncs the non-secret properties with Consul.
* [config-client-lib](https://github.com/steve-perkins/config-client-lib) - Client library that loads properties from 
  Consul and Vault.
* [config-sample-app](https://github.com/steve-perkins/config-sample-app) - Demo web app, using the client library to 
  load properties.

Spring Cloud Config demo
------------------------
A Spring-specific demo of using Spring Cloud Config to manage configuration properties.  Uses a "composite environment 
repository" (coming in the next GA release)... which allows "non-secret" properties to be stored in Git, and "secret" 
properties stored in Vault.

* [spring-config-properties](https://github.com/steve-perkins/spring-config-properties) - Properties files.
* [spring-config-server](https://github.com/steve-perkins/spring-config-server) - Instance of Spring Cloud Config 
  Server, configured as a composite environment repository.
* [spring-config-sample-app](https://github.com/steve-perkins/spring-config-sample-app) - Demo Spring Boot app, using 
  the Spring Cloud Config Client to load properties.

TLS Security with Vault as a CA demo
------------------------------------
* [kafka-tls-demo](https://github.com/steve-perkins/kafka-tls-demo) - Instructions for configuring Kafka with Vault, 
  sample message producer and consumers.

Vault client
------------
* [vault-java-driver](https://github.com/BetterCloud/vault-java-driver) - An open-source Java client for Vault, used 
  by the demos above.

