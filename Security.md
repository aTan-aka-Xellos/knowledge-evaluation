# [Security - Java](https://confluence.softserveinc.com/display/AbilitonKnowledgeModel/Security-Java)

__Qualification Requirements Overview:__  
Base security principles and secure coding practices.

## [Basic security principles](https://en.wikipedia.org/wiki/Information_security)

![CIA](https://www.ibm.com/blogs/cloud-computing/wp-content/uploads/2018/01/TRIAD.png)

The __CIA__ triad of confidentiality, integrity, and availability is at the heart of information security.  
Confidentiality, integrity and availability, also known as the CIA triad, is a model designed to guide policies for information security within an organization.

__Confidentiality__ involves a set of rules or a promise usually executed through confidentiality agreements that limits access or places restrictions on certain types of information.  
Confidentiality is roughly equivalent to privacy.  

__Integrity__ involves maintaining the consistency, accuracy, and trustworthiness of data over its entire life cycle.

__Availability__ refers to the actual availability of your data. Authentication mechanisms, access channels and systems all have to work properly for the information they protect and ensure it's available when it is needed.  

## [Secure communications fundamentals (SSL, TLS, HTTPS)](https://en.wikipedia.org/wiki/Transport_Layer_Security#SSL_2.0)

Used on application layer lvl of OSI.  
In applications design, TLS is usually implemented on top of Transport Layer protocols, encrypting all of the protocol-related data of protocols such as HTTP, FTP, SMTP, NNTP and XMPP.  

TSL and SSL are cryptographic protocols designed to provide communications security over a computer network. 
The TLS protocol aims primarily to provide privacy and data integrity.  

### SSL

SSL (Secure Sockets Layer) stands for Secure Sockets Layer and, in short, it's the standard technology for keeping an internet connection secure and safeguarding any sensitive data that is being sent between two systems, preventing criminals from reading and modifying any information transferred, including potential personal details.  

TLS (Transport Layer Security) is just an updated, more secure, version of SSL.  
Latest version: TLS 1.3  

HTTPS (Hyper Text Transfer Protocol Secure) appears in the URL when a website is secured by an SSL certificate.  

The Hypertext Transfer Protocol (HTTP) is an application protocol for distributed, collaborative, hypermedia information systems.  
In HTTPS, the communication protocol is encrypted using Transport Layer Security (TLS), or, formerly, its predecessor, Secure Sockets Layer (SSL). The protocol is therefore also often referred to as HTTP over TLS, or HTTP over SSL.  

## [Understanding of basic security risks](https://www.owasp.org/index.php/Category:OWASP_Top_Ten_2017_Project)

Top 10 OWASP risks:
* Injection
* Broken Authentication
* Sensitive Data Exposure
* XML External Entities (XXE)
* Broken Access Control
* Security Misconfiguration
* Cross-Site Scripting (XSS)
* Insecure Deserialization
* Using Components with Known Vulnerabilities
* Insufficient Logging&Monitoring

## [Java SE Security Overview](https://docs.oracle.com/javase/7/docs/technotes/guides/security/)
https://docs.oracle.com/javase/7/docs/technotes/guides/security/overview/jsoverview.html

#### Java Language Security and Bytecode Verification
A compiler translates Java programs into a machine-independent bytecode representation. A bytecode verifier is invoked to ensure that only legitimate bytecodes are executed in the Java runtime. It checks that the bytecodes conform to the Java Language Specification and do not violate Java language rules or namespace restrictions. The verifier also checks for memory management violations, stack underflows or overflows, and illegal data typecasts. Once bytecodes have been verified, the Java runtime prepares them for execution.

#### Basic Security Architecture
The Java platform defines a set of APIs spanning major security areas, including cryptography, public key infrastructure, authentication, secure communication, and access control. These APIs allow developers to easily integrate security into their application code. They were designed around the following principles:

##### Implementation independence
Applications do not need to implement security themselves. Rather, they can request security services from the Java platform. Security services are implemented in providers (see below), which are plugged into the Java platform via a standard interface. An application may rely on multiple independent providers for security functionality.
##### Implementation interoperability
Providers are interoperable across applications. Specifically, an application is not bound to a specific provider, and a provider is not bound to a specific application.
##### Algorithm extensibility
The Java platform includes a number of built-in providers that implement a basic set of security services that are widely used today. However, some applications may rely on emerging standards not yet implemented, or on proprietary services. The Java platform supports the installation of custom providers that implement such services.

#### File Locations
Certain aspects of Java security mentioned in this paper, including the configuration of providers, may be customized by setting security properties. You may set security properties statically in the security properties file, which by default is the java.security file in the lib/security directory of the directory where the Java™ Runtime Environment (JRE) is installed. Security properties may also be set dynamically by calling appropriate methods of the Security class (in the java.security package).

#### Cryptography
The Java cryptography architecture is a framework for accessing and developing cryptographic functionality for the Java platform.

#### Public Key Infrastructure
Public Key Infrastructure (PKI) is a term used for a framework that enables secure exchange of information based on public key cryptography.

#### Key and Certificate Storage
The Java platform provides for long-term persistent storage of cryptographic keys and certificates via key and certificate stores.

#### Authentication
The Java platform provides APIs that enable an application to perform user authentication via pluggable login modules.

#### Secure Communication
The Java platform also provides API support and provider implementations for a number of standard secure communication protocols.

#### SSL/TLS
The Java platform provides APIs and an implementation of the SSL and TLS protocols that includes functionality for data encryption, message integrity, server authentication, and optional client authentication. Applications can use SSL/TLS to provide for the secure passage of data between two peers over any application protocol, such as HTTP on top of TCP/IP.


## [Java SE Message Dig-esters SHA2, MD5](https://docs.oracle.com/javase/7/docs/api/java/security/MessageDigest.html)
MessageDigest class provides applications the functionality of a message digest algorithm, such as SHA-1 or SHA-256. Message digests are secure one-way hash functions that take arbitrary-sized data and output a fixed-length hash value.

## [Java EE Introduction to Security in the Platform](https://docs.oracle.com/javaee/7/tutorial/security-intro.htm)

Security for components is provided by their containers. A container provides two kinds of security: declarative and programmatic.
* Declarative security expresses an application component's security requirements by using either deployment descriptors or annotations.
* Programmatic security is embedded in an application and is used to make security decisions.


## Java EE Characteristics of Application Security (Authentication, Authorization, Data integrity

Identification is a process that enables recognition of an entity by a system.  
Authentication is a process that verifies the identity of a user, device, or other entity in a computer system, usually as a prerequisite to allowing access to resources in a system.  

* Authentication: The means by which communicating entities, such as client and server, prove to each other that they are acting on behalf of specific identities that are authorized for access. This ensures that users are who they say they are.

* Authorization, or access control: The means by which interactions with resources are limited to collections of users or programs for the purpose of enforcing integrity, confidentiality, or availability constraints. This ensures that users have permission to perform operations or access data.

* Data integrity: The means used to prove that information has not been modified by a third party, an entity other than the source of the information. For example, a recipient of data sent over an open network must be able to detect and discard messages that were modified after they were sent. This ensures that only authorized users can modify data.

* Confidentiality, or data privacy: The means used to ensure that information is made available only to users who are authorized to access it. This ensures that only authorized users can view sensitive data.

* Non-repudiation: The means used to prove that a user who performed some action cannot reasonably deny having done so. This ensures that transactions can be proved to have happened.

* Quality of Service: The means used to provide better service to selected network traffic over various technologies.

* Auditing: The means used to capture a tamper-resistant record of security-related events for the purpose of being able to evaluate the effectiveness of security policies and mechanisms. To enable this, the system maintains a record of transactions and security information.

## [Java EE Security Mechanisms (Application, Transport, Message Layer)](https://docs.oracle.com/javaee/7/tutorial/security-intro002.htm#BNBWY)

### Application-Layer Security
In Java EE, component containers are responsible for providing application-layer security, security services for a specific application type tailored to the needs of the application. At the application layer, application firewalls can be used to enhance application protection by protecting the communication stream and all associated application resources from attacks.

The advantages of using application-layer security:
* Security is uniquely suited to the needs of the application.
* Security is fine grained, with application-specific settings.

The disadvantages of using application-layer security:
* The application is dependent on security attributes that are not transferable between application types.
* Support for multiple protocols makes this type of security vulnerable.
* Data is close to or contained within the point of vulnerability.

### Transport-Layer Security
Transport-layer security is provided by the transport mechanisms used to transmit information over the wire between clients and providers; thus, transport-layer security relies on secure HTTP transport (HTTPS) using Secure Sockets Layer (SSL). Transport security is a point-to-point security mechanism that can be used for authentication, message integrity, and confidentiality. 

Transport-layer security is performed in a series of phases, as follows:
* The client and server agree on an appropriate algorithm.
* A key is exchanged using public-key encryption and certificate-based authentication.
* A symmetric cipher is used during the information exchange.

The advantages of using transport-layer security:
* It is relatively simple, well-understood, standard technology.
* It applies to both a message body and its attachments.

The disadvantages of using transport-layer security:
* It is tightly coupled with the transport-layer protocol.
* It represents an all-or-nothing approach to security. This implies that the security mechanism is unaware of message contents, so that you cannot selectively apply security to portions of the message as you can with message-layer security.
* Protection is transient. The message is protected only while in transit. Protection is removed automatically by the endpoint when it receives the message.
* It is not an end-to-end solution, simply point-to-point.

### Message-Layer Security
In message-layer security, security information is contained within the SOAP message and/or SOAP message attachment, which allows security information to travel along with the message or attachment. For example, a portion of the message may be signed by a sender and encrypted for a particular receiver. When sent from the initial sender, the message may pass through intermediate nodes before reaching its intended receiver. In this scenario, the encrypted portions continue to be opaque to any intermediate nodes and can be decrypted only by the intended receiver. For this reason, message-layer security is also sometimes referred to as end-to-end security.  

The advantages of message-layer security:
* Security stays with the message over all hops and after the message arrives at its destination.
* Security can be selectively applied to different portions of a message and, if using XML Web Services Security, to attachments.
* Message security can be used with intermediaries over multiple hops.
* Message security is independent of the application environment or transport protocol.

The disadvantage of using message-layer security is that it is relatively complex and adds some overhead to processing.  

## Java EE Authentication types (Basic, Form-Based, Digest Authentication)

### Basic authentication
Specifying HTTP basic authentication requires that the server request a user name and password from the web client and verify that the user name and password are valid by comparing them against a database of authorized users in the specified or default realm.   

Basic authentication is the default when you do not specify an authentication mechanism.  

When basic authentication is used, the following actions occur.
1. A client requests access to a protected resource.
2. The web server returns a dialog box that requests the user name and password.
3. The client submits the user name and password to the server.
4. The server authenticates the user in the specified realm and, if successful, returns the requested resource.

![steps_basic](https://docs.oracle.com/javaee/7/tutorial/img/jeett_dt_045.png)

Disadvantagaes:
* Not sucure over HTTP
* Send login/password with each request
* Password cached in browser

### Form-Based Authentication
Form-based authentication allows the developer to control the look and feel of the login authentication screens by customizing the login screen and error pages that an HTTP browser presents to the end user. When form-based authentication is declared, the following actions occur.  

When you create a form-based login, be sure to maintain sessions using cookies or SSL session information.  

It is more secure than basic auth when it comes to properly logging the user off after a certain period of inactivity or if the user no longer requires use of the system and decides to log out.  

![steps_form-based](https://docs.oracle.com/javaee/7/tutorial/img/jeett_dt_046.png)

### Digest Authentication
Like basic authentication, digest authentication authenticates a user based on a user name and a password. However, unlike basic authentication, digest authentication does not send user passwords over the network. Instead, the client sends a one-way cryptographic hash of the password and additional data. Although passwords are not sent on the wire, digest authentication requires that clear-text password equivalents be available to the authenticating container so that it can validate received authenticators by calculating the expected digest.  

The server gives the client a one-time use number (a nonce) that it combines with the username, realm, password and the URI request. The client runs all of those fields through an MD5 hashing method to produce a hash key.  

It sends this hash key to the server along with the username and the realm to attempt to authenticate.  

Server-side the same method is used to generate a hashkey, only instead of using the password typed in to the browser the server looks up the expected password for the user from its user DB. It looks up the stored password for this username, runs in through the same algorithm and compares it to what the client sent. If they match then access is granted, otherwise it can send back a 401 Unauthorized (no login or failed login) or a 403 Forbidden (access denied).  


