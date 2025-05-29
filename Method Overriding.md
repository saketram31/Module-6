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
