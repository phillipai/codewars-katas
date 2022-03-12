## [Calculate average](https://www.codewars.com/kata/57a2013acf1fa5bfc4000921)

### Instructions

---

Write a function which calculates the average of the numbers in a given list.

Note: Empty arrays should return 0.

---

### Starting Code


```python
def find_average(numbers):
    # your code here
    pass
```

---

### Solution


```python
def find_average(numbers):
    if not numbers: return 0
    return sum(numbers) / len(numbers)
```

---

### Sample Tests

```python
import codewars_test as test
from solution import find_average

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(find_average([1, 2, 3]), 2)
```
