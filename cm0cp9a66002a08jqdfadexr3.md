---
title: "F-Strings in Python: What They Are and How to Use Them"
seoTitle: "Mastering Python F-Strings"
seoDescription: "Learn about Python F-strings, their benefits, and how to use them for efficient and readable string formatting"
datePublished: Tue Aug 27 2024 17:27:07 GMT+0000 (Coordinated Universal Time)
cuid: cm0cp9a66002a08jqdfadexr3
slug: f-strings-in-python-what-they-are-and-how-to-use-them
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1724748544588/a3c3f16e-9458-4da8-bda1-18cae7765dd6.png
tags: python, hashnode, python-beginner

---

F-strings (Formatted strings) in Python are an easy way to add expressions in Strings. It was first introduced in [Python 3.6](https://docs.python.org/3/whatsnew/3.6.html), making string formatting much more readable and easy.

In this guide, we will understand what f-strings are and why it is so much better than using the standard formatting method, `str.format()`.

## What are F-strings?

F-string is a formatting technique introduced to Python that makes it so much easier to play around with expressions and strings; it is usually defined by the prefix, `f` and using the curly brackets, `{}` to format your value or to interpolate.

When it comes to f-strings, it has so many benefits, such as:

* **Readability:** F-strings lets you embed expressions directly within the string, which makes it easy to read and understand.
    
* **Performance:** F-strings are faster than your average string formatting, like `str.format()` or `%` because f-strings do not need any overhead of method calls.
    
* **Easy to Use**: With f-strings, you do not need to remember different formatting methods or symbols; you only need to prefix your string.
    
* **Flexibility:** When using f-strings, expressions defined can include any valid Python expression inside the curly brackets an not just variables.
    
* **Type safety:** F-strings automatically convert your expressions to strings, thereby reducing the chance of type conversion errors.
    

## What is `str.format()` all about?

`str.format()` is the OG formatting method. This method is still useful when you need to reuse your format technique more than once with different values or data types or if you are working on a project that uses Python versions earlier than 3.6.

Aside from using it with older Python version projects, `str.format()` is also useful when dealing with more advanced formatting options like padding, number formatting, alignment, etc, or when formatting dictionaries or objects, making dealing with structured data so easy.

While this method is useful, it is also very slow because of many function calls when formatting values. `str.format()` is just as useful as f-strings, depending on your use case.

Let's look at a code example of how `str.format()`:

```python
name = "Sophia"
age = 30

# Using str.format() to format the string
formatted_string = "My name is {} and I am {} years old.".format(name, age)

print(formatted_string)
```

Your response will look like this:

```python
My name is Sophia and I am 30 years old.
```

## Basic Syntax of F-string

As stated earlier, f-strings are prefixed `f` before the string, and inside the string, you add the variable or the expression within curly brackets, `{}` .

Here's a basic syntax that shows how variables can be defined within the f-string.

```python
name = "Sophia"
country = "Nigeria"

greetings = f"Hello, I am {name.capitalize()} and I am {country}"
print(greetings)
```

Your response will look like this:

```bash
I am Sophia and I am from Nigeria
```

## Adding Expressions within F-strings

Now, let’s look at adding expressions inside f-strings. You can also add the expressions within curly brackets.

Here’s a code example:

```python
a = 10
b = 8

result = f"The sum of {a} and {b} is {a + b}"
print(result)
```

Your response will look like this:

```bash
The sum of 10 and 24 is 34
```

## Formatting Numbers within F-strings

Let’s take another look at how we can use f-strings. You can format numbers within the curly braces.

Here's a code example:

```python
value = 500.287018 

formatted_value = f"The {value} in two decimal places is {value:.2f}"
print(formatted_value)
```

Your response will look like this:

```bash
The 500.287018 in two decimal places is 500.29
```

## Using F-strings in multiple lines

Lastly, let’s see if the f-strings can be used in multiple lines using triple quotes.

Here's a code example:

```python
name = "Mercedes"
year = "2009"

result = f"""
Name : {name}
Year the car was made: {year}
"""
print(result)
```

Your response will look like this:

```bash

Name : Mercedes
Year the car was made: 2009
```

## Conclusion

Voila! Congrats you now understand what f-strings are and how this is a great formatting method for your projects.

In this guide, I focused on formatting strings and numbers, but f-strings can be used to format all data types in Python.

If you prefer the video version of this guide, check it out below:

<iframe width="560" height="315" src="https://www.youtube.com/embed/k6ZEKNHQIuo"></iframe>