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
* what is the difference between primitives and Object in Java?
* read about
  * basic Java language: types, operators
  * auto boxing/un-boxing
  * exceptions : what's the difference between Error/Exception/RuntimeException ?
  * package : different modifiers public/private/protected/default
* String class
  * basic string manipulation (indexOf, lastIndexOf, trim, concat)
  * format to a String
* Cloneable interface
* Object methods

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

##### java.collections

##### java threads
* Runnable interface
* how to create threads
* Thread Executors

### Advanced stuff

##### Generics

##### use Maven to create a basic JAR
* download Maven
* make sure you have `M2_HOME` env variable set
* add `M2HOME/bin` to your `PATH` env variable
* read about
  * Maven repository
  * Maven default lifecycles
  * Maven JAR archetype
* create a Maven executable JAR project and run it
  * add JODA TIME 3rd party library and use it in your JAR, to show formatted current date to the console

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
