# Week 2: Python OOP (Object-Oriented Programming)

Building on the Python basics from Week 1, this week dives into Object-Oriented Programming (OOP) concepts. You'll learn how to create classes, work with objects, and implement key OOP principles like inheritance, polymorphism, and abstraction. These concepts are crucial for understanding Django's structure and building scalable applications.

## Topics Covered

1. **Classes and Objects**
   - Defining classes
   - Creating objects (instances)
   - Class attributes and instance attributes
   - Methods (instance methods, class methods, static methods)

2. **Inheritance**
   - Creating subclasses
   - Overriding methods
   - Using `super()` function
   - Multiple inheritance

3. **Polymorphism**
   - Method overriding
   - Method overloading (using *args and **kwargs)
   - Duck typing

4. **Encapsulation**
   - Private attributes and methods
   - Property decorators (@property, @setter)
   - Data hiding

5. **Abstraction**
   - Abstract base classes (ABC)
   - Abstract methods
   - Interfaces

6. **Special Methods (Dunder Methods)**
   - `__init__`, `__str__`, `__repr__`
   - Operator overloading

## Resources

### Arabic Resources
- [Osama Elzero Python OOP Playlist](https://www.youtube.com/playlist?list=PLUgz8T_NoattU54gGARPXPmmawQNl-1_T)

### English Resources
- [Bro Code Python OOP Tutorial](https://www.youtube.com/watch?v=IbMDCwVm63M)

## Tasks

Apply OOP concepts to build upon the tasks from Week 1. Focus on creating reusable, organized code.

### Task 1: Person Class with OOP
Create a `Person` class with attributes and methods as specified.

**Requirements:**
- Attributes: name, country, date_of_birth
- Method to calculate age (use datetime module)
- Method to print user name
- Method to print user country
- Create instances and demonstrate the methods

**Example Code:**
```python
from datetime import datetime

class Person:
    def __init__(self, name, country, date_of_birth):
        self.name = name
        self.country = country
        self.date_of_birth = date_of_birth
    
    def calculate_age(self):
        today = datetime.today()
        birth_date = datetime.strptime(self.date_of_birth, "%Y-%m-%d")
        age = today.year - birth_date.year - ((today.month, today.day) < (birth_date.month, birth_date.day))
        return age
    
    def print_name(self):
        print(f"Name: {self.name}")
    
    def print_country(self):
        print(f"Country: {self.country}")

# Create and test instances
person1 = Person("John Doe", "USA", "1990-05-15")
person1.print_name()
person1.print_country()
print(f"Age: {person1.calculate_age()}")
```

### Task 2: Inheritance Implementation
Extend the Person class from Task 1 with inheritance.

**Requirements:**
- Create a subclass (e.g., `Student` or `Employee`)
- Add additional attributes and methods to the subclass
- Override at least one method from the parent class
- Demonstrate inheritance by creating instances of both classes

### Task 3: Polymorphism Implementation
Implement polymorphism in your classes from Task 2.

**Requirements:**
- Create multiple subclasses with the same method name but different implementations
- Demonstrate polymorphism by calling the same method on different objects
- Show how the correct method is called based on the object type

### Task 4: Abstract Class
Create an abstract class and implement abstract methods.

**Requirements:**
- Use the `abc` module to create an abstract base class
- Define abstract methods that must be implemented by subclasses
- Create concrete subclasses that implement the abstract methods
- Demonstrate the abstract class usage

## Tips for Success

- OOP can be challenging at first, so take your time to understand each concept
- Practice creating classes for real-world objects (cars, animals, etc.)
- Read about design patterns early, as they'll help you understand OOP better
- Use the interactive Python shell to experiment with classes and objects
- Don't worry if it feels abstract at first – it will click with practice

## Next Steps

After completing Week 2, you'll have a strong foundation in Python OOP. In Week 3, we'll move into databases, which will prepare you for working with Django's ORM. Review your OOP code and think about how you might refactor your Week 1 tasks using classes.

Keep coding! 🚀
