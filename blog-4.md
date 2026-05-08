4. How do the four pillars of OOP—Inheritance, Polymorphism, Abstraction, and Encapsulation—help manage logic and reduce complexity in large-scale TypeScript projects?  


  In large-scale TypeScript projects, managing complex logic becomes difficult if everything is written in a single place. The four pillars of Object-Oriented Programming (OOP)—Inheritance, Polymorphism, Abstraction, and Encapsulation—help organize code in a structured, reusable, and maintainable way. 

বড় TypeScript প্রজেক্টে কোড জটিল হয়ে যায় যদি সবকিছু একসাথে লেখা হয়। এই জটিলতা কমাতে OOP-এর চারটি মূল ধারণা—Encapsulation, Inheritance, Polymorphism, Abstraction খুব গুরুত্বপূর্ণ ভূমিকা রাখে। 

1. Encapsulation (Data Hiding + Protection)
Encapsulation means wrapping data and methods inside a class and restricting direct access to some parts.
How it helps:
Protects data from unwanted changes
Makes code safer and easier to manage
Reduces dependency between components
 Encapsulation (ডাটা লুকানো ও সুরক্ষা)
Encapsulation মানে হলো ডাটা এবং ফাংশনকে একটি class-এর ভিতরে রাখা এবং সরাসরি access বন্ধ করা।
কিভাবে সাহায্য করে:
ডাটা নিরাপদ থাকে
ভুল পরিবর্তন থেকে রক্ষা করে
কোড সহজে manage করা যায়

Example: 

class BankAccount {
    private balance: number = 0;

    deposit(amount: number) {
        this.balance += amount;
    }


    getBalance(): number {
        return this.balance;
    }
}

2. Inheritance (Code Reusability)
Inheritance allows a class to reuse properties and methods from another class.
How it helps:
Avoids code duplication
Builds hierarchical structure
Makes code reusable and scalable
Inheritance (কোড পুনরায় ব্যবহার)
Inheritance দিয়ে একটি class অন্য class-এর properties ও methods ব্যবহার করতে পারে।
কিভাবে সাহায্য করে:
কোড পুনরায় লেখা লাগে না
structure পরিষ্কার থাকে
বড় প্রজেক্ট সহজ হয়

Example:
class Animal {
    move() {
        console.log("Moving...");
    }
}

class Dog extends Animal {
    bark() {
        console.log("Barking...");
    }
}


3. Polymorphism (One Interface, Many Forms)
Polymorphism allows the same method to behave differently in different classes.
How it helps:
Makes code flexible
Reduces if-else complexity
Easier to extend functionality
Polymorphism (একই ফাংশন, ভিন্ন আচরণ)
একই method বিভিন্ন class-এ ভিন্নভাবে কাজ করে।
কিভাবে সাহায্য করে:
if-else কমে যায়
কোড flexible হয়
নতুন feature যোগ করা সহজ হয়

Example:
class Animal {

    sound() {
        console.log("Some sound");
    }
}


class Cat extends Animal {
    sound() {
        console.log("Meow");
    }
}

class Dog extends Animal {
    sound() {
        console.log("Bark");
    }
}

4. Abstraction (Hiding Complexity)
Abstraction hides internal implementation and shows only necessary features.
How it helps:
Reduces complexity
Focuses only on important features
Improves code readability
 Abstraction (জটিলতা লুকানো)
Abstraction এর মাধ্যমে প্রয়োজনীয় অংশ দেখানো হয়, ভিতরের জটিলতা লুকানো থাকে।
কিভাবে সাহায্য করে:
জটিল কোড সহজ হয়
ব্যবহারকারী শুধু দরকারি অংশ দেখে
readability বাড়ে

Example:
abstract class Vehicle {
  
    abstract start(): void;
}

class Car extends Vehicle {
    start() {
        console.log("Car started");
    }
}

