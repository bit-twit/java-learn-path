java-learn-path
===============

# A reading list for Java beginners

### Basic stuff

##### setup 
* download Java (make sure you get the 32bit/64bit depending on your machine)
* make Java executable accesible from everywhere on your system
  * make sure you have `JAVA_HOME` env variable
  * make sure you have `JAVA_HOME/bin` added to your `PATH` env variable
  * try java/javac to compile/run a simple "hello world" file :
  ```java
  public class SimpleMain {
    public static void main (String... args) {
      System.out.println("Hello world!");
    }
  }
  ```

##### java.lang
* what's the difference between procedure/function/method ?
* what is the difference between primitives and objects in Java?
* read about
  * basic Java language: types, operators
  * auto (un)boxing
  * how to implement hash/equals
  * exceptions : what's the difference between Error/Exception/RuntimeException ?
  * package : different modifiers public/private/protected/default
* `String` class
  * basic string manipulation (indexOf, lastIndexOf, trim, concat)
  * format to a String
* `Enum` class
 * how to use Enum in a switch statement
 * how to get an Enum by name
 * how to create enums with custom fields
* `Cloneable` interface
* `Object`'s methods
* polymorphism
 * override: rules for overriding a method; what happens to exceptions ?
 * overload: rules for overloading
 * interfaces/abstract classes
 * types of inner classes
 * `{}` and `static {}` constructs
 * class hierarchies
  * what happens with the scope of private/protected variables defined in parent/child hierarchy
  * `is a` VS `has a`
* Patterns
 * Singleton
 * Factory
 * Builder
 * Command
 * Facade
 * Proxy
 * Decorator

##### JUnit
* create JUnit tests using Eclipse
* use JUnit for the examples in the next sections
  * make small tests to run examples of what you read

##### java.io
* Input/OutputStream
* PrintWriter
* File - read/write to a file
* loading files from classpath

##### java.util
* Pattern and Matcher classes - build some regular expression examples
* why are hash and equals important, especially for collections
* basic collection types and hierachies
 * Set
 * Map
 * List
 * Array
 * Vector
 * Queue
* Calendar class : how to get current date, how to get date based on timezone

##### java.util.concurrent
* Runnable interface
* how to create threads
* Executors

### Advanced stuff

##### Generics
* how does type erasure works
* implement generic class hierarchies

##### use Maven to create a basic JAR
* download Maven
* make sure you have `M2_HOME` env variable set
* add `M2HOME/bin` to your `PATH` env variable
* read about
  * Maven repository
  * Maven default lifecycles
  * Maven JAR archetype
* create a Maven executable JAR project and run it
* Mini-projects
  * add JODA TIME 3rd party library and use it in your JAR, to show formatted current date to the console
  * add JOG4J and SJFJ in your pom.xml and use it throughout your code
  * add tests for your code
  * add commons packages from Apache to your project and add code/tests for various functions
  * add JAXB dependency and use it to parse a simple XML file/content
  * add Jackson dependency and use it to parse simple JSON file/content

##### JVM memory management
* what is a classloader
* what is a garbage collector
* how are objects created/kept in Java memory at runtime [GC tuning](http://www.oracle.com/technetwork/java/javase/gc-tuning-6-140523.html)
  * what is tenure/eden space ?
  * what is perm gen space ?
* basic JVM params:
  * to increase heap
  ```
  -Xmx512m
  ```
  * to increase perm gen size
  ```
  -XX:MaxPermSize=128M
  ```
  * to connect in debug mode

### JEE stuff

###### use Maven to create a basic WAR application
* download Maven
* download Tomcat
* create a new WAR archetype application
  * read about
    * web.xml file 
    * WEB-INF/classes folder
    * Tomcat `<Context>` [here](http://tomcat.apache.org/tomcat-7.0-doc/config/context.html) 
    * Servlet lifecycle
      * make a simple servlet that handles Get/Post
      * test it with simple request, make it print parameters received
    * create a basic JSP file
      * how is the JSP loaded/handled by the Servlet Container
      * use JSTL tags to create a simple form in JSP and make it Post to your previously defined servlet

##### Spring
* create a new WAR project
* add Spring as dependency
* create a simple HelloWorld example (Controller, JSP, etc) with Spring
* read about:
  * what is dependency injection
  * Spring Context
  * Spring Beans
  * how does Spring handle exception (wraps compile-time exception to Runtime Exceptions)
  * Spring MVC
    * default beans instantiated by Spring (Resolvers, Converters, MessageContext, etc.)
    * how is the view handled by Spring (JSTL, URL, Tiles)
 * Spring Transaction support
    * add JPA and Hibernate to your project
    * add a DB (Postgresql) with a simple table to your project
    * add a Repository class to your project (Ex: UserRepository)
    * make a Service class and annotate it with @Transactional
    * show some objects from your service class in your JSP through your Controller
    * read about:
      * transaction support at DB level (Postgresql)
        * tables and PK/FK 
        * different types of relations
        * simple queries (SELECT,WHERE, INNER/OUTER JOIN, GROUP BY, )
        * ACID
      * JPA/JQL
      * Spring Transaction levels
      * ORM/Hibernate
      * Connection pool (c3p0, commons-pool, Tomcat 7 pool, dbcp)
  * EL language in JSP

### Frontend stuff

##### JS
* functions
* higher-order functions
* objects
* how to handle DOM events
 * event bubbling
* `eval()`
* scope of variables, global scope
* prototype
* extending objects
* `underscore.js`
* `angujar.js`

##### HTML
* basic HTML elements
* 

##### CSS
(TBD)

### Admin stuff
(TBD)

### Methodologies stuff
(TBD)

