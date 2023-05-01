# Exceptions In Python

- Exceptions are things that go wrong within our coding.

## Runtime Errors

Runtime errors refer to those created by unexpected behavior within your code.
For example, perhaps you intended for a user to input a number, but they input a character instead. Our program may throw an error because of this unexpected input from the user.

If we run run code `number.py`

```Python
x = int(input("What's x? "))
print(f"x is {x}")
```

Notice that by including the f, we tell Python to interpolate what is in the curly braces as the value of x. Further, testing out our code, we can imagine how one could easily type in a string or a character instead of a number. Even still, a user could type nothing at all – simply hitting the enter key.
As programmers, we should be defensive to ensure that our users are entering what we expected. We might consider “corner cases” such as `-1, 0` or `cat`
If we run this program and type in “cat”, we’ll suddenly see `ValueError: invalid literal for int() with base 10: cat`

Essentially, the Python interpreter does not like that we passed “cat” to the print function.
An effective strategy to fix this potential error would be to create “error handling” to ensure the user behaves as we intend.

## try

- In Python `try` and `except` are ways of testing out user input before something goes wrong.<br>
  For Example:

```Python
try:
    x = int(input("What's x?"))
    print(f"x is {x}")
except ValueError:
    print("x is not an integer")
```

When we run this code, inputting 50 will be accepted. However, typing in cat will produce an error visible to the user, instructing them why their input was not accepted.

- This is still not the best way to implement this code. Notice that we are trying to do two lines of code.<br>
  For best practice, we should only try the fewest lines of code possible that we are concerned could fail.

  Editing our code as:

```Python
try:
    x = int(input("What's x?"))
except ValueError:
    print("x is not an integer")

print(f"x is {x}")
```
