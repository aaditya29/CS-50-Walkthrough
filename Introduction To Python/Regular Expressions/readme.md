# Regular Expressions In Python

- Regular expressions or “regexes” will enable us to examine patterns within our code. For example, we might want to validate that an email address is formatted correctly. Regular expressions will enable us to examine expressions in this fashion.
- For example `code validate.py`:

```Python
email = input("What's your email? ").strip()

if "@" in email:
    print("Valid")
else:
    print("Invalid")
```

- `strip` will remove whitespace at the beginning or end of the input. Running this program, we will see that as long as an @ symbol is inputted, the program will regard the input as valid.
- However, one could input @@ alone and the input could be regarded as valid. We could regard an email address as having at least one @ and a . somewhere within it.
- Modifying your code as follows:

```Python
email = input("What's your email? ").strip()

if "@" in email and "." in email:
    print("Valid")
else:
    print("Invalid")

```
