# 🐍 Python OOP: Abstract Class & Method Example

## 🎯 AIM

To create an **abstract class** named `Shape` with an **abstract method** `calculate_area`, and implement this method in two subclasses: `Rectangle` and `Circle`.

---

## 🧠 ALGORITHM

1. **Import ABC module**:
   - Use `from abc import ABC, abstractmethod` to define abstract classes and methods.

2. **Create Abstract Class `Shape`**:
   - Define an abstract method `calculate_area()` with `@abstractmethod`.

3. **Create Subclass `Rectangle`**:
   - Set default values for `length` and `breadth`.
   - Override `calculate_area()` to compute the rectangle area.

4. **Create Subclass `Circle`**:
   - Set default value for `radius`.
   - Override `calculate_area()` to compute the circle area.

5. **Create Objects & Call Methods**:
   - Instantiate `Rectangle` and `Circle`.
   - Call their `calculate_area()` methods.

---

## 💻 Program
~~~
from abc import ABC, abstractmethod
import math


class Shape(ABC):
    @abstractmethod
    def calculate_area(self):
        pass


class Rectangle(Shape):
    def __init__(self, length=5, breadth=4):
        self.length = length
        self.breadth = breadth

    def calculate_area(self):
        return self.length * self.breadth


class Circle(Shape):
    def __init__(self, radius=3):
        self.radius = radius

    def calculate_area(self):
        return math.pi * self.radius * self.radius


rect = Rectangle()
circ = Circle()


print("Area of Rectangle:", rect.calculate_area())
print("Area of Circle:", round(circ.calculate_area(), 2))
~~~
## Output
![446215005-ba3c4a39-a9f6-4d10-bde9-ec1c4279aa1a](https://github.com/user-attachments/assets/b1ea92ab-1951-4ac0-b0f0-0b03b8041f9e)

## Result
The area of the rectangle and circle was correctly calculated and displayed.


# 🐍 Python OOP: Encapsulation with Private Members

## 🎯 AIM

To implement **Encapsulation** in Python by defining a class `Rectangle` with **private member variables** `__length` and `__breadth`.

---

## 🧠 ALGORITHM

1. **Define the Class**:
   - Create a class `Rectangle` with two private attributes: `__length` and `__breadth`.

2. **Initialize Variables**:
   - Use the `__init__()` constructor to set initial values for `__length` and `__breadth`.

3. **Print Values**:
   - Display the private variables from within the class to demonstrate access.

4. **Instantiate the Object**:
   - Create an object of the `Rectangle` class to trigger the constructor.

---

## 💻 Program
~~~
  class Rectangle:
    __length = 0 
    __breadth = 0
    def __init__(self):
      self.__length = 5
      self.__breadth = 3
      print(self.__length)
      print(self.__breadth)
   
  obj = Rectangle()
~~~
## Output
![446215506-d0ddc174-7444-4c30-9fb5-4a2a142998da](https://github.com/user-attachments/assets/3c2f25c9-0edb-4668-baa0-683b429e2fdb)

## Result
The program successfully implements encapsulation by using private variables and public methods to set and get data.


# 🐟 Method Overriding-Fish and Shark Class Inheritance in Python

## 🧠 AIM:
To write a Python program that demonstrates class inheritance by creating a parent class `Fish` with a method `type`, and a child class `Shark` that overrides the `type` method.

## 📋 ALGORITHM:

1. Define the `Fish` class with a method named `type()` that prints `"fish"`.
2. Define the `Shark` class as a subclass of `Fish`, and override the `type()` method to print `"shark"`.
3. Create an instance of the `Fish` class named `obj_goldfish`.
4. Create an instance of the `Shark` class named `obj_hammerhead`.
5. Use a `for` loop to iterate over both objects.
6. Within the loop, call the `type()` method using the loop variable.
7. Output will demonstrate method overriding: printing `"fish"` and `"shark"` accordingly.

## 💻 PROGRAM:
~~~
# Parent Class
class Fish:
    def type(self):
        print("This is a fish")

# Child Class
class Shark(Fish):
    def type(self):
        print("This is a shark")

# Creating objects
f = Fish()
s = Shark()


f.type()
s.type()
~~~
## OUTPUT
![446216430-c04a3102-59eb-4240-a7bb-b91ac30d9d5d](https://github.com/user-attachments/assets/8c5f152d-693c-45d5-aaf5-00278b7dbb12)

## RESULT
The program successfully demonstrates class inheritance and method overriding in Python.


# 🐍 Python OOP: Operator Overloading (Less Than `<`)

## 🎯 AIM

To write a Python program that demonstrates **operator overloading** by overloading the **less than (`<`)** operator using a custom class.

---

## 🧠 ALGORITHM

1. **Create Class `A`**:
   - Define the `__init__()` method to initialize the object with a value `a`.

2. **Overload the `<` Operator**:
   - Define the `__lt__()` method with logic:
     - If `self.a < o.a`, return `"ob1 is less than ob2"`
     - Else, return `"ob2 is less than ob1"`

3. **Create Objects**:
   - Instantiate two objects `ob1` and `ob2` with values.

4. **Use `<` Operator**:
   - Use `print(ob1 < ob2)` to trigger the overloaded behavior.

---

## 💻 Program
~~~
class A:
    def __init__(self,a):
        self.a=a
    def __lt__(self,other):
        return self.a<other.a
ob1 = A(2)

ob2 = A(3)
if ob2<ob1:
    print("ob2 is less than ob1")
else:
    print("ob1 is less than ob2")
~~~
## Output
![446216795-e1bacf9b-a522-4321-9dca-9c46947ff691](https://github.com/user-attachments/assets/e3c3d494-2586-4750-8bb2-c2da9573695b)

## Result
The program successfully demonstrates operator overloading by customizing the behavior of the < operator using the lt() method in a user-defined class.


# # 🐍 Python OOP: Polymorphism with Classes

## 🎯 AIM

To create two specific classes — `Beans` and `Mango`. Then, create a **generic function** that can accept any object and determine its **type** (Fruit or Vegetable) and **color**, using polymorphism.

---

## 🧠 ALGORITHM

1. **Create Class `Beans`**:
   - Define `type()` method that prints `"Vegetable"`.
   - Define `color()` method that prints `"Green"`.

2. **Create Class `Mango`**:
   - Define `type()` method that prints `"Fruit"`.
   - Define `color()` method that prints `"Yellow"`.

3. **Define Generic Function `func(obj)`**:
   - Call `obj.type()` and `obj.color()` — this works with both `Beans` and `Mango` objects, showcasing **polymorphism**.

4. **Create Objects**:
   - Instantiate `Beans` and `Mango`.
   - Pass them to `func()` and execute the program.

---

## 💻 Program
~~~
  class Beans ():
     def type(self):
        print("Vegetable")
     def color(self):
        print("Green")

  class Mango ():
     def type(self):
        print("Fruit")
     def color(self):
        print("Yellow")

     def func(obj):
        obj.type()
        obj.color()

  obj_beans = Beans()
  obj_mango = Mango()
  func(obj_beans)
  func(obj_mango)
~~~
## Output
![446218651-bf97b439-b2e6-4fd7-aaa1-906d7ff16d04](https://github.com/user-attachments/assets/8ad789c9-a00a-481b-9c2b-67be46e61457)

## Result
The program successfully demonstrates polymorphism by using a generic function that interacts with different object types (Beans and Mango) through common method interfaces.

