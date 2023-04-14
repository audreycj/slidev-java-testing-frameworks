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
- provides a structure for writing test cases and automates the process of executing them, reporting results, and providing feedback
- e.g. AssertJ, Data Faker, Easy Random, Easy Random JUnit Extension, ModelAssert, 

<br>

### **Testing Tool**
- a software application that helps developers automate and manage the process of testing software, providing functionality beyond what is available in testing libraries or frameworks
- e.g. JUnit Pioneer, Database Rider, TestContainers, Instancio, JetBrains Aqua

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

<!--

**Library** — a collection of pre-written code that can be called by your own code to perform specific tasks or functionalities. 

**Testing framework** — a set of guidelines, rules, and conventions that dictate how tests should be structured, written, and executed. 

-->

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

> A community-driven effort to improve the quality and effectiveness of JUnit tests,

> through the development and promotion of best practices, tools, and educational resources.

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

**Test isolation with separate class loaders**

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

**Type-specific assertions**
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

> A testing tool that simplifies the process of generating randomized test data in JUnit tests, reducing the amount of 

> boilerplate code required for data setup and allowing for more comprehensive and efficient testing.

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

**1. Model-based testing with graphs**


**2. Domain-specific assertions**


**3. Value object testing**


**4. Flexible model definition**


**5. Data-driven testing**

**6. Lightweight and easy to use**


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
4. Annotations
5. Flexible configuration
6. Test templates

<!-- 

**FEATURE 1.**


**FEATURE 2.**


**FEATURE 3.**


**FEATURE 4.**


**FEATURE 5.**


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

1. Integration with the Spring framework
2. Support for different types of testing
3. Auto-configuration
4. Embedded servers
5. Dependency management

<!-- 

**FEATURE 1.**


**FEATURE 2.**


**FEATURE 3.**


**FEATURE 4.**


**FEATURE 5.**


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
2. Wide range of supported containers
3. Automated container management
4. Dependency management
5. Simple API
6. Compatibility with existing testing frameworks

<!-- 

**FEATURE 1.**


**FEATURE 2.**


**FEATURE 3.**


**FEATURE 4.**


**FEATURE 5.**


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

**FEATURE 1.**


**FEATURE 2.**


**FEATURE 3.**


**FEATURE 4.**


**FEATURE 5.**


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

**FEATURE 1.**


**FEATURE 2.**


**FEATURE 3.**


**FEATURE 4.**


**FEATURE 5.**


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
3. UI automation
4. Web inspector
5. API testing and environment setup
6. Database
7. TMS


<!-- 

**FEATURE 1.**


**FEATURE 2.**


**FEATURE 3.**


**FEATURE 4.**


**FEATURE 5.**


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