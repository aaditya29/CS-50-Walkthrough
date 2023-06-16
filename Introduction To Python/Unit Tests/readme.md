# Unit Tests In Python

- Up until now, we have been likely testing our own code using print statements. It’s most common in industry to write code to test your own programs.

```Python
def main():
    x = int(input("What's x? "))
    print("x squared is", square(x))


def square(n):
    return n * n


if __name__ == "__main__":
    main()
```
