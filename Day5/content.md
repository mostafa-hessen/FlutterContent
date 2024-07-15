**super constructor**
```dart
*super Type 1
void main() {
  Child obj = Child(10, 2,4);
  print(obj.x + obj.y);
}

class Parent {
  int x;
  int y;
  Parent(this.x, this.y);
}

class Child extends Parent {
  // int s;
  Child(int c,int x,int y):super(x,y);
}```
===================================================
*super type 2
void main() {
  Child obj = Child(10, 2);
  print(obj.x + obj.y);
}

class Parent {
  int x;
  int y;
  Parent(this.x, this.y);
}

class Child extends Parent {
  // int s;
  Child(super.x, super.y);
}
```


**Override and polymorphism**

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

class Dog extends Animal{
  Dog(super.name, super.age);

  @override
  void makeSound() {
    print('hi');
  }
}
```


**Abstract**
```dart
abstract  class Animal {
  eat();

  s(){
    print('s');
  }
}

class Dog extends Animal{
  eat(){

  }
}
```

**Diffrent between explicit and implisit ans abstract**
1-implicit interface  
``` dart
 class Animal {
  eat(){

  }

  s() {
    print('s');
  }
}

class C implements Animal {
  
 

}

**we can make object instance from animal 
** we must make ovverid for all method in parent at child
** in class animal we must write a defention of method
```
2-Explicit interface 

```dart

abstract class Animal {
  eat();

  s(String h) {
    print('s$h');
  }
}

class C implements Animal {
  eat(){

  }
  @override
  s(String h) {
    // TODO: implement s
    throw UnimplementedError();
  }
 
  }
```
3- Abstract 
```dart

abstract class Animal {
  eat();


  s(String h) {
    print('s$h');
  }
}

class C extends Animal {
  @override
  eat() {
   print("hello:")
  }
 
  }
```

**complex implements 3**

```dart
void main() {
  // print(Anima)
    Dog dog = Dog();
  dog.makeSound(); // Dog barks
  dog.play();     // Dog is playing

}


abstract class Animal {
  void makeSound(); // دالة مجردة
}

abstract class Pet {
  void play(); // دالة مجردة
}

class Dog implements Animal, Pet {
  @override
  void makeSound() {
    print("Dog barks");
  }

  @override
  void play() {
    print("Dog is playing");
  }
}

```

**using extends with implement**
```dart
abstract class Animal {
  void makeSound(){
 print("d");   
  }
}

abstract class Pet {
  void play(){
    print("Dog is playing");
    
  }
}

class Dog extends Animal implements Pet {
 

  @override
  void play() {
    print("Dog is playing");
  }
}

void main() {
  Dog dog = Dog();
  dog.makeSound(); // Dog barks
  dog.play();      // Dog is playing
}
```
**named constrcutore**
```dart
void main() {
  Parent name = Parent.multibly(1, 2);

  // print(object);
}

class Parent {
  int? x;
  int? y;

  Parent(this.x, this.y) {
    print("hello $x  and $y");
  }

  Parent.multibly(this.x, this.y) {
    print(x);
  }
}

```

**mixin**
```dart
// Mixin لإضافة خاصية السباحة
mixin Swimmer {
  void swim() {
    print("Swimming...");
  }
}

// Mixin لإضافة خاصية الطيران
mixin Flyer {
  void fly() {
    print("Flying...");
  }
}

// فئة الحيوانات
class Animal {
  String name;

  Animal(this.name);
}

// فئة الطائر
class Bird extends Animal with Flyer {
  Bird(String name) : super(name);
}

// فئة السمكة
class Fish extends Animal with Swimmer {
  Fish(String name) : super(name);
}

void main() {
  Bird eagle = Bird("Eagle");
  eagle.fly(); // الطائر الذي تم انشاؤه يطير

  Fish shark = Fish("Shark");
  shark.swim(); // السمكة التي تم انشاؤها تسبح
}

```

**anonymous object**
```dart

void main(List<String> args) {
  List<P> list = [C(), B(), D()];

  print(list[0].nme);
}

class P {
  int nme = 1;
}

class C extends P {}

class B extends P {}

class D extends P {}

```


**Enums**

```dart
// تعريف Enum لأيام الأسبوع
enum Day {
  monday,
  tuesday,
  wednesday,
  thursday,
  friday,
  saturday,
  sunday
}

void main() {
  // استخدام قيم Enum
  Day today = 'wednesday';
  
  // طباعة قيم Enum
  print(today); // الناتج: Day.wednesday
  
  // مقارنة قيم Enum
  if (today == Day.wednesday) {
    print('Today is Wednesday');
  }
}
```