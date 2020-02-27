## Access Modifiers
- public, private

## Java OOP
- Objects with methods and variables
- classes are blueprints for objects
- objects represent real word things

### Main Ideas
- Abstraction
  - objects, classes, and variables representing more complex underyling code and data
  - lets us avoid repeating the same work

- Encapsulation
  - practice of keeping fields in private classes and providing access to them from public methods
  - protective way to keep data and code safe
  - most of the time; variables are kept private
    - to have access to them outside of a class; we need to create **getters** and **setters**
  
```java
//save as Student.java
package com.javatpoint;
public class Student {
 private String name;
 public String getName() {
  return name;
 }
 public void setName(String name) {
  this.name = name
 }
}
//save as Test.java
package com.javatpoint;
class Test {
 public static void main(String[] args) {
  Student s = new Student();
  s.setName(“vijay”);
  System.out.println(s.getName());
 }
}
```  

- Inheritance
  - create new classes that share some of the attributes of exisiting classes
  - use 'extends'
    - Example1 extends Example2
      - Example1 is considered subclass
      - Example2 is considered super class
  
```java
class Mammal {

}
class Dolphin extends Mammal {

}
```

- Polymorphism
  - use the same word to mean different contexts
  - Overloading
    - different meanings are implied by the code itself
    - you can have multiple methods with the same name with different parameters
  - Overriding
    - different meanings are implied by the values of the supplied variables
    - if example1 has the same name of a method from example2 with the same number of parameters; example1's method overrides example2's method
    
    
```java
class Person {
 void walk() {
  System.out.println(“Can Run….”);
 }
}
class Employee extends Person {
 void walk() {
  System.out.println(“Running Fast…”);
 }
 public static void main(String arg[]) {
  Person p = new Employee(); //upcasting
  p.walk();
 }
}
```

- Interface 
  - a list of variables and methods
  - real world application: maybe you want a list or blueprint of a feature you want to build out
```java
public interface Example1 {
 final String flavor = "Beef";
 
 void openBag();
}
```
```java
public class Example2 implements Example1 {
  public static void main() {
    Example2 e2 = new Example2();
    e2.openBag();
  }
  
  @Override
  public void openBag() {
    System.out.println("Bag opened!")
  }
}
```
