# File I/O

- File I/O is the ability of a program to take a file as input or create a file as output.
- Typing in the terminal window `code names.py`:

```Python
name = input("What's your name?" )
print(f"hello, {name}")
```

- Running this code has the desired output. The user can input a name. The output is as expected.
- What if we wanted to allow multiple names to be inputted? To achieve this recall that a list is a data structure that allows us to store multiple values into a single variable.

```Python
names = []

for _ in range(3):
    name = input("What's your name?" )
    names.append(name)

```

- The user will be prompted three times for input. The `append` method is used to add the name to our names list.
- Simplifying above code:

```Python
names = []

for _ in range(3):
    names.append(input("What's your name?" ))
```

- Making list as sorted

```Python
names = []

for _ in range(3):
    names.append(input("What's your name?" ))

for name in sorted(names):
    print(f"hello, {name}")
```

- Once this program is executed, all information is lost. File I/O allows your program to store this information such that it can be used later.
