# Java Study Guide: Beginner to Advanced

---

**Contents**
1. [Introduction to Java](#introduction-to-java)
2. [Java Basics](#java-basics)
3. [Control Flow Statements](#control-flow-statements)
4. [Object-Oriented Programming](#object-oriented-programming)
5. [Exception Handling](#exception-handling)
6. [Strings and String Handling](#strings-and-string-handling)
7. [Arrays and Collections](#arrays-and-collections)
8. [Searching and Sorting](#searching-and-sorting)
9. [Working with Date and Time](#working-with-date-and-time)
10. [Problem Solving and Sample Exercises](#problem-solving-and-sample-exercises)
11. [**DSA Java**](#DSA-Java)

---

### 1. Introduction to Java

Java is a **platform-independent** language, meaning it can run on any device that has a Java Virtual Machine (JVM). It's known for its **object-oriented** structure and **simplicity**, making it a powerful language for beginners and advanced users alike.

#### Example: "Hello, World!" in Java
The first step in learning any language is to write a program that prints "Hello, World!" to the screen.

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

- **Explanation**:
  - `public class HelloWorld`: Defines a class named `HelloWorld`. In Java, all code should be inside a class.
  - `public static void main(String[] args)`: The main method is the entry point for any Java program. It must be written exactly as shown.
  - `System.out.println("Hello, World!");`: This line prints "Hello, World!" to the console.

- **Output**:
  ```
  Hello, World!
  ```

---

### 2. Java Basics

#### Data Types
Java supports several **primitive data types**:
- **int**: Stores integers (e.g., `10`, `-45`).
- **double**: Stores decimal numbers (e.g., `3.14`).
- **char**: Stores single characters (e.g., `'A'`).
- **boolean**: Stores true/false values.

#### Example
```java
int age = 25;
double salary = 50000.50;
char grade = 'A';
boolean isStudent = false;

System.out.println("Age: " + age);
System.out.println("Salary: " + salary);
System.out.println("Grade: " + grade);
System.out.println("Is Student: " + isStudent);
```

- **Output**:
  ```
  Age: 25
  Salary: 50000.5
  Grade: A
  Is Student: false
  ```

#### Variables and Constants
Variables store values that can change, while constants use `final` to prevent changes.

```java
int num = 5;           // Variable
final double PI = 3.14; // Constant
```

---

### 3. Control Flow Statements

Control flow statements determine the order in which statements are executed in a program.

#### if-else Statement
Used for **conditional logic**.

```java
int age = 20;
if (age >= 18) {
    System.out.println("Adult");
} else {
    System.out.println("Minor");
}
```

- **Explanation**: Checks if `age` is 18 or more; if true, it prints "Adult"; otherwise, "Minor."
- **Output**:
  ```
  Adult
  ```

#### Loops
- **for loop**: Executes a set number of times.
- **while loop**: Repeats while a condition is true.

```java
for (int i = 0; i < 5; i++) {
    System.out.println("Iteration: " + i);
}
```

- **Output**:
  ```
  Iteration: 0
  Iteration: 1
  Iteration: 2
  Iteration: 3
  Iteration: 4
  ```

#### switch-case
Switch-case is used to select one of many code blocks based on the value of a variable.

```java
int day = 3;
switch(day) {
    case 1: System.out.println("Monday"); break;
    case 2: System.out.println("Tuesday"); break;
    case 3: System.out.println("Wednesday"); break;
    default: System.out.println("Invalid day");
}
```

- **Output**:
  ```
  Wednesday
  ```

---

### 4. Object-Oriented Programming

Java is **object-oriented**, which means it models real-world entities using **classes** and **objects**.

#### Class and Object
A **class** is a blueprint, and an **object** is an instance of a class.

```java
class Car {
    String color;
    int speed;

    Car(String color, int speed) {
        this.color = color;
        this.speed = speed;
    }
    
    void display() {
        System.out.println("Color: " + color + ", Speed: " + speed);
    }
}

public class Main {
    public static void main(String[] args) {
        Car myCar = new Car("Red", 100);
        myCar.display();
    }
}
```

- **Explanation**: `Car` class has properties `color` and `speed`, and a method `display` to show them.
- **Output**:
  ```
  Color: Red, Speed: 100
  ```

#### Inheritance, Polymorphism, Encapsulation, and Abstraction
- **Inheritance**: Allows a class to inherit properties from another.
- **Polymorphism**: Lets an object take many forms (method overloading/overriding).
- **Encapsulation**: Hides data using `private` and exposes it through `public` methods.
- **Abstraction**: Shows only essential details; hides the complex parts.

---

### 5. Exception Handling

Java's **exception handling** ensures errors are caught and managed without crashing.

```java
try {
    int result = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("Cannot divide by zero!");
} finally {
    System.out.println("Done!");
}
```

- **Output**:
  ```
  Cannot divide by zero!
  Done!
  ```

---

### 6. Strings and String Handling

Java has the `String` class with powerful methods for handling text.

```java
String s = "Hello, World!";
System.out.println("Length: " + s.length());
System.out.println("Uppercase: " + s.toUpperCase());
System.out.println("Substring: " + s.substring(7));
```

- **Output**:
  ```
  Length: 13
  Uppercase: HELLO, WORLD!
  Substring: World!
  ```

---

### 7. Arrays and Collections

#### Array
An array is a fixed-size collection of elements of the same type.

```java
int[] numbers = {1, 2, 3};
System.out.println(numbers[0]); // Accessing element
```

#### ArrayList (Dynamic Array)
Part of `java.util`, it allows dynamic resizing.

```java
ArrayList<String> list = new ArrayList<>();
list.add("Element");
System.out.println(list.get(0));
```

- **Output**:
  ```
  Element
  ```

---

### 8. Searching and Sorting

#### Linear Search
Sequentially checks each element until the desired one is found.

```java
public static int linearSearch(int[] array, int key) {
    for (int i = 0; i < array.length; i++) {
        if (array[i] == key) return i;
    }
    return -1;
}
```

#### Binary Search
Efficient for **sorted arrays** by repeatedly dividing the search interval.

```java
Arrays.binarySearch(array, key);
```

#### Sorting
- **Arrays.sort()**: Sorts arrays.
- **Collections.sort()**: Sorts collections.

---

### 9. Working with Date and Time

The `java.time` package provides classes to work with date and time.

```java
LocalDate date = LocalDate.now();
System.out.println("Today's date: " + date);
```

- **Output**:
  ```
  Today's date: 2023-10-30 (example)
  ```

---

### 10. Problem Solving and Sample Exercises

**Reverse a String**
```java
public static String reverse(String str) {
    return new StringBuilder(str).reverse().toString();
}
```

**Output**:
  ```
  reverse("Java") -> "avaJ"
  ```

---
---

# DSA Java

### Table of Contents
1. [Introduction to Java DSA](#1-introduction-to-java-dsa)
2. [Arrays](#2-arrays)
3. [Linked Lists](#3-linked-lists)
4. [Stacks](#4-stacks)
5. [Queues](#5-queues)
6. [Trees](#6-trees)
7. [Graphs](#7-graphs)
8. [Sorting Algorithms](#8-sorting-algorithms)
9. [Searching Algorithms](#9-searching-algorithms)
10. [String Manipulation](#10-string-manipulation)
11. [Hashing](#11-hashing)
12. [Recursion](#12-recursion)
13. [Dynamic Programming](#13-dynamic-programming)
14. [Conclusion and Best Practices](#14-conclusion-and-best-practices)

---

### 1. Introduction to Java DSA
Data Structures and Algorithms (DSA) in Java are essential for efficient problem-solving and optimizing code performance. Key concepts include:
- **Data Structures**: Organize data for efficient access.
- **Algorithms**: Step-by-step instructions for solving problems.

---

### 2. Arrays
Arrays store elements in contiguous memory locations.

#### Syntax
```java
int[] arr = new int[5];
int[] arr = {1, 2, 3, 4, 5};
```

#### Example
```java
int[] numbers = {10, 20, 30, 40, 50};
for (int number : numbers) {
    System.out.println(number);
}
```

**Output**
```
10
20
30
40
50
```

---

### 3. Linked Lists
Linked Lists consist of nodes connected by pointers. Types include singly, doubly, and circular linked lists.

#### Syntax
```java
class Node {
    int data;
    Node next;
}
```

#### Example (Singly Linked List)
```java
class Node {
    int data;
    Node next;
    Node(int data) { this.data = data; }
}

class LinkedList {
    Node head;

    public void add(int data) {
        Node newNode = new Node(data);
        if (head == null) {
            head = newNode;
        } else {
            Node temp = head;
            while (temp.next != null) temp = temp.next;
            temp.next = newNode;
        }
    }

    public void display() {
        Node temp = head;
        while (temp != null) {
            System.out.print(temp.data + " ");
            temp = temp.next;
        }
    }
}

public class Main {
    public static void main(String[] args) {
        LinkedList list = new LinkedList();
        list.add(10);
        list.add(20);
        list.add(30);
        list.display();
    }
}
```

**Output**
```
10 20 30
```

---

### 4. Stacks
Stacks use LIFO (Last-In, First-Out) order.

#### Syntax
```java
Stack<Integer> stack = new Stack<>();
```

#### Example
```java
Stack<Integer> stack = new Stack<>();
stack.push(10);
stack.push(20);
System.out.println(stack.pop());
System.out.println(stack.peek());
```

**Output**
```
20
10
```

---

### 5. Queues
Queues use FIFO (First-In, First-Out) order.

#### Syntax
```java
Queue<Integer> queue = new LinkedList<>();
```

#### Example
```java
Queue<Integer> queue = new LinkedList<>();
queue.add(10);
queue.add(20);
System.out.println(queue.remove());
System.out.println(queue.peek());
```

**Output**
```
10
20
```

---

### 6. Trees
A tree is a hierarchical structure with nodes and edges.

#### Syntax (Binary Tree)
```java
class Node {
    int data;
    Node left, right;
}
```

#### Example (Binary Tree Traversal)
```java
class Node {
    int data;
    Node left, right;

    public Node(int data) { this.data = data; }
}

public class Tree {
    Node root;

    public void inOrder(Node node) {
        if (node == null) return;
        inOrder(node.left);
        System.out.print(node.data + " ");
        inOrder(node.right);
    }

    public static void main(String[] args) {
        Tree tree = new Tree();
        tree.root = new Node(1);
        tree.root.left = new Node(2);
        tree.root.right = new Node(3);
        tree.inOrder(tree.root);
    }
}
```

**Output**
```
2 1 3
```

---

### 7. Graphs
Graphs consist of vertices connected by edges. They can be represented using adjacency lists or matrices.

#### Example (Adjacency List Representation)
```java
class Graph {
    private int V;
    private LinkedList<Integer> adj[];

    Graph(int v) {
        V = v;
        adj = new LinkedList[v];
        for (int i = 0; i < v; ++i)
            adj[i] = new LinkedList();
    }

    void addEdge(int v, int w) {
        adj[v].add(w);
    }

    void printGraph() {
        for (int i = 0; i < V; i++) {
            System.out.print("Node " + i + ":");
            for (Integer pCrawl : adj[i]) {
                System.out.print(" -> " + pCrawl);
            }
            System.out.println("\n");
        }
    }
}

public class Main {
    public static void main(String args[]) {
        Graph g = new Graph(4);
        g.addEdge(0, 1);
        g.addEdge(0, 2);
        g.addEdge(1, 2);
        g.addEdge(2, 0);
        g.addEdge(2, 3);
        g.addEdge(3, 3);
        g.printGraph();
    }
}
```

**Output**
```
Node 0: -> 1 -> 2
Node 1: -> 2
Node 2: -> 0 -> 3
Node 3: -> 3
```

---

### 8. Sorting Algorithms
Popular sorting algorithms include:
- **Bubble Sort**
- **Selection Sort**
- **Merge Sort**
- **Quick Sort**

---

### 9. Searching Algorithms
Popular searching algorithms include:
- **Linear Search**
- **Binary Search**

---

### 10. String Manipulation
String handling involves processing and modifying strings efficiently.

---

### 11. Hashing
Hashing stores data in a structure called a hash table.

---

### 12. Recursion
Recursion involves functions that call themselves to solve subproblems.

---

### 13. Dynamic Programming
Dynamic Programming (DP) optimizes recursive solutions by storing subproblem results.

---

### 14. Conclusion and Best Practices
To excel in Java DSA:
- Focus on mastering data structures.
- Practice solving algorithmic problems.
- Use Java’s built-in libraries for efficient coding where possible.
