# Week 5: Django Basics

Welcome to Django! After building a strong foundation in Python, OOP, databases, and DSA, you're now ready to learn the Django web framework. This week introduces Django's core concepts, architecture, and basic usage. You'll create your first Django project and understand how Django handles web development.

## Topics Covered

1. **What is Django?**
   - Overview of Django framework
   - Django vs other frameworks
   - Django's philosophy and design principles

2. **Django Architecture**
   - MTV (Model-Template-View) pattern
   - How Django processes requests
   - Django apps vs projects

3. **Setting Up Django**
   - Installing Django
   - Creating a new project
   - Running the development server
   - Django project structure

4. **Django Apps**
   - Creating and configuring apps
   - App structure and files
   - When to create new apps

5. **Models**
   - Defining models
   - Field types
   - Model relationships
   - Migrations

6. **Views and URLs**
   - Function-based views
   - URL patterns and routing
   - HttpResponse and render

7. **Templates**
   - Django template language
   - Template inheritance
   - Static files

8. **Admin Interface**
   - Setting up Django admin
   - Registering models
   - Customizing admin

## Resources

- [What is Django?](https://www.youtube.com/watch?v=t_p4ZyAYyaY)
- [Django Architecture](https://www.youtube.com/watch?v=xFkzKUzrRRFnZ7TSV)
- [Django Getting Started Playlist](https://www.youtube.com/playlist?list=PL2z1gXAKH9c3XUn2HYMWRbAon4z6AQ4CL) (Videos 1-36)

## Tasks

### Task 1: Django Installation and Setup
Set up Django on your system and create your first project.

**Requirements:**
- Install Django using pip
- Create a new Django project
- Run the development server
- Access the Django welcome page
- Explore the project structure

**Commands:**
```bash
pip install django
django-admin startproject myproject
cd myproject
python manage.py runserver
```

### Task 2: Create Your First App
Create a Django app and understand the app structure.

**Requirements:**
- Create a new app (e.g., 'blog' or 'todo')
- Add the app to INSTALLED_APPS in settings.py
- Create basic models, views, and templates
- Set up URL routing

**Example App Structure:**
```
myproject/
├── myproject/
│   ├── settings.py
│   ├── urls.py
│   └── ...
├── blog/
│   ├── migrations/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── tests.py
│   ├── urls.py
│   └── views.py
└── manage.py
```

### Task 3: Build a Simple Blog
Create a basic blog application with models, views, and templates.

**Requirements:**
- Create Post model with title, content, author, created_date
- Create views for listing posts and viewing individual posts
- Create templates for post list and post detail
- Set up URL patterns
- Add some sample data via Django shell or admin

**Example Models:**
```python
from django.db import models
from django.contrib.auth.models import User

class Post(models.Model):
    title = models.CharField(max_length=200)
    content = models.TextField()
    author = models.ForeignKey(User, on_delete=models.CASCADE)
    created_date = models.DateTimeField(auto_now_add=True)
    
    def __str__(self):
        return self.title
```

### Task 4: Django Admin Setup
Set up and customize the Django admin interface.

**Requirements:**
- Create a superuser
- Register your models with admin
- Customize admin display (list_display, search_fields)
- Add filters and ordering
- Explore admin customization options

## Tips for Success

- Follow the official Django tutorial alongside the video resources
- Pay attention to Django's project vs app distinction
- Practice the MTV pattern by thinking about each component's role
- Use Django's built-in features before trying to reinvent the wheel
- Read Django's excellent documentation regularly
- Don't worry if it feels overwhelming – Django has a learning curve, but it's worth it

## Next Steps

Congratulations on creating your first Django project! In Week 6, we'll cover Git and GitHub, which are essential for version control and collaboration. Meanwhile, continue exploring Django by adding features to your blog app or creating a new simple app.

Django is powerful, but remember: it's just Python with batteries included. Your Python skills from previous weeks will serve you well here. Keep building! 🚀
