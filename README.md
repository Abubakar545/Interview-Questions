# Interview-Questions
List of interview questions for different companies 


**Lufthanasasystems Interview ---- 28 feb 2026**
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Java Coding
Q1) using stream String = "My. name, is Abc" the output should be "yM. eman, si cbA";

import java.util.Arrays;
import java.util.stream.Collectors;

public class ReverseEachWord {
    public static void main(String[] args) {

        String s = "My, Name. Is Abc";

        String output = Arrays.stream(s.split(" "))
                .map(ReverseEachWord::reverseWordKeepPunctuation)
                .collect(Collectors.joining(" "));

        System.out.println(output);
    }

    private static String reverseWordKeepPunctuation(String word) {
        char[] arr = word.toCharArray();

        int left = 0;
        int right = arr.length - 1;

        while (left < right) {

            if (!Character.isLetter(arr[left])) {
                left++;
            } else if (!Character.isLetter(arr[right])) {
                right--;
            } else {
                char temp = arr[left];
                arr[left] = arr[right];
                arr[right] = temp;
                left++;
                right--;
            }
        }
        return new String(arr);
    }
}

Q2) Deadlock and RaceCondition
Q3) Relationship between == and equals()
Q4) How Auto configuration works in spring
Q5) How to make a class imutable in Java
Q6) Types of injections? difference between Constructor and field injection
Q8) HashMap and LinkedHashMap differnce
Q9) What is the role of consumer in kafka
Q10) 



**Combined 3 compiences interview**
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
🔹 Java Core & Collections

1) Declare a 2D array and iterate over it using an enhanced for loop (for-each) in Java.
Given:
int[] arr = {1,2,2,3,3,3,4,4,4,4,5,5};
2) Remove duplicates without using any additional array and fill remaining slots with null.
3) Difference between throw and throws.
4) Write a program to reverse an integer number.
5) Explain internal working of HashMap.
6) What is a lambda expression?
7) What is a functional interface? Can it have static and default methods?

🔹 OOP Concepts
1) Explain inheritance and polymorphism.
2) Explain SOLID principles.
3) What design patterns do you know in Java?
4) Write a program to create a Singleton class.
5) How can you optimize Singleton in a multithreaded environment? (using synchronized / double-checked locking)
6) What is a synchronized block?

🔹 Java 8 / Streams / Collections
1) Given a list:
["ram","sita","rahul", null, null, "deepak"]
Convert it to output:
[null, null, "ram","sita","rahul","deepak"] using Java 8.
2) Print numbers from 1 to 100 using 3 threads (Executor Framework) and print thread names.
🔹 Multithreading & Executor Framework
3) What is the Executor Framework in Java?
4) How do you create a fixed thread pool of size 3?
5) How do you manage task execution using multiple threads?

🔹 Spring Boot / Microservices
1) How can we configure timeout for a REST API?
2) How to convert a monolithic application into microservices?
3) What is dependency injection and what are its types?
4) What will @Autowired do internally?

🔹 JPA / Hibernate
1) What are criteria queries in JPA?
2) Explain JPA Criteria API and its use cases.

🔹 Scenario Based / SQL / Design
1) From a given employee table, find the manager having the maximum number of subordinates.
2) Why do we store LDAP user personal data in DB tables after syncing? Is it really needed?

🔹 Additional Conceptual Questions
1) Can we apply abstract to non-volatile variables?
2) Explain Java 17 features you implemented in your project.
3) Explain LRU Cache implementation using LinkedList (or other DS).



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
2) redux and context api
3) difference between fetch and axios
4) 

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

----------------------------------------------------------------------------------------------------------------------------------------------
Altimetric Interview questions
----------------------------------------------------------------------------------------------------------------------------------------------
1) What happens if we remove an element from a collection inside a for-each loop? Why does it cause ConcurrentModificationException?

2) Why do the methods clone(), notify(), and notifyAll() belong to the Object class and not to user-defined classes?

3) In a Singleton class, cloning can create multiple objects. How do you prevent cloning from breaking the Singleton pattern?

4) Can a Singleton class be serialized? If yes, how do you prevent multiple instances during deserialization?

5) In Spring Boot, can we replace @Controller and @Service annotations with @Component? If yes, why do we still prefer specialized annotations?

6) How can we configure timeout settings for a REST API in Spring Boot? Write the code.

7) Where do we use synchronous and asynchronous communication in microservices? Explain with a real-time example.

8) Which authentication mechanisms are you familiar with? Explain briefly.

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

List<Integer> list = Arrays.asList(1, 3, 5, 7, 9, 13, 23);
int target = 5;

linear approach
-------------------------
List<Integer> list = new ArrayList<>(Arrays.asList(1,3,5,7,9,13,23));
int target = 5;
int index = -1;

for (int i = 0; i < list.size(); i++) {
    if (list.get(i) == target) {
        index = i;
        break;
    } else if (list.get(i) > target) {
        list.add(i, target);
        index = i;
        break;
    }
}

if (index == -1) {
    list.add(target);
    index = list.size() - 1;
}

System.out.println("Index: " + index);
System.out.println("List: " + list);


optimal solution
------------------------
List<Integer> list = new ArrayList<>(Arrays.asList(1,3,5,7,9,13,23));
int target = 5;

int low = 0, high = list.size() - 1;
int index = -1;

while (low <= high) {
    int mid = (low + high) / 2;

    if (list.get(mid) == target) {
        index = mid;
        break;
    } else if (list.get(mid) < target) {
        low = mid + 1;
    } else {
        high = mid - 1;
    }
}

if (index == -1) {
    list.add(low, target); // correct sorted position
    index = low;
}

System.out.println("Index: " + index);
System.out.println("List: " + list);





