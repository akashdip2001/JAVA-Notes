# Java Study Guide


---

Contents

1. Introduction to Java


2. Java Basics


3. Control Flow Statements


4. Object-Oriented Programming


5. Exception Handling


6. Strings and String Handling


7. Arrays and Collections


8. Searching and Sorting


9. Working with Date and Time


10. Problem Solving and Sample Exercises




---

1. Introduction to Java

Java is a platform-independent language, meaning it can run on any device that has a Java Virtual Machine (JVM). It's known for its object-oriented structure and simplicity, making it a powerful language for beginners and advanced users alike.

Example: "Hello, World!" in Java

The first step in learning any language is to write a program that prints "Hello, World!" to the screen.

public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}

Explanation:

public class HelloWorld: Defines a class named HelloWorld. In Java, all code should be inside a class.

public static void main(String[] args): The main method is the entry point for any Java program. It must be written exactly as shown.

System.out.println("Hello, World!");: This line prints "Hello, World!" to the console.


Output:

Hello, World!



---

2. Java Basics

Data Types

Java supports several primitive data types:

int: Stores integers (e.g., 10, -45).

double: Stores decimal numbers (e.g., 3.14).

char: Stores single characters (e.g., 'A').

boolean: Stores true/false values.


Example

int age = 25;
double salary = 50000.50;
char grade = 'A';
boolean isStudent = false;

System.out.println("Age: " + age);
System.out.println("Salary: " + salary);
System.out.println("Grade: " + grade);
System.out.println("Is Student: " + isStudent);

Output:

Age: 25
Salary: 50000.5
Grade: A
Is Student: false


Variables and Constants

Variables store values that can change, while constants use final to prevent changes.

int num = 5;           // Variable
final double PI = 3.14; // Constant

3. Control Flow Statements

Control flow statements determine the order in which statements are executed in a program.

if-else Statement

Used for conditional logic.

int age = 20;
if (age >= 18) {
    System.out.println("Adult");
} else {
    System.out.println("Minor");
}

Explanation: Checks if age is 18 or more; if true, it prints "Adult"; otherwise, "Minor."

Output:

Adult


Loops

for loop: Executes a set number of times.

while loop: Repeats while a condition is true.


for (int i = 0; i < 5; i++) {
    System.out.println("Iteration: " + i);
}

Output:

Iteration: 0
Iteration: 1
Iteration: 2
Iteration: 3
Iteration: 4


switch-case

Switch-case is used to select one of many code blocks based on the value of a variable.

int day = 3;
switch(day) {
    case 1: System.out.println("Monday"); break;
    case 2: System.out.println("Tuesday"); break;
    case 3: System.out.println("Wednesday"); break;
    default: System.out.println("Invalid day");
}

Output:

Wednesday


4. Object-Oriented Programming

Java is object-oriented, which means it models real-world entities using classes and objects.

Class and Object

A class is a blueprint, and an object is an instance of a class.

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

Explanation: Car class has properties color and speed, and a method display to show them.

Output:

Color: Red, Speed: 100


Inheritance, Polymorphism, Encapsulation, and Abstraction

Inheritance: Allows a class to inherit properties from another.

Polymorphism: Lets an object take many forms (method overloading/overriding).

Encapsulation: Hides data using private and exposes it through public methods.

Abstraction: Shows only essential details; hides the complex parts.


5. Exception Handling

Java's exception handling ensures errors are caught and managed without crashing.

try {
    int result = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("Cannot divide by zero!");
} finally {
    System.out.println("Done!");
}

Output:

Cannot divide by zero!
Done!


6. Strings and String Handling

Java has the String class with powerful methods for handling text.

String s = "Hello, World!";
System.out.println("Length: " + s.length());
System.out.println("Uppercase: " + s.toUpperCase());
System.out.println("Substring: " + s.substring(7));

Output:

Length: 13
Uppercase: HELLO, WORLD!
Substring: World!


7. Arrays and Collections

Array

An array is a fixed-size collection of elements of the same type.

int[] numbers = {1, 2, 3};
System.out.println(numbers[0]); // Accessing element

ArrayList (Dynamic Array)

Part of java.util, it allows dynamic resizing.

ArrayList<String> list = new ArrayList<>();
list.add("Element");
System.out.println(list.get(0));

Output:

Element


8. Searching and Sorting

Linear Search

Sequentially checks each element until the desired one is found.

public static int linearSearch(int[] array, int key) {
    for (int i = 0; i < array.length; i++) {
        if (array[i] == key) return i;
    }
    return -1;
}

Binary Search

Efficient for sorted arrays by repeatedly dividing the search interval.

Arrays.binarySearch(array, key);

Sorting

Arrays.sort(): Sorts arrays.

Collections.sort(): Sorts collections.


9. Working with Date and Time

The java.time package provides classes to work with date and time.

LocalDate date = LocalDate.now();
System.out.println("Today's date: " + date);

Output:

Today's date: 2023-10-30 (example)


10. Problem Solving and Sample Exercises

Reverse a String

public static String reverse(String str) {
    return new StringBuilder(str).reverse().toString();
}

Output:

reverse("Java") -> "avaJ"


---



