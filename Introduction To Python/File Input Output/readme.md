# File I/O In Python

## File I/O

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

## `open`

- `open` is a functionality built into Python that allows us to open a file and utilize it in our program. The `open` function allows us to open a file such that you can read from it or write to it.
- Enabling file I/O in program:

```Python
name = input("What's your name? ")

file = open("names.txt", "w")
file.write(name)
file.close()

```

- The `open` function opens a file called `names.txt` with writing enabled, as signified by the `w`. The code above assigns that opened file to a variable called `file`. The line `file.write(name)` writes the name to the text file. The line after that closes the file.
- Ideally, we want to be able to append each of our names to the file. Removing the existing text file by typing `rm names.txt` in the terminal window. Then, modifying our code as follows:

```Python
name = input("What's your name? ")

file = open("names.txt", "a")
file.write(name)
file.close()
```

- Notice that the only change to our code is that the w has been changed to a for “append”.
