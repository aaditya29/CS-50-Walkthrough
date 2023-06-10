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
