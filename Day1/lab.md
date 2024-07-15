



### Training Tasks on Variables, Operators, and Control Statements

#### Task 1: Working with Variables
1. **Define and Print Variables**
   - Write a Dart program that defines variables of different types (`int`, `double`, `String`, `bool`) and prints their values.
  

2. **Variable Reassignment**
   - Define a `String` variable and assign a value to it. Reassign a new value to the same variable and print both values.
  

3. **Constant Variables**
   - Define a `const` and a `final` variable and print their values.
   - tell me what the diffrent between const and final


#### Task 2: Using Arithmetic and Logical Operators
1. **Arithmetic Operations**
   - Write a Dart program that performs and prints the results of addition, subtraction, multiplication, division, and modulus operations between two integers.
   
   - take this list [1,3,2,4,5,6,7,8,9,10] need to print only odd numbers

2. **Logical Operations**
   - Write a Dart program that uses logical operators 
    (`&&`, `||`, `!=`) 
   

#### Task 3: Control Statements
1. **If-Else Statements**
   - Write a Dart program that uses an `if-else` statement to check if a number is positive, negative, or zero and prints the result.
   

2. **For Loop**
   - Write a Dart program that uses a `for` loop to print the numbers from 1 to 10.
   

3. **While Loop**
   - Write a Dart program that uses a `while` loop to print the even numbers from 2 to 20.
   

4. **Do-While Loop**
   - Write a Dart program that uses a `do-while` loop to print the numbers from 10 to 1.
   

5. **Nested Loops**
   
   
   





<!-- mandatory search diffrent between var and dynamic  and solve this-->
### Exercise 1: Using `var`

Write a Dart program that defines a variable using `var` and assigns an initial value to it. Then, try changing the variable's type and see what happens.

```dart
void main() {
  var age = 25; // The variable type is int
  print(age);
  
  // Try changing the type to String
  // age = 'Twenty five'; 
}
```

### Exercise 2: Using `dynamic`

Write a Dart program that defines a variable using `dynamic` and assigns an initial value to it. Then, try changing the variable's type and see what happens.

```dart
void main() {
  dynamic value = 10; // The variable type is int
  print(value);
  
  value = 'Hello'; // The variable type changes to String
  print(value);
}
```