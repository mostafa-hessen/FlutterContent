// 1- implicit interface
class Parent {
  name() {
    print("hello my name is ahmed");
  }

  eyes();//not word
}
class Child implements Parent {}

// 1- you must overrid all methodes   2-  you  can  get object form the Parent  3- you must declare the function

===================================================================================================================================
//  2- explicict interface

abstract class Parent {
  name() {
    print("hello parent");
  }

  eyes();
}

class Child implements Parent {}

// 1- you must make ovverid   2- class type abstract  3- you can make method without declar  4- you can't take object instance

===================================================================================================================================
