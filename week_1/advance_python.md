## Advance Python

**Instance Method**

Instance methods are the most common type of methods in Python classes. They are associated with instances of a class and operate on the instance’s data. When defining an instance method, the method’s first parameter is typically named self, which refers to the instance calling the method. This allows the method to access and manipulate the instance’s attributes.
```
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def introduce(self):
        return f"Hi, I'm {self.name} and I'm {self.age} years old."


# Creating an instance of the class
person1 = Person("Kishan", 20)

# Calling the instance method
print(person1.introduce())  # Output: Hi, I'm Kishan and I'm 30 years old.
```
 - Exercise
   - Define a Rectangle class with attribures `width`, `height`. Wrire a instance methods to calculate area of the rectangle and perimeter of the rectangle.

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
- [https://www.geeksforgeeks.org/decorators-in-python/?ref=header_search](https://www.geeksforgeeks.org/decorators-in-python/?ref=header_search)
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

**Comprehenssion**
  - [https://www.geeksforgeeks.org/comprehensions-in-python/](https://www.geeksforgeeks.org/comprehensions-in-python/)
- Exercises
   1. Given a list of numbers, remove all odd numbers from the list.
   2. Create a dictionary of squares of numbers from 1 to 10 using dictionary comprehenssion.
   3.  Create a dictionary of even numbers as keys and their squares as values using dictionary comprehenssion.
   4.  Generate a set of squares of numbers from 1 to 10 using set comprehenssion.
   5.  Generate a set of tuples containing numbers and their squares using set comprehenssion.

**Extended Keywords** (**args, kwargs**)
 - [https://www.geeksforgeeks.org/args-kwargs-python/](https://www.geeksforgeeks.org/args-kwargs-python/)

- Exercise
   1. Write a function calculate that takes any number of positional and keyword arguments. If a keyword argument operation is provided, it performs the specified operation (add, subtract, multiply, divide) on all the positional arguments. If no operation is provided, it should default to add.
   2. Write a function process_data that takes any number of positional and keyword arguments, prints the sum of all positional arguments, and then prints all the keyword arguments.
 
**Iterator and Generators**
 - [https://www.w3schools.com/python/python_iterators.asp](https://www.w3schools.com/python/python_iterators.asp)
 - [https://www.geeksforgeeks.org/generators-in-python/](https://www.geeksforgeeks.org/generators-in-python/)

- Exercise
   1. Write a Python program that creates a generator function that yields cubes of numbers from 1 to n. Accept n from the user.
   2.  Write a Python program to implement a generator that generates random numbers within a given range.

**Indexing And Slicing**
   - [https://www.geeksforgeeks.org/how-to-index-and-slice-strings-in-python/](https://www.geeksforgeeks.org/how-to-index-and-slice-strings-in-python/)
   - [https://realpython.com/lessons/indexing-and-slicing/](https://realpython.com/lessons/indexing-and-slicing/)
