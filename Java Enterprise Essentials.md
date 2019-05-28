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







