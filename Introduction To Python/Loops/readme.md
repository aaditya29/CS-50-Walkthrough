# Loops In Python

<b>Loops are a way to do something over and over again.</b>

## While-Loop

- The `while` loop is nearly universal throughout all coding languages.
- Such a loop will repeat a block of code over and over again.

```Python
i = 3
while i != 0:
    print("meow")
```

This code will execute print("meow") multiple times, it will never stop! It will loop forever. `while` loops work by repeatedly asking if the condition of the loop has been fulfilled. In this case, the compiler is asking “does i not equal zero?” When you get stuck in a loop that executes forever, you can press `control-c` on your keyboard to break out of the loop.

- To fix this loop that lasts forever, we can edit our code as follows:

```Python
i = 3
while i != 0:
  print("meow")
  i = i - 1
```

Now our code executes properly, reducing `i` by `1` for each “iteration” through the loop. This term iteration has special significance within coding. By iteration, we mean one cycle through the loop. The first iteration is the “0th” iteration through the loop. The second is the “1st” iteration. In programming we count starting with 0, then 1, then 2.

- We can further improve our code as follows:

```Python
i = 1
  while i <= 3:
      print("meow")
      i = i + 1
```

## For Loop
