## [Can we divide it?](https://www.codewars.com/kata/5a2b703dc5e2845c0900005a)

### Instructions

---

Your task is to create the functionisDivideBy (or is_divide_by) to check if an integer number is divisible by both integers a and b.

A few cases:

```python
(-12, 2, -6)  ->  true
(-12, 2, -5)  ->  false

(45, 1, 6)    ->  false
(45, 5, 15)   ->  true

(4, 1, 4)     ->  true
(15, -5, 3)   ->  true
```

---

### Starting Code


```python
def is_divide_by(number, a, b):
    return # good luck
```

---

### Solution


```python
def is_divide_by(number, a, b):
    return number % a == 0 and number % b == 0
```

---

### Sample Tests

```python
import codewars_test as test
from solution import is_divide_by

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(is_divide_by(8, 2, 4), True)
        test.assert_equals(is_divide_by(12, -3, 4), True)
        test.assert_equals(is_divide_by(8, 3, 4), False)
        test.assert_equals(is_divide_by(48, 2, -5), False)
        test.assert_equals(is_divide_by(-100, -25, 10), True)
        test.assert_equals(is_divide_by(10000, 5, -3), False)
        test.assert_equals(is_divide_by(4, 4, 2), True)
        test.assert_equals(is_divide_by(5, 2, 3), False)
        test.assert_equals(is_divide_by(-96, 25, 17), False)
        test.assert_equals(is_divide_by(33, 1, 33), True)
```
