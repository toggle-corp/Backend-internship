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
