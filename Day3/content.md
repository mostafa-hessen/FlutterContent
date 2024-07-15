### Today's Lecture Schedule: Higher Order Functions, Import, Lists, Maps, Sets, and Try-Catch

### 1. Higher Order Functions (30 minutes)

**Content:**
- Definition of Higher Order Functions.
- Using Higher Order Functions to pass functions as arguments.
- Returning functions from other functions.

**Examples:**

```dart
void printMessage(String message) {
  print(message);
}

void executeFunction(Function callback, String value) {
  callback(value);
}

void main() {
  executeFunction(printMessage, 'Hello, Dart!');
}
```

```dart
Function makeMultiplier(num multiplier) {
  return (num value) => value * multiplier;
}

void main() {
  var triple = makeMultiplier(3);
  print(triple(5)); // Output: 15
}
```

**Practical Exercise:**
- Write functions that accept other functions as arguments and return functions as values.

---

### 2. Importing Functions (30 minutes)

**Content:**
- How to organize code across multiple files.
- Using `import` to bring in code from other files.
- Dart standard libraries and how to import them.

**Examples:**

```dart
// In file1.dart
String greet(String name) => 'Hello, $name!';

// In main.dart
import 'file1.dart';

void main() {
  print(greet('Alice'));
}
```

**Practical Exercise:**
- Organize a Dart project using multiple files and import code between them.

---

### 3. Lists, Maps, and Sets (60 minutes)

**Content:**
- Definition and use of Lists.
- Definition and use of Maps.
- Definition and use of Sets.

**Examples:**

```dart
// List
void main() {
  List<int> numbers = [1, 2, 3, 4, 5];
  numbers.add(6);
  print(numbers); // Output: [1, 2, 3, 4, 5, 6]
}

// Map
void main() {
  Map<String, int> studentScores = {
    'Alice': 90,
    'Bob': 85,
    'Charlie': 95,
  };
  
  // إضافة طالب جديد
  studentScores['David'] = 88;
  
  // تحديث علامة طالب
  studentScores['Alice'] = 92;
  
  // التكرار على بيانات الطلاب
  studentScores.forEach((student, score) {
    print('Student: $student, Score: $score');
  });
  
  // الحصول على علامة طالب محدد
  print('Alice\'s score: ${studentScores['Alice']}'); // Output: Alice's score: 92
  
  // إزالة بيانات طالب
  studentScores.remove('Bob');
  
  print(studentScores); // Output: {Alice: 92, Charlie: 95, David: 88}
  

// Set
void main() {
  Set<String> fruits = {'apple', 'banana', 'orange'};
  fruits.add('apple'); // Duplicate entry will be ignored
  print(fruits); // Output: {apple, banana, orange}
}
```

**Practical Exercise:**
- Write programs using Lists, Maps, and Sets to manage data.

---

### 4. Try-Catch (30 minutes)

**Content:**
- Concept of error handling in Dart.
- Using `try`, `catch`, `finally` to handle errors.

**Examples:**

```dart
void main() {
  try {
    int result = 12 ~/ 0;
    print(result);
  } catch (e) {
    print('Error: $e');
  } finally {
    print('This is always executed.');
  }
}
```

**Practical Exercise:**
- Write programs using `try-catch` to handle various errors.

---

### Total: 3 Hours

### Tasks on List, Set, Map, and Try-Catch

#### 1. **Lists**

**Task:**
- Create a list containing the names of some fruits, add new fruits to it, and then print all the fruits.

- ["a","b","c"] => reverce it and print first 

- use x.add(5) with List x= List.filed(7,0) and print




#### 2. **Sets**

**Task:**
Create a set of unique numbers, add some new numbers to it, and print all the numbers.
- merge [1,3,3,2] [4,6,2,2] to set and tell what happend

#### 3. **Maps**

**Task:**
Create a map to store the names and ages of some people, add new entries to the map, and print all the entries by() for each loop )or (for in loop )
- writ a map and print keys and value



#### 4. **Try-Catch**

**Task:**
Write a program that attempts to divide a number by zero and handles the exception using try-catch. Print an error message if an exception occurs.


