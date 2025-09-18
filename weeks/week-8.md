# Week 8: Intermediate Django

Now that you have Django basics, this week dives into intermediate concepts that will make you a more proficient Django developer. You'll learn about Django ORM in depth, REST APIs, Django Rest Framework, authentication, and more advanced Django features.

## Topics Covered

1. **Django ORM Advanced**
   - Complex queries with Q objects
   - Select related and prefetch related
   - Custom managers and querysets
   - Database optimization techniques

2. **REST APIs**
   - REST principles
   - HTTP methods and status codes
   - API design best practices
   - Building APIs with Django

3. **Django Rest Framework (DRF)**
   - Serializers
   - ViewSets and Routers
   - Authentication and permissions
   - Pagination and filtering

4. **Authentication & Authorization**
   - Django's authentication system
   - User models and permissions
   - Login/logout views
   - Custom user models

5. **JWT (JSON Web Tokens)**
   - JWT fundamentals
   - Implementing JWT in Django
   - Token-based authentication
   - Refresh tokens

6. **Postman for API Testing**
   - Setting up Postman
   - Creating request collections
   - Environment variables
   - API documentation

## Resources

- [Django ORM Playlist](https://www.youtube.com/playlist?list=PLdLYbRBk3sGmWHmS4fYTucOImkssv8K3R)
- [REST APIs](https://www.youtube.com/playlist?list=PLTCrU9sGybupzS5-3iYTsYUI1emBDKdHu)
- [Postman Tutorial](https://www.youtube.com/watch?v=zD8HaT7uX5A)
- [Django Rest Framework Arabic](https://www.youtube.com/watch?v=TJnvIyk_7xU&list=PLXqhO5lRtxJV6oWcW2vlPHRzRFF6gVvc3)
- [Django Rest Framework English](https://www.youtube.com/watch?v=tujhGdn1EMI)
- [Django Serializers](https://www.youtube.com/watch?v=hSGVNlEmmyE)
- [Authentication & Authorization](https://www.youtube.com/watch?v=7ijBiXddB7w)
- [JWT](https://www.youtube.com/watch?v=B-x7eeYtFIA)
- [JWT with DRF](https://www.youtube.com/watch?v=KLua_cYGLec)

## Tasks

### Task 1: Advanced Django ORM
Practice complex database queries and optimization.

**Requirements:**
- Create models with relationships (ForeignKey, ManyToMany)
- Use Q objects for complex queries
- Implement select_related and prefetch_related
- Create custom managers
- Optimize database queries

**Example:**
```python
# Complex query with Q objects
from django.db.models import Q

# Get posts by user or with specific tags
posts = Post.objects.filter(
    Q(author__username='john') | Q(tags__name='python')
).distinct()

# Optimize with select_related
posts = Post.objects.select_related('author').all()

# Custom manager
class PublishedManager(models.Manager):
    def get_queryset(self):
        return super().get_queryset().filter(status='published')
```

### Task 2: Build REST API with DRF
Create a RESTful API for your blog application.

**Requirements:**
- Install and configure Django Rest Framework
- Create serializers for your models
- Build ViewSets for CRUD operations
- Set up URL routing with routers
- Add pagination and filtering

**Example Serializer:**
```python
from rest_framework import serializers
from .models import Post

class PostSerializer(serializers.ModelSerializer):
    author_name = serializers.CharField(source='author.username', read_only=True)
    
    class Meta:
        model = Post
        fields = ['id', 'title', 'content', 'author', 'author_name', 'created_date']
        read_only_fields = ['author', 'created_date']
```

### Task 3: Authentication System
Implement user authentication and permissions.

**Requirements:**
- Set up Django authentication
- Create login/logout views
- Add user registration
- Implement permissions for API endpoints
- Use JWT for API authentication

### Task 4: API Testing with Postman
Create comprehensive API tests using Postman.

**Requirements:**
- Create a Postman collection for your API
- Test all CRUD operations
- Set up authentication flows
- Create environment variables
- Generate API documentation
- Test error scenarios

### Task 5: Todo App with DRF
Build a complete todo application with DRF and JWT.

**Requirements:**
- Create Todo model
- Build REST API endpoints
- Implement JWT authentication
- Add proper permissions
- Create Postman collection
- Write basic tests

## Tips for Success

- DRF has excellent documentation – use it extensively
- Start with simple APIs and gradually add complexity
- Always consider authentication and permissions early
- Use Postman to test your APIs thoroughly
- Practice writing clean, reusable serializers

## Next Steps

You've now covered intermediate Django concepts! In Week 9, we'll focus on testing and design patterns. Meanwhile, continue building APIs and experimenting with DRF features.

Remember: APIs are the backbone of modern web applications. Master these skills! 🔌
