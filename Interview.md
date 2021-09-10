# Java

1. How Java achieves platform independence? (Hint:  bytecode and Java Virtual Machine)
2. What is `ClassLoader` in Java? (Hint: part of JVM that loads bytecodes for classes)
3. Difference between `ArrayList` and `HashSet` in Java? (Hint: ordering, duplicates, random search, etc.)
4. Difference between Serializable and Externalizable in Java? (Hint: Externalizable gives you more control over the Serialization process)
5. Can we override the `private` method in Java? (Hint: No, because it's not visible in the subclass, a primary requirement for overriding a method in Java)
6. Difference between wait and sleep in Java? (Hint: The `wait()` method releases the lock or monitor, while sleep doesn't)
7. Difference between `notify` and `notifyAll` in Java? (Hint: `notify` notifies one random thread is waiting for that lock while `notifyAll` inform to all threads waiting for a monitor. If you are certain that only one thread is waiting then use `notify`, or else `notifyAll` is better)
8. Why you override `hashCode()`, along with `equals()` in Java? (Hint: to be compliant with equals and hashcode contract, which is required if you are planning to store your object into collection classes, e.g. `HashMap` or `ArrayList`)
9. Difference between Polymorphism and Inheritance in Java? (Hint: Inheritance allows code reuse and builds the relationship between class, which is required by Polymorphism, which provides dynamic behavior)
10. Difference between checked and unchecked Exception in Java? (Hint: In case of checked, you must handle exception using catch block, while in case of unchecked, it's up to you; compile will not bother you)
11. Difference between race condition and deadlock in Java? (Hint: both are errors that occur in a concurrent application, one occurs because of thread scheduling while others occur because of poor coding)

# Spring Boot

1. What Are the Basic Annotations that Spring Boot Offers?

   The primary annotations that Spring Boot offers reside in its `org.springframework.boot.autoconfigure` and its sub-packages. Here are a couple of basic ones:

   `@EnableAutoConfiguration` – to make Spring Boot look for auto-configuration beans on its classpath and automatically apply them.

   `@SpringBootApplication` – used to denote the main class of a Boot Application. This annotation combines `@Configuration`, `@EnableAutoConfiguration`, and `@ComponentScan` annotations with their default attributes.

2.  Can we create a non-web application in Spring Boot?

   Yes, we can create a non-web application by removing the web dependencies from the `classpath` along with changing the way Spring Boot creates the application context.

3. How to disable a specific auto-configuration class?

   You can use exclude attribute of `@EnableAutoConfiguration` if you want auto-configuration not to apply to any specific class.

   ```java
   @EnableAutoConfiguration(exclude={className})
   ```

4. Explain `@RestController` annotation in Sprint boot?

   It is a combination of `@Controller` and `@ResponseBody`, used for creating a restful controller. It converts the response to JSON or XML. It ensures that data returned by each method will be written straight into the response body instead of returning a template.

5. Describe the flow of HTTPS requests through the Spring Boot application?

   <img src="https://s3.ap-south-1.amazonaws.com/myinterviewtrainer-domestic/public_assets/assets/000/000/247/original/Spring_Boot_Flow_Architecture.png?1616151707" alt="img"  />

   6. Why Spring Boot over Spring?

      Below are some key points which spring boot offers but spring doesn’t:

      - Starter POM.
      - Version Management.
      - Auto Configuration.
      - Component Scanning.
      - Embedded server.
      - InMemory DB.
      - Actuators

      Spring Boot simplifies the spring feature for the user:

      <img src="https://s3.ap-south-1.amazonaws.com/myinterviewtrainer-domestic/public_assets/assets/000/000/245/original/Difference_Between_Spring_and_Spring_Boot.png?1616150564" alt="img" style="zoom: 20%;" />

      7. What is the difference between `@RequestMapping` and `@GetMapping`?

         RequestMapping can be used with GET, POST, PUT, and many other request methods using the method attribute on the annotation. Whereas getMapping is only an extension of RequestMapping which helps you to improve on clarity on request.

      8. What is the use of Profiles in spring boot?

         While developing the application we deal with multiple environments such as dev, QA, Prod, and each environment requires a different configuration. For eg., we might be using an embedded H2 database for dev but for prod, we might have proprietary Oracle or DB2. Even if DBMS is the same across the environment, the URLs will be different.

         To make this easy and clean, Spring has the provision of Profiles to keep the separate configuration of environments.

      9. What is dependency Injection?

         The process of injecting dependent bean objects into target bean objects is called dependency injection.

         - Setter Injection: The IOC container will inject the dependent bean object into the target bean object by calling the setter method.
         - Constructor Injection: The IOC container will inject the dependent bean object into the target bean object by calling the target bean constructor.
         - Field Injection: The IOC container will inject the dependent bean object into the target bean object by Reflection API.

      10. What is an IOC container?

          IoC Container is a framework for implementing automatic dependency injection. It manages object creation and its life-time and also injects dependencies into the class.



### Additional

https://www.marcobehler.com/guides/spring-boot-interview-questions





# React.js

### Additional

https://www.simplilearn.com/tutorials/reactjs-tutorial/reactjs-interview-questions

https://www.fullstack.cafe/blog/react-js-interview-questions

# CI/CD