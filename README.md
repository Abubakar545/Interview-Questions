# Interview-Questions
List of interview questions for different companies 


**CitiusTech**          --- 24 Jan 2026
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Java
----------------------
1) java 17 features and what you implemented in your project.
2) how to convert monolithic to microservices
3) How can we implement LRU cache and what are all the steps and methods we have in it. i.e LinkedList
4) can we perform abstract on non volatile instances
5) what is executor framework in multithreading and what are all the methods present in it.
6) new features indroduced in hashmap after java 8
7) 

coding
----------------------


MySQL
---------------------
1) what is view
2) can we create index on view
3) types on index
4) 


React.js
---------------------------
1) what is prop drilling, how can we handle it by using framework and tools
2) 

Mindtree Interview         --- 20th jan 2026
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
1) print the dublicate elements using stream
List<String> names = Arrays.asList("Alice", "Bob", "Charlie", "Alice", "Bob", "David");

HashSet<String> seen = new HashSet<String>();
names.stream().filter(name-> !seen.add(name)).distinct().Collect(Collections.asList);
2) print only body data from this
String str = "[
    {
        "id": 1,
        "body": "First Item",
        "severity": 1,
        "status": 0
    },
    {
        "id": 2,
        "body": "Second Item",
        "severity": 2,
        "status": 1
    }
]";

   ObjectMapper mapper = new ObjectMapper();
        JsonNode root = mapper.readTree(str);

        for (JsonNode node : root) {
            System.out.println(node.get("body").asText());
        }
        
3) how can we use 2 dbs at one time
@Configuration
public class DataSourceConfig {

    @Primary
    @Bean(name = "dataSource1")
    public DataSource dataSource1() {
        return DataSourceBuilder.create()
                .url("jdbc:mysql://localhost:3306/db1")
                .username("user1")
                .password("pass1")
                .build();
    }

    @Bean(name = "dataSource2")
    public DataSource dataSource2() {
        return DataSourceBuilder.create()
                .url("jdbc:mysql://localhost:3306/db2")
                .username("user2")
                .password("pass2")
                .build();
    }
}

4) write custom exception classes
5)functional interface methods
6)how we communicate between microservices
7) diff between resttemplate and webclient
8) ArrayList and LinkedList diff
9)which design pattren have you used in your project
10) create custom mutuable class 
11) immutable classes in java
12) what are functional interface classes in java
13) what is concurrent modification exception 
14) fail fast and fail safe, when to use this?


PWC Interview              --- 20th jan 2026
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
1) Functional Interface
2) Inheritance and it's type
3) Polymorphism and it's types
4) JDBC and Hibernate differnce
5) can add or fetch queries in Hibernate, and it is
6) monolithic and microservices differnce
7) how microservices communicate with each other
8) what is virtual dom in react
9) what fregment
10) what are props
11) what is prop drilling, and how can we over come this
12) What is state react, and how state management works
13) what is redux
14) create a table, where i has object with id, name and age and display this details in that table using react UI


List of All Important Questions
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Java – Coding / Core / Advanced
--------------------------------------------------------
1) Filter age using Stream API
2) list.stream().filter(s -> s.getPrice() > 100).collect(Collectors.toList());
3) Write a program to find unique words from a sentence and sort them
4) SOLID principles
5) Explain MVC architecture in brief
6) Java 8 features
7) Java 17 features
8) AOP (Aspect-Oriented Programming)
9) Transient vs Volatile
10) OAuth
11) Performance tuning in Java
12) Caching
14) Spring Boot annotations
15) Functional interface types
16) Types of exceptions in Java
17) How can we avoid finally block execution
18) Deadlock condition
19) Thread life cycle
20) Spring Security architecture
21) CompletableFuture
22) Memory leaks in Java
23) What do you mean by try-with-resources
24) Abstract class vs Interface
25) Dependency Injection
26) What is design pattern you know or implemented
27) How to implement Singleton pattern
28) What if two separate threads try to create object of Singleton class
29) HashMap vs Hashtable vs ConcurrentHashMap
30) Fail-fast vs Fail-safe
31) Types of operations in Stream API
32) Best practices for performance tuning Spring Boot applications

✅ MySQL / Database
**------------------------------------------------------------**
1) What is a View
2) Triggers
3) Sequence
4) Joins
5) What is Index
6) Objects in MySQL
7) Stored Procedure
8) Indexing
9) Types of Joins
10) Query to find Second Highest Salary
11) What is Index in Database

## ✅ **JAVA QUESTIONS**
**---------------------------------------------------------------**

### Core Java

* SOLID principles
* Java 8 features
* Java 17 features
* Abstract class vs Interface
* Types of exceptions in Java
* Transient vs Volatile
* Try-with-resources
* Dependency Injection (concept)
* Circular dependency – what is it? how Spring handles it
* Thread life cycle
* Deadlock condition
* How can we avoid finally block execution
* Memory leaks in Java

### Collections & Concurrency

* Collection framework
* HashMap vs Hashtable vs ConcurrentHashMap
* Fail-fast vs Fail-safe
* Functional interface types

### Design Patterns

* What design patterns do you know / implemented
* Singleton design pattern
* How to implement Singleton
* What if two threads try to create object of Singleton class

### Java Stream API

* Types of operations in Stream API
* Filter age using Stream API


## ✅ **MYSQL QUESTIONS**
**-----------------------------------------------------------**

* What is Index in database
* Indexing
* Views
* Triggers
* Sequence
* Objects
* Stored Procedure
* Joins
* Types of Joins
* Second highest salary (SQL query)

---

## ✅ **SPRING / SPRING BOOT QUESTIONS**

* Explain MVC architecture in brief
* AOP (Aspect Oriented Programming)
* OAuth
* Spring Boot annotations
* Spring Security architecture
* Caching (Spring caching / Redis)
* Performance tuning in Spring Boot
* Best practices to improve Spring Boot application performance

---

## ✅ **CODING / PROGRAMMING QUESTIONS**

### Java Programs

* Java program to get price greater than 100 using Stream
* Write a program to find unique words from a sentence and sort alphabetically
* Get first non-repeating character from a string (`"leetcode"` → `l`)

### Stream API Programs

* Find sum of all values in a list using Stream
* Get duplicate values from a list using Stream

Example list:

```java
List<Integer> list = Arrays.asList(1,2,3,3,4,5,5);
```







