## [Function 3 - multiplying two numbers](https://www.codewars.com/kata/523b66342d0c301ae400003b)

### Instructions

---

Implement a function which multiplies two numbers.

---

### Starting Code


```python
#your code here
```

---

### Solution


```python
def multiply(a, b):
    return a * b
```

---

### Sample Tests

```python
import codewars_test as test
from solution import multiply

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(multiply(2, 3), 6)   
```
