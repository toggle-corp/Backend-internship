## Advance Python

**Static Method**

Static methods, as the name suggests, are not bound to either the class or its instances. They are defined using the @staticmethod decorator and do not take a reference to the instance or the class as their first parameter. Static methods are essentially regular functions within the class namespace and are useful for tasks that do not depend on instance-specific or class-specific data.

```
class MathOperations:
    @staticmethod
    def add(x, y):
        return x + y

    @staticmethod
    def subtract(x, y):
        return x - y

# Using static methods without creating an instance
print(MathOperations.add(5, 3))        # Output: 8
print(MathOperations.subtract(10, 4))  # Output: 6
```
In this example, the MathOperations class features static methods add and subtract for performing basic arithmetic operations. These methods can be directly invoked on the class without creating an instance, providing a convenient and state-independent way to perform mathematical operations.

 - Exercise
    1. Create a class called `StringOperations` with a static method `is_palindrome` that takes a string as an argument and returns `True` if the string is a palindrome, and `False` otherwise.
    2. Create a class called `DateUtils` with a static method `format_date` that takes a date object and returns it as a string in the format `YYYY-MM-DD`.

**Class Methods**

Class methods are associated with the class rather than instances. They are defined using the @classmethod decorator and take the class itself as the first parameter, usually named cls. Class methods are useful for tasks that involve the class rather than the instance, such as creating class-specific behaviors or modifying class-level attributes.
```
class MyClass:
    class_variable = 0

    def __init__(self, value):
        self.instance_variable = value

    @classmethod
    def class_method(cls, x):
        cls.class_variable += x
        return cls.class_variable

# Creating instances of the class
obj1 = MyClass(5)
obj2 = MyClass(10)

# Calling the class method
print(MyClass.class_method(3))  # Output: 3
print(MyClass.class_method(7))  # Output: 10
```
- Exercise
    1. Create a class `Counter` with a class attribute `count`. Add a class method increment that increments the count by 1. Add another class method reset that sets the count back to 0.
    2. Create a class `Date` with attributes `day`, `month`, and `year`. Add a class method `today` that returns a new instance of Date with the current date.

**Decorator**
- [https://www.geeksforgeeks.org/decorators-in-python/?ref=header_search]()
- Exercise
   1. Create a decorator that modifies the return value of a function by doubling it.
   2. Write a Python program to create a decorator function to measure the execution time of a function.

**Lambda Function**

Python Lambda Functions are anonymous functions means that the function is without a name. As we already know the def keyword is used to define a normal function in Python. Similarly, the lambda keyword is used to define an anonymous function in python.

Difference Between Lambda functions and def defined function
The code defines a cube function using both the ‘def' keyword and a lambda function. It calculates the cube of a given number (5 in this case) using both approaches and prints the results. The output is 125 for both the ‘def' and lambda functions, demonstrating that they achieve the same cube calculation.

```
def cube(y):
	return y*y*y

lambda_cube = lambda y: y*y*y
print("Using function defined with `def` keyword, cube:", cube(5))
print("Using lambda function, cube:", lambda_cube(5))
```

- Exercise
   1. Write a Python program to filter a list of even integers using Lambda.
   2. Write a Python program to filter a list of odd integers using Lambda.
   3. Write a Python program to square and cube every number in a given list of integers using Lambda.
