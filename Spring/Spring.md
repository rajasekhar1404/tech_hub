### 1. What is Spring Framework?
- Spring framework is a opensource, light-weighted, loosely-coupled framework for java based applications
### 2. What are the key features of Spring ?
- Spring is a loosely-coupled ,
- easy to test
- Spring provides AOP
- Spring security
- Spring Data
- Spring Batch
### 3. What are the modules Spring Supports?
-  Spring supports various modules they are :
- Test
- spring  Core Container : (core, beans, Context, Expression Language )
- AOP,Messaging , Aspects, Instrumentation
- Data Access/Integration :(JDBC, ORM, ORX, JMS), Transactions
- Web(MVC/ Remoting) :(Web, Servlet, Portlet, webSocket)
### 4. Explain about IOC container in Spring?
- Inversion of Control(IOC) : Ioc is  a design pattern where the control of object creation and dependency injection is shifted from application code to container , 
- In Spring Ioc  is responsible for creating objects and configure instance and assembles their dependencies
- There are two types of Ioc containers they are :
- Bean Factory, Application Context
### 5. What is the difference between Bean Factory and Application Context?
-  Bean Factory and Applications Context both are used for managing and accessing the beans but the major differences are :
- Bean Factory is a basic interface for managing and accessing the beans Where Application Context extends the Bean Factory which provides some additional features
#### Eager and Lazy loading : 
- Bean Factory   : Beans are loaded lazily , beans are only created when ever they are requested for the first time
- Application Context :  Application Context supports Eager Loading if we want load lazily we need to specify them explicitly by marking bean as lazy-initialized
#### Application Context Awareness:
- Bean Factory : Bean Factory itself doesn't aware of the specific application context in which it operates
- Application Context : it aware of which specific application context operates and it provides the additional services like resources loading and event publishing
#### Integration with Spring Apo :
- Bean Factory : it integrate with APO but it requires explicit configurations
- Application Context :it integrates ith APO and it automatically detects
### 6.Explain about Dependency Injection?
- Dependency Injection is a technique for achieving the loosely coupled in Spring
- there are three types of Dependency Injection . they are : Constructor Injection, Setter Injection, Method Injection
#### Constructor Injection:
- Dependencies are provided to a class through class constructor 
- Constructor Injection are ensures that the dependencies are explicitly stated and cannot be changed once they are created 
#### Setter Injection :
- Dependencies are provided through the setter method , setter injection allows flexibility can be change or update at run time 
#### Method Injection:
- Dependencies are provided through specific method ,these are less common than Constructor and Setter Injection and useful in Specific Scenarios
#### Major difference b/w Constructor Injection and Setter Injection.
##### Constructor Injection: 
- No Partial Injection
- if both setter and constructor injections are provide constructor injection cannot override the setter
- it creates new instance if any modification occurs
- better for too many properties
##### Setter Injection: 
- partial injection
- they can override the Constructor 
- no need to create new instance whenever changes occurs
- better for few properties
### 7. What is autowiring in spring? What are the autowiring modes?
- AutoWire : it automatically injects the bean if it is present in container
- modes are :
- on : this is default model, it means autowiring is disabled
- byName : injects bean by property name uses in setter injection
- byType : injects bean through property type uses in setter injection
- constructor : injects bean using constructor
### 8. What are the different bean scopes in spring?
- There are 5 bean scopes in spring they are:
- Singleton : Bean instance will be  created  only once and same instance is returned to the ioc
- ProtoType : bean instance will be created each time when requested
- request : bean instance will be created per http request
- session :bean instance will be created per http session
- globalsession : bean instance will be created per http global session . it can used in portlet context only
### 9.  In which scenario, you will use singleton and prototype scope?
- singleton scope should be used in EJB stateless session bean 
- ProtoType scope used in EJB stateful session bean
### 10. What are the transaction management supports provided by spring?
- Spring supports 2 types Transaction
- Programmatic Transaction management: used for few transaction operations
- Declarative  Transaction Management : it used for many transactions operations
## Spring MVC Interview Questions
### 11. What is the front controller class of Spring MVC?
- Dispatcher Servlet is the front controller in spring mvc . 
- it receives the request from client and determine to appropriate controller
- controller performs appropriate actions and return ModelAndView
- View Resolver determine the appropriate view for rendering the response and this response go to the dispatch servlet 
### 12. What does @Controller annotation?
- @Controller annotation is used in spring mvc to make a class as a controller component which accepts the http requests and contains methods to process the requests
- it is applied at class level 
### 13. What does @RequestMapping annotation?
- @RequestMapping annotation used to map http request with the specific method 
- it is applied both for class and method level
- if it is applied for class level url is applied to every request in that controller 
- if it is applied at method level url is applied to specific method
### 14. What does the ViewResolver class?
- ViewResolver class resolves the view component invoked for the request . it defines suffix, prefix properties to resolve the view component
### 15. Which ViewResolver class is widely used?
- The org.springframework.web.servlet.view.InternalResourceViewResolver class is widely used.
### 16. Does spring MVC provide validation support?
- Yes
## Spring AOP Interview Questions
### 17.What is AOP?
- AOP stands for Aspect oriented programming 
- it is a methodology of breaking program code into pieces or parts or concerns
- it increase the modularity and key unit is aspect
### 18. What are the advantages of spring AOP?
- 