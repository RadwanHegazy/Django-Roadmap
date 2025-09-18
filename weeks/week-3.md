# Week 3: Database Fundamentals

This week introduces you to the world of databases, a crucial component of backend development. You'll learn about relational databases (SQL), NoSQL databases (MongoDB), and Object-Relational Mapping (ORM). Understanding databases is essential for working with Django's ORM and building data-driven applications.

## Topics Covered

1. **Relational Databases (SQL)**
   - What is SQL?
   - Basic SQL commands (SELECT, INSERT, UPDATE, DELETE)
   - Table relationships (one-to-one, one-to-many, many-to-many)
   - Joins and aggregations

2. **Database Normalization**
   - First Normal Form (1NF)
   - Second Normal Form (2NF)
   - Third Normal Form (3NF)
   - Benefits of normalization

3. **NoSQL Databases**
   - Introduction to MongoDB
   - Document-based storage
   - When to use NoSQL vs SQL

4. **Object-Relational Mapping (ORM)**
   - What is ORM?
   - Benefits of using ORM
   - How ORM translates between objects and database tables
   - Introduction to Django's ORM (preview for next weeks)

5. **Database Design**
   - Entity-Relationship Diagrams (ERD)
   - Primary keys, foreign keys
   - Indexing for performance

## Resources

- [SQL Crash Course](https://www.youtube.com/watch?v=HXV3zeQKqGY)
- [Database Normalization](https://www.youtube.com/watch?v=1HEHa_EJa0k)
- [MongoDB Crash Course](https://www.youtube.com/watch?v=ofme2o29ngU&t=1526s)
- [What is Database ORM?](https://www.youtube.com/watch?v=KthQ0UmBmxE)

## Tasks

### Task 1: SQL Practice
Set up a local database (SQLite for simplicity) and practice basic SQL operations.

**Requirements:**
- Create a database for a simple blog application
- Create tables for: Users, Posts, Comments
- Insert sample data
- Write queries to:
  - Get all posts by a specific user
  - Get comments for a specific post
  - Count total posts per user

**Example SQL:**
```sql
-- Create tables
CREATE TABLE users (
    id INTEGER PRIMARY KEY,
    username TEXT NOT NULL,
    email TEXT UNIQUE
);

CREATE TABLE posts (
    id INTEGER PRIMARY KEY,
    title TEXT NOT NULL,
    content TEXT,
    user_id INTEGER,
    created_at DATETIME DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (user_id) REFERENCES users(id)
);

-- Insert data
INSERT INTO users (username, email) VALUES ('john_doe', 'john@example.com');

-- Query examples
SELECT * FROM posts WHERE user_id = 1;
SELECT COUNT(*) as post_count FROM posts GROUP BY user_id;
```

### Task 2: Database Normalization Exercise
Take an unnormalized table and normalize it step by step.

**Requirements:**
- Start with a denormalized table (e.g., customer orders with repeated data)
- Apply 1NF, 2NF, and 3NF
- Create normalized tables
- Write SQL to recreate the relationships

### Task 3: MongoDB Introduction
If possible, set up MongoDB locally or use a cloud service like MongoDB Atlas.

**Requirements:**
- Create a database and collection
- Insert documents (similar to JSON objects)
- Query documents
- Update and delete documents
- Compare MongoDB operations with SQL

**Example MongoDB:**
```javascript
// Insert document
db.users.insertOne({
    username: "john_doe",
    email: "john@example.com",
    posts: [
        { title: "My First Post", content: "Hello World!" }
    ]
});

// Query
db.users.find({ username: "john_doe" });
```

### Task 4: Simple ORM Concept
Create a simple Python class that mimics ORM behavior (without using actual ORM libraries).

**Requirements:**
- Create a class that represents a database table
- Implement methods to "save" and "find" objects
- Use a list or dictionary to simulate database storage
- Demonstrate CRUD operations

## Tips for Success

- Start with SQLite for SQL practice – it's built into Python
- Use database visualization tools like DB Browser for SQLite
- Practice writing SQL queries regularly
- Understand the trade-offs between SQL and NoSQL databases
- Focus on database design principles – they'll serve you well in Django

## Next Steps

Database knowledge is fundamental for Django development. In Week 4, we'll explore Data Structures and Algorithms, which will sharpen your problem-solving skills. Meanwhile, start thinking about how databases will integrate with the web frameworks you'll learn in upcoming weeks.

Keep exploring the data world! 📊
