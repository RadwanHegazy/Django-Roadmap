# Week 9: Testing & Design Patterns

This week focuses on writing tests for your Django applications and understanding design patterns that help you write clean, maintainable, and scalable code. Testing ensures your code works as expected, while design patterns provide reusable solutions to common problems.

## Topics Covered

1. **Django Testing**
   - Writing unit tests
   - Testing views, models, and forms
   - Using Django’s test client
   - Test-driven development (TDD) basics

2. **Design Patterns**
   - Introduction to design patterns
   - Creational design patterns (Singleton, Factory, Builder)
   - Structural design patterns (Adapter, Decorator, Facade)
   - Behavioral design patterns (Observer, Strategy, Command)

3. **Clean Code Principles**
   - SOLID principles
   - KISS (Keep It Simple, Stupid)
   - DRY (Don't Repeat Yourself)
   - YAGNI (You Aren't Gonna Need It)

## Resources

- [Django Testing Playlist](https://www.youtube.com/playlist?list=PLbpAWbHbi5rMF2j5n6imm0enrSD9eQUaM)
- [Creational Design Patterns](https://www.youtube.com/@devgeeksacademy3340)
- [SOLID Principles](https://www.youtube.com/playlist?list=PLwWuxCLlF_uevri_OpofVLXkRRFnZ7TSV)
- [KISS Principle](https://www.youtube.com/watch?v=Dd67djMNe8E)
- [DRY Principle](https://www.youtube.com/watch?v=znpdlYgvU3M)
- [YAGNI Principle](https://www.youtube.com/watch?v=_Al7qI4vMt0)

## Tasks

### Task 1: Write Unit Tests for Django App
Write tests for your existing Django applications.

**Requirements:**
- Write tests for models, views, and forms
- Use Django’s TestCase class
- Test CRUD operations
- Run tests using `python manage.py test`
- Aim for good test coverage

**Example Test:**
```python
from django.test import TestCase
from .models import Post

class PostModelTest(TestCase):
    def setUp(self):
        Post.objects.create(title="Test Post", content="Test content")

    def test_post_content(self):
        post = Post.objects.get(id=1)
        self.assertEqual(post.title, "Test Post")
```

### Task 2: Implement Creational Design Patterns
Practice implementing creational design patterns in Python.

**Requirements:**
- Implement Singleton pattern
- Implement Factory pattern
- Implement Builder pattern
- Provide examples and use cases

### Task 3: Apply Clean Code Principles
Refactor your existing codebase applying clean code principles.

**Requirements:**
- Identify code smells and refactor
- Apply SOLID principles
- Remove duplicate code (DRY)
- Simplify complex code (KISS)
- Avoid unnecessary features (YAGNI)

### Task 4: Design Pattern Examples
Create examples for structural and behavioral design patterns.

**Requirements:**
- Implement Adapter, Decorator, Facade patterns
- Implement Observer, Strategy, Command patterns
- Explain when to use each pattern

## Tips for Success

- Write tests early and often
- Use tests to guide your development (TDD)
- Understand the problem before applying design patterns
- Don’t overuse patterns; use them when they add value
- Keep your code simple and readable

## Next Steps

Testing and design patterns are key to professional software development. In Week 10, we'll explore advanced topics like caching, web sockets, Celery, Docker, and deployment. Meanwhile, keep practicing writing tests and refactoring your code.

Quality code is maintainable code. Build it right! 🛠️
