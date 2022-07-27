# Functions And Variables In Python

## Strings And Parameters

- A string, known as a `str` in Python, is a sequence of text.

```Python
# Ask the user for their name
name = input("What's your name? ")
print("hello,")
print(name)
```

### Formatting Strings

Probably the most elegant way to use strings would be as follows:

```Python
# Ask the user for their name
name = input("What's your name? ")
print(f"hello, {name}")
```

Notice the f in print(f"hello, {name}"). This f is a special indicator to Python to treat this string a special way, different than previous approaches.

### More On Strings

By utilizing the method strip on name as name = name.strip(), it will strip all the whitespaces on the left and right of the users input. You can modify your code to be:

```Python
# Ask the user for their name
name = input("What's your name? ")

# Remove whitespace from the str
name = name.strip()

# Print the output
print(f"hello, {name}")
```

## Functions In Python

In any programming language, functions facilitate code reusability. In simple terms, when you want to do something repeatedly, you can define that something as a function and call that function whenever you need to.

### Python Function Syntax

The following snippet shows the general syntax to define a function in Python:

```Python
def function_name(parameters):
    # What the function does goes here
    return result
```
