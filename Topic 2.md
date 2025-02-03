## Core Concepts of OOP with Examples

1.  **Reusability:**  Using existing code (like classes and methods) in new programs without rewriting it.
    ```java
    class Vehicle {
        int speed;
        int fuel;

        void displayInfo() {
            System.out.println("Speed: " + speed + " Fuel: " + fuel);
        }
    }

    class Car extends Vehicle {
        String brand;
    }
    ```

2.  **Encapsulation:** Wrapping data (attributes) and methods (behaviors) together in a single unit (class) and restricting direct access to some parts of the data.
    ```java
    class BankAccount {
        private double balance; // Cannot be accessed directly

        public void deposit(double amount) {
            balance += amount;
        }

        public double getBalance() {
            return balance;
        }
    }
    ```

3.  **Instantiating:** The process of creating an object from a class.
    ```java
    class Dog {
        String name;
    }

    public class Main {
        public static void main(String[] args) {
            Dog myDog = new Dog(); // Instantiating a Dog object
            myDog.name = "Buddy";
            System.out.println("Dog's name: " + myDog.name);
        }
    }
    ```

4.  **Abstraction:** Hides unnecessary details and shows only the essential features.
    ```java
    abstract class Animal {
        abstract void sound(); // Abstract method, no implementation
    }

    class Cat extends Animal {
        void sound() {
            System.out.println("Meow");
        }
    }
    ```

5.  **Inheritance:** Allows a class (child) to inherit properties and methods from another class (parent).
    ```java
    class Animal {
        void eat() {
            System.out.println("This animal eats food.");
        }
    }

    class Dog extends Animal {
        void bark() {
            System.out.println("The dog barks.");
        }
    }
    ```

6.  **Composition:** When a class is made up of objects of other classes ("has-a" relationship).
    ```java
    class Engine {
        void start() {
            System.out.println("Engine starts");
        }
    }

    class Car {
        Engine engine = new Engine(); // Composition

        void drive() {
            engine.start();
            System.out.println("Car is moving");
        }
    }
    ```

7.  **Aggregation:** A specialized form of composition where one class uses another but doesn’t own it ("has-a" relationship, weaker than composition).
    ```java
    class Player {
        String name;
        Player(String name) {
            this.name = name;
        }
    }

    class Team {
        String teamName;
        Player[] players;

        Team(String teamName, Player[] players) {
            this.teamName = teamName;
            this.players = players;
        }
    }
    ```

8.  **Overriding:** Allows a subclass to provide its own implementation of a method from the parent class.
    ```java
    class Animal {
        void sound() {
            System.out.println("Some sound...");
        }
    }

    class Dog extends Animal {
        @Override
        void sound() {
            System.out.println("Bark!");
        }
    }
    ```

9.  **Polymorphism:** Allows objects to take many forms. A method can behave differently depending on the object calling it.
    ```java
    class Shape {
        void draw() {
            System.out.println("Drawing a shape");
        }
    }

    class Circle extends Shape {
        void draw() {
            System.out.println("Drawing a circle");
        }
    }
