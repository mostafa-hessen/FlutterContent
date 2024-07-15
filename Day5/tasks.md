### Task List

1. **Super Constructor Type 1**

**Description:** Create a Dart program using the `super` constructor to initialize properties of a parent class from a child class.

**Requirements:**
- Define a `Parent` class with two properties `x` and `y`.
- Define a `Child` class that extends `Parent` and initializes the `x` and `y` properties using the `super` constructor.
- In the `main` function, create an instance of the `Child` class and print the sum of `x` and `y`.

2. **Super Constructor Type 2**

**Description:** Create a Dart program using a shorter syntax to initialize properties of a parent class from a child class using `super`.

**Requirements:**
- Define a `Parent` class with two properties `x` and `y`.
- Define a `Child` class that extends `Parent` and initializes the `x` and `y` properties using the shorter `super` syntax.
- In the `main` function, create an instance of the `Child` class and print the sum of `x` and `y`.

3. **Override and Polymorphism**

**Description:** Create a Dart program to demonstrate method overriding and polymorphism using a parent class `Animal` and a child class `Dog`.

**Requirements:**
- Define an `Animal` class with properties `name` and `age`, and a method `makeSound`.
- Define a `Dog` class that extends `Animal` and overrides the `makeSound` method.
- In the `main` function, create an instance of the `Dog` class and call the `makeSound` method.

4. **Abstract Class Implementation**

**Description:** Create a Dart program using an abstract class `Animal` with a child class `Dog` implementing the abstract method `eat`.

**Requirements:**
- Define an abstract class `Animal` with an abstract method `eat` and a non-abstract method `s`.
- Define a `Dog` class that extends `Animal` and implements the `eat` method.
- In the `main` function, create an instance of the `Dog` class and call both the `eat` and `s` methods.

5. **Implicit Interface**

**Description:** Create a Dart program to demonstrate implicit interfaces using a class `Animal` and another class `C` implementing `Animal`.

**Requirements:**
- Define a class `Animal` with methods `eat` and `s`.
- Define a class `C` that implements `Animal`.
- Ensure that `C` overrides all methods from `Animal`.

6. **Explicit Interface**

**Description:** Create a Dart program to demonstrate explicit interfaces using an abstract class `Animal` and another class `C` implementing `Animal`.

**Requirements:**
- Define an abstract class `Animal` with an abstract method `eat` and a non-abstract method `s`.
- Define a class `C` that implements `Animal`.
- Ensure that `C` implements and overrides all methods from `Animal`.

7. **Abstract Class**

**Description:** Create a Dart program using an abstract class `Animal` with a child class `C` extending `Animal`.

**Requirements:**
- Define an abstract class `Animal` with an abstract method `eat` and a non-abstract method `s`.
- Define a class `C` that extends `Animal` and implements the `eat` method.
- In the `main` function, create an instance of the `C` class and call both the `eat` and `s` methods.


10. **Named Constructor**

**Description:** Create a Dart program to demonstrate the use of named constructors in a class `Parent`.

**Requirements:**
- Define a class `Parent` with properties `x` and `y` and a default constructor that initializes these properties.
- Define a named constructor `multiply` that prints the values of `x` and `y`.
- In the `main` function, create an instance of the `Parent` class using the named constructor.

11. **Mixin**

**Description:** Create a Dart program to demonstrate the use of mixins for adding functionality to classes.

**Requirements:**
- Define a mixin `Swimmer` with a method `swim`.
- Define a mixin `Flyer` with a method `fly`.
- Define a class `Animal` with a property `name`.
- Define a class `Bird` that extends `Animal` and uses the `Flyer` mixin.
- Define a class `Fish` that extends `Animal` and uses the `Swimmer` mixin.
- In the `main` function, create instances of `Bird` and `Fish` and call their respective methods.



13. **Enums**

**Description:** Create a Dart program to demonstrate the use of enums for defining a set of named values.

**Requirements:**
- Define an enum `Day` with values for each day of the week.
- In the `main` function, use an enum value to represent the current day.
- Print the current day and compare it to another enum value.