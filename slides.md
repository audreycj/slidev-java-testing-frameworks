---
# theme for all slides; choose here: https://sli.dev/themes/gallery.html#official-themes
theme: default

# background photo
background: "/assets/images/cat.jpeg"

# apply any windi css classes to the current slide
# https://windicss.org/features/
class: text-center

# tool used for highlighting code
highlighter: shiki

# show line numbers when showing code blocks
lineNumbers: true

# some information about the slides (you can write in markdown syntax)
info: |
    ## audrey's slidev template
    github: https://github.com/audreycj

# persist drawings in exports and build
drawings:
    persist: false

# slide transition
transition: slide-left

# use UnoCSS
css: unocss
---

# Java Unit Testing Frameworks, Libraries, and Tools

by Audrey Nanual

---
layout: center
---

### **Testing Framework**
-  a collection of reusable code that provides functionality to support unit testing, such as _assertion methods_, _mock objects_, or _test data generators_
- e.g. JUnit 5, Mockito, SpringFramework Testing, Spring Boot Testing, Selenide

<br>

### **Testing Library**
- a set of conventions and rules that define how tests are written, organized, and executed
- e.g. AssertJ, Data Faker, Easy Random, Easy Random JUnit Extension, ModelAssert, 

<br>

### **Testing Tool**
- a software application that helps developers automate and manage the process of testing software
- e.g. JUnit Pioneer, Database Rider, TestContainers, Instancio, JetBrains Aqua

<!-- 

**Testing Library**
- provides a structure for writing test cases and automates the process of executing them, reporting results, and providing feedback

**Testing Tool**
- ...providing functionality beyond what is available in testing libraries or frameworks

 -->

---
layout: center
---

# Frameworks, libraries, and tools for today

1. JUnit 5
2. JUnit Pioneer
3. AssertJ
4. Data Faker
5. Mockito
6. Easy Random
7. Easy Random JUnit Extension
8. Database Rider
9. ModelAssert
10. SpringFramework Testing
11. Spring Boot Testing
12. TestContainers
13. Instancio
14. Selenide
15. JetBrains Aqua

---
layout: center
---

# JUnit 5

“Powerful and flexible Java testing framework”

> Latest version of the popular Java testing framework, JUnit.

> Provides a range of new features and enhancements to help developers write more efficient, effective, and maintainable tests.

<style>
blockquote {
  code {
    @apply text-teal-500 dark:text-teal-400;
  }
}
</style>

<br>

1. Modular and extensible architecture
2. New programming model (i.e., @Nested, @ParameterizedTest, @DynamicTest)
3. Improved exception handling
4. Test templates
5. Parallel test execution
6. Improved reporting

<!-- 

**1. Modular and extensible architecture**
- Has a modular architecture that allows you to use only the parts of the framework that you need.
- Allows you to add your own custom extensions to the framework, making it more flexible and adaptable to your specific testing needs.

**2. New programming model**
- Includes annotations and interfaces for writing tests and test extensions.
- Allows for more flexible and expressive tests, with features like nested tests (_@Nested_), parameterized tests (_@ParameterizedTest_), and dynamic tests (_@DynamicTest_).
- 

**3. Improved exception handling**
- Provides a new _assertThrows()_ method that makes it easier to test for expected exceptions.
- This method takes a lambda expression and checks that it throws an exception of the specified type.

**4. Test templates**
- Includes a new _@TestTemplate_ annotation that allows you to define a test template that can be reused across multiple test cases.
- This can save time and reduce duplication in your tests.

**5. Parallel test execution**
- Supports parallel test execution, which can greatly reduce the time it takes to run your test suite.
- You can configure JUnit to run tests in parallel across multiple threads or processes, depending on your needs.

**6. Improved reporting**
- Provides more detailed and customizable test reports, with support for different output formats and styles.
- Can help you to better understand the results of your tests and identify areas for improvement.

 -->

---
layout: center
---

# JUnit Pioneer

“Making JUnit 5 testing simpler and more accessible”

> An open-source testing tool that extends JUnit 5 to provide additional testing features.

<style>
blockquote {
  code {
    @apply text-teal-500 dark:text-teal-400;
  }
}
</style>

<br>

1. Enhanced test reporting
2. Improved parameterized tests
3. Test fixtures with constructor injection
4. Enhanced test data management
5. Test isolation with separate class loaders

<!-- 

**1. Enhanced test reporting**
- Provides more informative test reporting than standard JUnit 5, with additional information such as the stack traces of all exceptions thrown during a test run.
- The test results can be easily customized to include the information that you need.

**2. Improved parameterized tests**
- Are more flexible and informative than in standard JUnit 5.
- Provide better test output and reporting.
- e.g. Test inputs and outputs can be automatically formatted and displayed in a readable format, making it easier to understand and debug tests.

**3. Test fixtures with constructor injection**

**_Test fixture_** — refers to the preparation of the environment, including the [1] creation of objects, [2] setting up the required data, and [3] defining the initial state of the system under test, to ensure that the test is executed in a known and controlled context. 

- Supports test fixtures with constructor injection, which allows for more flexible test setup and teardown.
- Enables you to declare constructor parameters and initialize them automatically before each test.
- Constructor injection can be used to set up objects that will be used in multiple tests.

**4. Enhanced test data management**
- Provides annotations and utilities for defining and managing test data, making it easier to write test cases that cover different scenarios.
- Allows you to define complex test data structures and manage them with ease.
- Can also help avoid code duplication by allowing you to reuse test data across multiple test cases.

**5. Test isolation with separate class loaders**

**_Class loader_** — responsible for finding and loading Java classes (from the file system, network or other sources) into memory as they are referenced by a Java program at runtime. 

- Allows you to run tests in separate class loaders, which can improve test isolation and reduce test execution time. 
- Allows you to run tests in parallel without having to worry about shared state or dependencies.
- Mkes it easier to test code that depends on external resources, such as databases or web services, by isolating the test environment from the production environment.

 -->

---
layout: center
---

# AssertJ

“Readable and comprehensive assertions for Java”

> A fluent assertions library for Java that provides a more

> readable and comprehensive way of writing assertions in unit tests.

<style>
blockquote {
  code {
    @apply text-teal-500 dark:text-teal-400;
  }
}
</style>

<br>

1. Fluent interface —— ❌ assertTrue(x > 0) | ✅ assertThat(x).isGreaterThan(0)
2. Type-specific assertions (i.e., collections, strings, dates, and exceptions)
3. Chained assertions
```java
assertThat(str)
      .startsWith("JUnit")
      .endsWith("framework")
      .contains("unit testing");
```
4. Soft assertions

5. Custom error messages

<!-- 

**1. Fluent interface**
- Allows you to write assertions that read like natural language statements.
- e.g. Instead of writing _assertTrue(x > 0)_, you can write _assertThat(x).isGreaterThan(0)_.

**2. Type-specific assertions**
- Provides specific assertion methods for different types of objects, such as collections, strings, dates, and exceptions
- Makes it easy to write assertions that are tailored to the specific types you are working with.

**3. Chained assertions**
- You can chain multiple assertions together using the and method.
- Allows you to perform multiple assertions on the same object in a single statement, which can make your tests more readable and concise.

**4. Soft assertions**
- Supports soft assertions, which allow you to continue running assertions even if one of them fails.
- Can be useful in cases where you want to report all the failures in a test, rather than stopping at the first failure.

**5. Custom error messages**
- Allows you to provide custom error messages for your assertions, which can make it easier to understand what went wrong when an assertion fails.

 -->

---
layout: center
---

# Data Faker

“Realistic data generation made easy”

> A Java library that generates realistic and randomized test data for a wide range of data types,

> allowing developers to quickly and easily populate their unit tests with diverse and comprehensive test data.

<style>
blockquote {
  code {
    @apply text-teal-500 dark:text-teal-400;
  }
}
</style>

<br>

1. Wide variety of data types
2. Localization support
3. Customization
4. Easy integration
5. High-quality data

<!-- 

**1. Wide variety of data types**
- Supports a wide range of data types such as names, addresses, phone numbers, dates, times, credit card numbers, and more.
- Makes it easy to generate realistic test data for a variety of applications.

**2. Localization support**
- Supports multiple languages and locales, which allows you to generate data that is specific to a particular country or region.
- e.g. You can generate names, addresses, and phone numbers that are specific to the United States, United Kingdom, or France.

**3. Customization**
- Provides a way to customize the generated data by specifying your own data patterns or by providing your own data sets.
- Is useful when you need to generate data that is specific to your application or domain.

**4. Easy integration**
- Can be easily integrated into your Java projects using Maven or Gradle.
- Provides a simple API that allows you to generate data programmatically in your Java code.

**5. High-quality data**
- Generates high-quality data that is realistic and conforms to common patterns and formats.
- Ensures that your tests are accurate, reliable, and comprehensive.

 -->

---
layout: center
---

# Mockito

“Mocking framework for unit testing in Java”

>  A Java mocking framework that allows developers to create mock objects, stub method behavior,

> and verify the interactions between objects in unit tests.

<style>
blockquote {
  code {
    @apply text-teal-500 dark:text-teal-400;
  }
}
</style>

<br>

1. Simple and intuitive syntax
2. Stubbing
3. Verification
4. Spying
5. Argument matching (i.e., exact matches, wildcard matches, and argument capture)
6. Annotation support (i.e., @Mock, @InjectMocks)
7. Ability to mock final classes and methods

<!-- 

**_Mock object_** — a test double that is configured to simulate the behavior of a real object, but without actually invoking its methods.

**Stub object_** — a test double that is configured to provide specific responses to method calls made by the unit under test.

They allow developers to isolate and control the behavior of dependencies, making it easier to test the functionality of individual units in a controlled environment.

==================

**1. Simple and intuitive syntax**
- Is designed to be simple and easy to read, even for developers who are new to mocking frameworks.
- Uses static methods to create and configure mock objects, which makes it easy to understand what is happening in your test code.

**2. Stubbing**
- Allows developers to create stubs for their mocked objects. 
- **Stubs** are methods that are used to simulate behavior or return values for the mocked object.
- Its flexible capabilities allow developers to configure the mock object to return a specific value, throw an exception, or execute custom code.

**3. Verification**
- Provides powerful verification capabilities that allow developers to check if certain methods or behaviors have been called on their mock objects.
- Can verify that a method was called with specific arguments, or that a method was called a certain number of times.

**4. Spying**
- Allows developers to create spies, which are mock objects that wrap around a real object.
- **Spies** allow developers to selectively mock or verify certain methods on the real object, while still executing the real implementation for other methods.
- Can be useful for testing complex objects or for selectively mocking parts of an object's behavior.

**5. Argument matching**
- Provides several ways to match arguments passed to mock methods, including exact matches, wildcard matches, and argument capture.
- Argument matching is important because it allows developers to test their code with a wide range of input data, without having to create a separate test case for each set of input data.


**6. Annotation support**
- Supports annotations, which allows developers to easily create and manage their mocks within their test classes.
- Provides several annotations, including _@Mock_, which is used to create a mock object, and _@InjectMocks_, which is used to inject mocks into a real object.

**7. Ability to mock final classes and methods**
- Supports the mocking of final classes and methods, which is not possible with many other mocking frameworks.
- Can be useful for testing code that relies on third-party libraries or external APIs, which may have final classes or methods.

 -->

---
layout: center
---

# Easy Random

“Flexible test data generation”

> A Java library that simplifies the process of generating randomized test data,

> making it easier to write comprehensive and efficient tests.

<style>
blockquote {
  code {
    @apply text-teal-500 dark:text-teal-400;
  }
}
</style>

<br>

1. Fluent interface
2. Customizable
3. Supports complex object generation
4. Supports a wide range of data types
5. Automatic configuration
6. Easy integration
7. Provide randomness control

<!-- 

**1. Fluent interface**
- Is easy to use and understand. It has a simple and intuitive interface that makes it easy to create random data for your Java code.

**2. Customizable**
- Lets you make your own custom data types, which means you can create data that is unique to your needs.
- You can customize Easy Random by telling it how to generate data. For example, you can tell it to make all strings between 5 and 10 characters long.

**3. Supports complex object generation**
- Can create complex objects with many different fields.
- You can make objects that have other objects inside them, like a person object that has an address object inside it.

**4. Supports a wide range of data types**
- Can create all kinds of data, like numbers, strings, dates, and even custom data types that you create yourself.

**5. Automatic configuration**
- can automatically configure itself based on the types of objects that need to be generated.
- You don't need to manually configure Easy Random for every object you need to generate.

**6. Easy integration**
- Is available on Maven Central and can be easily integrated into your Java projects using Maven, Gradle, or any other build tool that supports dependency management.

**7. Provide randomness control**
- You can control the randomness of the data that Easy Random generates.
- You can make sure that the same data is generated every time you run your code.

 -->

---
layout: center
---

# Easy Random JUnit Extension

“Seamless test data generation”

> An extension to the Easy Random library that integrates with JUnit 5 to generate random test data.

<style>
blockquote {
  code {
    @apply text-teal-500 dark:text-teal-400;
  }
}
</style>

<br>

1. @EasyRandom
2. @WithEasyRandom
3. @EasyRandomResource
4. @Randomizer
5. @Random
6. @RandomBean

<!-- 

**1. @EasyRandom**
- Used to tell the Easy Random JUnit Extension to create an instance of the tested class with randomized data.
- By using this annotation, you don't need to manually create test data for each test case.
- Instead, the Easy Random library will generate random values for the fields of the class.

**2. @WithEasyRandom**
- Used to specify the Easy Random configuration to use for a particular test method.
- Can be used to override the default configuration provided by the @EasyRandom annotation.

**3. @EasyRandomResource**
- Used to inject an instance of the EasyRandom class into a test class or test method.
- Allows you to use the Easy Random library directly in your test methods.

**4. @Randomizer**
- Used to specify a custom randomizer class for a particular field or type.
- A **_randomizer_** is a class that generates random values for a specific type.
- By using this annotation, you can provide your own custom logic for generating random values for a particular field.

**5. @Random**
- Used to generate a random value for a particular field.
- By default, the Easy Random library will generate random values for fields based on their type.
- However, you can use the @Random annotation to override the default behavior and specify a custom random value.

**6. @RandomBean**
- Used to generate a fully populated instance of a Java bean with randomized data.
- Particularly useful when you need to create complex objects with multiple fields and nested objects.
- By using this annotation, you can generate a random instance of a bean with a single line of code.


 -->

---
layout: center
---

# Database Rider

“Database testing made easy”

> A testing tool that provides support for testing database-related functionality in Java applications,

> allowing developers to create and manage test data and execute tests in an automated and repeatable manner.

<style>
blockquote {
  code {
    @apply text-teal-500 dark:text-teal-400;
  }
}
</style>

<br>

1. Supports multiple database types
2. Supports data-driven testing
3. Provides fluent API for database operations
4. Integration with JUnit and TestNG
5. Supports transaction management
6. Supports assertions on database state

<!-- 

**1. Supports multiple database types**
- Supports a wide range of database types, including MySQL, PostgreSQL, Oracle, and more.
- Allows developers to test their database-related code against a variety of different database platforms, ensuring that their code is portable and works correctly in different environments.

**2. Supports data-driven testing**
- Makes it easy to perform data-driven testing by allowing developers to define test data in external files such as CSV or XML. - This approach allows developers to easily manage large amounts of test data, and also makes it easy to add new test cases as needed.

**3. Provides fluent API for database operations**
- Provides a fluent API for interacting with the database, which simplifies the process of writing database-related test cases. - The API includes methods for performing CRUD (create, read, update, delete) operations on the database, as well as for executing SQL queries and scripts.

**4. Integration with JUnit and TestNG**
- Integrates seamlessly with popular Java testing frameworks such as JUnit and TestNG, allowing developers to easily incorporate database-related tests into their existing test suites.

**5. Supports transaction management**
- Provides support for transaction management, allowing developers to easily manage database transactions within their test cases.
- This helps ensure that test data is properly cleaned up after each test run, and also makes it easy to isolate individual test cases from one another.

**6. Supports assertions on database state**
- Provides a rich set of assertions that developers can use to verify the state of the database after a test has run.
- These assertions include checks for the existence of specific data, the number of rows returned by a query, and more.

 -->

---
layout: center
---

# ModelAssert

“Model-based testing”

> A Java testing library that allows developers to define models for objects and collections,

> and then use these models to assert that the state and behavior of objects and collections conform to expected models.

<style>
blockquote {
  code {
    @apply text-teal-500 dark:text-teal-400;
  }
}
</style>

<br>

1. Model-based testing with graphs
2. Domain-specific assertions
3. Value object testing
4. Flexible model definition
5. Data-driven testing
6. Lightweight and easy to use

<!-- 

**_Model_** — refers to an object model, which is a set of classes and objects that represent a system, component, or application. The model contains properties, methods, and behaviors that describe the characteristics and functionality of the system being modeled.

**1. Model-based testing with graphs**
- Provides a model-based testing approach that allows you to specify the expected behavior of your code using a graph-based representation.
- This approach allows you to visualize and reason about the behavior of your code in a more intuitive way.

**2. Domain-specific assertions**
- Provides a set of domain-specific assertions that are tailored to specific domains.
- e.g. There are assertions for checking the behavior of collections, assertions for checking the behavior of time-based operations, and so on.
- By using domain-specific assertions, you can write more expressive tests that are easier to read and understand.

**3. Value object testing**
- Provides support for testing value objects, which are objects that are defined by their values rather than their identity.
- Value objects are often used in domain-driven design to represent concepts such as money, dates, and times.
- By providing value object testing support, ModelAssert can help you ensure that your value objects behave correctly in all scenarios.

**4. Flexible model definition**
- Provides a flexible model definition approach that allows you to define your models in a way that suits your needs.
- You can define your models using plain Java objects, or you can use a fluent API to define your models in a more concise and expressive way.

**5. Data-driven testing**
- Provides support for data-driven testing, which allows you to test your code with multiple sets of input data.
- By using data-driven testing, you can ensure that your code behaves correctly for a range of input values and edge cases.

**6. Lightweight and easy to use**
- Is a lightweight testing library that is designed to be easy to use.
- Has a small footprint and minimal dependencies, making it easy to integrate into your existing testing framework.
- Also provides clear and concise error messages that make it easy to diagnose and fix issues in your tests.

 -->

---
layout: center
---

# SpringFramework Testing

“Simplified testing of Spring applications”

> Provides support for testing Spring-based applications, including unit testing, integration testing, 

> and end-to-end testing, using a variety of testing frameworks and tools.

<style>
blockquote {
  code {
    @apply text-teal-500 dark:text-teal-400;
  }
}
</style>

<br>

1. Integration testing
2. Mock objects
3. Dependency injection
4. Annotations (i.e., @RunWith, @ContextConfiguration, and @Autowired)
5. Flexible configuration
6. Test templates

<!-- 

**_Spring_** — a popular open-source framework for building Java applications. 

**1. Integration testing**
- Allows developers to test their application's integration with other technologies and systems, such as databases, messaging systems, and web services.
- This is particularly important in enterprise applications, which often rely on complex systems and architectures.

**2. Mock objects**
- Allows developers to create mock objects, which are fake versions of other components in the application.
- This allows developers to test their code in isolation, without having to set up a complete environment with all the components.

**3. Dependency injection**
- Uses the same dependency injection mechanism as the rest of the Spring framework, which makes it easy to configure and manage dependencies between components in the application. 
- **_Dependency injection_** — a technique where the required dependencies of an object are provided to it from outside, rather than the object creating them itself.

**4. Annotations**
- Provides a set of annotations that developers can use to write tests, such as _@RunWith_, _@ContextConfiguration_, and _@Autowired_. These annotations make it easy to set up and configure the testing environment, and to inject dependencies into test classes.

**5. Flexible configuration**
- Allows you to configure your tests in a flexible way.
- Provides support for loading configuration files, setting up test data, and configuring mock objects.

**6. Test templates**
- Provides a set of templates that developers can use to write different types of tests, such as unit tests, integration tests, and end-to-end tests. 

 -->

---
layout: center
---

# Spring Boot Testing

“Testing made easy for Spring Boot”

> A module of the Spring Boot framework that provides support for testing Spring Boot applications,

> including unit testing, integration testing, and end-to-end testing.

<style>
blockquote {
  code {
    @apply text-teal-500 dark:text-teal-400;
  }
}
</style>

<br>

1. Auto-configuration
2. Mocking and testing
3. Integration testing
4. Test annotations (i.e., _@SpringBootTest_, _@MockBean_)
5. Test utilities (i.e., _TestRestTemplate_ class)
6. Test slices (i.e., _@WebMvcTest_, _@DataJpaTest_ )

<!-- 

**1. Integration with the Spring framework**
- Includes auto-configuration, which allows you to automatically configure the test environment based on your application's settings.
- Makes it easy to get started with testing and reduces the amount of boilerplate code you need to write.

**2. Mocking and testing**
- Provides support for mocking and testing controllers, repositories, and other components.
- Allows you to test individual components of your application in isolation, without having to start up the entire application.

**3. Integration testing**
- Provides support for integration testing, where you can test the interactions between different parts of your application in a real-world environment.
- Allows you to test the behavior of your application as a whole, including its interactions with external services and databases.

**4. Test annotations**
- Includes a set of test annotations that make it easy to write tests for your application.
- e.g. The @SpringBootTest annotation can be used to load the entire Spring application context for testing, while the @MockBean annotation can be used to mock out specific beans in the application context.

**5. Test utilities**
- Includes a set of test utilities that make it easy to write tests for your application.
- e.g. The _TestRestTemplate_ class can be used to make HTTP requests to your application and assert the responses, while the TestEntityManager class can be used to interact with the application's database in a test environment.

**6. Test slices**
- Includes the concept of "test slices", which are subsets of the application context that can be used to test specific parts of your application.
- The _@WebMvcTest_ annotation can be used to test just the web layer of your application, while the _@DataJpaTest_ annotation can be used to test just the data access layer. This makes it easier to write focused tests that are faster to run.

 -->

---
layout: center
---

# TestContainers

“Containerized testing made simple”

> A Java testing library that allows developers to easily create and manage disposable test containers,

> such as databases, for their unit and integration tests.

<style>
blockquote {
  code {
    @apply text-teal-500 dark:text-teal-400;
  }
}
</style>

<br>

1. Containerization
2. Wide range of supported containers (i.e., MySQL, PostgreSQL, Oracle, RabbitMQ, Apache Kafka)
3. Automated container management
4. Dependency management
5. Simple API
6. Compatibility with existing testing frameworks

<!-- 

**_Container_** — refers to a disposable instance of a software component, such as a database or a messaging system, that is created and managed dynamically during the execution of a test case. 

**1. Containerization**
- Allows developers to define and manage the lifecycle of lightweight, throwaway instances of external services directly in their Java test code.
- This means that developers can run integration tests in an environment that closely mimics production, without the need for complex setup or manual configuration.


**2. Wide range of supported containers**
- Supports a wide range of containerized services, including databases like MySQL, PostgreSQL, and Oracle, as well as messaging systems like RabbitMQ and Apache Kafka.
- Also supports other services like Selenium WebDriver and Elasticsearch.

**3. Automated container management**
- Automatically starts and stops the containers as needed, reducing the need for manual intervention during testing.
- This allows developers to focus on writing tests rather than managing container lifecycles.

**4. Dependency management**
- Automatically manages dependencies between containers, ensuring that containers are started and stopped in the correct order.
- This helps to avoid issues with race conditions or other problems that can occur when containers are started or stopped in the wrong order.

**5. Simple API**
- Has a simple, easy-to-use API that makes it easy to define and manage containers directly in Java test code.
- The library also provides a number of convenient utilities that make it easy to work with containerized services.

**6. Compatibility with existing testing frameworks**
- TestContainers is compatible with existing Java testing frameworks like JUnit and TestNG, making it easy to integrate with existing testing processes.

 -->

---
layout: center
---

# Instancio

“Dynamic test data generation library”

> A library for instantiating and populating objects with random data, making your tests more dynamic

<style>
blockquote {
  code {
    @apply text-teal-500 dark:text-teal-400;
  }
}
</style>

<br>

1. Reduces manual data setup in unit tests
2. Non-intrusive and concise API
3. Allows customization of generated objects
4. Requires no changes to production code
5. Can be used out-of-the-box with zero config

<!-- 

**GOAL 1**
- There are several existing libraries for generating realistic test data (i.e., addresses, first and last names)
- While Instancio also supports this use case, this is not its goal.
- The idea behind the project is that most unit tests do not care what the actual values are. They just require the presence of a value.
Therefore, the main goal of Instancio is simply to generate fully populated objects with random data, including arrays, collections, nested collections, generic types, and so on. And it aims to do so with as little code as possible to keep the tests concise.

**GOAL 2**
- Another goal of Instancio is to make the tests more dynamic.
- Since each test run is against random values, the tests become alive.
- They cover a wider range of inputs, which might help uncover bugs that may have gone unnoticed with static data.
- In many cases, the random nature of the data also removes the need for parameterising test methods.

**GOAL 3**
- Finally, Instancio aims to provide reproducible data.
- It uses a consistent seed value for each object graph it generates.
- Therefore, if a test fails against a given set of inputs, Instancio supports re-generating the same data set in order to reproduce the failed test.

 -->

---
layout: center
---

# Selenide

"Java UI testing made easy."

> A concise and easy-to-use Java-based UI automation testing framework that leverages the Selenium WebDriver library.

<style>
blockquote {
  code {
    @apply text-teal-500 dark:text-teal-400;
  }
}
</style>

<br>

1. Concise and readable syntax
2. Automatic waits
3. Screenshots on failures
4. Support for multiple browsers
5. Page Object Model (POM) support
6. Fluent API
7. Automatic handling of iframes
8. Advanced assertions

<!-- 

**_Selenium WebDriver_** — a popular open-source library that provides a programming interface to interact with web browsers and automate browser activities, such as clicking buttons, filling out forms, and navigating through pages. 

**1. Concise and readable syntax** (uses a jQuery-style selector syntax)
- Selenide provides a simple and readable syntax for writing tests.
- The library uses a jQuery-style selector syntax that is easy to learn and use.
- This makes it easy for developers to write and maintain tests.


**2. Automatic waits**
- Automatically waits for elements to become visible or interactable before performing actions on them.
- This eliminates the need for manual waits in test code and makes tests more reliable.

**3. Screenshots on failures**
- Takes screenshots automatically when a test fails.
- This helps developers to quickly identify the cause of test failures and fix them.

**4. Support for multiple browsers**
- Supports testing in multiple browsers, including Chrome, Firefox, Edge, and Safari.
- This makes it easy to test web applications across different platforms and browsers.

**5. Page Object Model (POM) support**
- Supports the Page Object Model (POM), which allows developers to create reusable page objects and keep test code organized and maintainable.

**6. Fluent API**
- Provides a fluent API that allows developers to chain together multiple actions in a single statement.
- This makes test code more concise and readable.

**7. Automatic handling of iframes**
- Automatically switches to iframes when necessary, making it easy to test web applications that use iframes.

**8. Advanced assertions**
- Provides advanced assertion capabilities, including _soft assertions_ and _custom assertions_.
- _Soft assertions_ allow developers to continue executing a test even if an assertion fails, while _custom assertions_ allow developers to create their own custom assertions.


 -->

---
layout: center
---

# JetBrains Aqua

"A powerful new IDE for test automation"

> A powerful tool for testing automation that incorporates parts of various IDEs, targeting the testing automation process.

<style>
blockquote {
  code {
    @apply text-teal-500 dark:text-teal-400;
  }
}
</style>

<br>

1. Intelligent coding assistance
2. Unit test frameworks
3. UI automation (i.e., New Project wizard, Code Insight, Page Object Templates)
4. Web inspector
5. API testing and environment setup (i.e., HTTP, Docker)
6. Database
7. Test management systems (TMS)


<!-- 

**1. Intelligent coding assistance**
- Take advantage of language-aware code completion, error detection, and on-the-fly code fixes

**2. Unit test frameworks**
- Create and run your tests with coding assistance and a GUI-based test runner. With JetBrains Aqua you can write, run, and debug your unit tests using JUnit, TestNG, Pytest, Jest, Mocha, and other popular frameworks. Reviewing the test results inside the IDE allows you to easily navigate in a tree view and to the test source.

**3. UI automation**
- **New Project Wizard:** Aqua can generate a new UI test project for the JVM stack, allowing you to specify the JDK, build tool (Maven or Gradle), test runner (JUnit or TestNG), and language from the New Project wizard.
- **Code Insight:** Aqua provides rich support for the Selenium API and Selenide, offering code insight for the CSS, XPath, and JavaScript fragments used in the Selenium API and many other libraries for UI testing. 
- **Page Object Templates:** When following the Page Object pattern, the IDE helps you create and maintain new page object files from the New File menu and respects the selected page object pattern when adding locators.

**4. Web inspector**
- The embedded Web Inspector allows you to view web applications in Aqua and capture page elements required for automated tests.
- Aqua generates a unique CSS or XPath locator for the selected element on the web page and helps add it to the source code. 

**5. API testing and environment setup**
- **HTTP Client:** When developing a web service that sends and receives HTTP requests, you can easily create and edit requests in Aqua’s built-in HTTP client and receive extensive code assistance, including code completion, highlighting, refactorings, and more.
- **Docker:** With Aqua, you get access to your Docker containers, allowing you to run and debug them, download and build images, and run multi-container applications.

**6. Database**
- JetBrains Aqua does not require any extra tools to prepare your application data.
- You can seamlessly handle multiple databases, develop SQL scripts, and perform low-level data assertions right in the IDE. 
- Aqua provides connections to live databases, runs queries, exports data, and allows you to manage schemes in a visual interface.
- This means you can access Oracle, SQL Server, PostgreSQL, MySQL, and other databases from the IDE.

**7. Test management systems (TMS)**
- Tests usually contain links to issue trackers and TMS (test management systems).
- To make it possible to include them, developers use reporting libraries (i.e., Allure Framework) or built-in test framework mechanisms (i.e.m Serenity BDD).
We have added support for the annotations of these libraries, and the IDE allows you to open issues or TMS cases in a web browser just by clicking on the issue IDs.

 -->

---
layout: center
---

# Summary

1. **_JUnit 5_** — A popular unit testing framework for Java.
2. **_JUnit Pioneer_** — An open-source testing tool that extends JUnit 5 to provide additional testing features.
3. **_AssertJ_** — A library that provides fluent assertions for Java.
4. **_Data Faker_** — A library that generates random data for testing purposes.
5. **_Mockito_** — A mocking framework for Java that allows you to create mock objects for testing.

---
layout: center
---

# Summary (cont.)

6. **_Easy Random_** — A library that generates random data for testing purposes.
7. **_Easy Random JUnit Extension_** — An extension to the Easy Random library that integrates with JUnit 5 to generate random test data.
8. **_Database Rider_** — A testing tool that provides a convenient way to manage and populate database instances for testing purposes.
9. **_ModelAssert_** — A library that provides fluent assertions for testing object models.
10. **_SpringFramework Testing_** — A testing framework that provides support for testing Spring-based applications.

---
layout: center
---

# Summary (cont.)

11. **_Spring Boot Testing_** — A testing framework that provides support for testing Spring Boot applications.
12. **_TestContainers_** — A testing tool that allows you to easily run applications in containers for testing purposes.
13. **_Instancio_** — A testing tool that generates test data by analyzing the source code of the classes being tested.
14. **_Selenide_** — A testing framework that provides a concise API for writing UI tests using Selenium WebDriver.
15. **_JetBrains Aqua_** — A testing tool that provides a simple and intuitive way to test Java applications using a web-based interface.






---
layout: center
---

### More info on the presented testing tools

<img src="/assets/images/notes.png" class="m-5 h-100 rounded shadow" />

---
layout: end
---