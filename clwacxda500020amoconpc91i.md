---
title: "Secure Your Django App with Parameterized Queries"
seoTitle: "Django App Security: Use Parameterized Queries"
seoDescription: "Secure your Django app from SQL injection attacks with parameterized queries. Learn how to implement them using Django ORM for enhanced security"
datePublished: Fri May 17 2024 07:27:34 GMT+0000 (Coordinated Universal Time)
cuid: clwacxda500020amoconpc91i
slug: secure-your-django-app-with-parameterized-queries
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1715898628039/0b8c7f11-ce2b-485d-b0e7-3da4e8309e4f.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1715898704491/5cffbb81-fc17-4856-b1e1-bb5dd4b90ea7.png
tags: django, web-development, security, backend

---

Building software goes beyond creating a functional application or solution. You also need to protect user data and privacy, which shows you care not only for the problem your application solves but also for your users.

In this short guide, we will discuss parameterized queries and how they help improve the security of your django application.

Let's learn!

## What are Parameterized Quieres?

Parameterized Quieres are security measures to prevent SQL injection attacks when taking user-generated data. They ensure that the data from the client side is validated and that SQL commands within the user data are separated.

On the server side, when handling user-generated data, instead of embedding it within an SQL query, you use parameters so the database can tell the difference between code and data and prevent malicious input from being treated as part of the query.

## How Does Parameterized Queries Work in Django?

[Django](https://docs.djangoproject.com/en/5.0/) follows a Model-View-Controller (MVC) architectural pattern, which allows parameterized queries to be implemented using query parameters.

Here is how these queries work:

### Define the query:

In Django, you can easily use the [Django Object-Relational Mapping](https://www.geeksforgeeks.org/django-orm-inserting-updating-deleting-data/) (ORM) to define the structure of your SQL query. Instead of directly embedding user-generated input within the query, Django ORM lets you use placeholders or parameters.

**Instead of doing this:**

```python
# Directly embedding user input in the query
user_id = request.POST['user_id']
query = "SELECT * FROM users WHERE id = " + user_id
cursor.execute(query)
```

In this code snippet, it exposes the `user_id` because the data is not validated and sanitized, so an attacker could manipulate the `user_id` input to inject malicious SQL code.

**Do this instead:**

```python
# Using parameterized query with Django ORM
from django.db import models

# Define the User model
class User(models.Model):
    id = models.IntegerField(primary_key=True)
    username = models.CharField(max_length=255)
 
# Retrieve user data using Django ORM with parameterized query
user_id = request.POST['user_id']
user = User.objects.get(id=user_id)
```

In this code snippet, the Django ORM defines the `User` model, which represents the structure of the ***users'*** table in a database. The `get()` method then retrieves a user based on the provided `user_id`; the ORM automatically handles the parametrized queries to ensure the user input is properly sanitized and handled.

### Executing Queries:

When executing queries in Django, Django ORM sends SQL queries to the database to get the results. Using Django ORM ensures safe communication with the database.

**Instead of using the user input in the query:**

```python
def search_books(request):
    if 'q' in request.GET:
        query = request.GET['q']
        # Directly using user input in the query
        books = Book.objects.filter(title=query)
    else:
        books = None

    return render(request, 'search_results.html', {'books': books})
```

In this snippet, you are directly using the `q` parameter in the SQL query, which makes it vulnerable to SQL injections as the `q` can be manipulated.

**You can do this instead:**

```python
def search_books(request):
    if 'q' in request.GET:
        query = request.GET['q']
        # Using parameterized query
        books = Book.objects.filter(title__contains=query)
    else:
        books = None

    return render(request, 'search_results.html', {'books': books})
```

Instead, you could use the `__contains` lookup within the `title` field to sanitize the query and ensure the user input is treated as data, not SQL commands.

Parameterized queries are a crucial security measure in web development, and Django provides built-in support to help developers write secure code and protect their applications from potential vulnerabilities.

## Conclusion

By using parameterized queries, Django automatically handles the much-needed security to prevent attacks when taking user inputs and prevents SQL injections.

Please note that Django ORM automatically handles parameterized queries for you. You do not need to define them manually in your views file, but you would need to define them if you use raw SQL queries when interacting with a database.

Did I miss anything while explaining this concept? Let me know in the comments.

Happy Coding!