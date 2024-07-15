
### Task 1: Using `reduce`

**Description**: Write a Dart function that takes a list of integers and returns 
the product of all the elements in the list using the `reduce` method. [1,2,68,120,13]


### Task 2: Using `where`
- Write a Dart function that takes a list of strings and returns a new list containing 
only the strings that start with the letter 'a' (case-insensitive) using the `where` method.
["ahmed","mostafa","adel"]


### Task 3: Creating and Using Extension Functions
-DeCreate an extension on the `String` class that adds a method called `reverse` which returns the reverse of the string. Then, use this extension in a Dart program.
=> mostafa => afatsom=> .split(' ')


Here’s a task focused on inheritance in Dart.

### Task: Implementing Inheritance in Dart

**Description**: Create a base class `Animal` with properties `name` and `age`, and a method `makeSound`. Then, create a derived class `Dog` that inherits from `Animal` and call methodes with change sound

```dart
class Animal {
  // Define properties
  String name;
  int age;

  // Constructor to initialize properties
  Animal(this.name, this.age);

  // Method to make a sound (to be overridden in derived classes)
  void makeSound() {
    print('Some generic animal sound');
  }
}
```

**Description**:
 - use the code below and make 2 instance Cat and doge give name,age and edite the sound  

**Example**:
```dart
void main() {
  // Create instances of the Dog and Cat classes

}

class Animal {
  // Define properties
  String name;
  int age;

  // Constructor to initialize properties
  Animal(this.name, this.age);

  // Method to make a sound (to be overridden in derived classes)
  void makeSound() {
    print('Some generic animal sound');
  }
}


##Encapsolation 

-make newfile by name privatClass and in your dart file make instance by your name try to set your name and get it
class Employee {
  String _name="name";
  int age=20;
  
  }
