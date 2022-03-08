## [Sum of all the multiples of 3 or 5](https://www.codewars.com/kata/57f36495c0bb25ecf50000e7)

### Instructions

Your task is to write function `findSum`.

Upto and including `n`, this function will return the sum of all multiples of 3 and 5.

For example:

`findSum(5)` should return 8 (3 + 5)

`findSum(10)` should return 33 (3 + 5 + 6 + 9 + 10)

---

### Starting Code


```python
def find(n):
    # Code here
```

---

### Solution


```python
def find(n):
    total = 0
    for e in range(1, n + 1):
        if e %3 == 0 or e %5 == 0:
            total += e
    return total
```

---

### Sample Tests

```python
test.assert_equals(find(5), 8)
test.assert_equals(find(10), 33)
```
