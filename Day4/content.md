**Session one**

# Key Concepts of Higher-Order Functions and Extintion Function
**1- Higher order function**
a. **Functions as Parameters:**
   A higher-order function can take a function as an argument.

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

b. **Functions as Return Values:**
   A higher-order function can return another function.

   ```dart
   Function makeMultiplier(num multiplier) {
     return (num value) => value * multiplier;
   }

   void main() {
     var triple = makeMultiplier(3);
     print(triple(5)); // Output: 15
   }
   ```

c. **Combined Usage:**
   Higher-order functions can combine both concepts: taking functions as parameters and returning functions.

   ```dart
   Function applyOperation(Function operation, num value) {
     return (num x) => operation(x, value);
   }

   num add(num a, num b) => a + b;

   void main() {
     var addFive = applyOperation(add, 5);
     print(addFive(10)); // Output: 15
   }
   ```

### Practical Examples

1. **Using `map` with Lists:**
   The `map` function is a higher-order function that transforms each element of a list using a provided function.

   ```dart
   void main() {
     List<int> numbers = [1, 2, 3, 4, 5];
     List<int> doubled = numbers.map((num) => num * 2).toList();
     print(doubled); // Output: [2, 4, 6, 8, 10]
   }
   ```

2. **Using `forEach` with Lists:**
   The `forEach` method executes a function for each element in the list.

   ```dart
   void main() {
     List<String> fruits = ['apple', 'banana', 'cherry'];
     fruits.forEach((fruit) => print(fruit));
   }
   ```

3. **Using `reduce` with Lists:**
   The `reduce` method combines all elements of the list into a single value using a provided function.

   ```dart
   void main() {
     List<int> numbers = [1, 2, 3, 4, 5];
     int sum = numbers.reduce((a, b) => a + b);
     print(sum); // Output: 15
   }
   ```

4. **Filtering with `where`:**
   The `where` method filters elements based on a condition provided by a function.

   ```dart
   void main() {
     List<int> numbers = [1, 2, 3, 4, 5];
     List<int> evenNumbers = numbers.where((num) => num.isEven).toList();
     print(evenNumbers); // Output: [2, 4]
   }
   ```

   **2- Extiontion Function**
   
  ```dart


  EX1:
  String numberString = "123";
  print(numberString.toIntSafe()); // Output: 123

  String invalidNumberString = "abc";
  print(invalidNumberString.toIntSafe()); // Output: 0

  

  extension StringParsing on int {
  int toIntSafe() {
    return int.tryParse(this) ?? 0;
  }
   }



    Ex2:
    
   ```
