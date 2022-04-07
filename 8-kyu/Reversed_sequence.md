## [Reversed sequence](https://www.codewars.com/kata/5a00e05cc374cb34d100000d)

### Instructions

---

Build a function that returns an array of integers from n to 1 where `n>0`.

Example :`n=5` --> `[5,4,3,2,1]`

---

### Starting Code


```python
def reverse_seq(n):
    pass
```

---

### Solution


```python
def reverse_seq(n):
    list = []
    for e in range(1, n+1):
        list.append(e)
    return list[::-1]
```

---

### Sample Tests

```python
import codewars_test as test
from solution import reverse_seq

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(reverse_seq(5),[5,4,3,2,1])
```
