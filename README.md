# sabanci-it526-notes
## My Notes on Enterprise Java Course

- JPA nedir?

Object Oriented dünya ile Database’ler arasındaki bir katman. JPA JDBC üzerine konulmuş bir API katmanı ve bir soyutlama katmanı. Java Persistence API (Application Programming Interface). Hibernate JPA’nın implementasyonu.

- POJO nedir? 
  
Plain Old Java Object.

- Declarative yöntem nedir?
   
Nasıl yapılacağını sen söylersin gerisini framework hallede. XML gibi konfigürasyonlar kullanırsın.

- Entity nedir?
  
Classın Database tablosuyla konuşmasını sağlayan şey.

- What does Maven do? 
  
Dependency’leri yönetiyor. Build alıyoruz Maven’la. Kütüphaneleri path’imize eklememizi sağlıyor.

- pom.xml’i hangi taraf için kullanıyoruz?
   
maven dependency’leri yönetmek için kullanıyoruz.

- Primary key olarak neleri kullanabiliyoruz?
   
Primitive’leri kullanabiliyoruz.

- Persistence.xml’de neyi söylüyoruz?
   
Mesela MySql bağlantısını söylüyoruz.

- ORM nedir?
    
Object Relational Mapping. Java objesi ile Database tablosu arasındaki mapping. Entitymanager aracılığıyla DB’ye yeni kayıt eklemek istiyoruz diyelim. Save, update, insert, read işlemini entitymanager vasıtasıyla sağlıyoruz.

- String Common Pool ya da String Literal Pool nedir?
    
Memory common bir Alan var stringler var. Eğer atamak istediğin string poolda varsa nesne gider poolda olan yeri gösterir.

- JPQL nedir? (HQL)
    
Java Persistence Query Language - Hibernate Query Language

- Aggregation ve Composition farkı nedir?
    
Composition —-> Ev Oda ——- Ev olmadan odanın bir anlamı yok. 

Aggregation —-> Araba Yolcu ——- Birbirine bağlılıkları yukarıdaki kadar derin değil.

- Cascade nedir SQL’de?
    
In SQL, the term "cascade" refers to the automatic propagation of operations from one table to related tables. Specifically, when a particular operation is performed on a row in a table, such as a delete or update operation, the cascade feature will automatically perform the same operation on all related rows in other tables that are connected to the original table through a foreign key constraint.
    For example, if you have two tables, "orders" and "order_items", and there is a foreign key constraint between them such that each "order_items" row is associated with an "orders" row, then a delete operation on an "orders" row with the "CASCADE" option specified will also delete all related "order_items" rows. This can simplify database management and ensure data consistency. However, it should be used with caution to avoid unintended data loss.

- Bean nedir?
    
Standart Java sınıflarımızla aynı aslında. Bean Spring tarafından yönetilen Java sınıflarıdır.

- AOP nedir? (Eklemedim, buna bak)
    
Aspect Oriented Programming. Separation of Concerns denilen durumlar vardır. Buna bakabilirsin. Interceptor’lar ile yönetiyoruz bunları da.

- IoC nedir?
    
Inversion of Control. Bir obje construct etmiyoruz, Spring’i IoC container’ına veriyoruz. Biz sadece runtime’da referansını tanımlıyoruz. Kontrolü Spring’e devrediyoruz.

- Dependency Injection nedir?
    
In the context of Spring Boot, Dependency Injection (DI) is a design pattern that allows developers to write loosely coupled code by allowing Spring to manage the dependencies between classes. In Spring Boot, DI is achieved through the use of the Inversion of Control (IoC) container.
    The IoC container is responsible for managing the dependencies between classes. When a class requires a dependency, the container injects the dependency into the class, allowing the class to use it without having to create an instance of the dependency itself. This allows for more modular and maintainable code, as dependencies can be easily swapped out and updated.

- Spring boot, plain Spring arasındaki fark nedir?
    
Spring and Spring Boot are both frameworks for building Java applications, but they differ in their approach and purpose. Spring is a modular framework for building enterprise-level applications in Java. It provides various modules for different functionalities such as Spring Core, Spring MVC, Spring Data, Spring Security, etc. Spring provides a lot of flexibility and customization options, but it also requires a significant amount of configuration.
    Spring Boot, on the other hand, is an opinionated framework built on top of the Spring framework that simplifies the configuration and setup process. Spring Boot comes with preconfigured settings for various Spring modules, making it easy to get started quickly. It also includes an embedded server, so you can run your application without needing to deploy it to an external server.
    In summary, Spring Boot is an opinionated framework that provides a streamlined approach to building Spring applications, while Spring provides more flexibility and customization options.

- @Autowired nedir?
    
In the Spring Boot context, @Autowired is an annotation used for automatic dependency injection. When a class is annotated with @Autowired, Spring Boot will automatically search for a matching bean in the application context and inject it into the class.
    For example, if a class has a dependency on another class that is also defined as a bean in the application context, Spring Boot will automatically inject an instance of that bean into the class. This helps to reduce boilerplate code and allows for more efficient development.

- Annotationlar nasıl kullanılıyor? (Anlamadım buna bak)


- Springboot’un default @Scope’u nedir?
    
Singleton: This is the default scope in Spring. When a bean is defined with the singleton scope, Spring creates only one instance of the bean and reuses it throughout the application.

- HTTP nedir?
  
HTTP stands for Hypertext Transfer Protocol, which is a protocol used for communication between web servers and web clients (browsers). It is the foundation of data communication for the World Wide Web.
    HTTP is an application layer protocol, which means it defines how messages are formatted and transmitted between web servers and clients. It uses a request-response model where the client sends a request to the server, and the server responds with the requested data.
    HTTP uses a set of standard methods or verbs, including GET, POST, PUT, DELETE, HEAD, and OPTIONS, to indicate the type of action being requested by the client. The responses sent by the server include status codes, which indicate the success or failure of the request.
    HTTP is a stateless protocol, meaning that each request sent by the client is independent of any previous request. However, there are mechanisms, such as cookies and session management, that allow web servers to maintain stateful interactions with clients.

- REST nedir?
    
REST (Representational State Transfer) is an architectural style for designing web services. It defines a set of constraints that should be followed while creating web services to promote scalability, simplicity, and modifiability.

A RESTful web service follows the client-server architecture and is stateless, meaning each request from the client must contain all the necessary information for the server to fulfill the request. The server responds with the requested data in a format that can be understood by the client, usually JSON or XML.

REST uses HTTP methods, such as GET, POST, PUT, and DELETE, to perform operations on resources, which are identified by URIs (Uniform Resource Identifiers). For example, a GET request to http://example.com/customers/1 retrieves information about the customer with ID 1.

In a RESTful architecture, resources are represented as nouns, and actions are represented as verbs. For example, a resource could be a customer, and actions could be GET (retrieve), POST (create), PUT (update), and DELETE (delete). By following this convention, RESTful web services become easy to understand, predictable, and consistent.

- HTTP methodları nelerdir?
    
GET / POST / PUT / DELETE

- Get, Post farkı nedir?
    
GET and POST are HTTP methods used to perform operations on resources in a web service. The main difference between GET and POST is how the data is transmitted:
    GET requests are used to retrieve data from a server. Data is transmitted as a query string appended to the URL. GET requests are typically used for safe operations that do not modify data on the server, such as retrieving information about a resource.
    POST requests are used to submit data to a server. Data is transmitted in the body of the request. POST requests are typically used for operations that modify data on the server, such as creating or updating a resource.
    Another important difference is that GET requests can be cached by the client or intermediary servers, while POST requests cannot. This means that GET requests are faster and more efficient for retrieving frequently accessed data, while POST requests are more secure and appropriate for sending sensitive data or modifying data on the server.
    In general, it is important to use the appropriate HTTP method for the type of operation being performed in order to ensure that the web service functions correctly and efficiently.
- REST Architecture nedir?
    
Stateless architecture. Request yolladın response dönüyor, uygulama bunda bir state tutmuyor. Spring boot da bu kapsamda. Log tutmazsan geçmiş olsun.

- Rest ve SOAP farkı nedir?
    
REST (Representational State Transfer) and SOAP (Simple Object Access Protocol) are two popular web service architectures used for building distributed applications. Here are the main differences between the two:

Architecture: REST is an architectural style while SOAP is a protocol.
Data Format: REST uses a lightweight data exchange format such as JSON or XML while SOAP uses XML.
Messaging Pattern: REST uses a stateless client-server model, while SOAP uses a stateful messaging protocol with request-response message exchange pattern.
Transport Protocol: REST typically uses HTTP while SOAP can use a variety of protocols such as HTTP, SMTP, or JMS.
Ease of Use: REST is simpler and easier to implement and understand than SOAP.
Performance: REST is faster and more efficient than SOAP as it uses smaller message formats and has less overhead.
In summary, REST is a lightweight and efficient architecture for building web services, while SOAP is a more heavyweight and feature-rich protocol that is better suited for enterprise-level applications with complex security and transactional requirements.

- HTTP status code’ları nelerdir?
    
HTTP status codes are three-digit numbers that are sent by web servers to web clients in response to a request for a resource. They indicate the status of the request and the outcome of the server's attempt to fulfill it. The status codes are grouped into five categories:

1xx Informational: The request was received, and the server is continuing to process it.

2xx Success: The request was successful, and the server has delivered the requested resource.

3xx Redirection: The requested resource is not available at the requested location, and the client should try a different location.

4xx Client Error: The request was malformed or invalid, and the server cannot process it.

5xx Server Error: The server encountered an error while attempting to fulfill the request.

Some of the most commonly encountered HTTP status codes include:

200 OK: The request was successful and the requested resource was delivered.
301 Moved Permanently: The requested resource has been permanently moved to a new location.
400 Bad Request: The request was malformed or invalid, and the server cannot process it.
404 Not Found: The requested resource could not be found on the server.
500 Internal Server Error: The server encountered an error while attempting to fulfill the request.
HTTP status codes are useful for developers and system administrators, as they provide information about the success or failure of requests and can be used for debugging and troubleshooting.

- Rest endpoint naming convention’ları nelerdir?
    
The conventions generally recommend using plural nouns to represent resources, avoiding verbs in URI, using hyphen or underscore as word separators, and including version information in the URI. For example, a URI for a collection of customers might be /api/v1/customers, and a URI for a specific customer might be /api/v1/customers/{customer_id}.

- Spring boot nedir?
    
Spring ekosisteminde bir frameworktür. Onun soyutlamasını sağlıyor. Spring boot is not an application server.

- Clone ile fork arasındaki fark nedir?
    
In Git, both Clone and Fork are used to create a copy of a repository, but there are some differences:
    Clone:
    Creates a copy of an existing repository on your local machine.
    You can make changes to the code and push them back to the original repository.
    You have read/write access to the repository.
    You are not associated with the original repository or its owner.
    Fork:
    Creates a copy of an existing repository on a remote server (e.g., GitHub).
    You can make changes to the code and push them back to the original repository through a pull request.
    You have read/write access to the forked repository.
    You are associated with the forked repository and can manage it (e.g., add collaborators, change settings).

- Jar neyin kısaltması?
    
Java Archive

- Restful uygulama nedir?
    
Server client arasında data gidip gelmesi lazım. Bu datanın standart protokollerinden biri. Http üzerinden koşabilir. Json objeleri geçer rahatlıkla. SOAP gibi xml kullanabilirsiniz. Doküman transferi de yapabilirsiniz.
    Spring web’i de bunu sağlamak için seçiyoruz.

- Rest’in alternatifi nedir?

    
GraphQL: A query language for APIs that allows clients to specify exactly what data they need and get only that data in a single request.
    
gRPC: A high-performance, open-source framework that uses protocol buffers for message serialization and provides a more efficient way of communicating between microservices.
    
Falcor: A JavaScript library that allows developers to retrieve and manipulate JSON data on the client side without needing to write manual AJAX requests.
    
SOAP: A protocol that uses XML for message exchange and provides more features than REST, such as security, transaction management, and message validation.
    
JSON-RPC: A lightweight protocol for remote procedure calls that uses JSON for message serialization and provides a simpler alternative to SOAP.
    
OData: A REST-based protocol that allows for the querying and manipulation of data from various sources using a standardized syntax and set of conventions.

- Rest’i hangi projelerde kullanırsın?

REST is generally preferred for projects that prioritize simplicity, scalability, and flexibility. It is a lightweight and efficient architecture that uses a stateless client-server model, making it ideal for building web services that need to handle large amounts of data traffic. REST is also a good choice when working with resource-centric applications, where resources are represented as nouns and actions are represented as verbs.
SOAP, on the other hand, is preferred for projects that require more advanced features such as complex security, reliable messaging, and distributed transactions. It is a feature-rich protocol that uses a stateful messaging model with request-response message exchange pattern. SOAP can also use a variety of transport protocols, making it a more flexible option for distributed applications that need to communicate across different networks.
In summary, REST is a simpler and more flexible option that is ideal for building lightweight web services, while SOAP is a more advanced protocol that is better suited for enterprise-level applications with complex security and transactional requirements.

- HTTP default portu nedir?
    
8080

- Https default portu nedir?
    
443

- Apache Tomcat nedir?

    Apache Tomcat, also known as Tomcat Server, is an open-source web server and servlet container developed by the Apache Software Foundation. It provides a platform for running Java-based web applications by implementing the Java Servlet, JavaServer Pages (JSP), and WebSocket specifications.

    Tomcat is a lightweight and fast web server that can be used as a standalone server or integrated into larger enterprise solutions. It is widely used in enterprise-level applications for hosting web applications, including e-commerce sites, content management systems, and other web-based software.
    Tomcat is also highly configurable, with a range of features and options that can be customized to meet specific application requirements. It is cross-platform, running on Windows, Linux, and other operating systems, and can be integrated with other Apache projects, such as Apache HTTP Server, to provide a complete web hosting solution.

- Tomcat Spring olmadan çalışır mı?
    
Çalışır abi başka uygulamadır bu.

- In the Default Lifecycle, what are phases in Maven?
    
clean: target klasörünü siler.
    
validate: javanın beklediği yapıyı sağlıyor muyuz diye check eder.
compile: compile eder zaten.
    
test: kodu test eder. Test klasörünün altındaki testleri veya ekstra testler yazdıysak onları bu test fazında koşarız. Sadece unit testleri koşuyor.
    
package: jar, bor, ear paketlerinden herhangi birine paketler. Biz hangisini istiyorsak.
    
verify: entegrasyon testlerini koşar.
    
install: mevcut artifacti pc’ne indiriyor. Lokale indiriyor.
    
deploy: maven sadece dependency’lerle uğraşmaz. Deploy plug-in’leriyle birlikte deploy işine de yarıyor maven.
- Uberjar, fatjar nedir?
    
Uberjar and fatjar are both ways of packaging Java applications that include all the necessary dependencies in a single, self-contained JAR (Java Archive) file. This makes it easier to distribute and deploy the application, as there is no need to manage separate dependencies or classpath configurations.
    
The term "uberjar" is often used to refer to a JAR file that includes all the application's classes and dependencies, but does not include any of the classes or resources from the application's runtime environment.
    
The term "fatjar", on the other hand, is often used to refer to a JAR file that includes not only the application and its dependencies, but also any necessary classes or resources from the runtime environment (such as servlet containers or other libraries).
    
In general, the term "uberjar" is used more frequently in the context of build tools like Maven and Gradle, which provide specific plugins to create an uberjar. The term "fatjar", on the other hand, is often used more generally to describe any self-contained JAR file that includes all dependencies and runtime resources.

- Install ve package arasındaki fark nedir?
    
Install, artifactini lokal bilgisayarına gider, otomatik olarak .m2 uzantılı bir dosyaya download eder. Cache’liyor aslında. Sürekli internete gitmemek için.
- Spring frameworkünün lifecycle’ı nedir? (Anlamadım buna bak)


- Servlet nedir? (Anlamadım buna bak)
    
Kurumsal java mimarilerinin temelidir. Servlet java sınıfıdır. Spring de servletlerden oluşuyor. Http requestlerini karşılayan ve bunlara response’lar dönen classlardır.

A servlet is a Java program that runs on a web server and dynamically generates web pages by responding to requests from web clients. It is a Java class that extends the functionality of a web server and provides a platform-independent way of building web-based applications.

When a client sends a request to the server, the server passes the request to the appropriate servlet based on the URL of the request. The servlet then processes the request, generates a response, and sends it back to the client. Servlets are often used to implement web applications that require dynamic content generation or interaction with databases.
Servlets conform to the Java Servlet API, which provides a standard interface for developing servlets. The API defines methods for handling requests and responses, managing sessions and cookies, and other tasks required for building web applications. The most commonly used servlet containers are Apache Tomcat, Jetty, and GlassFish.

- API’nin diğer isimleri nelerdir?
    
Service ve Endpoint.

- Browser ne isteği üretir linke gittiğimizde?
    
GET.

- JSON ?
    
JavaScript Object Notation.

- What is DAO?
    
DAO stands for Data Access Object, which is a design pattern used in software engineering to abstract the communication with a database or other persistent storage mechanism. The DAO pattern separates the data access logic from the business logic and provides a layer of abstraction between them.
    
In Java, DAO is commonly used with JDBC to provide a way to interact with a database. The DAO class encapsulates the details of the underlying database access and provides a simple interface for other parts of the application to access and manipulate data.
    
By using the DAO pattern, it becomes easier to change the database implementation without affecting the rest of the application. This pattern also makes it easier to test the application, as the DAO can be mocked or stubbed out to simulate database access during unit testing.

- Checked - Unchecked Exception farkı nedir?

Checked exceptions are those that are checked at compile-time. This means that the Java compiler checks to make sure that any method that throws a checked exception either handles the exception using a try-catch block or declares that it throws the exception using the "throws" keyword. Examples of checked exceptions include IOException and SQLException.

On the other hand, unchecked exceptions are not checked at compile-time. This means that the Java compiler does not force the programmer to handle or declare these exceptions. Examples of unchecked exceptions include NullPointerException and ArrayIndexOutOfBoundsException.

In summary, the main difference between checked and unchecked exceptions is that checked exceptions are checked at compile-time and must be handled or declared, while unchecked exceptions are not checked at compile-time and do not need to be handled or declared.

- Exception handling basic syntax’ı nedir?

        try {
        // code that might throw an exception
        } catch (ExceptionType e) {
        // code to handle the exception
        } finally {
        // code to be executed regardless of whether an exception is thrown or not
        }

In this syntax, the finally block is executed after the catch block and before the try-catch statement completes. The code in the finally block is usually used to release resources that were acquired in the try block, such as closing a file or a database connection.

- PathVariable ve RequestParam arasındaki fark nedir?

@PathVariable is used to extract data from the path portion of the URL, and it is annotated on a method parameter. For example, if you have a URL like /user/123, where 123 is the user ID, you can extract the user ID using @PathVariable("id") int id. The value of id will be set to 123 in this case.

On the other hand, @RequestParam is used to extract data from the query string portion of the URL, and it is also annotated on a method parameter. For example, if you have a URL like /search?q=spring+framework, you can extract the search query using @RequestParam("q") String query. The value of query will be set to "spring framework" in this case.

In summary, @PathVariable is used to extract data from the path portion of the URL, while @RequestParam is used to extract data from the query string portion of the URL.

- Char tek tırnak mı çift tırnak mı?
    
Tek tırnak

- @RequestBody anotasyonu nedir?
    
In Spring Boot, @RequestBody is an annotation used to indicate that a method parameter should be bound to the body of the HTTP request. When a REST API receives an HTTP request with a JSON or XML payload in the body, @RequestBody can be used to map the JSON or XML request body to a Java object.

- Postman nedir?
    
Http client.

- Niye repository annotationını kullanıyoruz?
    
Database hatalarını daha detaylı ve temiz bir şekilde gösteriyor.

In Spring, the @Repository annotation is used to indicate that a class is a repository or data access object (DAO) component.

The main purpose of using the @Repository annotation is to provide an interface between the application code and the persistence layer. The repository layer provides a set of methods to access, persist, and manage data from the database.

By using the @Repository annotation, Spring automatically creates an instance of the annotated class that can be injected into other Spring components using the @Autowired annotation.

Additionally, the @Repository annotation provides some other benefits, such as exception translation, which translates any SQL exception into a more user-friendly Spring-specific exception, making it easier to handle exceptions in the application.

- CRUD nedir?

CRUD stands for Create, Read, Update, and Delete. It is a set of basic operations that are commonly used in databases and other data storage systems. These operations are used to manage data and perform basic data manipulation tasks. The basic idea behind CRUD is to provide a simple and standard way of managing data in a system. The Create operation is used to create new data, the Read operation is used to retrieve existing data, the Update operation is used to modify existing data, and the Delete operation is used to remove existing data.

- JDBC nedir?

JDBC stands for Java Database Connectivity. It is a standard API for connecting Java applications to a database. With JDBC, developers can write Java code that can interact with any relational database that supports JDBC.
