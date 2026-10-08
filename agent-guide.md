# Fibonacci Sequence Guide

## What it is

The Fibonacci sequence starts with 0 and 1. Each following number is the sum of the two before it:

```
0, 1, 1, 2, 3, 5, 8, 13, 21, 34, ...
```

Formally: `F(0) = 0`, `F(1) = 1`, `F(n) = F(n-1) + F(n-2)`.

## Where it appears

- Spiral patterns in plants, such as sunflower seeds and pinecones
- Algorithm teaching: recursion, dynamic programming
- The ratio of consecutive terms approaches the golden ratio (about 1.618)

## Small Python function

An iterative version is fast and avoids the repeated work of naive recursion:

```python
def fibonacci(n):
    """Return the first n Fibonacci numbers as a list."""
    seq = []
    a, b = 0, 1
    for _ in range(n):
        seq.append(a)
        a, b = b, a + b
    return seq

print(fibonacci(10))
```

## Example output

Expected output for `fibonacci(10)` (written by hand from the definition, not from a run):

```
[0, 1, 1, 2, 3, 5, 8, 13, 21, 34]
```

## Tips

- Use iteration or memoization for large `n`.
- Python integers grow as needed, so overflow is not a concern.
- Decide up front whether your sequence starts at 0 or 1; conventions differ.
