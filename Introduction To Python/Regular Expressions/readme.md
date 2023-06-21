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

- Notice that while this works as expected, our user could be adversarial, typing simply `@.` would result in the program returning valid.
- Modifying the code as follows:

```Python
email = input("What's your email? ").strip()

username, domain = email.split("@")

if username and "." in domain:
    print("Valid")
else:
    print("Invalid")
```

- The `strip` method is used to determine if username exists and if . is inside the domain variable. Running this program, a standard email address typed in by us could be considered valid. Typing in abc@harvard alone, we’ll find that the program regards this input as invalid.
  Modifying further:

```Python
email = input("What's your email? ").strip()

username, domain = email.split("@")

if username and domain.endswith(".edu"):
    print("Valid")
else:
    print("Invalid")

```

- The endswith method will check to see if domain contains .edu. However, a nefarious user could still break our code. For example, a user could type in abc@.edu and it would be considered valid.
