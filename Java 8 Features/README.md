# Java 8 Features

## Content
* Lambda Expressions
* Functional Interfaces
* Default Methods in Interface
* Static Methods in Interface
* Predicate
* Function
* Consumer
* Double Colon Operator
    * Method Reference
    * Constructor Reference
* Stream API
* Date and Time API (Joda API)


### Lambda Expression
* It is anonymous function
    * Not having name
    * Not having modifier
    * Not having return type

#### Characteristics / Properties of Lambda Expression
* A lambda expression can take any number of parameters.
    ```java
    () -> System.out.println("Hello");
    (s) -> s.length();
    (a, b) -> System.out.println(a + b);
    ```
* If multiple parameters present then these parameters should be separated with ,
    ```java
    (a, b) -> System.out.println(a + b);
    ```
* If only one parameter is present then parenthesis are optional
    ```java
    (s) -> s.length(); => s -> s.length();
    ```
* Usually we can specify the type of parameter if compiler guess/expects the type based on context then we can remove type
    ```java
    (int a, int b) -> 
    ```
* Similar to method body, lambda expression body can contains any number of statements. If multiple statements are there then we should enclose within curly braces
    ```java
    () -> {
        // statement 1;
        // statement 2;
        // statement 3;
    }
    ```
    If body contains only one statement then curly braces are optional
    ```java
    () -> System.out.println("Hello");
    ```
* If lambda expression return something then we can remove return keyword
    ```java
    s -> s.length();
    ```