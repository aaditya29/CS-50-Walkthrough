# Libraries In Python

## Libraries

- Generally, libraries are bits of code written by us or others we can use in our program.
- Python allows us to share functions or features with others as “modules”.
- If we copy and paste code from an old project, chances are we can create such a module or library that we could bring into our new project.

## random In Python

- random is a library that comes with Python that we could import into our own project.
- So, how do we load a module into our own program? We can use the word import in our program.
- Inside the random module, there is a built-in function called random.choice(seq). random is the module we are importing Inside that module, there is the choice function. That function takes into it a seq or sequence that is a list.

```Python
import random

coin = random.choice(["heads", "tails"])
print(coin)
```

- We can improve our code. `from` allows us to be very specific about what we’d like to import. Prior, our import line of code is bringing the entire contents of the functions of random. However, what if we want to only load a small part of a module?

- Modifying our code as follows:

```Python
from random import choice

coin = choice(["heads", "tails"])
print(coin)
```

- Here, we now can import just the choice function of `random`
- From that point forward, we no longer need to code random.choice. We can now only code choice alone. choice is loaded explicitly into our program. This saves system resources and potentially can make our code run faster!

- Now consider the function random.randint(a, b). This function will generate a random number between a and b.
- Modifying our code as follows:

```Python
import random

number = random.randint(1, 10)
print(number)
```

- We can introduce into our card random.shuffle(x) where it will shuffle a list into a random order.

```Python
import random

cards = ["jack", "queen", "king"]
random.shuffle(cards)
for card in cards:
    print(card)
```

## Statistics

- Python comes with a built-in statistics library.

### Using This Module

- `average` is a function of this library that is quite useful.
- Typing code average.py:

```Python
import statistics

print(statistics.mean([100, 90]))
```

Here, we imported a different library called statistics. The mean function takes a list of values. This will print the average of these values. In your terminal window, type python average.py.

## Command-Line Arguments

- What if we wanted to be able to take input from the command-line? For example, rather than typing python average.py in the terminal, what if we wanted to be able to type python average.py 100 90 and be able to get the average between 100 and 90?
- `sys` is a module that allows us to take arguments at the command line.
- `argv` is a function within the sys module that allows us to learn about what the user typed in at the command line.

```Python
import sys

print("hello, my name is", sys.argv[1])
```

- The program is going to look at what the user typed in the command line. Currently, if you type python name.py David into the terminal window, you will see hello, my name is David. Notice that sys.argv[1] is where David is being stored. Why is that? Well, in prior lessons, you might remember that lists start at the 0th element. What do you think is held currently in sys.argv[0]? If you guessed name.py, you would be correct!
