# [Construction - Java Enterprise Essentials](https://confluence.softserveinc.com/display/AbilitonKnowledgeModel/Java+Enterprise+Essentials)


## CL1 (Qualified) 
__Qualification Requirements Overview:__  
The main goal of this level is to get acquainted with Java Enterprise Edition 6’s components 
and being able to execute simple operations in Application/Web Server (also it is not limited to Tomcat/JBoss/Glassfish, 
please use the one that you are working with on the project) . Java EE 6 Pocket Guide book is recommended as a start point.  
Other item that is covered in this level is introduction to Spring/EJB. 
Please note that only one is required - either Spring or EJB.

## JEE platform components
https://javaee.github.io/tutorial/overview008.html
https://en.wikipedia.org/wiki/Java_Platform,_Enterprise_Edition

### Enterprise JavaBeans Technology
An Enterprise JavaBeans (EJB) component, or enterprise bean, is a body of code that has fields 
and methods to implement modules of business logic. You can think of an enterprise bean as a building block 
that can be used alone or with other enterprise beans to execute business logic on the Java EE server.  

Enterprise beans are either session beans or message-driven beans.  

A session bean represents a transient conversation with a client. When the client finishes executing, 
the session bean and its data are gone.  

A message-driven bean combines features of a session bean and a message listener, allowing a business component 
to receive messages asynchronously. Commonly, these are Java Message Service (JMS) messages.  

### Java Servlet Technology
Java Servlet technology lets you define HTTP-specific servlet classes.  
A servlet class extends the capabilities of servers that host applications accessed by way of a request-response programming model. 
Although servlets can respond to any type of request, they are commonly used to extend the applications hosted by web servers.

### JavaServer Faces Technology

JavaServer Faces technology is a user interface framework for building web applications.  
The main components of JavaServer Faces technology are as follows:
* A GUI component framework.
* A flexible model for rendering components in different kinds of HTML or different markup languages and technologies. A Renderer object generates the markup to render the component and converts the data stored in a model object to types that can be represented in a view.
* A standard RenderKit for generating HTML 4.01 markup.

The following features support the GUI components:

* Input validation
* Event handling
* Data conversion between model objects and components
* Managed model object creation
* Page navigation configuration
* Expression Language (EL)

All this functionality is available using standard Java APIs and XML-based configuration files.  

### JavaServer Pages Technology
JavaServer Pages (JSP) technology lets you put snippets of servlet code directly into a text-based document.  
A JSP page is a text-based document that contains two types of text:
* Static data, which can be expressed in any text-based format, such as HTML or XML
* JSP elements, which determine how the page constructs dynamic content

### JavaServer Pages Standard Tag Library

The JavaServer Pages Standard Tag Library (JSTL) encapsulates core functionality common to many JSP applications. 
Instead of mixing tags from numerous vendors in your JSP applications, you use a single, standard set of tags. 
This standardization allows you to deploy your applications on any JSP container that supports JSTL and makes it more likely that the implementation of the tags is optimized.

### Java Persistence API

The Java Persistence API (JPA) is a Java standards–based solution for persistence. 
Persistence uses an object/relational mapping approach to bridge the gap between an object-oriented model and a relational database. The Java Persistence API can also be used in Java SE applications outside of the Java EE environment.  
Java Persistence consists of the following areas:
* The Java Persistence API
* The query language
* Object/relational mapping metadata

№№№ Java Transaction API

The Java Transaction API (JTA) provides a standard interface for demarcating transactions. The Java EE architecture provides a default auto commit to handle transaction commits and rollbacks. An auto commit means that any other applications that are viewing data will see the updated data after each database read or write operation. However, if your application performs two separate database access operations that depend on each other, you will want to use the JTA API to demarcate where the entire transaction, including both operations, begins, rolls back, and commits.


### Java API for RESTful Web Services

The Java API for RESTful Web Services (JAX-RS) defines APIs for the development of web services built according to the Representational State Transfer (REST) architectural style. A JAX-RS application is a web application that consists of classes packaged as a servlet in a WAR file along with required libraries.

In the Java EE 8 platform, new RESTful web services features include the following:

* Reactive Client API
When the results of an invocation on a target resource are received, enhancements to the completion stage APIs in Java SE allow the sequence of those results to be specified, prioritized, combined, or concatenated, and how exceptions can be handled.

* Enhancements in support for server-sent events
Clients may subscribe to server-issued event notifications using a long-running connection. Support for a new media type, text/event-stream, has been added.

* Support for JSON-B objects, and improved integration with CDI, Servlet, and Bean Validation technologies

### Managed Beans

Managed Beans, lightweight container-managed objects (POJOs) with minimal requirements, support a small set of basic services, such as resource injection, lifecycle callbacks, and interceptors. Managed Beans represent a generalization of the managed beans specified by JavaServer Faces technology and can be used anywhere in a Java EE application, not just in web modules.

### Bean Validation
The Bean Validation specification defines a metadata model and API for validating data in JavaBeans components. Instead of distributing validation of data over several layers, such as the browser and the server side, you can define the validation constraints in one place and share them across the different layers.

In the Java EE 8 platform, new Bean Validation features include the following:
* Support for new features in Java SE 8, such as the Date-Time API
* Addition of new built-in Bean Validation constraints


### Contexts and Dependency Injection for Java EE

Contexts and Dependency Injection for Java EE (CDI) defines a set of contextual services, provided by Java EE containers, that make it easy for developers to use enterprise beans along with JavaServer Faces technology in web applications. Designed for use with stateful objects, CDI also has many broader uses, allowing developers a great deal of flexibility to integrate different kinds of components in a loosely coupled but typesafe way.

In the Java EE 8 platform, new CDI features include the following:
* An API for bootstrapping a CDI container in Java SE 8
* Support for observer ordering, which determines the order in which the observer methods for a particular event are invoked, and support for firing events asynchronously
* Configurators interfaces, which are used for dynamically defining and modifying CDI objects
* Built-in annotation literals, a convenience feature for creating instances of annotations, and more


### Dependency Injection for Java

Dependency Injection for Java defines a standard set of annotations (and one interface) for use on injectable classes.  

In the Java EE platform, CDI provides support for Dependency Injection. Specifically, you can use injection points only in a CDI-enabled application.

### Java Message Service API

The Java Message Service (JMS) API is a messaging standard that allows Java EE application components to create, send, receive, and read messages. It enables distributed communication that is loosely coupled, reliable, and asynchronous.

### JavaMail API

Java EE applications use the JavaMail API to send email notifications. The JavaMail API has two parts:
* An application-level interface used by the application components to send mail
* A service provider interface

The Java EE platform includes the JavaMail API with a service provider that allows application components to send Internet mail.

### Java API for WebSocket

WebSocket is an application protocol that provides full-duplex communications between two peers over TCP. The Java API for WebSocket enables Java EE applications to create endpoints using annotations that specify the configuration parameters of the endpoint and designate its lifecycle callback methods.

### Java API for JSON Processing

JavaScript Object Notation (JSON) is a text-based data exchange format derived from JavaScript that is used in web services and other connected applications. The Java API for JSON Processing (JSON-P) enables Java EE applications to parse, transform, and query JSON data using the object model or the streaming model.


### Java API for JSON Binding

The Java API for JSON Binding (JSON-B) provides a binding layer for converting Java objects to and from JSON messages. JSON-B also supports the ability to customize the default mapping process used in this binding layer through the use of Java annotations for a given field, JavaBean property, type or package, or by providing an implementation of a property naming strategy.

### Concurrency Utilities for Java EE

Concurrency Utilities for Java EE is a standard API for providing asynchronous capabilities to Java EE application components through the following types of objects: managed executor service, managed scheduled executor service, managed thread factory, and context service.

### Batch Applications for the Java Platform
Batch jobs are tasks that can be executed without user interaction. 

### Java Authorization Contract for Containers

The Java Authorization Contract for Containers (JACC) specification defines a contract between a Java EE application server and an authorization policy provider. All Java EE containers support this contract.

The JACC specification defines java.security.Permission classes that satisfy the Java EE authorization model. The specification defines the binding of container-access decisions to operations on instances of these permission classes. It defines the semantics of policy providers that use the new permission classes to address the authorization requirements of the Java EE platform, including the definition and use of roles.

### Java Authentication Service Provider Interface for Containers

The Java Authentication Service Provider Interface for Containers (JASPIC) specification defines a service provider interface (SPI) by which authentication providers that implement message authentication mechanisms may be integrated in client or server message-processing containers or runtimes. Authentication providers integrated through this interface operate on network messages provided to them by their calling containers. The authentication providers transform outgoing messages so that the source of each message can be authenticated by the receiving container, and the recipient of the message can be authenticated by the message sender. Authentication providers authenticate each incoming message and return to their calling containers the identity established as a result of the message authentication.


### Java EE Security API
The Java EE Security API specification defines portable, plug-in interfaces for HTTP authentication and identity stores, and an injectable SecurityContext interface that provides an API for programmatic security.

Implementations of the HttpAuthenticationMechanism interface can be used to authenticate callers of web applications. An application can supply its own HttpAuthenticationMechanism, or use one of the default implementations provided by the container.

Implementations of the IdentityStore interface can be used to validate user credentials and retrieve group information. An application can provide its own IdentityStore, or use the built in LDAP or Database store.

The HttpAuthenticationMechanism and IdentityStore APIs provide an advantage over container-provided implementations in that they allow an application to control the authentication process, and the identity stores used for authentication, in a standard, portable way.

The SecurityContext API is intended for use by application code to query and interact with the current security context. The specification also provides for default group-to-role mapping, and defines a principal type called CallerPrincipal that can represent the identity of an application caller.


### Java EE Connector Architecture

The Java EE Connector Architecture is used by tools vendors and system integrators to create resource adapters that support access to enterprise information systems that can be plugged in to any Java EE product. A resource adapter is a software component that allows Java EE application components to access and interact with the underlying resource manager of the EIS. Because a resource adapter is specific to its resource manager, a different resource adapter typically exists for each type of database or enterprise information system.


# Competent
Competent level questions are focused on DI, Bean Validation and practical experience and skills with either Spring 3 or EJB 3.2. Please note that theoretical knowledge is not enough to be evaluated as Competent! It is recommended to use Pro Spring 3 book and Spring Documentation for Spring related topics, however other sources are applicable as well  

## DI: Interceptors and Decorators

http://www.mastertheboss.com/jboss-frameworks/cdi/interceptors-and-decorators-tutorial

## DI: Scopes and Contexts

https://docs.oracle.com/javaee/6/tutorial/doc/gjbbk.html  
* @RequestScoped
* @SessionScoped
* @ApplicationScoped
* @Dependent
* @ConversationScoped


## DI: Producer, Disposer, Stereotypes, Events


## Spring

Bean scopes
* singleton
* prototype
* request 
* session 
* globalSession 

### Bean validtion: create custom validation

### Bean validation: organize validation in Validation Groups

https://docs.jboss.org/hibernate/validator/5.1/reference/en-US/html/chapter-groups.html

### Bean validation: integration with JPA

https://www.logicbig.com/tutorials/java-ee-tutorial/jpa/bean-validation.html


## [Deployment descriptor: Web Fragments](https://www.oracle.com/technetwork/javaee6overview-part2-136353.html)

Web fragments enable web frameworks to self-register, eliminating the need for you to register them through deployment descriptors.  


## DI containers (Spring/Google Guice/EJB3): configuration

http://spring-projects.ru/guides/lessons/lesson-2  
https://www.javacodegeeks.com/2017/11/difference-component-service-controller-repository-spring.html  

@Configuration  
@Bean - can be used both in @Configuration and @Component














