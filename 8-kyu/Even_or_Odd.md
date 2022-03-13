## [Even or Odd](https://www.codewars.com/kata/53da3dbb4a5168369a0000fe)

### Instructions

---

Create a function that takes an integer as an argument and returns "Even" for even numbers or "Odd" for odd numbers.

---

### Starting Code


```python
def even_or_odd(number):
```

---

### Solution


```python
def even_or_odd(number):
    if number % 2 == 0: return 'Even'
    return 'Odd'
```

---

### Sample Tests

```python
import codewars_test as test
from solution import even_or_odd

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(even_or_odd(2), "Even")
        test.assert_equals(even_or_odd(1), "Odd")
        test.assert_equals(even_or_odd(0), "Even")
        test.assert_equals(even_or_odd(1545452), "Even")
        test.assert_equals(even_or_odd(7), "Odd")
        test.assert_equals(even_or_odd(78), "Even")
        test.assert_equals(even_or_odd(17), "Odd")
        test.assert_equals(even_or_odd(74156741), "Odd")
        test.assert_equals(even_or_odd(100000), "Even")
        test.assert_equals(even_or_odd(-123), "Odd")
        test.assert_equals(even_or_odd(-456), "Even")
```
